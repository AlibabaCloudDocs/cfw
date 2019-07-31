# Best practices for defense against unauthorized access to MongoDB {#concept_cpt_f2t_2hb .concept}

Unauthorized access to MongoDB could lead to data disclosure or deletion extortion.

To ensure the security of your business and applications, Cloud Firewall provides a solution to fix this vulnerability.

## Hazards { .section}

By default, a MongoDB database requires no authentication if you do not set any parameters when activating the MongoDB service. Without any passwords, users who have logged on to the service can use the default port to remotely access the database and perform any operations \(including high-risk operations such as add, delete, edit, and query\) on the database.

## Solution { .section}

1.  **Configure an access control policy in Cloud Firewall.** 
    1.  Log on to the Cloud Firewall console. Choose **Network Traffic Analysis** \> **Internet Access Activities** \> **Open Applications**. On the Open Applications tab, check the public IP address of the MongoDB service. If the MongoDB service provides services only for intranet servers, we recommend that you disable the MongoDB service from being open to the Internet.

![](images/41436_en-US.png)

Bind the MongoDB service to a specified IP address so that the MongoDB service provides services only for intranet servers. \(In this example, the MongoDB instance listens only on the requests sent from intranet IP address 10.0.0.1.\)

```
mongod --bind_ip 10.0.0.1
```

    2.  **Configure an access control policy for MongoDB in Cloud Firewall to allow only trusted IP addresses to access the MongoDB service.** 

        Log on to the Cloud Firewall console. Choose **Security Policy** \> **Access Control** \> **Internet Border Firewall** \> **Internet-to-Intranet**In the dialog box that appears, configure an access control policy to allow only the MongoDB servers to access the MongoDB service.

        1.  Add all trusted IP addresses that are allowed to access the MongoDB service to an IP address book.

            ![](images/41444_en-US.png)

        2.  Allow trusted IP addresses to access the MongoDB service.

            ![](images/41446_en-US.png)

            -   **Source**: The address box in which you have configured all trusted IP addresses that are allowed to access the MongoDB service.
            -   **Destination**: The IP address of the MongoDB service.
            -   **Protocol Type**: Select TCP, which indicates that this policy applies to access traffic from the Internet.
            -   **Port**: Set this parameter to 0/0, which indicates that this policy applies to all ports corresponding to trusted IP addresses.
    3.  **Disallow non-trusted IP addresses to access the MongoDB service.** 

        ![](images/41455_en-US.png)

        -   **Source**: Set this parameter to Any, which indicates that this policy applies to all non-trusted access IP addresses.
        -   **Destination**: The public IP address of the MongoDB service.
        -   **Protocol Type**: Select TCP, which indicates that this policy applies to access traffic from the Internet.
        -   **Port**: Set this parameter to 0/0, which indicates that this policy applies to all ports corresponding to non-trusted IP addresses.
2.  **Enable role-based logon authentication.** 

    1.  Create a user in the admin database.
    2.  Log on to the database with authentication disabled.

        ```
        [mongodbrac3 bin]$ ./mongo 127.0.0.1:27028 // The default port is changed.
        MongoDB shell version: 2.0.1
        connecting to: 127.0.0.1:27028/test
        ```

    3.  Switch to the admin database.

        ```
        > use admin
        switched to db admin
        ```

    4.  Create an administrator account.

        **Note:** In MongoDB V3 and later, the addUser method is no longer used. You can run the db.createUser command instead to create users.

        ```
        > db.addUser("supper", "supWDxsf67%H") or
        { "n" : 0, "connectionId" : 4, "err" : null, "ok" : 1 }
        > db.createUser({user:"****",pwd:"***********",roles:["root"]})
        {
        "user" : "****",
        "readOnly" : false,
        "pwd" : "**************","_id"
        ObjectId("4f2bc0d357a309043c6947a4")
        }
        # The administrator account information is in the system.users collection.
        > db.getCollectionNames()
        [ "system.indexes", "system.users", "system.version" ]
        ```

        **Note:** The account name cannot be a common word. The password must contain at least eight characters, including at least one uppercase letter, one lowercase letter, one number, and one special character. Do not use a common password, such as a birth date, a name, or an ID number.

    5.  Verify that the user has been created.

        ```
        # Terminate the process and restart the MongoDB service.
        > db.auth("user","password")
        > exit
        bye
        ./mongod --dbpath=/path/mongodb --bind_ip=10.0.0.1 --port=27028 --fork=true logpath=/path/mongod.log &
        ```

    **Note:** 

    -   The admin.system.users collection has the super privilege. It stores the information of users who have higher user privileges than users in other databases. That is, users created in the admin database can perform operations on data in other databases in MongoDB.
    -   In the MongoDB system, a database is created by a super user. A database may contain multiple users, but a single user may only exist in one database at a time. Users in different databases may share the same name, however.
    -   User1 in a particular database \(such as DB1\) cannot access database DB2, but can access data created by other users in DB1.
    -   Users with the same name in different databases cannot log on to other databases. For example, if both DB1 and DB2 have user1. After user1 logs on to DB1, it cannot log on to DB2.
    -   Users created in the admin database have the super privilege, and can perform operations on any data object in any database in the MongoDB system.
    -   You can use the db.auth \(\) method to validate users in the database. If the validation is successful, a value of 1 is returned. Otherwise, a value of 0 is returned. The db.auth\(\) method can only validate the user information in the database to which the user belongs, and cannot validate user information in other databases.

## Check for intrusion risks { .section}

If you are a MongoDB administrator, you can take the following measures to check for further intrusion:

-   Check whether the MongoDB log is complete and confirm the source IP address, time, and activity of the request for deleting the database.
-   Run the db.system.users.find\(\) command to check whether any MongoDB account has no password.
-   Run the db.fs.files.find\(\) command to check whether any file is stored in GridFS.
-   Run the show log global command to view the log file and check whether other users have accessed MongoDB.


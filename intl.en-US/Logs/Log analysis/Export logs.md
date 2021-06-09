# Export logs

The log analysis feature allows you to export log query results to your local disk. You can download logs on a specific page as a CSV file or download all logs as a TXT file. This topic describes how to export logs in the Cloud Firewall console.

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext).

2.  In the left-side navigation pane, choose **Logs** \> **Log Analysis**.

3.  Click **Logs** and **Raw Logs**. In the upper right corner, click ![Download icon](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/3936009851/p13508.png).

    ![Log download](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/3919751161/p69924.png)

4.  In the **Log Download** dialog box that appears, select a method to download logs.

    -   Select **Download Log in Current Page** and click **OK**.

        ![Download Log in Current Page](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/3936009851/p37902.png)

        Logs on the current page are downloaded in a CSV file.

    -   Select **Download All Logs with Cloud Shell**.

        ![Download All Logs with Cloud Shell](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/3919751161/p69927.png)

        1.  Click **OK** to go to the Cloud Shell command line.
        2.  Follow the instructions that appear on the page to enter the required information.
        3.  Specify a local path where you want to store the log file.
        All logs are downloaded.

        **Note:** Currently, Cloud Shell is deployed in the China \(Shanghai\) region. If the current Logstore is not in the China \(Shanghai\) region, downloading log data incurs data consumption fees. Click **Log Service Pricing** to learn more about the pricing of data usage.

    -   Select **Download All Logs Using Command Line Tool**.

        ![Download All Logs Using Command Line Tool](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/4936009851/p13509.png)

        1.  Click **Documentation** in the Log Download dialog box to learn how to install a command line tool.
        2.  Install the command line tool.
        3.  Click **Security information management** to view and copy the AccessKey ID and AccessKey secret of the current user.
        4.  Click **Copy Command** and replace the `AccessKey ID in step 2` and `AccessKey secret in step 2` with those of the current user.
        5.  Run the command in the CLI command line tool.
        After the command is executed, all logs are downloaded to the **download\_data.txt** file in the directory where the command is executed.



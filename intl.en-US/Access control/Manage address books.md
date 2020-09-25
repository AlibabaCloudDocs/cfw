# Manage address books

An address book is a collection of IP addresses, ports, or domain names. You can configure address books in the Cloud Firewall console to simplify the configuration of access control policies. You can add trusted or untrusted addresses to the same address book. This topic describes how to add, view, and modify an address book.

Cloud Firewall synchronizes malicious IP addresses and domain names detected across Alibaba Cloud to cloud address books. It also adds the back-to-origin addresses of Anti-DDoS and WAF instances under your Alibaba Cloud account to cloud address books. You can configure fine-grained access control policies for these cloud address books.

When you configure access control policies, you can:

-   Allow traffic of IP addresses and domain names in trusted address books.
-   Deny traffic of IP addresses and domain names in untrusted address books.

**Note:**

-   One IP address or port number can be added to multiple address books.
-   Cloud Firewall provides default global address books that you cannot modify or delete.
-   You cannot modify or delete cloud address books.
-   If you change the IP addresses, domain names, or ports in an address book, the changes are automatically updated in the policies that reference this address book.

## Procedure

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext).

2.  In the left-side navigation pane, choose **Security Policies** \> **Access Control**.

3.  In the upper-right corner of the **Internet Firewall** tab, click **Address Books**.

4.  In the dialog box that appears, manage address books.

    ![Manage address books](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/2518686851/p66579.png)

    You can perform the following operations:

    -   **Add an address book.**

        You can add both trusted and untrusted address books based on the access control policies you want to configure. Cloud Firewall allows you to add **IP**, **port**, and **domain name** address books. For more information, see [Add an address book](#section_5oq_swo_qzs).

    -   **Modify an address book.**

        On the **IP Address Books**, **Port Address Books**, or **Domain Address Books** tab, find the target address book. Click **Modify** in the **Actions** column to modify the address book.

        **Note:** You cannot change the **type** or **name** of an address book.

    -   **View cloud address books.**

        On the **Cloud Address Books** tab, view the names, types, IP addresses \(domain names\) and their quantity, numbers of references, and descriptions of cloud address books.

        ![Cloud Address Books](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/2518686851/p66622.png)

        Click **View** in the **Actions** column to view the configuration of a cloud address book.

        ![Cloud address book configuration](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/2518686851/p66619.png)

    -   **Delete an address book.**

        On the **IP Address Books**, **Port Address Books**, or **Domain Address Books** tab, find the target address book. Click **Delete** in the **Actions** column. In the dialog box that appears, and click **OK**.

        **Note:** You cannot delete an address book that is being referenced by access control policies.


## Add an address book

1.  In the upper-right corner of the **IP Address Books**, **Port Address Books**, or **Domain Address Books** tab, click **Create Address Book**.

2.  In the **Create Address Book**, **Create Port Address Book**, or **Create Domain Address Book** dialog box, configure the following parameters.

    -   **IP address book**

        ![Create an IP address book](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/2518686851/p66584.png)

    -   **Port address book**

        ![Create a port address book](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/2518686851/p66610.png)

    -   **Domain address book**

        ![Create a domain address book](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/3518686851/p66612.png)

    |Type|Parameter|Description|
    |----|---------|-----------|
    |IP address book|Address Book Type|Select the type of the IP address book, which can be the following:     -   **IP Addresses**
    -   **ECS Tags** |
    |IP Address|Enter one or more CIDR blocks. **Note:** Separate CIDR blocks with commas \(,\). This parameter is available when you set **Address Book Type** to **IP Addresses**. |
    |Add ECS of Specified Tags|Automatically add ECS instances that have specific tags to this address book. This function is enabled automatically and cannot be disabled. **Note:** This parameter is available when you set **Address Book Type** to **ECS Tags**. |
    |ECS Tags|Select ECS tags created under your Alibaba Cloud account. Cloud Firewall automatically adds public IP addresses of ECS instances that have the tags you specify to an address book. Click **Add Tag** to specify more ECS tags.

 After you select an ECS tag, information about the ECS instance is displayed under **ECS Tags**, including the VPC name and IP address. |
    |Port address book|Ports|Enter one or more port ranges and separate them with commas \(,\).|
    |Domain address book|Domain|Enter one or more domain names and separate them with commas \(,\). Each domain name must be unique.|
    |Common parameters|Address Book Name|Enter a name for the address book. You can use the name to identify the address book.|
    |Description|Enter an application scenario for the address book.|

3.  Click **Submit**.

    The new address book is displayed in the list. You can view its name, number of references, and description, and delete or modify it.


## References

[Outbound and inbound traffic control on the Internet firewall](/intl.en-US/Access control/Outbound and inbound traffic control on the Internet firewall.md)

[Access control on VPC firewalls](/intl.en-US/Access control/Access control on VPC firewalls.md)

[Intrusion prevention policies](/intl.en-US/Intrusion prevention/Intrusion prevention policies.md)


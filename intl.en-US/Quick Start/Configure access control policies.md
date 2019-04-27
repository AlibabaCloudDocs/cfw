# Configure access control policies {#concept_c5d_1sh_cfb .concept}

Cloud Firewall allows you to configure access control policies to specify the accessible ports on your assets and control the access from your assets to the Internet. You can use access control policies to control inbound and outbound traffic.

You could add a group of IP addresses or ports to the Address Books. With this Address Book, you can quickly configure the control policy with multiple IP or addresses.

## Procedure {#section_gvh_pwh_cfb .section}

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext#/overview).
2.  On the **Access Control** \> **Internet firewall** page of the console, click **Create Policy** to configure an access control policy.

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21211/155639177537813_en-US.png)

    Configurations are as follows:

    -   Source Type: The data sender type. Select IP or Address book.
    -   Source: The address of data sender. If you select IP for Source Type, you must enter an IP address or CIDR block in **Access Source**.
    -   Destination Type: The type of the data's destination. You can select IP, Address Book or Domian Name.
    -   Destination: The data's destination address.
    -   Protocol: The protocol of the data. The supported protocols include TCP, UDP, and ICMP.
    -   Port Type: The type of the port, including Ports and Address Book.
    -   Destination Port: The port of the data's recipient.
    -   Application: The application to which the access control policy applies in the specified protocol.
    -   Policy Action: The action on the access traffic. You can select **Allow**, **Monitor** or **Deny**.
    -   Description: The remarks on the access control policy.

Click **Address books** on the **Internet Firewall** page, you can create new address books, or modify/delete existing address books.

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21211/155639177545653_en-US.png)

**Note:** Except for certain necessary/safe external connection activities, we recommend that you select **Deny** for all the other outbound access to the Internet .


# Block access from regions outside China

If you want to block access to your assets from regions outside China, you can go to the Cloud Firewall console and configure an access control policy. This topic describes how to configure a policy to block access from regions outside China in the Cloud Firewall console.

**Internet Firewall** is enabled. Otherwise, the access control policies you configured on the Internet firewall do not take effect. For more information, see [Enable or disable Internet Firewall](/intl.en-US/Firewall Settings/Enable or disable Internet Firewall.md).

![Internet firewall](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/7856586851/p77607.png)

On the Internet Firewall tab, you can configure **inbound policies** to control access by region.

## Create an access control policy

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext).

2.  In the left-side navigation pane, choose **Access Control** \> **Access Control**.

3.  On the **Internet Firewall** tab, click **Inbound Policies**.

4.  On the **Inbound Policies** tab, click **Create Policy**.

    ![Create Policy](../images/p290361.png)

5.  In the **Create Inbound Policy** dialog box, configure the parameters.

    Set **Source Type** to **Region**, **Source** to Regions Outside China, and **Policy Action** to **Deny**. Then, click **Submit**. The following table describes the parameters.

    ![Create Inbound Policy](../images/p290575.png)


|Parameter|Description|
|---------|-----------|
|**Source Type**|The type of the source address. Valid values: -   **IP**: Enter a CIDR block in the **Source** field.
-   **Address Book**: Select a preconfigured address book.

**Note:** You can add multiple CIDR blocks to an address book to simplify policy configurations. |
|**Source**|The source CIDR block of the traffic. **Note:** You can enter only one CIDR block, for example, 1.1.1.1/32.

If you set **Source Type** to **Address Book**, select a preconfigured address book.

**Note:**

-   In an outbound access control policy, if **Source Type** is set to Address Book, you can only select an IP address book. However, if Destination Type is set to Address Book, you can select an IP address book, domain address book, or cloud address book.
-   In an inbound access control policy, if **Source Type** is set to Address Book, you can select an IP address book or cloud address book. However, if Destination Type is set to Address Book, you can select only an IP address book.
-   You can select only one address book at a time. If you want to use multiple address books, click **Create Policy**. |
|**Destination Type**|Set this parameter in the following way: -   If you select **IP**, enter a CIDR block in the Destination field.
-   If you select **Address Book**, select a preconfigured address book.
-   If you select **Domain Name**, set the destination to a domain name. You can specify a wildcard domain name, for example, `*.aliyun.com`.

**Note:** By default, if an HTTP header does not contain the host field or an HTTPS request does not contain the Server Name Indication \(SNI\), Cloud Firewall **allows** the traffic.

-   If you select **Region**, select a region as the destination. You can select a region inside or outside China. |
|**Destination**|If you set Destination Type to IP, the destination must be set to a CIDR block. Only one CIDR block can be configured. If you set **Destination Type** to Domain Name, set the destination to a domain name. Wildcard domain names are supported.

**Note:**

-   In an outbound access control policy, if Source Type is set to Address Book, you can select only an IP address book. However, if Destination Type is set to Address Book, you can select an IP address book, domain address book, or cloud address book.
-   In an inbound access control policy, if Source Type is set to Address Book, you can select an IP address book or cloud address book. However, if Destination Type is set to Address Book, you can select only an IP address book.
-   You can select only one address book at a time. If you want to use multiple address books, click **Create Policy**. |
|**Protocol**|Valid values: -   ANY: any protocol type
-   TCP
-   UDP
-   ICMP |
|**Port Type**|Set this parameter in the following way: -   If you select **Ports**, enter a port range.
-   If you select **Address Book**, select a preconfigured **port address book**. A port address book contains multiple ports, which simplifies policy configurations. |
|**Ports**|Specify the ports on which you want to control traffic. If Port Type is set to Ports, enter a port number range. If Port Type is set to Address Book, find the required port address book and click **Select** in the Actions column.**Note:**

-   You can select only one address book at a time. If you want to use multiple address books, click **Create Policy**.
-   If you set Protocol to ICMP, the port configuration does not take effect. If you set Protocol to ANY, the destination ports you specify do not take effect in controlling ICMP traffic. |
|**Application**|Valid values: ANY, HTTP, HTTPS, Memcache, MongoDB, MQTT, MySQL, RDP, Redis, SMTP, SMTPS, SSH, and VNC. If **Protocol** is set to TCP, the preceding protocols are supported. If Protocol is set to another value, you can select only ANY.

**Note:** Cloud Firewall identifies applications based on packet characteristics, instead of port numbers. If Cloud Firewall fails to identify an application in a packet, it allows the packet. If you want to block traffic from unknown applications, we recommend that you enable the strict mode. For more information, see [Strict mode of the Internet firewall](/intl.en-US/Toolbox/Strict mode of the Internet firewall.md). |
|**Policy Action**|Specifies whether the Internet firewall allows or denies the traffic. Set this parameter in the following way: -   **Allow**: If traffic meets the preceding conditions that you specify for the policy, the traffic is allowed.
-   **Deny**: If traffic meets the preceding conditions that you specify for the policy, the traffic is denied, and no notifications are sent.
-   **Monitor**: If traffic meets the preceding conditions that you specify for the policy, the traffic is recorded and allowed. After you observe the traffic for a period of time, you can change the policy action to **Allow** or **Deny**. |
|**Description**|Enter a description to identify the policy.|
|**Priority**|The priority of a policy, Set this parameter in the following way: -   **Lowest**: The policy takes effect in the last priority.
-   **Highest**: The policy takes effect in the first priority.

The default value is Lowest. |

## Check whether access traffic hits a control policy

By default, an access control policy takes effect immediately after it is created. However, if the policy parameters are incorrectly configured or the Internet firewall is disabled, the policy does not take effect.

In the access control policy list, if the number in the **Hits** column is greater than 0 for an access control policy, access traffic hits the policy. The number in the **Hits** column indicates the number of times traffic hits the policy.

![Hits](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/9389034161/p183926.png)

You can click the number in the **Hits** column to go to the **Traffic Logs** tab. On the **Traffic Logs** tab, you can view the names of access control policies that the traffic hits in the **Policy Name** column.

**Note:** This tab displays information about the traffic generated in the last seven days. If the last access control policy hit was more than seven days ago, no data is displayed.

## Modify an access control policy

After an access control policy is created, you can modify the access control policy based on your business requirements.

To modify an access control policy, find the access control policy on the Inbound Policies tab and click **Modify** in the **Actions** column. In the **Modify Policy** panel, modify the parameters of the access control policy.


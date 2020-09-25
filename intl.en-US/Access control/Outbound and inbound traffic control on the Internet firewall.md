# Outbound and inbound traffic control on the Internet firewall

Cloud Firewall supports access control on the Internet firewall. You can configure policies to control the traffic between the Internet and your ECS instances.

The firewall for ECS instances is enabled on the **Internet Firewall** tab. Otherwise, the access control policies you configure do not take effect.

![Internet Firewall](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/7856586851/p77607.png)

You can configure **outbound** and **inbound** access control policies.

## Outbound traffic control

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext).

2.  In the left-side navigation pane, choose **Security Policies** \> **Access Control**.

3.  Navigate to **Internet Firewall** \> **Outbound Policies**, click **Create Policy**.

    ![Outbound policies](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/8856586851/p77608.png)

4.  In the Create Outbound Policy dialog box, configure the policy parameters.

    ![Create outbound policy](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/8856586851/p77609.png)

    1.  In the first outbound policy, **allow** traffic from trusted IP addresses.
        1.  Configure the following parameters.

            |Parameter|Description|
            |---------|-----------|
            |**Source Type**|Select IP or Address Book.             -   **IP**: Specify only one CIDR block.
            -   **Address Book**: Select a pre-configured address book. The address book contains multiple CIDR blocks, which simplifies the configuration of access control policies. |
            |**Source**|Specify the source addresses that are allowed to access the Internet.             -   If Source Type is set to **IP**, enter a CIDR block, for example, 1.1.1.1/32.
            -   If Source Type is set to **Address Book**, find the target address book and click **Select** in the Actions column to configure IP addresses in the address book as the source. |
            |**Destination Type**|Select IP, Address Book, Domain Name, or Region.

**Note:** If you select Region, you can select a destination from all seven continents in the world and regions in China. The regions in China include 23 provinces, 4 municipalities, 5 autonomous regions, and 2 special administrative regions. |
            |**Destination**|Specify the destination address that can be accessed.|
            |**Protocol**|Specify the protocol used in outbound traffic, which can be TCP, UDP, or ICMP. If you are not sure about the protocol, select ANY, which means that all protocols are matched.|
            |**Port Type**|Select Port or Address Book.             -   **Port**: Enter only one port range.
            -   **Address Book**: Select a pre-configured **port address book**, which contains multiple ports. |
            |**Ports**|Specify the ports whose traffic is to be allowed or denied. Enter a port number range or select a port address book, depending on whether you select **Ports** or **Address Book** in the **Port Type** field.|
            |**Application**|Select the application to which the policy applies. **Note:** If **Destination Type** is set to Domain Name, you can set this parameter to HTTP, HTTPS, SMTP, or SMTPS. |
            |**Policy Action**|Specify whether the policy allows or denies traffic on the Internet firewall. Select Allow for this policy.|
            |**Description**|Enter a description to identify the policy.|
            |**Priority**|Configure the priority of the policy, which defaults to **Lowest**.|

        2.  Click **Submit**.

            **Note:** The created policy is displayed in the last row on the last page of the policy list.

    2.  In the second **outbound** policy, deny traffic from all other IP addresses.

        Set **Source** to `0.0.0.0/0` and **Policy Action** to **Deny** to prevent all unauthorized access activities. Configure the other parameters according to the descriptions in the preceding table.

    3.  Check that the priority of the **allow** policy on the trusted IP addresses is higher than that of the **deny** policy.
    **Note:** By default, Cloud Firewall assigns priorities to access control policies based on the order in which they are created. A new policy has a lower priority than all existing policies. For more information about the policy priorities, see [Change the priority of an access control policy](/intl.en-US/Access control/Change the priority of an access control policy.md).

    For more information about policy parameters, see [Parameters in an access control policy](#section_3bh_qhl_8pt).


## Inbound traffic control

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext).

2.  In the left-side navigation pane, choose **Security Policies** \> **Access Control**.

3.  Navigate to **Internet Firewall** \> **Inbound Policies**, click **Create Policy**.

    ![Inbound policies](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/8856586851/p77612.png)

4.  In the Create Inbound Policy dialog box, create a policy to **allow** traffic from trusted external IP addresses.

    Set **Source** to a trusted CIDR block or an IP address book. Set **Policy Action** to **Allow**. For information about other parameters, see the parameter descriptions in [Outbound traffic control](#section_xpk_j45_ggb).

    **Note:** If you set **Source Type** to Address Book for an inbound policy, you can set **Source** to an IP address book or cloud address book. If you set Destination Type to Address Book, you can only set Destination to an IP address book.

5.  In the second inbound policy, **deny** the traffic from all other external IP addresses.

    Set **Source** to `0.0.0.0/0` and **Policy Action** to **Deny** to prevent all unauthorized access activities.

6.  Check that the priority of the **allow** policy on the trusted IP addresses is higher than that of the **deny** policy.


## Check whether the policies have taken effect

A created policy takes effect immediately. However, if the policy parameters are invalid or the Internet firewall is disabled, the policy does not take effect.

In the policy list, find the target policy and click the number in the Hits column. The Traffic Logs page appears. If the name of the policy is displayed in the **Policy Name** column, this policy has taken effect.

![View access control policies](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/8856586851/p77614.png)

**Note:** If you delete a policy, the allow or deny action configured in this policy becomes invalid. Exercise caution when you perform this operation.

## Parameters in an access control policy

|Parameter|Description|
|---------|-----------|
|Source Type|The type of the source address. You can select IP or Address Book. -   If you select **IP**, enter a CIDR block in the **Source** field.
-   If you select **Address Book**, set **Source** to a pre-configured address book.

You can add multiple IP addresses to an address book to simplify the policy configuration. |
|Source|The source IP address or CIDR block of the traffic. **Note:** You can only specify one CIDR block, for example, 1.1.1.1/32.

 If you set **Source Type** to **Address Book**, select a pre-configured address book as the source.

**Note:**

-   In an outbound policy, the source can only be an IP address book, but the destination can be an IP address book, domain address book, or cloud address book.
-   In an inbound policy, the source can be an IP address book or cloud address book, but the destination can only be an IP address book. |
|Destination Type|-   **IP**: Set the destination to an IP address or CIDR block.
-   **Address Book**: Set the destination to an address book.
-   **Domain Name**: Set the destination to a domain name. You can specify a wildcard domain name, for example, `*.aliyun.com`.

**Note:** By default, if an HTTP header does not contain the host field or an HTTPS request does not contain the Server Name Indication \(SNI\), Cloud Firewall **allows** the traffic.

-   **Region**: Set the destination to a region. You can select a region inside or outside China. |
|Destination|Set the destination to a CIDR block. If you set **Destination Type** to Domain Name, set the destination to a domain name. Wildcard domain names are supported.

 **Note:**

-   In an outbound policy, the source can only be an IP address book, but the destination can be an IP address book, domain address book, or cloud address book.
-   In an inbound policy, the source can be an IP address book or cloud address book, but the destination address book can only be an IP address book. |
|Protocol|-   ANY \(All protocols are matched.\)
-   TCP
-   UDP
-   ICMP |
|Port Type|Select **Port** or **Address Book**. -   **Port**: You can specify only one port range.
-   **Address Book**: You can select a pre-configured **port address book**, which contains multiple ports. |
|Ports|You can specify a port range. 0/0 indicates all ports can be matched. **Note:** If you set Protocol to ICMP, the destination ports are not required. If you set Protocol to `ANY`, the destination ports you specify do not take effect in ICMP traffic control. |
|Application|You can set the application to ANY, HTTP, HTTPS, Memcache, MongoDB, MQTT, MySQL, RDP, Redis, SMTP, SMTPS, SSH, or VNC. If **Protocol** is set to TCP, multiple applications are available. Otherwise, you can only set the application to ANY.

 **Note:** Cloud Firewall identifies applications based on packet characteristics, instead of port numbers. If Cloud Firewall fails to identify the application in a packet, it **allows** the packet. |
|Policy Action|Specify whether the policy allows or denies traffic. -   **Allow**: Matched traffic is allowed.
-   **Deny**: Matched traffic is denied without notifications.
-   **Monitor**: Matched traffic is monitored but allowed. After you observe the traffic for a period of time, you can change the policy action to **Allow** or **Deny**. |
|Description|Enter a description to identify the policy.|
|Priority|The priority of the policy, which defaults to Lowest. -   **Lowest**: The policy takes effect in the last priority.
-   **Highest**: The policy takes effect in the first priority. |


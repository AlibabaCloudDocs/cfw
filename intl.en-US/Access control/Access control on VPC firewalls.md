# Access control on VPC firewalls

This topic describes how to configure access control policies on VPC firewalls. Cloud Firewall uses VPC firewalls to detect and control traffic between VPCs.

VPC firewalls are not enabled by default. Before you configure access control policies for VPCs, you must create and enable a VPC firewall.

Access control policies take effect only after you enable the VPC firewall.

![VPC Firewall](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/7313686851/p77683.png)

## How it works

A VPC firewall allows all traffic by default. If you want to control traffic between VPCs, you can configure access control policies to deny traffic from untrusted sources. You can also allow traffic from trusted sources and deny traffic from all other sources.

## Procedure

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext).
2.  In the left-side navigation pane, choose **Security Policies** \> **Access Control**.
3.  On the VPC Firewall tab, click **Create**.

    ![Add a policy](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/7313686851/p77685.png)

4.  In the Create VPC Firewall Policy dialog box, configure the policy. For information about parameters in a policy, see the [Policy parameters](#table_uwr_dgz_sd3) table in this topic.

    ![Add a VPC firewall policy](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/7313686851/p77694.png)

    You can choose one of the following configuration methods based on your needs:

    -   Create a policy to **deny** traffic from untrusted sources.
    -   Create a policy to **allow** traffic from trusted sources, and then create another to **deny** traffic from all other sources. Make sure that the **allow** policy has a higher priority than the **deny** policy. For more information about policy priorities, see [Change the priority of an access control policy](/intl.en-US/Access control/Change the priority of an access control policy.md).
    **Note:** A VPC firewall allows all traffic by default.


Policy parameters

|Parameter|Description|
|---------|-----------|
|**Source Type**|The type of the traffic source. You can select IP or Address Book. -   If you select **IP**, enter a CIDR block in the **Source** field.
-   If you select **Address Book**, select a pre-configured address book in the **Source** field.

**Note:** You can add multiple IP addresses to an address book to simplify policy configuration. |
|**Source**|The source CIDR block of the traffic. **Note:** You can enter only one CIDR block, for example, 1.1.1.1/32.

 If you set **Source Type** to **Address Book**, select a pre-configured address book. |
|**Destination Type**|-   **IP**: Set the destination to a CIDR block.
-   **Address Book**: Set the destination to an address book.
-   **Domain Name**: Set the destination to a domain name. Wildcard domain names are supported, for example, \*.aliyun.com.

**Note:** By default, if an HTTP header does not contain the host field or an HTTPS request does not contain the Server Name Indication \(SNI\), Cloud Firewall **allows** the traffic. |
|**Destination**|The destination of the traffic. You can enter only one CIDR block. If you set **Destination Type** to Domain Name, enter a domain name. Wildcard domain names are supported, for example, \*.aliyun.com. |
|**Protocol**|-   ANY \(All protocols are matched.\)
-   TCP
-   UDP
-   ICMP |
|**Port Type**|You can select Ports or Address Book. -   **Ports**: Specify only one port range.
-   **Address Book**: Select a pre-configured **port address book**. A port address book contains multiple ports, which simplifies policy configuration. |
|**Ports**|You can specify a port range. 0/0 indicates all ports can be matched. **Note:** If you set Protocol to ICMP, the destination ports are not required. If you set Protocol to ANY, the destination ports you specify do not take effect in ICMP traffic control. |
|**Application**|You can set the application to ANY, HTTP, HTTPS, Memcache, MongoDB, MQTT, MySQL, RDP, Redis, SMTP, SMTPS, SSH, or VNC. If **Protocol** is set to TCP, multiple applications are available. Otherwise, you can only set the application to ANY.

 **Note:** Cloud Firewall identifies applications based on packet characteristics, instead of port numbers. If Cloud Firewall fails to identify the application in a packet, it **allows** the packet. |
|**Policy Action**|Specify whether the VPC firewall allows or denies traffic. -   **Allow**: Matched traffic is allowed.
-   **Deny**: Matched traffic is denied and no notifications are sent.
-   **Monitor**: Matched traffic is monitored but allowed. After you observe the traffic for a period of time, you can change the policy action to Allow or Deny. |
|**Description**|Enter a description to identify the policy.|
|**Priority**|The priority of a policy, which defaults to Lowest. -   **Lowest**: The policy takes effect in the last priority.
-   **Highest**: The policy takes effect in the first priority. |


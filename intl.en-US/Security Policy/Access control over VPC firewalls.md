# Access control over VPC firewalls {#concept_vgy_wgr_ggb .task}

This topic describes access control over VPC firewalls.

VPC firewalls are not automatically created. Before you create access control policies between two VPC networks, create and enable a VPC firewall first.

The access control policies take effect only after you have enabled the VPC firewall.

![VPC firewall](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/83631/156749780648189_en-US.png)

Cloud Firewall supports access control over VPC firewalls. You can use a VPC firewall to detect and control the traffic between two VPC networks.

## Configure an access control policy {#section_7k2_h44_dws .section}

A VPC firewall allows all traffic by default. To control the traffic between VPC networks, you can deny the traffic from untrusted sources. Or, you can allow the traffic from trusted sources and then deny the traffic from all other sources.

## Procedure {#section_ha8_pwo_aak .section}

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext#/overview).
2.  In the left pane, choose **Security Policies** \> **Access Control** \> **VPC Firewall**.

    ![VPC Access Control](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/83631/156749780648035_en-US.png)

3.  Click **Create**.
4.  In the **Create VPC Firewall Policy** dialog box, configure the access control policy.

    ![Create VPC Firewall Policy](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/83631/156749780648187_en-US.png)

    You can choose either of the following configuration methods based on your needs:

    -   Create a policy to **deny** the traffic from untrusted sources.
    -   Create a policy to **allow** the traffic from trusted sources, and then create another policy to **deny** the traffic from all other sources. Make sure that the **allow** policy has a higher priority than the **deny** policy. For more information on policy priority, see [Set or modify the priority of an access control policy](../../../../reseller.en-US/Security Policy/Set or modify the priority of an access control policy.md#).
    For more information about the parameters in an access control policy, see the **Policy parameters** table in this topic.

    **Note:** A VPC firewall allows all traffic by default.


Policy parameters

|Parameter|Description|
|---------|-----------|
|Source type|The type of the source address. You can select IP or Address Book. -   If you select **IP**, enter a CIDR block in the **Source** field.
-   If you select **Address Book**, set **Source** to an existing address book.

You can add multiple IP addresses to an address book to simplify policy configuration.


 |
|Source|The source IP address or CIDR block of the traffic. **Note:** You can specify only one CIDR block, for example, 1.1.1.1/32.

 If you set **Source Type** to **Address Book**, select an existing address book as the source.

 |
|Destination type| -   **IP**: Set the destination to an IP address.
-   **Address Book**: Set the destination to an address book.
-   **Domain Name**: Set the destination to a domain name. You can specify a wildcard domain, for example, \*.a.com.

**Note:** If an HTTP header does not contain the host field or an HTTPS request does not contain Server Name Indication \(SNI\), the policy action is set to **Allow** by default.


 |
|Destination|Set the destination to a CIDR block. If you set the destination type to domain name, set the destination to a domain or a wildcard domain, for example, \*.a.com.

 |
|Protocol| -   ANY: Indicates any protocol.
-   TCP
-   UDP
-   ICMP

 |
|Destination ports|You can specify a port range. 0/0 indicates any port. **Note:** If you set the protocol to ICMP, the destination port configuration is not required. If you set the protocol to ANY, the destination port configuration does not take effect on ICMP traffic.

 |
|Application|You can set the application to ANY, HTTP, HTTPS, Memcached, MongoDB, MQTT, MySQL, RDP, Redis, SMTP, SMTPS, SSH, or VNC. If **Protocol** is set to TCP, multiple applications are available. Otherwise, you can set the application to ANY only.

 **Note:** The identification application relies on the application message characteristics \(the protocol identification is not based on the port\); when the application identification fails, the session traffic is Allow.

 |
|Policy action|Indicates whether Internet firewall allows or denies the traffic. -   **Allow**: The traffic is allowed.
-   **Deny**: The traffic is denied without any notification.
-   **Monitor**: The traffic is allowed. After monitoring the traffic for a period of time, you can change the policy action to Allow or Deny.

 |
|Description|A description or note about this policy. Enter a description of the policy so that you can distinguish the policies later.|
|Priority|Set the priority of the access control policy. The default priority is the Lowest.|


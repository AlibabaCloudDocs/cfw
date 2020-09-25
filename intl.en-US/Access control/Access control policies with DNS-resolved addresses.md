# Access control policies with DNS-resolved addresses

If the type of destination addresses is set to **Domain Name** in an access control policy for Internet Firewall, Cloud Firewall resolves the destination domain name and allows you to view IP addresses after the resolution. This topic describes how to configure access control policies for outbound traffic using the resolved addresses.

Since the release of the access control function, you can set the destination address type to **Domain Name** when configuring an access control policy for outbound traffic in the Cloud Firewall console. If you select **Domain Name**, the policy takes effect only on HTTP, HTTPS, SSL, SMTP, or SMTPS application packets transmitted using the TCP. \(The TCP is the default protocol and cannot be changed.\)

Now, Cloud Firewall updates the access control policies for **outbound** traffic by using dynamic DNS resolution, enhancing domain name-based access control. If the destination address type is set to **Domain Name**, Cloud Firewall automatically resolves the domain name and use the resolved address for access control. You can view the IP address after a resolution in real time and manually update it when it changes.

**Note:**

-   When the application type is HTTPS or SMTP, the host field is used for domain name-based access control.
-   When the application type is HTTPS, SMTP, or SSL, the SNI field is used for domain name-based access control.
-   You can view the IP addresses resolved from domains and use the IP addresses for access control only if the application protocol is not HTTP, HTTPS, SSL, SMTP, or SMTPS.

## How the protection feature works

For an access control policy for outbound traffic \(except HTTP, HTTPS, SSL, SMTP, or SMTPS traffic transmitted using the TCP\), DNS resolves the domain name into an IP address. After the policy is created, Cloud Firewall protects the IP address resolved from the domain name.

## Limits

Access control policies based on DNS-resolved addresses are not supported for the following scenarios:

-   Inbound traffic.

    Only access control policies for outbound traffic support this feature.

-   The domain name of the destination address is **Wildcard domain name**, such as \*.alibabacloud.com.
-   The destination address type is set to **Address Book**.
-   Users of Alibaba Gov Cloud, Alibaba Finance Cloud, and international site \(alibabacloud.com\).

    Only public cloud accounts at the China site support this feature.


**Note:** Pay attention to the following tips when you configure access control policies based on DNS resolution:

-   When you access external domain names from an ECS instance, you cannot change the default DNS server \(the ADNS\) configured for the instance. If you change the DNS server, the access control policy becomes invalid.
-   The access control policy may not meet your business needs if multiple domain names are resolved to the same IP address.

    For example, assume that you want to configure a policy to allow FTP traffic to access a.test.com. If the DNS resolution result of a.test.com based on the A record is 1.1.1.1, the rule issued to the engine allows FTP traffic to access the IP address 1.1.1.1. If b.test.com is also resolved to 1.1.1.1 based on the A record, FTP traffic bound to b.test.com is allowed.

-   Change of the DNS resolution result

    If the resolution result of domain name a.test.com changes from 1.1.1.1 to 2.2.2.2, the periodic resolution task of Cloud Firewall detects the change of the IP address in real time and automatically updates the access control policy. Cloud Firewall automatically refreshes the resolved IP address, ensuring that the real-time IP address corresponding to the domain name that you want to block or allow is included in the access control policy. The automatic update interval of a policy is 30 minutes. After the resolved address in a policy changes, the policy takes effect 30 minutes later.

    If you want to update your access control policy based on the dynamically changing resolved address, click **DNS** on the policy editing page to manually trigger DNS resolution and obtain the latest IP address, and then click **OK** to save the policy updates.


## Procedure

1.  Create an access control policy for **outbound** traffic.

    The following table describes the configuration items and methods of access control policies.

    |Item|Description|How to configure|
    |----|-----------|----------------|
    |**Source Type**|The type of the source address of data packets to which you want to apply the access control policy. Valid values:     -   **IP**: Specify one CIDR block.
    -   **Address Book**: Select a CIDR block from the IP address book that you have configured. The address book contains multiple CIDR blocks. This allows you to manage multiple IP addresses in policy configuration.
|Select IP or Address Book. If **Source Type** is set to IP, manually specify the CIDR block. If **Source Type** is set to Address Book, select a CIDR block from the address book that you have configured. |
    |**Source**|The source address of data packets to which you want to apply the access control policy.|Enter the source address. **Note:** You can specify only one CIDR block, for example, 1.1.1.1/32. |
    |**Destination Type**|The type of the destination address of the data packets to which you want to apply the access control policy. Valid values: IP Address, Address Book, Domain Name, and Region.|Select **Domain Name**.|
    |**Destination**|The destination address of the data packets to which you want to apply the access control policy.|Enter the domain name to which you want to apply the access control policy. **Note:** Only non-wildcard domain names support dynamic DNS resolution. |
    |**DNS**|Cloud Firewall automatically resolves destination domain names and controls access to the obtained IP addresses.|Click **DNS** to view the IP address resolved from the domain name in real time.|
    |**Protocol**|The protocol of the data packets to which you want to apply the access control policy. Valid values:     -   ANY: indicates any protocol.
    -   TCP
    -   UDP
    -   ICMP
|Select a protocol from the drop-down list.|
    |**Port Type**|You can select Ports or Address Book.|Select Ports.|
    |**Ports**|The ports that allow or block the outbound traffic.|Enter a port range. 0/0 indicates any port.|
    |**Application**|You can set the application to ANY, HTTP, HTTPS, Memcache, MongoDB, MQTT, MySQL, RDP, Redis, SMTP, SMTPS, SSH, or VNC. If **Protocol** is set to TCP, multiple application types are supported. If it is set to other values, you can only set the application type to ANY.

 **Note:** Applications are identified based on the characteristics of application packets \(protocol identification is not based on ports\). If application identification fails, the packets are **allowed**.

|Select the application type from the drop-down list.|
    |**Policy Action**|Indicates whether Internet firewall allows or denies the traffic.     -   **Allow**: The traffic is allowed.
    -   **Deny**: The traffic is denied without any notification.
    -   **Monitor**: The traffic is allowed. After you monitor the traffic for a period of time, you can change Policy Action to **Allow** or **Deny** based on your business needs.
|Select an action type from the drop-down list.|
    |**Description**|The description or note about a policy. Enter the description of the policy so that you can distinguish the policies later.|Enter the description.|
    |**Priority**|The priority of an access control policy. The default priority is Lowest.     -   **Lowest**: indicates that the access control policy takes effect at last.
    -   **Highest**: indicates that the access control policy takes effect first.
|Select **Highest** or **Lowest**.|

2.  Click **Submit** to complete the configuration of the access control policy.

    After the policy is submitted, you can view, edit, delete, copy, or change its priority by choosing **Internet Firewall** \> **Outbound Policies**.


You can check whether the policy takes effect by choosing **Firewall Settings** \> **Internet Firewall** in the Cloud Firewall console.


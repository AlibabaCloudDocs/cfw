# Configure access control policies for domain names

Cloud Firewall allows you to specify domain names as destinations for outbound traffic in access control policies. Cloud Firewall resolves domain names, displays resolution results, and controls the access to IP addresses that are mapped to the domain names. This topic describes how to configure an outbound access control policy for a domain name.

Cloud Firewall uses dynamic DNS resolution to optimize **outbound** access control policies for domain names. You can view the IP addresses that are mapped to the destination domain names and manually update the IP addresses.

If the destination in an outbound access control policy is set to a domain name, Cloud Firewall resolves the domain name into IP addresses and implements access control on the IP addresses. However, if the protocol type is set to TCP and the application type is set to HTTP, HTTPS, SSL, SMTP, or SMTPS, Cloud Firewall does not implement resolution or access control.

**Note:**

-   If the application type is HTTP or SMTP, Cloud Firewall first uses the host field to implement access control for domain names.
-   If the application type is HTTPS, SMTPS, or SSL, Cloud Firewall first uses the SNI field to implement access control for domain names.
-   If any application type other than HTTP, HTTPS, SSL, SMTP, or SMTPS is specified, Cloud Firewall resolves the domain names and implements access control. You can view the resolution results, which are IP addresses mapped to the domain names.

## Limits

Cloud Firewall does not apply access control policies for domain names in the following scenarios:

-   Access control policies are configured for inbound traffic.

    Only access control policies for outbound traffic are supported.

-   The destination is a **wildcard domain name**, for example, \*.example.com.
-   **Domain Address Books** is selected for the destination type

**Note:** When you configure access control policies for domain names, take note of the following items:

-   The default DNS server \(ADNS\) is used to resolve the external domain names that an ECS instance requests. DNS servers cannot be customized. If you change the DNS server of the ECS instance, the outbound access control policy for your ECS instance becomes invalid.
-   If multiple domain names are mapped to the same IP address, access control may be compromised.

    For example, assume that you want to configure an access control policy to allow FTP traffic destined for the domain name example1.aliyun.com. If the A record for the domain name example1.aliyun.com is 1.\*.\*.1, the FTP traffic destined for 1.\*.\*.1 is allowed. If the A record for the domain name example2.aliyun.com is also 1.\*.\*.1, the FTP traffic destined for example2.aliyun.com is also allowed.

-   If the IP addresses mapped to a domain name are changed, Cloud Firewall uses the up-to-date IP addresses and automatically updates the access control policy for the domain name.

    If the IP address mapped to the domain name example1.aliyun.com is changed from 1.\*.\*.1 to 2.\*.\*.2, Cloud Firewall automatically updates the access control policy for the domain name. Cloud Firewall uses the IP address 2.\*.\*.2 to ensure that the access control policy takes effect as expected. Cloud Firewall automatically updates the access control policy every 30 minutes, which means that a resolution record change is applied to the access control policy in 30 minutes.

    If you need to update your access control policy based on dynamic resolution records, click **DNS** on the policy editing page to manually trigger DNS resolution and obtain the up-to-date IP addresses. Then, click **OK** to save the policy updates.


## Procedure

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext).

2.  In the left-side navigation pane, choose **Security Policies** \> **Access Control**.

3.  Navigate to **Internet Firewall** \> **Outbound Policies**, click **Create Policy**.

    ![Outbound policies](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/8856586851/p77608.png)

4.  In the Create Outbound Policy dialog box, configure the policy parameters.

    ![Outbound access control policy for a domain name](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/1280247061/p77700.png)

    The following table describes the parameters of an access control policy.

    |Parameter|Description|Configuration method|
    |---------|-----------|--------------------|
    |**Source Type**|The type of the source address whose traffic is controlled by the access control policy. Valid values:     -   **IP**: Specify only one CIDR block.
    -   **Address Book**: Select a preconfigured address book. The address book contains multiple CIDR blocks, which simplifies the configuration of access control policies.
|Select IP or Address Book. If you set **Source Type** to IP, enter a CIDR block. If you set **Source Type** to Address Book, select a preconfigured IP address book. |
    |**Source**|The source address whose traffic is controlled by the access control policy.|Enter a source address. **Note:** You can specify only one public CIDR block, for example, 1.\*.\*.1/32. |
    |**Destination Type**|The type of the destination address whose traffic is controlled by the access control policy. Valid values: IP Address, Address Book, Domain Name, and Region.|Select **Domain Name**.|
    |**Destination**|The destination address whose traffic is controlled by the access control policy.|Enter a domain name. **Note:** Cloud Firewall implements access control based on dynamic DNS resolution only for non-wildcard domain names. |
    |**DNS**|Cloud Firewall automatically resolves the destination domain name and applies the access control policy to IP addresses mapped to the domain name.|Click **DNS** to view the IP addresses mapped to the domain name.|
    |**Protocol**|The protocol of traffic controlled by the access control policy. Valid values:     -   ANY: any protocol
    -   TCP
    -   UDP
    -   ICMP
|Select a protocol from the drop-down list.|
    |**Port Type**|The type of the port. Valid values: Ports and Address Book.|Select Ports.|
    |**Ports**|The port range. Traffic sent to the specified ports is controlled by the access control policy.|Enter a port range. 0/0 indicates any port.|
    |**Application**|The type of the application. Valid values: ANY, HTTP, HTTPS, Memcache, MongoDB, MQTT, MySQL, RDP, Redis, SMTP, SMTPS, SSH, and VNC. If you set **Protocol** to TCP, multiple application types are available. If you set Protocol to a value other than TCP, only ANY is available.

**Note:** Cloud Firewall identifies applications based on packet characteristics, instead of port numbers. If Cloud Firewall fails to identify an application, it **allows** the packets for the application.

|Select an application type from the drop-down list.|
    |**Policy Action**|Specifies whether the Internet firewall allows or blocks traffic.     -   **Allow**: If traffic meets the conditions that you specify for the access control policy, the traffic is allowed.
    -   **Deny**: If traffic meets the conditions that you specify for the access control policy, the traffic is blocked.
    -   **Monitor**: If traffic meets the conditions that you specify for the access control policy, the traffic is recorded and allowed. After you observe the traffic for a period, you can change the policy action to **Allow** or **Deny**.
|Select an action from the drop-down list.|
    |**Description**|A description of the access control policy to help identify the policy.|Enter a description.|
    |**Priority**|The priority of the access control policy. The default value is Lowest.     -   **Lowest**: The access control policy has the lowest priority and is the last one to take effect.
    -   **Highest**: The access control policy has the highest priority and is the first one to take effect.
|Select **Highest** or **Lowest**.|

5.  Click **Submit**.

    After you submit the access control policy, you can perform the following operations on the Outbound Policies page: view, edit, delete, or copy the policy, or change the priority of the policy.



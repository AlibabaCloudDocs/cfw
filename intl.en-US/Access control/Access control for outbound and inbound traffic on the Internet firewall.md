# Access control for outbound and inbound traffic on the Internet firewall

Cloud Firewall supports access control on the Internet firewall. You can configure policies to control the traffic between the Internet and your ECS instances.

**Internet Firewall** is enabled. Otherwise, the access control policies you configured on the Internet firewall do not take effect. For more information, see [Enable or disable Internet Firewall](/intl.en-US/Firewall Settings/Enable or disable Internet Firewall.md).

![Internet firewall](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/7856586851/p77607.png)

The Internet firewall allows you to configure **Outbound Policies** and **Inbound Policies**.

## Outbound access control

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext).

2.  In the left-side navigation pane, click**Access Control** \> **Access Control** .

3.  On the Internet Firewall page, click the Outbound Policies tab.

4.  On the Outbound Policies tab, click **Create Policy**.

5.  In the Create Outbound Policy dialog box, perform the following operations to create an outbound access control policy.

    ![Create an access control outbound policy](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/8856586851/p77609.png)

    1.  In the first outbound policy, **allow** traffic from trusted IP addresses.
        1.  Configure the parameters as described in the following table. For more information, see [Parameters in an access control policy](#section_3bh_qhl_8pt).

            |Parameter|Description|
            |---------|-----------|
            |**Source Type**|Select IP or Address Book.             -   **IP**: Specify only one CIDR block.
            -   **Address Book**: Select a preconfigured address book. The address book contains multiple CIDR blocks, which simplifies the configuration of access control policies. |
            |**Source**|The source IP address \(public IP address\) of the request.             -   If Source Type is set to **IP**, enter a CIDR block, for example, 1.1.1.1/32. You can configure only one CIDR block for each policy.
            -   If Source Type is set to Address Book, find the required address book and click Select in the Actions column to configure IP addresses in the address book as the source.

**Note:** You can select only one address book at a time. If you want to use multiple address books, click **Create Policy**. |
            |**Destination Type**|Select IP, Address Book, Domain Name, or Region.

**Note:** If you select Region, you can select a destination from all seven continents in the world and regions in China. The regions in China include 23 provinces, 4 municipalities, 5 autonomous regions, and 2 special administrative regions. |
            |**Destination**|Specify the destination addresses that can be accessed.             -   If Destination Type is set to **IP**, enter a CIDR block, for example, 1.1.1.1/32. You can configure only one CIDR block for each policy.
            -   If Destination Type is set to Address Book, find the required address book and click Select in the Actions column to configure IP addresses in the address book as the destination.

**Note:** You can select only one address book at a time. If you want to use multiple address books, click **Create Policy**.

            -   If Destination Type is set to **Domain Name**, Cloud Firewall automatically resolves the domain name and implements access control. For more information, see [Configure access control policies for domain names](/intl.en-US/Access control/Configure access control policies for domain names.md).
            -   If Destination Type is set to **Region**, select the region where the **destination** resides. |
            |**Protocol**|Select the protocol for outbound traffic. Valid values: TCP, UDP, ICMP, and ANY. If you are not sure about the protocol, select ANY, which means that all protocols are matched.|
            |**Port Type**|Valid values: Ports and Address Book.             -   **Ports**: Specify only one port range.
            -   **Address Book**: Select a preconfigured **port address book**. A port address book contains multiple ports, which simplifies policy configuration. |
            |**Ports**|Specify the ports on which you want to control traffic. If Port Type is set to Ports, enter a port number range. If Port Type is set to Address Book, find the required port address book and click Select in the **Actions** column.**Note:** You can select only one address book at a time. If you want to use multiple address books, click **Create Policy**. |
            |**Application**|Select the application to which the policy applies. **Note:** If **Destination Type** is set to Domain Name, you can set **Application** to HTTP, HTTPS, SMTP, or SMTPS. |
            |**Policy Action**|Specify whether the Internet firewall allows or denies the traffic of the protocol type. Select Allow in this step.|
            |**Description**|Enter a description to identify the policy.|
            |**Priority**|Configure the priority of the policy. The default priority is **Lowest**.|

        2.  Click **Submit**.

            **Note:** The created policy is displayed in the last row on the last page of the policy list.

    2.  In the second **outbound** access control policy, deny traffic from all unauthorized IP addresses.

        Set **Source** to `0.0.0.0/0` and **Policy Action** to **Deny** to prevent all unauthorized access activities. Configure other parameters based on the descriptions in the preceding table.

    3.  Make sure that the priority of the **allow** policy on the trusted IP addresses is higher than that of the **deny** policy.
    **Note:** By default, Cloud Firewall assigns priorities to access control policies based on the order in which the policies are created. A new policy has a lower priority than existing policies. For more information about the policy priorities, see [Change the priority of an access control policy](/intl.en-US/Access control/Change the priority of an access control policy.md).

    For more information about policy parameters, see [Parameters in an access control policy](#section_3bh_qhl_8pt).


## Inbound access control

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext).

2.  In the left-side navigation pane, click **Access Control** \> **Access Control** .

3.  On the **Internet Firewall** tab, click the **Inbound Policies** tab. Then, click **Create Policy**.

    ![Inbound policies](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/8856586851/p77612.png)

4.  In the Create Inbound Policy dialog box, create a policy to **allow** traffic from trusted external IP addresses.

    Set **Source** to a trusted CIDR block or IP address book. Set **Policy Action** to **Allow**. For information about how to configure other parameters, see the parameter descriptions in [Outbound access control](#section_xpk_j45_ggb).

    **Note:** If **Source Type** is set to Address Book, you can select an IP address book or a cloud address book as the **source**. If Destination Type is set to Address Book, you can select only an IP address book as the destination.

5.  Create another **inbound** access control policy to deny the traffic from all unauthorized external IP addresses.

    Set **Source** to `0.0.0.0/0` and **Policy Action** to **Deny** to prevent all unauthorized access activities.

6.  Make sure that the priority of the **allow** policy on the trusted IP addresses is higher than that of the **deny** policy.


## Export policies

You can export inbound or outbound policies for the Internet firewall based on your business requirements.

![Export policies](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/9389034161/p204925.png)

## Search for a specific policy based on the policy ID

Each access control policy for the Internet firewall has a policy ID. You can use this policy ID to identify a specific access control policy. This gives you the ability to know the status of the policy and adjust the policy based on your business requirements.

To view the ID of a policy, you can find the policy on the Internet Firewall tab and move the pointer over the ![Policy display icon](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/9389034161/p204923.png) icon in the **Description/Policy ID** column.

![View the ID of a policy](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/9389034161/p204922.png)

## Check whether access traffic hits a control policy

By default, an access control policy takes effect immediately after it is created. However, if the policy parameters are incorrectly configured or the Internet firewall is disabled, the policy does not take effect.

In the access control policy list, if the number in the **Hits** column is greater than 0 for an access control policy, access traffic hits the policy. The number in the **Hits** column indicates the number of times traffic hits the policy.

![Hits](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/9389034161/p183926.png)

You can click the number to go to the Traffic Logs tab. On the **Traffic Logs** tab, the names of access control policies the traffic hits are displayed in the **Policy Name** column.

**Note:** This tab displays the traffic generated in the last seven days. If the traffic hits an access control policy more than seven days ago, this policy is not displayed on the Traffic Logs tab.

## Parameters in an access control policy

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

## Related operations

After an access control policy is created, you can perform the following operations in the policy list: modify, delete, or copy the policy, or change its priority.

**Note:** After you delete an access control policy, Cloud Firewall does not control the traffic to which the policy applies. Perform this operation with caution.


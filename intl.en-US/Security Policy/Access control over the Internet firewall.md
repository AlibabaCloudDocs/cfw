# Access control over the Internet firewall {#concept_xx1_wgr_ggb .task}

Cloud Firewall supports access control over the Internet firewall. You can configure policies to control the traffic between the Internet and your servers.

To make sure that the Internal firewall policies take effect on an instance, you must enable **Internet firewall** for this instance.

![Internet firewall](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/83630/156750444047922_en-US.png)

Internet firewall allows you to configure both **outbound** and **inbound** access policies.

## Outbound traffic control {#section_xpk_j45_ggb .section}

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext#/overview).
2.  In the left pane, choose **Security Policies** \> **Access Control** \> **Internet Firewall** \> **Outbound Policies**. 

    ![Outbound Policies](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/83630/156750444035485_en-US.png)

3.  In the upper-left corner of the **Outbound Policies** tab page, click **Create**. The **Create Outbound Policy** dialog box is displayed. 

    ![Create Outbound Policy](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/83630/156750444035483_en-US.png)

4.  Create an **outbound** access control policy. 

    1.  In the first outbound policy, **allow** traffic from trusted source IP addresses.
        1.  Configure the rule parameters according to the steps in the table.

            |Steps|Parameter name|Parameter configuration|
            |-----|--------------|-----------------------|
            |1|**Source Type**|Select IP or Address Book.             -   **IP**: You can specify one CIDR block.
            -   **Address Book**: You can select from the IP address books that you have configured. An IP address book is a set of CIDR blocks. This allows you to manage multiple IP addresses in policy configuration.
 |
            |2|**Source**|The source address of the traffic. In this policy, set **Source** to internal IP addresses that can access the Internet.             -   If the source type is **IP**, you must set the source to a CIDR block. For example, 1.1.1.1/32.
            -   If the **source type** is Address Book, click **Select Address Book**, and select an IP address book as the **source**.
 |
            |3|**Destination Type**| You can select IP, Address Book, Domain Name, or Region.

**Note:** If you select Region, you can select a destination from the seven continents and all regions in China, including 23 provinces, four municipalities, five autonomous regions, and two special administrative regions.

 |
            |4|**Destination**|The destination of the traffic. In this policy, set **Destination** to a public IP address that can be accessed by an internal IP address.|
            |5|**Protocol**|The protocol of the traffic. If you are not sure which protocol is used, select ANY.|
            |6|**Port Type**|Select Ports or Address Book.             -   **Ports**: You can specify a port number or a port range.
            -   **Address Book**: You can select from the **port address books** that you have configured. A port address book contains multiple ports.
 |
            |7|**Ports**|The ports to which you want to apply this policy. If **Port Type** is Ports, specify a port number. You can also click **Select Address Book** to select a **port address book** that you have configured.|
            |8|**Application**|The application where the traffic is bound to. **Note:** If **Destination Type** is set to Domain Name, you can set **Application** to HTTP, HTTPS, SMTP, or SMTPS.

 |
            |9|**Policy Action**|Indicates whether Internet firewall allows or denies the traffic. Select Allow for this policy.|
            |10|**Description**|Enter a description of the policy so that you can quickly distinguish the purpose of each policy when you view it later.|
            |11|**Priority**|Select the priority of this policy, the default is the Lowest.|

        2.  Click **Submit**.

            **Note:** The latest policy is displayed in the last row on the last page of the policy list.

    2.  In the second **outbound** policy, deny the traffic from all internal IP addresses to the Internet.

        Set **Source** to `0.0.0.0/0` and **Policy Action** to **Deny** to prevent all unauthorized access activities. Configure the other parameters by referring to the preceding parameter descriptions.

    3.  Make sure that the priority of the **allow** policy on the trusted IP addresses is higher than that of the **deny** policy.
    **Note:** Cloud Firewall assigns priorities to access control policies based on the policy creation time. A new policy has a lower priority than all existing policies. For more information about the policy priority, see [Set or modify the priority of an access control policy](reseller.en-US/Security Policy/Set or modify the priority of an access control policy.md#).

    For more information about policy configuration parameters, see[Parameters of an access control policy](#section_3bh_qhl_8pt).


## Inbound traffic control {#section_ytb_p6d_ivw .section}

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext#/overview).
2.  In the left pane, choose **Security Policies** \> **Access Control** \> **Internet Firewall** \> **Inbound Policies**. 

    ![外对内](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/1318789/156750444055070_en-US.png)

3.  In the upper-left corner of the **Inbound Policies** tab page, click **Create**. The **Create Inbound Policy** dialog box is displayed. 

    ![新增外-内策略](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/1318789/156750444055072_en-US.png)

4.  In the first **inbound** policy, **allow** traffic from trusted external IP addresses. 

    Set **Source** to a trusted CIDR block or an IP Address Book that you have configured. Set **Policy Action** to **Allow**. For more information about configuring other parameters, see the parameter descriptions in [Outbound traffic control](#section_xpk_j45_ggb).

    **Note:** If you set **Source Type** to Address Book for an inbound policy, you can set **Source** to an IP address book or a cloud address book. If you set Destination Type to Address Book, you can only set Destination to an IP address book.

5.  In the second **inbound** policy, deny the traffic from all the other external IP addresses to the internal network. 

    Set **Source** to `0.0.0.0/0` and **Policy Action** to **Deny** to prevent all unauthorized access activities.

6.  Make sure that the priority of the **allow** policy on the trusted IP addresses is higher than that of the **deny** policy.

## Check whether the policies have taken effect {#section_p76_eep_mi6 .section}

A newly created policy takes effect immediately by default. However, if the policy parameters are invalid or the Internet firewall is disabled, the policy may not take effect.

In the policy list, click the number in the Hits column of a policy. The Traffic Logs page is displayed. If the name of the policy is displayed in the **Policy Name** column on the **Traffic Logs** page, this policy has taken effect.

![check policies](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/83630/156750444147923_en-US.png)

**Note:** After you delete a policy, the allow or deny policy that you have configured becomes invalid. Exercise caution.

## Parameters of an access control policy {#section_3bh_qhl_8pt .section}

|Parameter|Description|
|---------|-----------|
|Source type|The type of the source address. You can select IP or Address Book. -   If you select **IP**, enter a CIDR block in the **Source** field.
-   If you select **Address Book**, set **Source** to an existing address book.

You can add multiple IP addresses to an address book to simplify policy configuration.


 |
|Source|The source IP address or CIDR block of the traffic. **Note:** You can specify only one CIDR block, for example, 1.1.1.1/32.

 If you set **Source Type** to **Address Book**, select an exiting address book as the source.

**Note:** 

-   In an outbound policy, the source address book can be an IP address book only, and the destination address book can be an IP address book, a domain address book, or a cloud address book.
-   In an inbound policy, the source address book can be an IP address book or a cloud address book, and the destination address book can be an IP address book only.

 |
|Destination type| -   **IP**: Set the destination to an IP address.
-   **Address Book**: Set the destination to an address book.
-   **Domain Name**: Set the destination to a domain name. You can specify a wildcard domain, for example, `*.a.com`.

**Note:** 

    -   Only in an **outbound policy** can you set the destination type to IP, domain name, or region.
    -   If an HTTP header does not contain the host field or an HTTPS request does not contain Server Name Indication \(SNI\), the policy action is set to **Allow** by default.

 |
|Destination|Set the destination to a CIDR block. If you set the **destination type** to domain name, set the destination to a domain or a wildcard domain.

 **Note:** 

-   In an outbound policy, the source address book can be an IP address book only, and the destination address book can be an IP address book, a domain address book, or a cloud address book.
-   In an inbound policy, the source address book can be an IP address book or a cloud address book, and the destination address book can be an IP address book only.

 |
|Protocol| -   ANY: Indicates any protocol.
-   TCP
-   UDP
-   ICMP

 |
|Destination ports|You can specify a port range. 0/0 indicates any port. **Note:** If you set the protocol to ICMP, the destination port configuration is not required. If you set the protocol to `ANY`, the destination port configuration does not take effect on ICMP traffic.

 |
|Application|You can set the application to ANY, HTTP, HTTPS, Mamcache, MongoDB, MQTT, MySQL, RDP, Redis, SMTP, SMTPS, SSH, or VNC. If **Protocol** is set to TCP, multiple applications are available. Otherwise, you can set the application to ANY only.

 **Note:** The identification application relies on the application message characteristics \(the protocol identification is not based on the port\); when the application identification fails, the session traffic is Allow.

 |
|Policy action|Indicates whether Internet firewall allows or denies the traffic. -   **Allow**: The traffic is allowed.
-   **Deny**: The traffic is denied without any notification.
-   **Monitor**: The traffic is allowed. After monitoring the traffic for a period of time, you can change the policy action to **Allow** or **Deny**.

 |
|Description|A description or note about this policy. Enter a description of the policy so that you can distinguish the policies later.|
|Priority|Set the priority of the access control policy. The default priority is the Lowest.|


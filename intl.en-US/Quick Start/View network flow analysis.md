# View network flow analysis {#concept_nfg_rsh_cfb .concept}

Network flow analysis provides you with full visibility of flows across the entire network. You can view real-time activities in your assets, including threat events, network activities, traffic trends, access traffic blocked by IPS, and external connection activities.

## External Connections {#section_g54_3wl_cfb .section}

The **External Connections** page displays the details on your assets' external connections, including the connected domain names, external IP addresses, the applied protocols and your assets' info. This helps you identify the suspicious assets activities in a timely manner.

**Procedure**

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext#/overview).
2.  In the left-side navigation pane, go to **Network Flow Analysis** \> **External Connections** to check your assets' external connection activities.

    You can perform the follows operations on External Connections page:

    -   Monitor the summaries on external connection data, including the amounts of external domains, external IP addresses, assets request for external connections and the relevant protocols.

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21213/155638475945640_en-US.png)

    -   Monitor the outbound traffic analysis, including the average traffic and peak traffic.

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21213/155638475945641_en-US.png)

    -   Monitor the Top 10/20/50 traffic of external connections, with the relevant IP address, request/response rate, and logs recorded by Cloud Firewall.

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21213/155638475945642_en-US.png)

    -   Monitor the protocol analysis for external connections, including the information on applications, ports and corresponding connection numbers.

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21213/155638475945643_en-US.png)

    -   View the protocol details, and follow or ignore the specified protocols.

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21213/155638475945644_en-US.png)

    -   View the protocol details, and follow or ignore the specified protocols.

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21213/155638475945644_en-US.png)


## Internet Access {#section_v8o_cud_b5m .section}

The Internet Access page displays the details on the internet access traffic, including the open applications/ports/internet IP and the correlated cloud products.

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21213/155638476045649_en-US.png)

## VPC Access {#section_cfp_ud9_iut .section}

The VPC Access page displays the details on the traffic in VPC networks, including the traffic between VPCs, ranking of the sessions between VPCs, and the open ports and assets in VPC firewall.

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21213/155638476045652_en-US.png)

## IPS Analysis {#section_ixf_jwl_cfb .section}

The IPS Analysis page displays the details on blocked traffic in real time.

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21213/155638476045648_en-US.png)

**Procedure**

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext#/overview).
2.  In the left-side navigation pane, go to **Traffic Analysis** \> **IPS Analysis**.
3.  In the **Direction** area, click **Inbound** or **Outbound** to view the corresponding blocked inbound or outbound traffic.
4.  Select **Time** by one hour, one day, last seven days, one month, or a custom time range to display the required blocking traffic.

    You could monitor the following information on the blocked traffic:

    -   the most blocked source locations
    -   blocked destination IP addresses
    -   blocked applications
    -   IPS settings
    -   blocked event list

        In the blocked event list, specify the blocking source, direction, defense status, detection time, or source IP address to **search** for blocking events and to view details.


## All Access Activities {#section_p2h_jwl_cfb .section}

The All Access Activities page displays the details on activity data about all hosts protected by Cloud Firewall in real time. The data includes all traffic trends, top N source regions of inbound and outbound application access, the percentage of each region, top N session addresses, and the percentage of each address.

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21213/155638476045650_en-US.png)

**Procedure**

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext#/overview).
2.  In the left-side navigation pane, go to **Traffic Analysis** \> **All Access Activities**.

    You can view the historical trends for all the access activities in the last 15 minutes, 1 hour, 4 hours, 1 day, 7 days, or a custom time range.

    **Note:** You can specify any time range without limitations.

    Select a search condition from the **Condition** drop-down list and enter or select the condition details. Click **Search** to query the historical traffic trend based on the selected condition.

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21213/155638476045651_en-US.png)

    In the **Rankings of Visits by Traffic** area, view the top 10 source regions and application types with the most requested inbound/outbound traffic and top N session addresses. You can also view the percentage of each source location, application protocol, or session address.



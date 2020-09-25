# View network flow analysis

Network flow analysis provides you with full visibility of flows across the entire network. You can view real-time activities in your assets, including threat events, network activities, traffic trends, access traffic blocked by IPS, and external connection activities.

## External Connections

The **External Connections** page displays the details on your assets' external connections, including the connected domain names, external IP addresses, the applied protocols and your assets' info. This helps you identify the suspicious assets activities in a timely manner.

**Procedure**

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext#/overview).
2.  In the left-side navigation pane, go to **Network Flow Analysis** \> **External Connections** to check your assets' external connection activities.

    You can perform the follows operations on External Connections page:

    -   Monitor the summaries on external connection data, including the amounts of external domains, external IP addresses, assets request for external connections and the relevant protocols.

        ![](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21213/156689774645640_en-US.png)

    -   Monitor the outbound traffic analysis, including the average traffic and peak traffic.

        ![](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21213/156689774645641_en-US.png)

    -   Monitor the Top 10/20/50 traffic of external connections, with the relevant IP address, request/response rate, and logs recorded by Cloud Firewall.

        ![](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21213/156689774745642_en-US.png)

    -   Monitor the protocol analysis for external connections, including the information on applications, ports and corresponding connection numbers.

        ![](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21213/156689774745643_en-US.png)

    -   View the protocol details, and follow or ignore the specified protocols.

        ![](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21213/156689774745644_en-US.png)

    -   View the protocol details, and follow or ignore the specified protocols.

        ![](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21213/156689774745644_en-US.png)


## Internet Access

The Internet Access page displays the details on the internet access traffic, including the open applications/ports/internet IP and the correlated cloud products.

![](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21213/156689774745649_en-US.png)

## VPC Access

The VPC Access page displays the details on the traffic in VPC networks, including the traffic between VPCs, ranking of the sessions between VPCs, and the open ports and assets in VPC firewall.

![](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21213/156689774745652_en-US.png)

## IPS Analysis

The IPS Analysis page displays the details on blocked traffic in real time.

![](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21213/156689774845648_en-US.png)

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


## All Access Activities

The All Access Activities page displays the details on activity data about all hosts protected by Cloud Firewall in real time. The data includes all traffic trends, top N source regions of inbound and outbound application access, the percentage of each region, top N session addresses, and the percentage of each address.

![](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21213/156689774845650_en-US.png)

**Procedure**

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext#/overview).
2.  In the left-side navigation pane, go to **Traffic Analysis** \> **All Access Activities**.

    You can view the historical trends for all the access activities in the last 15 minutes, 1 hour, 4 hours, 1 day, 7 days, or a custom time range.

    **Note:** You can specify any time range without limitations.

    Select a search condition from the **Condition** drop-down list and enter or select the condition details. Click **Search** to query the historical traffic trend based on the selected condition.

    ![](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21213/156689774845651_en-US.png)

    In the **Rankings of Visits by Traffic** area, view the top 10 source regions and application types with the most requested inbound/outbound traffic and top N session addresses. You can also view the percentage of each source location, application protocol, or session address.



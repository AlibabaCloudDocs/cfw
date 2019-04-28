# External connections {#concept_vc3_qk4_cfb .concept}

The **External Connections** page displays the details on your assets' external connections, including the connected domain names, external IP addresses, the applied protocols and your assets' info. This helps you identify the suspicious assets activities in a timely manner

## Procedure {#section_bdz_2r3_etc .section}

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext#/overview).
2.  In the left-side navigation pane, go to **Network Flow Analysis** \> **External Connections** to check your assets' external connection activities.

    You can perform the follows operations on External Connections page:

    -   Monitor the overview of external connection data, including the amounts of external domains, external IP addresses, assets request for external connections and the relevant protocols.

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21268/155645313345821_en-US.png)

        In the overview area of external connection data, risky event number and total number of each item are displayed.

        Click the **Risky** or **All** button to go to the detailed external connection list.

    -   Monitor the outbound traffic analysis, including the average traffic and peak traffic.

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21268/155645313345822_en-US.png)

        In **Outbound Traffic** module, you can monitor traffic rate within the selected time range.

        Click the time on the timeline, you can see the corresponding rankings for the most visited IPs of the outbound traffic. You can choose to display top 10, 20 or 50 outbound IPs by clicking the **Rankings of IP Addresses by Traffic** drop-down list.

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21268/155645313345823_en-US.png)

    -   Monitor the Top 10/20/50 traffic of external connections, with the relevant IP address, request/response rate, and logs recorded by Cloud Firewall.

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21268/155645313345824_en-US.png)

        Click **View Logs**, **Logs** \> **Access Log** is displayed, and automatically filtered with **Outbound** direction. You can check the details on the Outbound traffic, including the time of access, source/destination IP and port, access application, protocol, bytes/packets of the access traffic, and applied access control policy.

    -   Monitor the protocol analysis for external connections, including the information on applications, ports and corresponding connection numbers.

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/64123/155645313345705_en-US.png)

    -   View the protocol details, and **Follow**/**Ignore** or **View the Logs** of the specified protocols.

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/64123/155645313345705_en-US.png)

    -   Monitor the detailed outbound traffic list, including external domains, IP addresses and assets.

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/64123/155645313345699_en-US.png)

        In the **Action** column, you can view details or logs, follow/unfollow or ignore the specified external domain/IP address.

        Click **View Details** to open the details page of external domain/IPs.

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/64123/155645313445701_en-US.png)



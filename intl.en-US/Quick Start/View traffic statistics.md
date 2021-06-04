---
keyword: [Cloud Firewall, traffic statistics]
---

# View traffic statistics

The traffic analysis feature provides real-time traffic statistics, such as threats, network access activities, traffic trends, traffic blocked by the intrusion prevention system \(IPS\), and outbound connections.

Traffic statistics are the basis for configuring access control policies. Before you configure access control policies, we recommend that you check the traffic statistics of your assets.

## Outbound connections

The Outbound Connections page displays information about the traffic that is initiated from private and public IP addresses of Elastic Compute Service \(ECS\) instances. These IP addresses include source network address translation \(SNAT\) IP addresses. The information includes the traffic volumes, IP addresses, ports, and domain names. The information is used to detect suspicious hosts.

You can configure access control policies based on the traffic statistics on the Outbound Connections page.

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext).

2.  In the left-side navigation pane, choose **Traffic Analysis** \> **Outbound Connections**.

3.  On the Outbound Connections page, view details about the outbound connections from your assets over the last 1 hour, 24 hours, 7 days, or a custom time range.

    For more information, see [Outbound connections](/intl.en-US/Traffic Analysis/Outbound connections.md).


## Internet access

The Internet Access page displays information about the services that are provided by ECS instances and access to the ECS instances over the Internet. The information includes ports, applications, and IP addresses. The information is used to identify normal traffic and potential intrusions. You can configure access control policies for **outbound traffic** based on the traffic statistics on the Internet Access page.

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext).

2.  In the left-side navigation pane, choose **Traffic Analysis** \> **Internet Access**.

3.  On the Internet Access page, view the open public IP addresses, ports, and applications of your assets.


## VPC access

The VPC Access page displays information about the traffic between VPCs. The information is used to detect abnormal traffic and potential attacks.

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext).

2.  In the left-side navigation pane, choose **Traffic Analysis** \> **VPC Access**.

3.  On the VPC Access page, view information about the traffic between VPCs, rankings of sessions, open ports, and assets.


## All access activities

The All Access Activities page displays real-time traffic information about IP addresses.

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext).

2.  In the left-side navigation pane, choose **Traffic Analysis** \> **All Access Activities**.

3.  On the All Access Activities page, perform the following operations based on your business requirements:

    -   View all access activities and trend charts over the last 15 minutes, 1 hour, 4 hours, 1 day, 1 week, or a custom time range.

        **Note:** The time range that you can specify is not limited.

    -   Click the ![Drop-down icon](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/4867059161/p98238.png) icon next to **Condition**, select a search condition, and then enter or select the condition details. Then, Cloud Firewall displays historical traffic trends based on the condition.
    -   In the **Rankings of Visits by Traffic** section, view the top 10 traffic source locations, application protocols and percentages, and top 10 session addresses.


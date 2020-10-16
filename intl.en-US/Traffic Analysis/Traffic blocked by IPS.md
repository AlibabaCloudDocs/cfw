# Traffic blocked by IPS

The Traffic Blocked by IPS page displays real-time data of traffic blocked by the intrusion prevention system \(IPS\) of Cloud Firewall. The data includes source locations, destination IP addresses, and applications of the traffic, IPS modules used to block the traffic, and the traffic blocking event details. This topic describes data that is displayed on the Traffic Blocked by IPS page and the operations that you can perform on this page.

## Prerequisites

**Basic Policies** on the Intrusion Prevention page is turned on.

![Basic policies](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/7613382061/p77756.png)

## Overview

The Traffic Blocked by IPS page displays data of traffic blocked by the Internet firewall and VPC firewalls. You can view details on the Internet Traffic Blocking or VPC Traffic Blocking tab. To go to the Traffic Blocked by IPS page, choose **Traffic Analysis** \> **Traffic Blocked by IPS** in the left-side navigation pane.

![Traffic blocked by IPS](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/7613382061/p81782.png)

## Internet Traffic Blocking

On the Internet Traffic Blocking tab, you can view the inbound or outbound traffic that is blocked in the last one hour, one day, seven days, one month, or a custom time range within the last three months.

![Traffic Blocked by IPS](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/7613382061/p77498.png)

The Internet Traffic Blocking tab contains the following sections:

-   **The Most Blocked Source Locations** section displays the source and destination locations of inbound and outbound traffic blocked by the Cloud Firewall IPS.

    ![The Most Blocked Source Locations](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/7613382061/p77502.png)

-   The **Blocked Destination IP Addresses** section displays the destination IP addresses of inbound or outbound traffic blocked by the Cloud Firewall IPS.

    ![Blocked Destination IP Addresses](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/7613382061/p77504.png)

    If you want to view details about a blocked destination IP address, click the **View Logs** icon to go to the Log Audit page. In the log list, you can view the destination port and application of the IP address, and the actions that you can perform on the IP address.

-   The **Blocked Applications** section displays the top five applications whose inbound and outbound traffic is blocked by the Cloud Firewall IPS.

    ![Blocked Applications](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/8613382061/p77507.png)

-   The **Blocking Criteria** section displays the percentage of traffic blocked by each IPS module.

    ![Blocking Criteria](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/8613382061/p77508.png)

-   The **Detailed Data** section displays details about each traffic blocking event, including the risk level, number of times the event occurred, source IP address, and destination IP address.

    ![Detailed Data](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/8613382061/p77510.png)

    In the **Detailed Data** section, you can perform the following operations:

    -   Search for events based on the risk level, module, traffic direction, or time range.
    -   Click **View Details** in the **Action** column to check details about a traffic blocking event.

        ![Event details](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/8613382061/p77512.png)


## References

-   [FAQ](/intl.en-US/FAQ/FAQ.md)
-   [Intrusion prevention](/intl.en-US/Intrusion prevention/Intrusion prevention.md)


# Intrusion prevention

The Intrusion Prevention page displays real-time data of traffic blocked by the intrusion prevention system \(IPS\) of Cloud Firewall. The data includes the source locations, destination IP addresses, and applications of the traffic, along with the IPS module used to block the traffic and the details of traffic blocking events. This topic describes the data that is displayed on the Intrusion Prevention page and the operations that you can perform on this page.

## Prerequisites

**Basic Policies** on the Prevention Configuration page is turned on. Otherwise, Cloud Firewall cannot block traffic, record the traffic data, or display the data on the Intrusion Prevention page.

![Basic Policies switch](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/7613382061/p77756.png)

## Overview

The **Intrusion Prevention** page displays the details of protection operations performed by Cloud Firewall on inbound and outbound traffic over the Internet and between virtual private clouds \(VPCs\). You can switch between the Internet Traffic Blocking and VPC Traffic Blocking tabs to view the details of specific events.

**Note:** If your Cloud Firewall runs the Premium Edition, the VPC Traffic Blocking tab does not appear.

## Internet Traffic Blocking

On the Internet Traffic Blocking tab, you can view the blocking events of inbound and outbound traffic from the last one hour, one day, seven days, one month, or a custom time range. You can specify a time range only from the last three months.

The Internet Traffic Blocking tab contains the following sections:

-   **Prevention Statistics**: contains the Attack Statistics, Attack Distribution by Type, and Blocking Statistics widgets. The Blocking Statistics widget provides the following tabs:
    -   **Top Blocked Destination IP Addresses**: displays the top 5 destination IP addresses that are most frequently used among the statistics on traffic blocked by Cloud Firewall.

        If you want to view the details of a blocked destination IP address, click the **View Logs** icon to go to the Log Audit page. In the log list, you can view the destination port and application type for the IP address, and the action that is performed on the IP address.

    -   **Blocking Criteria**: displays the top 5 modules that are most frequently used by Cloud Firewall to block traffic.
    -   **Blocked Applications**: displays the top 5 types of applications that are most frequently requested among the statistics on traffic blocked by Cloud Firewall.
-   **Detailed Data**: displays the details about each traffic blocking event, including the risk level, number of times the event occurred, source IP address, and destination IP address.

    ![Detailed Data list](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/8613382061/p77510.png)

    In the **Detailed Data** section, you can perform the following operations:

    -   Specify conditions to search for events. The conditions include the risk level, module, traffic direction, and time range.
    -   Find an event and click **View Details** in the **Actions** column to view the details of the event.

        ![Details panel of an IPS blocking event](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/5958136261/p211164.png)

    -   On the right of the search box, click the ![Download icon](../images/p286642.png) icon to download intrusion prevention policies. ![Export intrusion prevention policies](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/5958136261/p286614.png)

## VPC Traffic Blocking

On the VPC Traffic Blocking tab, you can view the information about unusual events on the traffic blocked between VPCs by Cloud Firewall. The information includes the name, risk level, and attack type. You can also specify a time range to view the information.

On the VPC Traffic Blocking tab, you can perform the following operations:

-   Specify conditions and click **Search** to search for events. The conditions include the risk level, defense mode, attack type, and time range.
-   Find an event and click **View Details** in the Actions column to view the details of the event. The details include the event description, rule ID, and defense mode.

    ![Event details](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/5958136261/p77596.png)


## References

-   [Protection scope of Cloud Firewall](/intl.en-US/FAQ/Protection scope of Cloud Firewall.md)
-   [Prevention configuration](/intl.en-US/Intrusion Prevention/Prevention configuration.md)


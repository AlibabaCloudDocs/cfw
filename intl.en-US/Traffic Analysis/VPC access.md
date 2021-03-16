# VPC access

The VPC Access page of the Cloud Firewall console provides real-time information about traffic between virtual private clouds \(VPCs\). This way, you can detect suspicious traffic and mitigate risks at the earliest opportunity. The VPC Access page provides statistics on the traffic, IP addresses, sessions, ports, and assets involved in communications between VPCs.

The required VPC firewall is enabled. Otherwise, the **VPC Access** page does not provide traffic analysis data.

For more information about how to enable a VPC firewall, see [Activate Cloud Firewall](/intl.en-US/Quick Start/Activate Cloud Firewall.md).

## Procedure

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext)[Cloud Firewall console](https://partners-yundun.console.aliyun.com/?p=cfwnext).

2.  In the left-side navigation pane, choose **Traffic Analysis** \> **VPC Access**.

3.  In the upper-right corner of the **VPC Access** page, specify a time range for query.

    You can select the following time ranges from the time drop-down list: **Recent 1 Hours**, **Last 24 Hours**, and **Last 7 Days**. You can also customize a time range within the last seven days by using the date and time picker.

    ![Specify a time range](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/2805685161/p237768.png)

4.  In the upper part of the **VPC Access** page, select the required VPC and VPC firewalls.

    ![Specify the VPC](../images/p237771.png)

5.  View the data about access of the selected VPC.

    You can view the following data:

    -   **Traffic Between VPCs**: You can view the peak and average volumes of both inbound and outbound traffic of the VPC. You can also view the trends in both inbound and outbound traffic.
    -   **Ranking of IP Addresses by Traffic**: You can view the top 10, 20, or 50 IP addresses with the highest traffic. You can also view the details of inbound and outbound traffic for each IP address.
    -   **Ranking of Sessions Between VPCs by Visits and Traffic**: You can view the ranking of sessions between VPCs. You can also view the traffic volume, session type, number of sessions, and ports for each type of session.

        In the **Rankings of Sessions Between VPCs by Visits and Traffic** section, you can click **View** in the **Ratio** column to view the proportions of ports in a specific type of session.

    -   **Open Ports by Traffic**: You can view the proportions of all open ports.
    -   **Open Ports** and **Assets**: You can view the details of traffic between VPCs. The details include basic information about open ports and your assets.

        You can click the ![Download ](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/7617085161/p237696.png) icon in the upper-right corner above the port or asset list to download the open ports or assets to a CSV file to your computer for check and analysis.

        ![VPC流量信息](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/6225315851/p58398.png)



# Internet access

The Internet Access page of the Cloud Firewall console provides an overview of the normal and abnormal inbound traffic of your assets, including the information about open applications, open ports, open public IP addresses, and cloud services to which inbound traffic flows.

The Internet firewall is enabled. Otherwise, the **Internet Access** page does not provide traffic analysis data.

For more information about how to enable the Internet firewall, see [Activate Cloud Firewall](/intl.en-US/Quick Start/Activate Cloud Firewall.md).

## Procedure

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext)[Cloud Firewall console](https://partners-yundun.console.aliyun.com/?p=cfwnext).

2.  In the left-side navigation pane, choose **Traffic Analysis** \> **Internet Access**.

3.  In the upper-right corner of the **Internet Access** page, specify a time range for query.

    You can select the following time ranges from the time drop-down list: **Last 1 Hour**, **Last 24 Hours**, and **Last 7 Days**. You can also customize a time range within the last seven days by using the date and time picker.

    ![Specify a time range](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/2805685161/p237768.png)

4.  View the data about access over the Internet.

    You can view the following data:

    -   Overview of Internet access activities: You can view the numbers of total and risky items below **Open Public IP Addresses**, **Open Ports**, and **Open Applications**. You can also view the number of risky public IP addresses specified by **Public IP** and the total number of open ports specified by **Open ports** below **Cloud Products**.

        ![Overview of Internet access activities](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/1998570061/p77461.png)

    -   **IP Traffic** and **Trends of Traffic**

        ![IP Traffic and Trends of Traffic](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/1998570061/p77478.png)

        -   **IP Traffic**: You can view public IP addresses in descending order based on their transmission rates at a specific point in time. The point is represented by **IP Ranking** in the x-axis of the chart in the **Trends of Traffic** section.

            You can perform the following operations in the **IP Traffic** ranking list:

            -   Find a public IP address and choose **More** \> **View Trend**. Then, you can view the traffic trend of the public IP address in the **Trends of Traffic** section.
            -   Find a public IP address and choose **More** \> **View Logs**. Then, the **Traffic Logs** tab of the **Log Audit** page appears. You can view the inbound traffic of the public IP address. For more information, see [Log audit](/intl.en-US/Logs/Log audit.md).
        -   **Trends of Traffic**: You can view the peak transmission rates of request and response traffic on all assets.
    -   Details of Internet access activities: You can view **Open Public IP Addresses**, **Open Ports**, **Open Applications**, **Details**, and **Cloud Products**.

        You can click the ![Download ](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/7617085161/p237696.png) icon in the upper-right corner above each list to download the data to a CSV file to your computer for check and analysis.

        ![Details of Internet access activities](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/1998570061/p77481.png)



# Internet access

The Internet Access page in the Cloud Firewall console provides an overview of normal and abnormal inbound traffic of your assets, including information about open applications, open ports, open public IP addresses, and cloud products to which inbound traffic flows.

The **Internet Access** page displays traffic analysis data only after you activate Cloud Firewall. For information about how to activate Cloud Firewall, see [Activate Cloud Firewall](/intl.en-US/Quick Start/Activate Cloud Firewall.md).

## Procedure

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext).

2.  In the left-side navigation pane, choose **Traffic Analysis** \> **Internet Access**.

3.  On the **Internet Access** page, perform the following operations:

    -   View overall information about Internet access activities, including the number of total and risky open applications, open ports, and open public IP addresses, as well as the number of public IP addresses and open ports of the cloud products.

        ![Internet access statistics](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/1998570061/p77461.png)

    -   View information in the **IP Traffic** and **Trends of Traffic** sections. The **IP Traffic** section lists public IP addresses in descending order based on their transmission rates at a specified time point. The time point is represented by **IP Ranking** in the horizontal axis in the chart in the **Trends of Traffic** section. The **Trends of Traffic** section displays the peak transmission rates of request and response traffic on all assets.

        ![IP traffic and traffic trends](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/1998570061/p77478.png)

        In the **IP Traffic** section, find the IP address that you want to query, click the drop-down arrow next to **More** in the Actions column, and then click **View Logs**. On the **Traffic Logs** tab, view the inbound traffic of the IP address.

        In the **IP Traffic** section, find the IP address that you want to query, click the drop-down arrow next to **More** in the Actions column, and then click **View Trend**. In the **Trends of Traffic** section, view traffic trends of the IP address.

    -   View the details of Internet access activities, including open public IP addresses, open ports, open applications, assets, and cloud products.

        ![Internet access details](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/1998570061/p77481.png)


## References

[Traffic from unknown applications accounts for a large proportion of all traffic. Does this occur because Cloud Firewall cannot identify the applications that generate traffic in the Internet?](/intl.en-US/FAQ/FAQ.md)


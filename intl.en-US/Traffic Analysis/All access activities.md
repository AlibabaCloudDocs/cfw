# All access activities

The All Access Activities page displays real-time activity information about all hosts protected by Cloud Firewall. Such information includes traffic trends, as well as source locations and sessions of inbound and outbound traffic.

The All Access Activities page displays the analysis data only after you activate Cloud Firewall. For information about how to activate Cloud Firewall, see [Activate Cloud Firewall](/intl.en-US/Quick Start/Activate Cloud Firewall.md).

## Procedure

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext).

2.  In the left-side navigation pane, choose **Traffic Analysis** \> **All Access Activities**.

3.  On the All Access Activities page, view the threat activities and trend charts in the last 15 minutes, 1 hour, 4 hours, 1 day, 7 days, or a specified time range.

    ![Select a time range](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/9621670061/p77534.png)

    **Note:** You can specify a time range as required.

    -   Select a search condition from the **Condition** drop-down list and enter or select the condition details. Click **Query** to query historical traffic trends that meet the condition. To delete the search condition, click **Reset**.

        ![Search condition](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/9621670061/p77535.png)

        **Note:** You can click **Add** to add search conditions. All conditions take effect at the same time when you click Query. You can configure a maximum of three conditions.

    -   In the **Historical Trends** section, view the trend charts of inbound and outbound traffic, the number of new connections, and concurrent traffic.

        ![Historical trends](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/9621670061/p77542.png)

        You can select **Traffic**, **New**, or **Concurrent** to switch between the trend charts of inbound and outbound traffic, the number of new connections, and the inbound and outbound concurrent traffic.

        **Note:** A trend chart displays traffic data in the last 15 minutes, 1 hour, 4 hours, 1 day, 7 days, or a specified time range. You can specify a time range as required.

    -   In the **Rankings of Visits by Traffic** section, you can view top 10 source locations and applications of inbound and outbound traffic, as well as the percentages of traffic for each source location and application.

        ![Rankings of Visits by Traffic](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/0721670061/p77544.png)

    -   Click **View Details** to check the statistics on source or destination locations or application protocols.
    -   Click **Add to Condition** to add the condition to the query condition setting section. After you click Query, the **Historical Trends** and **Rankings of Visits by Traffic** sections display trend charts of access activities that meet the condition.

## References

[Traffic from unknown applications accounts for a large proportion of all traffic. Does this occur because Cloud Firewall cannot identify the applications that generate traffic in the Internet?](/intl.en-US/FAQ/FAQ.md)


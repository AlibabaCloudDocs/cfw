# Log reports

Log reports in Cloud Firewall provide data collected by Log Analysis, such as basic traffic metrics, inbound and outbound traffic distribution. You can specify a time range, subscribe to log reports, and set a refresh frequency to view data in the dashboards.

The **Status** switch in the upper-right corner of the **Log Analysis** page must be **turned on**. If the switch is **turned off**, Log Analysis is disabled, and you cannot view log reports.

![Enable Log Analysis](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/3206686851/p64720.png)

## Procedure

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext).

2.  In the left-side navigation pane, choose **Logs** \> **Log Analysis**.

3.  In the upper-right corner of the **Reports** tab, click **Please Select**.

    ![Select a time range](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/3206686851/p77800.png)

4.  On the **Time** page, specify a time range for displaying reports of Internet traffic logs. You can specify a time range in the **Relative**, **Time Frame**, or **Custom** section.

    ![Time settings](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/3206686851/p64732.png)

    |Section|Description|
    |-------|-----------|
    |Relative|Displays log data collected within a specified time range going back from the current time. This time range is accurate to seconds. Assume that the current time is 2019-10-17 23:08:00. The value 2019-10-17 23:07:00~2019-10-17 23:08:00 indicates that log data collected in the last minute is displayed. You can specify a time range in days, hours, minutes, or seconds. |
    |Time Frame|Displays log data collected within a specified time range. For example, the value 2019-10-10 00:00:00~2019-10-17 00:00:00 indicates that log data was collected for the week starting from 2019-10-10 00:00:00. You can specify a time range in days, hours, or minutes. |
    |Custom|Displays log data collected within a custom time range. The start and end time is accurate to minutes.|

    After you specify a time range, all dashboards on the Reports tab are refreshed to display data within this time range.

    For more information about the dashboards, see [Log report dashboards](#section_y10_64h_n3u).

    **Note:** The specified time range is only valid on the current page. The next time you open the Reports tab, the time range of the dashboards is restored to the default.

5.  On the **Reports** tab, perform operations on a dashboard.

    In the upper-right corner of the target dashboard, click the ![Function button](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/4206686851/p64739.png) icon to show the menu.

    The menu of a dashboard supports the following operations:

    -   **Select Time Range**: The dashboard displays basic metrics within the specified time range. You can specify a relative time range, time frame, or custom time range. For more operations, see the descriptions in [step 4](#step_bdh_v13_mwo).
    -   **Download Log**: Select this option to save the logs as an Excel file to your computer.
    -   **Download Chart**: Select this option to save the dashboard as a PNG file to your computer.
    -   **Preview Query Statement**: Click the ![Preview](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/4206686851/p64744.png) icon to view the query statement of the log metrics in the dashboard. You can use the statement to query the log data on the Logs tab. For more information about log queries, see [Log search and analysis](/intl.en-US/Logs/Log analysis/Log analysis.md).

        ![query statement](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/4206686851/p64745.png)

6.  Subscribe to log reports. You can specify the frequency at which the system sends log data notifications by email or DingTalk chatbot.

    In the upper-right corner of the Reports tab, click **Subscribe**. On the **Create Subscription** page that appears, subscribe to Internet traffic log reports.

    1.  In Subscription Configuration, configure the following parameters.

        |Parameter|Description|
        |---------|-----------|
        |**Subscription Name**|The name of the log report subscription. A default name is provided, but you can change it as needed.|
        |**Frequency**|The frequency at which log report notifications are sent. Valid values:         -   **Hourly**: A notification is sent every hour.
        -   **Daily**: A notification is sent each day at a specified hour between 00:00 and 23:00.
        -   **Weekly**: A notification is sent each week on a specified day at a specific hour between 00:00 and 23:00.
        -   **Fixed Interval**: A notification is sent at a specified interval. You can select **Days** or **Hours**.
        -   **Cron**: Use a cron expression to customize the frequency. The time specified in a cron expression is accurate to minutes and is in the 24-hour notation. You can refer to the examples in the console to write a cron expression. |
        |**Add Watermark**|The address that sends the notification is attached to the image as a watermark. It can be an email address or a webhook URL of the DingTalk chatbot.|

    2.  Click **Next** to set a notification type.

        ![Notification type](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/4206686851/p64752.png)

        |Notification type|Parameter|Description|
        |-----------------|---------|-----------|
        |Email|**Recipients**|The email address of the recipient. You can add more than one recipient.|
        |**Subject**|The subject of the email. A default subject is provided, but you can change it as needed.|
        |WebHook-DingTalk Bot|**Request URL**|The webhook URL requested. For more information about how to obtain the webhook URL, see [Configure DingTalk chatbot notifications](/intl.en-US/Settings/Notifications.md).|
        |**Title**|The title of the webhook. A default title is provided, but you can change it as needed.|

    3.  Click **Submit**.

    4.  In the dialog box that appears, click **OK**.

    After the subscription is created, you can move the pointer over the **Subscribe** button on the **Reports** tab to view the subscription.

    You can also click **Subscribe** to **modify** the subscription configurations and notification type or **cancel** the subscription.

    ![Modify or cancel the subscription](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/4206686851/p64754.png)

    **Note:** You can only create one subscription. To create a new subscription, you must **cancel** the existing one.

7.  In the upper-right corner of the **Reports** tab, click **Refresh** to set the frequency to refresh log reports.

    ![Refresh](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/4206686851/p64756.png)

    |Frequency|Description|
    |---------|-----------|
    |Once|Trigger a refresh immediately.|
    |Auto Refresh|Specify a refresh frequency. You can set it to 15 seconds, 60 seconds, 5 minutes, or 15 minutes.|


## Log report dashboards

Log reports provide a global view of Internet traffic, including basic traffic metrics, inbound and outbound traffic trends, and traffic distribution. The following table describes all dashboards supported by Cloud Firewall.

|Dashboard|Type|Default time range|Description|Example|
|---------|----|------------------|-----------|-------|
|Total number of Intercepting|Numeric value|1 hour \(relative\)|The number of Internet access requests blocked by Cloud Firewall for a specified time range.|10|
|Inbound Traffic|Numeric value|1 hour \(relative\)|The volume of inbound traffic from the Internet for a specified time range.|10 MB|
|Outbound Traffic|Numeric value|1 hour \(relative\)|The volume of outbound traffic to the Internet for a specified time range.|10 GB|
|SSH Access|Numeric value|1 hour \(relative\)|The number of SSH access requests for a specified time range.|10|
|RDP Access|Numeric value|1 hour \(relative\)|The number of RDP access requests for a specified time range.|10|
|FTP Access|Numeric value|1 hour \(relative\)|The number of FTP access requests for a specified time range.|10|
|Interception trend|Line chart|1 hour \(relative\)|The trend for the number of times inbound traffic is blocked for a specified time range.|-|
|Intercepted Source Applications|Pie chart|1 hour \(relative\)|The top 10 applications \(such as HTTP, SNMP, SIP, and SSH\) requested by blocked inbound traffic for a specified time range.|-|
|Sources – Global|World map|1 hour \(relative\)|The geographical distribution of inbound traffic sources for a specified time range.|-|
|Source Applications – Top 10|Pie chart|1 hour \(relative\)|The top 10 applications \(such as HTTP and SSH\) requested by inbound traffic for a specified time range.|-|
|Source Regions – Top 10|Pie chart|1 hour \(relative\)|The top 10 source regions with the most inbound traffic for a specified time range.|-|
|Source Ports – Top 20|Treemap chart|1 hour \(relative\)|The top 20 ports that are accessed by inbound traffic for a specified time range.|-|
|Interception trend|Line chart|1 hour \(relative\)|The trend for the number of times outbound traffic is blocked for a specified time range.|-|
|Intercepted External Applications|Pie chart|1 hour \(relative\)|The top 10 applications \(such as HTTP and SSH\) requested by blocked outbound traffic for a specified time range.|-|
|External Ports – Top 20|Treemap chart|1 hour \(relative\)|The top 20 ports accessed by outbound traffic for a specified time range.|-|
|External IP Addresses – Top 10|Pie chart|1 hour \(relative\)|The top 10 IP addresses requested by outbound traffic for a specified time range.|-|
|External Domains – Top 10|Treemap chart|1 hour \(relative\)|The top 10 domain names requested by outbound traffic for a specified time range.|-|
|External Applications – Top 10|Pie chart|1 hour \(relative\)|The top 10 applications \(such as HTTP and SSH\) requested by outbound traffic for a specified time range.|-|


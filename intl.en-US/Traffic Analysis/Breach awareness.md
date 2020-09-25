# Breach awareness

The Breach Awareness page displays intrusion events detected by the intrusion prevention system \(IPS\).

The Breach Awareness page displays the detected intrusion events only after you enable Internet Firewall. For information about how to enable Internet Firewall, see [Activate Cloud Firewall](/intl.en-US/Quick Start/Activate Cloud Firewall.md).

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext).

2.  In the left-side navigation pane, choose **Traffic Analysis** \> **Breach Awareness**.

3.  On the **Breach Awareness** page, view the details of intrusion events.

    ![Breach Awareness page](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/6138816951/p77490.png)

    You can perform the following operations on the **Breach Awareness** page as required:

    -   In the intrusion event list, view the event details, such as risk levels, IP addresses of the affected assets, and the event status.
    -   Specify a filter condition. such as a risk level, status, or time range, or enter an instance IP address, and then click **Search** to search for intrusion events that meet the condition.
    -   If an intrusion event is a normal activity, click **Ignore** in the **Actions** column to ignore this event.

        **Note:** After you click **Ignore**, the intrusion event is removed from the list, and Cloud Firewall no longer reports alerts for this event.

    -   View details of an event. Find the intrusion event that you want to view details and click **View Details** in the **Actions** column. In the Details pane, you can view the details of the intrusion event and the security tips.

        **Note:** The **Block** function does not take effect on single events. You can enable this function to enable the Intrusion Prevention feature provided by Cloud Firewall.



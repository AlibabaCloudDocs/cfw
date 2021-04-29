# Modify notification and contact settings

You can modify notification and contact settings in the Cloud Firewall console. If Cloud Firewall detects exception events in your assets, it notifies you by email. The exception events include abnormal traffic, compromised hosts, suspicious outbound connections, vulnerabilities, unprotected public IP addresses, and disabled intrusion prevention.

Cloud Firewall can send notifications for the following types of events:

-   **Abnormal Traffic**: If Cloud Firewall detects that the volume of peak Internet traffic exceeds its processing capability, it sends a notification.
-   **Infected Host**: If Cloud Firewall detects compromised hosts, it sends a notification. Some notifications are sent one day later to avoid false positives.
-   **Suspicious Outbound Connection**: If Cloud Firewall detects that a host communicates with a risky IP address or domain name, it sends a notification.
-   **Protection Against Vulnerabilities**: If Cloud Firewall detects that the vulnerabilities of your assets are exploited to launch attacks, it sends a notification.
-   **Asset Protection**: If Cloud Firewall detects unprotected public IP addresses or virtual private clouds \(VPCs\) within your account, it sends a notification.
-   **Intrusion Prevention**: If Cloud Firewall detects that the intrusion prevention feature is disabled, it sends a notification. If the intrusion prevention feature is disabled, attacks are not automatically blocked.
-   **New Public IP Address**: If Cloud Firewall detects new public IP addresses within your account, it sends a notification.
-   **Intelligent Policy**: Cloud Firewall automatically learns traffic and notifies you of intelligent protection policies.

You can modify the notification and contact settings based on your business requirements so that Cloud Firewall can send the notifications of specific events to specified contacts by email. The notification settings include the periods, event levels, and methods to send notifications.

## Modify notification settings

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext).

2.  In the left-side navigation pane, choose **Settings** \> **Alert Notifications**.

3.  On the **Alert Notifications** tab, find the **Notification Settings** section and modify notification settings.

    **Note:** The notification settings immediately take effect.

    Cloud Firewall provides different types of notifications. You can modify the settings of **Time**, **Concerned Levels**, and **Method** based on your business requirements. The following list describes the details:

    -   **Time**: You can select **8:00~20:00** or **24 Hours**.

        The default value is **8:00~20:00**, which indicates that Cloud Firewall sends notifications only in this period. If Cloud Firewall detects exception events at other times, it does not send the notifications until the specified period arrives.

        If you want to receive the notifications of specific events at the earliest opportunity, change the value of **Time** to **24 Hours**. Then, Cloud Firewall sends notifications immediately after events are detected.

    -   **Concerned Levels**: You can select the levels for specific types of events on which you want to receive notifications. For example, if you select High for a specific type of event, Cloud Firewall sends notifications only when it detects the events and the events are at high risk. You can select the levels for the following types of events:
        -   **Infected Host**: You can select **High**, **Low**, or both.
        -   **Suspicious Outbound Connection**: You can select **Risk**, **Non-Whitelist Alert**, or both.

            **Note:** If you select **Non-Whitelist Alert**, Cloud Firewall sends notifications if it detects that a host communicates with an IP address or domain name that is not in the whitelist. You can configure the whitelist based on your business requirements. For more information, see [Outbound connections](/intl.en-US/Traffic Analysis/Outbound connections.md).

        -   **Protection Against Vulnerabilities**: You can select **High**, **Medium**, **Low**, or a combination.
    -   **Method**: You can select only **Email**.

        By default, **Email** is selected. In this case, Cloud Firewall sends notifications to specified contacts by email.

        **Note:** You can add contacts or modify contact information in the Contact Settings section. For more information, see [Add a contact](#section_apm_stl_unk).


## Add a contact

By default, Cloud Firewall sends notifications to the contact registered for your Alibaba Cloud account. If you want multiple contacts to receive notifications from your Cloud Firewall, you can add them in the Contact Settings section. You can add a maximum of 10 contacts to receive notifications from Cloud Firewall.

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext).

2.  In the left-side navigation pane, click **Settings**.

3.  On the **Alert Notifications** tab, find the **Contact Settings** section and click **Add Contact**.

4.  Enter the contact name and email address.Then, click **Save**.

    After you add a contact, the contact is enabled by default. Cloud Firewall sends notifications to both the contact registered for your Alibaba Cloud account and the contacts that you add in the contact list.

    If you do not want an added contact to receive notifications, you can turn off the switch in the **Enabled** column. You can also click **Edit** or **Delete** in the Actions column to modify contact information or remove a contact based on your business requirements.



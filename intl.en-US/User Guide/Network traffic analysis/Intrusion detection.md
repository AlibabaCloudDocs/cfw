# Intrusion detection {#concept_qfm_llb_kfb .concept}

The **Intrusion Detection** page displays the intrusions and details detected by IPS.

## Procedure {#section_sm4_l32_kfb .section}

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext#/overview).
2.  In the left-side navigation pane, click **Traffic Analysis** to go to the network flow analysis page.
3.  Click **Intrusion Detection** and view the intrusion event list.

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/22642/155645703834787_en-US.png)

    -   In the **intrusion event** list, you can view the details about all intrusion events. The details include the risk level, IP address of the affected asset, and event processing status.
    -   You can specify conditions such as the risk level, processing status, detection time range, and instance IP address to search for a single intrusion event.![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/22642/155645703834788_en-US.png)
    -   If you determine that an intrusion event is a normal activity, click **Ignore** in the **Action** column to ignore the event.

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/22642/155645703934789_en-US.png)

        **Note:** An **ignored** intrusion event is removed from the intrusion event list. Cloud Firewall no longer reports alarms for this event.

    -   Click **View Details** in the **Action** column to go to the details page of an intrusion event and view the event details and security suggestions. You can also enable or disable IPS features on the **Event Details** page.

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/22642/155645703913423_en-US.png)

        Click **Block** to enable the Threat Engine of IPS.



# IPS analysis {#concept_int_klb_kfb .concept}

The **IPS analysis** tab page displays the threats detected by IPS, including details on the blocked events, blocked destination IP and application.

## Procedure {#section_lw7_u6h_zr5 .section}

Cloud Firewall can detect the IPS blocking events that occurred in the last one hour, one day, seven days, and one month. You can also select and display the blocked events in the customized time range.

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/64122/155654180936537_en-US.png)

**Note:** The blocked traffic in IPS Analysis is blocked by the IPS treat engines. Mare sure you've selected **Traffic Control Mode** and enabled the **Basic Protections** and the **Patches** in Intrusion Prevention page.

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext#/overview).
2.  In the left-side navigation pane, go to **Traffic Analysis** \> **IPS Analysis**.
3.  In the **Direction** area, click **Inbound** or **Outbound** to view the corresponding blocked inbound or outbound traffic.

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/64122/155654180945710_en-US.png)

4.  Select **Time** by one hour, one day, last seven days, one month, or a custom time range to display the required blocking traffic.

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/64122/155654180945711_en-US.png)

    You could monitor the following information on the blocked traffic:

    -   The most blocked source locations with the corresponding proportion in percentage.

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/64122/155654180945731_en-US.png)

    -   Blocked destination IP addresses with IP type and location.

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/64122/155654181245733_en-US.png)

        If you want to view the details of a certain blocked destination IP, click **View Logs** to open the Access Log.

    -   Blocked application with its proportion in percentage.

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/64122/155654181245749_en-US.png)

    -   IPS threat engines that block the traffic.

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/64122/155654181445753_en-US.png)

    -   Blocked event list with the events details.

        In the blocked event list, specify the blocking source, direction, defense status, detection time, or source IP address to search for blocking events and to view details.

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/64122/155654181445765_en-US.png)

        Click **View Details** to open the detailed page of the specified blocked event. You can view the event description on the Details page.

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/64122/155654181445767_en-US.png)



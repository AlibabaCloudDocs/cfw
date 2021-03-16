# Outbound connections

After the Internet firewall is enabled for your network assets, the Outbound Connections page displays real-time information about outbound connections initiated by your servers. This helps you detect suspicious servers. This topic describes the information displayed and operations that you can perform on this page.

## Overview

After you enable the Internet firewall for your network assets, you can log on to the [Cloud Firewall console](https://yundunnext.console.aliyun.com/?p=cfwnext)[Cloud Firewall console](https://partners-yundunnext.console.aliyun.com/?p=cfwnext) and choose **Traffic Analysis** \> **Outbound Connections** in the left-side navigation pane to view traffic analysis data. For more information, see the following sections:

-   [Outbound connection statistics](#section_18l_93v_ny7)
-   [Outbound traffic](#section_p15_t48_wz2)
-   [Visualized analysis](#section_oqf_ktv_0dq)

**Note:** The **Outbound Connections** page displays traffic analysis data only after you enable the Internet firewall. For information about how to enable the Internet firewall, see [Activate Cloud Firewall](/intl.en-US/Quick Start/Activate Cloud Firewall.md).

In the upper-right corner of the Outbound Connections page, you can customize a time range from the date and time picker. You can also select **Recent 1 Hours**, **Last 24 Hours**, or **Last 7 Days** from the time drop-down list. You can specify a custom time range that is no more than seven days.

**Note:** Otherwise, the system displays an error message to prompt you that the time range you specify is invalid and you must select a time range within seven days.

![Date and time picker](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/3997570061/p13367.png)

## Outbound connection statistics

This section is in the upper part of the **Outbound Connections** page. It provides the following statistics:

![Outbound connection statistics](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/7617085161/p72797.png)

-   **Outbound Domains**: the total number of domain names and the number of risky domain names in outbound connections.

    You can click this section to view details about the domain names on the [Outbound Domains](#li_a6j_faq_8cq) tab of the **Outbound traffic** tab.

-   **Outbound IP Addresses**: the total number of destination IP addresses and the number of risky destination IP addresses in outbound connections.

    You can click this section to view details about the outbound IP addresses on the [Outbound IP Addresses](#li_9z3_mh9_zh0) tab of the **Outbound traffic** tab.

-   **Assets**: the total number of assets that initiate outbound connections and the number of assets that initiate risky outbound connections.

    You can click this section to view details about the assets on the [Assets](#li_s00_cl3_j3o) tab of the **Outbound traffic** tab.

-   **Protocol Analysis**: the analysis results of protocols used in outbound connections, including the total number of protocols and the proportion of outbound connections with unidentified protocols.

    You can click this section to view details about the IP address traffic and analysis results of protocols in the **Visualized analysis** tab. This tab displays [IP Traffic](#li_2mv_ajy_f88) and [Protocol Analysis](#li_7qv_psx_wgk).


## Outbound traffic

The **Outbound traffic** tab displays domain names, destination IP addresses, and assets used in outbound connections. You can click the **Outbound Domains**, **Outbound IP Addresses**, or **Assets** tab to view details.

-   **Outbound Domains**

    ![Outbound traffic](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/7617085161/p72801.png)

    Each record includes the following information: **Domain Name**, **Traffic**, **Requests**, **Category**, **Intelligence Tag**, and **Recommended Operation**. **Category** and **Intelligence Tag** are website attributes that Cloud Firewall adds based on the Internet information of a domain name. For more information about the tags, see [FAQ about network traffic analysis](/intl.en-US/FAQ/FAQ about network traffic analysis.md).

    You can click the ![Download icon](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/7617085161/p237696.png) icon in the upper-right corner above the outbound domain name list to download the list to your computer in the CSV format for check and analysis.

    You can perform the following operations on the outbound domain names:

    -   **Ignore**: Find a domain name and click **Ignore** in the Recommended Operation column. The domain name is added to the **Destination Domain** tab of the **Ignored** tab.

        To remove a domain name from the Ignored tab, click **Ignored** in the upper-right corner. On the **Destination Domain** tab, find the domain name and click **Cancel Ignore** in the Actions column.

        ![Cancel Ignore](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/7617085161/p237701.png)

    -   **Follow**: Find a domain name and choose **More** \> **Follow** in the Recommended Operation column. The domain name is added to the **Destination Domain** tab of the **Followed** tab.

        To unfollow a domain name, click **Followed** in the upper-right corner. On the **Destination Domain** tab, find the domain name and click **Unfollow** in the Actions column.

        ![Unfollow](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/7617085161/p237704.png)

    -   **View Logs**: Find a domain name and choose **More** \> **View Logs** in the Recommended Operation column. On the **Traffic Logs** tab of the **Log Audit** page, view the traffic information about the domain name. For more information, see [Log audit](/intl.en-US/Logs/Log audit.md).
    -   **View Details**: Find a domain name and choose **More** \> **View Details** in the Recommended Operation column. In the Outbound Domains panel, view the access details of the domain name. The details include the IP addresses of ECS instances that access the domain name, the time when the outbound connections are initiated, the transmission rates of request and response traffic, and the number of requests. The following figure shows the access details of a domain name.

        ![View Details](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/4997570061/p80383.png)

-   **Outbound IP Addresses**

    ![Outbound IP Addresses](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/7617085161/p80639.png)

    Each record includes the following information: **Destination IP**, **Applications/Ports**, **Traffic**, **Sessions**, **Category**, **Address Book**, **Intelligence Tag**, and **Recommended Operation**. **Category** and **Intelligence Tag** are website attributes that Cloud Firewall adds based on the Internet information of a domain name. For more information about the tags, see [FAQ about network traffic analysis](/intl.en-US/FAQ/FAQ about network traffic analysis.md).**Address Book** indicates the address book that stores the destination IP address.更多信息，请参见[Manage address books](/intl.en-US/Access control/Manage address books.md)。

    You can click the ![Download icon](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/7617085161/p237696.png) icon in the upper-right corner above the outbound IP address list to download the list to your computer in the CSV format for check and analysis.

    You can perform the following operations on the outbound IP addresses:

    -   **Ignore**: Find an IP address and click **Ignore** in the Recommended Operation column. The IP address is added to the **Destination IP** tab of the **Ignored** tab.

        To remove an IP address from the Ignored tab, click **Ignored** in the upper-right corner. On the **Destination IP** tab, find the IP address and click **Cancel Ignore** in the Actions column.

        ![Ignore](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/7617085161/p148044.png)

    -   **Follow**: Find an IP address and choose **More** \> **Follow** in the Recommended Operation column. The IP address is added to the **Destination IP** tab of the **Followed** tab.

        To unfollow an IP address, click **Followed** in the upper-right corner. On the **Destination IP** tab, find the IP address and click **Unfollow** in the Actions column.

        ![Follow](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/8617085161/p148048.png)

    -   **View Logs**: Find an IP address and choose **More** \> **View Logs** in the Recommended Operation column. On the **Traffic Logs** tab of the **Log Audit** page, view the traffic information about the IP address. For more information, see [Log audit](/intl.en-US/Logs/Log audit.md).
    -   **View Details**: Find a domain name and choose **More** \> **View Details** in the Recommended Operation column. In the Outbound IP Addresses panel, view the access details of the IP address. The details include the IP address of ECS instances that access this IP address, the time when outbound connections are initiated, transmission rates of request and response traffic, and the number of requests. The following figure shows the access details of a destination IP address.

        ![View details](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/5997570061/p80634.png)

-   **Assets**

    ![Assets](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/8617085161/p80638.png)

    Each record includes the following information: **Asset IP**, **Asset Type**, **Instance ID/Name**, **Region**, **Traffic**, **Requests**, **Security Risk**, and **Actions**. **Security Risk** indicates the status that Cloud Firewall sets for an asset based on outbound connection records.

    You can click the ![Download icon](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/7617085161/p237696.png) icon in the upper-right corner above the asset list to download the list to your computer in the CSV format for check and analysis.

    You can perform the following operations on the asset IP addresses:

    -   **Follow**: Find an asset IP address and choose **More** \> **Follow** in the Actions column. The IP address is added to the **Asset IP** tab of the **Followed** tab.

        To unfollow an asset IP address, click **Followed** in the upper-right corner. On the **Asset IP** tab, find the IP address and click **Unfollow** in the Actions column.

        ![Unfollow an asset IP address](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/8617085161/p237730.png)

    -   **View Logs**: Find an asset IP address and choose **More** \> **View Logs** in the Actions column. On the **Traffic Logs** tab of the **Log Audit** page, view the traffic information about the asset IP address, which indicates the source IP address of an outbound connection. For more information, see [Log audit](/intl.en-US/Logs/Log audit.md).
    -   To view more details about an asset IP address, click the ![Plus icon](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/8574685161/p237734.png) icon next to the asset IP address.

        The details include **Outbound Domains/Outbound IP Addresses**, **Requests**, **Category**, **Tag**, and **Recommended Operation**. **Category** and **Intelligence Tag** are website attributes that Cloud Firewall adds based on the Internet information of a domain name. For more information about the tags, see [FAQ about network traffic analysis](/intl.en-US/FAQ/FAQ about network traffic analysis.md).

        You can perform the following operations on an outbound domain name or IP address that is displayed in the details:

        -   **Ignore**: Find an outbound domain name or IP address and click **Ignore** in the Recommended Operation column. The domain name or IP address is added to the **Destination Domain** or **Destination IP** tab of the **Ignored** tab.

            To remove a domain name or IP address from the Ignored tab, click **Ignored** in the upper-right corner. On the **Destination Domain** tab, find the domain name or IP address and click **Cancel Ignore** in the Actions column.

        -   **Follow**: Find an outbound domain name or IP address and choose **More** \> **Follow** in the Recommended Operation column. The domain name or IP address is added to the **Destination Domain** or **Destination IP** tab of the **Followed** tab.

            To unfollow a domain name or IP address, click **Followed** in the upper-right corner. On the **Destination Domain** or **Destination IP** tab, find the domain name or IP address and click **Unfollow** in the Actions column.

        -   **View Logs**: Find an outbound domain name or IP address and choose **More** \> **View Logs** in the Recommended Operation column. On the **Traffic Logs** tab of the **Log Audit** page, view the traffic information about the domain name or IP address. For more information, see [Log audit](/intl.en-US/Logs/Log audit.md).

## Visualized analysis

The **Visualized analysis** tab displays the **IP traffic statistics** and **protocol analysis** modules.

-   **IP traffic statistics**

    This module provides IP address lists in the **IP Traffic** section and traffic trends of IP addresses in the **Trends of Traffic** section. You can click an IP address in the lists to view its traffic trend.

    ![IP traffic statistics](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/3997570061/p72799.png)

    **IP Traffic**: lists private and public IP addresses in descending order based on their response traffic at a specific point in time.

    -   Click the **Private IP** or **Public IP** tab to check the traffic of IP addresses.
    -   In the **Trends of Traffic** section, click a point in time on the x-axis to refresh the traffic rankings in the IP Traffic section.
    -   Find an IP address and choose **More** \> **View Logs**. On the **Traffic Logs** tab of the **Log Audit** page, view the traffic information about the IP address. For more information, see [Log audit](/intl.en-US/Logs/Log audit.md).

        ![View logs](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/3997570061/p80304.png)

    **Trends of Traffic**: displays the peak transmission rates of request and response traffic of specified or all network assets in real time. You can move the pointer over a position in the trend chart to view the peak transmission rates at the point in time that corresponds to the position.

    -   Specify a time range. By default, data of the last seven days is displayed. You can select a time range in the **IP Traffic** section.

        ![Date picker](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/3997570061/p80305.png)

        The following time ranges are available:

        -   **Previous Day**
        -   **Last 7 Days**
        -   **Last 30 Days**
    -   Specify a data range. By default, the traffic trends of all protected network assets are displayed. In the **IP Traffic** section, you can specify an IP address to view its trends by using one of the following methods:

        -   Click an IP address, or find an IP address and choose **More** \> **View Trend**.

            ![View traffic trends](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/4997570061/p80311.png)

        -   Click the search icon in the upper-right corner and enter a public or private IP address.

            **Note:** After you perform this operation, the IP Traffic section does not display traffic rankings.

            ![Search for an IP address](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/4997570061/p80312.png)

        The filter condition you specified is displayed above the chart.

        ![Filter condition](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/4997570061/p80340.png)

-   **Protocol analysis**

    This module contains the Protocol Analysis and **Protocol Details** sections. The Protocol Analysis section provides a pie chart of **Applications**.

    ![Protocol analysis](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/4997570061/p72800.png)

    **Applications**: displays the proportion of each application protocol used in outbound connections.

    **Protocol Details**: displays the details about application protocols used in outbound connections. You can find an application and click **View Logs** in the **Actions** column. On the Traffic Logs tab of the Log Audit page, you can view the traffic information about the application.


## References

-   [Activate Cloud Firewall](/intl.en-US/Quick Start/Activate Cloud Firewall.md)
-   [FAQ about network traffic analysis](/intl.en-US/FAQ/FAQ about network traffic analysis.md)
-   [Intelligent policies](/intl.en-US/Traffic Analysis/Intelligent policies.md)
-   [Manage address books](/intl.en-US/Access control/Manage address books.md)


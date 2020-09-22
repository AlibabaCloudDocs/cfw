# Outbound connections

After Cloud Firewall is activated for network assets, the Outbound Connections page displays information about outbound connections initiated by your servers in real time, which helps you detect suspicious servers. This topic describes the information on this page and operations that you can perform on this page.

## Overview

The Outbound Connections page consists of the following four modules. You can click a module name to view its details and perform required operations. To go to the Outbound Connections page, log on to the Cloud Firewall console, and choose **Traffic Analysis** \> **Outbound Connections** in the left-side navigation pane.

-   [Outbound connection statistics](#section_18l_93v_ny7)
-   [IP traffic statistics](#section_oqf_ktv_0dq)
-   [Protocol analysis](#section_aci_5zu_thf)
-   [Outbound connections](#section_4vp_qif_noe)

**Note:** The Outbound Connections page displays traffic analysis data only after you activate Cloud Firewall. For information about how to activate Cloud Firewall, see [Activate Cloud Firewall](/intl.en-US/Quick Start/Activate Cloud Firewall.md).

In the upper-right corner, click the date and time picker to specify a time range. You can select **Recent 1 Hours**, **Last 24 Hours**, **Last 7 Days**, or specify a time range that spans seven days. If you specify a time range that spans more than seven days, an error message appears.

![Date and time picker](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/3997570061/p13367.png)

## Outbound connection statistics

This module provides statistics on outbound connections.

![Outbound connection statistics](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/3997570061/p72797.png)

-   **Outbound Domains**: the total number of outbound domain names and the number of risky outbound domain names. You can click this section to view details about the outbound domain names.
-   **Outbound IP Addresses**: the total number of outbound IP addresses and the number of risky outbound IP addresses. You can click this section to view details about the outbound IP addresses.
-   **Assets**: the total number of assets that initiate outbound connections and the number of risky assets. You can click this section to view details about the assets.
-   **Protocol Analysis**: the analysis results of protocols used in outbound connections, including the total number of protocols and the proportion of outbound connections with unidentified protocols. You can click this section to view details about the protocols.

## IP traffic statistics

This module provides IP address lists in the **IP Traffic** section and traffic trends of IP addresses in the **Trends of Traffic** section. You can click an IP address in the lists to view its traffic trend.

![IP traffic statistics](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/3997570061/p72799.png)

**IP Traffic**: lists private and public IP addresses in descending order based on their response traffic at a specific point of time.

-   Click the **Private IP** or **Public IP** tab to check the traffic of IP addresses.
-   In the **Trends of Traffic** section, click a time point on the horizontal axis to refresh the traffic rankings in the IP Traffic section.
-   Find the IP address that you want to query, click the drop-down arrow next to **More** in the Actions column, and then click **View Logs**. The Traffic Logs tab appears, and you can view traffic logs of the IP address on this tab.

    ![View Logs](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/3997570061/p80304.png)


**Trends of Traffic**: displays the peak transmission rates of request and response traffic of specified or all network assets in real time. You can move the pointer to any position in the chart to view the peak transmission rates at the time point that corresponds to the position.

-   Specify the time range. By default, data of the last seven days is displayed. You can use the date picker in the upper-right corner of the **IP Traffic** section to specify a time range.

    ![Date picker](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/3997570061/p80305.png)

    The following time ranges are available:

    -   **Previous Day**
    -   **Last 7 Days**
    -   **Last 30 Days**
-   Specify the data range. By default, the overall traffic trends of all protected network assets are displayed. In the **IP Traffic** section, you can specify an IP address to view its trends by using one of following methods:

    -   Click the IP address or find the IP address, click the drop-down arrow next to **More** in the Actions column, and then click **View Trend**.

        ![View traffic trends](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/4997570061/p80311.png)

    -   Click the search icon in the upper-right corner and enter a public or private IP address.

        **Note:** After you perform this operation, the IP Traffic section does not display traffic rankings.

        ![Search for an IP address](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/4997570061/p80312.png)

    The filter condition you specified is displayed on top of the chart.

    ![Filter condition](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/4997570061/p80340.png)


## Protocol analysis

This module displays a pie chart in the **Applications** section and a table in the **Protocol Details** section.

![Protocol analysis](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/4997570061/p72800.png)

**Applications**: displays the proportions of application protocols used in outbound connections.

**Protocol Details**: displays the details about the application protocols used in outbound connections. You can follow or ignore a specific application or view its logs.

-   Follow an application: Find the application that you want to follow, click **More** in the Actions column, and then click **Follow**. The port of the followed application is added to the Destination Port tab on the Followed tab. You can click **Followed** in the upper-right corner, click the **Destination Port** tab, find the port, and then click **Unfollow** in the Actions column to unfollow it.
-   Ignore an application: Find the application that you want to ignore, click **More** in the Actions column, and click **Ignore**. The port of the ignored application is added to the Destination Port tab on the Ignored tab. The ignored application is removed from the Protocol Analysis section. You can click **Ignored** in the upper-right corner, click the **Destination Port** tab, find the port, and then click **Cancel Ignore** in the Actions column to unignore it.
-   View logs of an application: Find the application whose logs you want to view, click **More** in the Actions column, and then click **View Logs**. The Traffic Logs tab appears. You can view traffic logs of this application on this tab.

## Outbound connections

This module displays domain names, destination IP addresses, and assets used in outbound connections. Click the **Outbound Domains**, **Outbound IP Addresses**, or **Assets** tab to view details.

-   Outbound Domains

    ![Outbound connections](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/4997570061/p72801.png)

    Each record includes the following information: **Domain Name**, **Traffic**, **Requests**, **Category**, **Tag**, and **Recommended Operation**.

    -   **Category** and **Tag** are website attributes of an outbound domain name.
    -   **Recommended Operation**includes the following options: [Intelligent policies](/intl.en-US/Traffic Analysis/Intelligent policy delivery.md)
        -   **Follow**: Add the current outbound domain name to the followed list. You can click **Followed** in the upper-right corner, click the **Destination Domain** tab, find the domain name, and then click **Unfollow** to unfollow it.
        -   **Ignore**: Add the current outbound domain name to the ignored list. You can click **Ignored** in the upper-right corner, click the **Destination Domain** tab, find the domain name, and then click **Cancel Ignore** to unignore it.
        -   **View Logs**: View the detailed traffic information of an outbound domain name on the Traffic Logs tab.
        -   **View Details**: View the access details of an outbound domain name. The details include ECS instance IP addresses that are mapped to this domain name, the time outbound connections are initiated, transmission rates of request and response traffic, and the number of requests. The following figure shows the access details of an outbound domain name.

            ![View details](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/4997570061/p80383.png)

-   Outbound IP Addresses

    ![Outbound IP Addresses](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/4997570061/p80639.png)

    Each record includes the following information: **Destination IP**, **Applications/Ports**, **Traffic**, **Sessions**, **Category**, **Address Book**, **Tag**, and **Recommended Operation**.

    -   **Category** and **Tag** are website attributes of an outbound IP address.
    -   **Address Book** indicates the address book that stores an outbound IP address.
    -   **Recommended Operation** includes the following options: [Intelligent policies](/intl.en-US/Traffic Analysis/Intelligent policy delivery.md)
        -   **Follow**: Add the current outbound IP address to the followed list. You can click **Followed** in the upper-right corner, click the **Destination IP** tab, find the IP address, and then click **Unfollow** to unfollow it.
        -   **Ignore**: Add the current outbound IP address to the ignored list. You can click **Ignored** in the upper-right corner, click the **Destination IP** tab, find the IP address, and then click **Cancel Ignore** to unignore it.
        -   **View Logs**: View the detailed traffic information of an outbound IP address on the Traffic Logs tab.
        -   **View Details**: View the access details of an outbound IP address. The details include ECS instances bound to this IP address, the time outbound connections are initiated, transmission rates of request and response traffic, and the number of requests. The following figure shows the access details of an outbound IP address.

            ![View details](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/5997570061/p80634.png)

-   Assets

    ![Assets](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/5997570061/p80638.png)

    Each record includes the following information: **Asset IP**, **Asset Type**, **Instance ID/Name**, **Region**, **Traffic**, **Requests**, **Security Risk**, and **Actions**.

    -   **Security Risk** indicates the status Cloud Firewall sets for an asset based on outbound connection records.
    -   Supported operations in the **Actions** column include:
        -   **Follow**: Add the current asset IP address to the followed list. You can click **Followed** in the upper-right corner, click the **Asset IP** tab, find the asset IP address, and then click **Unfollow** to unfollow it.
        -   **Ignore**: Add the current asset IP address to the ignored list. You can click **Ignored** in the upper-right corner, click the **Asset IP** tab, find the asset IP address, and then click **Cancel Ignore** to unignore it.
        -   **View Logs**: View the detailed traffic information of an asset IP address \(the source IP address of an outbound connection\) on the Traffic Logs tab.
    Click the plus sign next to an asset to view more details about its outbound connections, including **Outbound Domains/Outbound IP Addresses**, **Requests**, **Category**, **Tag**, and **Recommended Operation**.

    -   **Category** and **Tag** are website attributes of an outbound IP address or domain name.
    -   **Recommended Operation** includes the following options: [Intelligent policies](/intl.en-US/Traffic Analysis/Intelligent policy delivery.md)
        -   **Follow**: Add the current outbound IP address or domain name to the followed list. You can click **Followed** in the upper-right corner, click the **Destination IP** or **Destination Domain** tab, find the IP address or domain name, and then click **Unfollow** to unfollow it.
        -   **Ignore**: Add the current outbound IP address or domain name to the ignored list. You can click **Ignored** in the upper-right corner, click the **Destination IP** or **Destination Domain** tab, find the IP address or domain name, and then click **Cancel Ignore** to unignore it.
        -   **View Logs**: View the detailed traffic information of an outbound IP address or domain name on the Traffic Logs tab.


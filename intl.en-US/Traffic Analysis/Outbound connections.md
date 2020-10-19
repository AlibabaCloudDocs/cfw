# Outbound connections

After Cloud Firewall is activated for network assets, the Outbound Connections page displays information about outbound connections initiated by your servers in real time, which helps you detect suspicious servers. This topic describes the information on this page and operations that you can perform on this page.

## Overview

To go to the Outbound Connections page, log on to the Cloud Firewall console, and choose **Traffic Analysis** \> **Outbound Connections** in the left-side navigation pane. You can click a module name on the Outbound Connections page to view the module details and perform required operations. The Outbound Connections page consists of the following modules:

-   [Outbound connection statistics](#section_18l_93v_ny7)
-   [IP traffic statistics](#section_oqf_ktv_0dq)
-   [Protocol analysis](#section_aci_5zu_thf)
-   [Outbound traffic](#section_4vp_qif_noe)

**Note:** The Outbound Connections page displays traffic analysis data only after you activate Cloud Firewall. For information about how to activate Cloud Firewall, see [Activate Cloud Firewall](/intl.en-US/Quick Start/Activate Cloud Firewall.md).

In the upper-right corner, click the date and time picker to specify a time range. You can select **Recent 1 Hours**, **Last 24 Hours**, **Last 7 Days**, or specify a time range that spans seven days. If you specify a time range that spans more than seven days, an error message appears.

![Date and time picker](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/3997570061/p13367.png)

## Outbound connection statistics

This module provides statistics on outbound connections.

![Outbound connection statistics](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/3997570061/p72797.png)

-   **Outbound Domains**: the total number of domain names and the number of risky domain names in outbound connections. You can click this section to view details about the domain names.
-   **Outbound IP Addresses**: the total number of outbound IP addresses and the number of risky outbound IP addresses. You can click this section to view details about the outbound IP addresses.
-   **Assets**: the total number of assets that initiate outbound connections and the number of risky assets. You can click this section to view details about the assets.
-   **Protocol Analysis**: the analysis results of protocols used in outbound connections, including the total number of protocols and the proportion of outbound connections with unidentified protocols. You can click this section to view details about the protocols.

## IP traffic statistics

This module provides IP address lists in the **IP Traffic** section and traffic trends of IP addresses in the **Trends of Traffic** section. You can click an IP address in the lists to view its traffic trend.

![IP traffic statistics](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/3997570061/p72799.png)

**IP Traffic**: lists private and public IP addresses in descending order based on their response traffic at a specific time point.

-   Click the **Private IP** or **Public IP** tab to check the traffic of IP addresses.
-   In the **Trends of Traffic** section, click a time point on the horizontal axis to refresh the traffic rankings in the IP Traffic section.
-   Find the IP address that you want to query, choose **More** \> **View Logs**. The Traffic Logs tab appears. You can view traffic logs of the IP address on this tab.

    ![View Logs](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/3997570061/p80304.png)


**Trends of Traffic**: displays the peak transmission rates of request and response traffic of specified or all network assets in real time. You can move the pointer to any position in the chart to view the peak transmission rates at the time point that corresponds to the position.

-   Specify the time range. By default, data of the last seven days is displayed. You can use the date picker in the upper-right corner of the **IP Traffic** section to specify a time range.

    ![Date picker](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/3997570061/p80305.png)

    The following time ranges are available:

    -   **Previous Day**
    -   **Last 7 Days**
    -   **Last 30 Days**
-   Specify the data range. By default, the overall traffic trends of all protected network assets are displayed. In the **IP Traffic** section, you can specify an IP address to view its trends by using one of following methods:

    -   Click the IP address or find the IP address and choose **More** \> **View Trend**.

        ![View traffic trends](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/4997570061/p80311.png)

    -   Click the search icon in the upper-right corner and enter a public or private IP address.

        **Note:** After you perform this operation, the IP Traffic section does not display traffic rankings.

        ![Search for an IP address](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/4997570061/p80312.png)

    The filter condition you specified is displayed on the top of the chart.

    ![Filter condition](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/4997570061/p80340.png)


## Protocol analysis

This module displays a pie chart in the **Applications** section and a table in the **Protocol Details** section.

![Protocol analysis](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/4997570061/p72800.png)

**Applications**: displays the proportion of each application protocol used in outbound connections.

**Protocol Details**: displays the details about application protocols used in outbound connections. You can find a required application, click **View Logs** in the **Actions** column, and then view the traffic logs of the application on the Traffic Logs tab.

## Outbound traffic

This module displays domain names, destination IP addresses, and assets used in outbound connections. You can click the **Outbound Domains**, **Outbound IP Addresses**, or **Assets** tab to view details.

-   Outbound Domains

    ![Outbound traffic](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/4997570061/p72801.png)

    Each record includes the following information: **Domain Name**, **Traffic**, **Requests**, **Category**, **Tag**, and **Recommended Operation**.

    -   **Category** and **Tag** are website attributes of a domain name.

        For more information about labels, see [What are the meanings of the tags of domain names on the Outbound Connections page?](/intl.en-US/FAQ/What are the meanings of the tags of domain names on the Outbound Connections page?.md).

    -   **Recommended Operation** includes the following options:
        -   **Ignore**: Click **Ignore** in the Recommended Operation column to add the current domain name to the **Destination Domain** tab under the **Ignored** tab. If you want to remove the domain name from the ignored list, click **Ignored** in the upper-right corner of the section. Then, on the **Destination Domain** tab, click **Cancel Ignore** in the Actions column in the row that the domain name is located.

            ![Ignore a domain name](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/6407482061/p148044.png)

        -   **Follow**: Choose **More** \> **Follow** to add the current domain name to the **Destination Domain** tab under the **Followed** tab.
        -   **Unfollow**: If you want to unfollow a domain name, find the domain name and choose **More** \> **Unfollow**. Alternatively, you can click **Followed** in the upper-right corner of the section. Then, on the **Destination Domain** tab, click **Unfollow** in the Actions column in the row that the domain name is located.

            ![Follow a domain name](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/6407482061/p148048.png)

        -   **View Logs**: View the detailed traffic information of a domain name on the Traffic Logs tab.
        -   **View Details**: View the access details of the domain name. The details include ECS instance IP addresses that are mapped to this domain name, the time outbound connections are initiated, transmission rates of request and response traffic, and the number of requests. The following figure shows the access details of a domain name.

            ![View details](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/4997570061/p80383.png)

-   Outbound IP Addresses

    ![Outbound IP Addresses](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/4997570061/p80639.png)

    Each record includes the following information: **Destination IP**, **Applications/Ports**, **Traffic**, **Sessions**, **Category**, **Address Book**, **Tag**, and **Recommended Operation**.

    -   **Category** and **Tag** are website attributes of an IP address.

        For more information about labels, see [What are the meanings of the tags of domain names on the Outbound Connections page?](/intl.en-US/FAQ/What are the meanings of the tags of domain names on the Outbound Connections page?.md).

    -   **Address Book** indicates the address book that stores an IP address.
    -   **Recommended Operation** includes the following options:
        -   **Ignore**: Click **Ignore** in the Recommended Operation column to add the current IP address to the **Destination IP** tab under the **Ignored** tab. If you want to remove the IP address from the ignored list, click **Ignored** in the upper-right corner of the section. On the Ignored tab, click the **Destination IP** tab. Then, click **Cancel Ignore** in the Actions column in the row that the IP address is located.

            ![Ignore an IP address](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/6407482061/p148044.png)

        -   **Follow**: Choose **More** \> **Follow** to add the current IP address to the **Destination IP** tab under the **Followed** tab.
        -   **Unfollow**: If you want to unfollow an IP address, find the IP address and choose **More** \> **Unfollow**. Alternatively, you can click **Followed** in the upper-right corner of the section. On the Followed tab, click the **Destination IP** tab. Then, click **Unfollow** in the Actions column in the row that the IP address is located.

            ![Follow an IP address](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/6407482061/p148048.png)

        -   **View Logs**: View the detailed traffic information of the IP address on the Traffic Logs tab.
        -   **View Details**: View the access details of the IP address. The details include ECS instances bound to this IP address, the time outbound connections are initiated, transmission rates of request and response traffic, and the number of requests. The following figure shows the access details of an IP address.

            ![View details](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/5997570061/p80634.png)

-   Assets

    ![Assets](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/5997570061/p80638.png)

    Each record includes the following information: **Asset IP**, **Asset Type**, **Instance ID/Name**, **Region**, **Traffic**, **Requests**, **Security Risk**, and **Actions**.

    -   **Security Risk** indicates the status Cloud Firewall sets for an asset based on outbound connection records.
    -   **Actions** include the following options:
        -   **Follow**: Add the current asset IP address to the **Asset IP** tab under the **Followed** tab. If you want to unfollow the IP address, click **Followed** in the upper-right corner of the section. On the Followed tab, click the **Asset IP** tab. Then, click **Unfollow** in the Actions column in the row that the IP address is located.
        -   **View Logs**: View the detailed traffic information of the asset IP address \(the source IP address of an outbound connection\) on the Traffic Logs tab.
    Click the plus sign next to an asset to view more details about its outbound connections, including **Outbound Domains/Outbound IP Addresses**, **Requests**, **Category**, **Tag**, and **Recommended Operation**.

    ![Assets](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/7407482061/p148071.png)

    -   **Category** and **Tag** are website attributes of a domain name or IP address.

        For more information about labels, see [What are the meanings of the tags of domain names on the Outbound Connections page?](/intl.en-US/FAQ/What are the meanings of the tags of domain names on the Outbound Connections page?.md).

    -   **Recommended Operation** includes the following options:
        -   **Ignore**: Click **Ignore** in the Recommended Operation column to add the current domain name or public IP address to **Destination Domain** or **Destination IP** tab under the **Ignore** tab. If you want to remove the domain name or IP address from the ignored list, click **Ignored** in the upper-right corner of the section. On the Ignored tab, click the **Destination Domain** or **Destination IP** tab. Then, click **Cancel Ignore** in the Actions column in the row that the domain name or IP address is located.
        -   **Follow**: Choose **More** \> **Follow** to add the current domain name or IP address to the **Destination Domain** or **Destination IP** tab under the **Followed** tab.
        -   **Unfollow**: If you want to unfollow a domain name or IP address, find the domain name and choose **More** \> **Unfollow**. Alternatively, you can click **Followed** in the upper-right corner of the section. On the Followed tab, click the **Destination Domain** or **Destination IP** tab, and then click **Unfollow** in the Actions column in the row that the domain name or IP address is located.
        -   **View Logs**: View the detailed traffic information of a domain name or IP address on the Traffic Logs tab.

## References

-   [Activate Cloud Firewall](/intl.en-US/Quick Start/Activate Cloud Firewall.md)
-   [What are the meanings of the tags of domain names on the Outbound Connections page?](/intl.en-US/FAQ/What are the meanings of the tags of domain names on the Outbound Connections page?.md)
-   [Intelligent policies](/intl.en-US/Traffic Analysis/Intelligent policy delivery.md)
-   [Manage address books](/intl.en-US/Access control/Manage address books.md)


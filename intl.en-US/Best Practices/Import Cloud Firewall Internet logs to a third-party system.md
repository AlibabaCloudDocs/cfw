# Import Cloud Firewall Internet logs to a third-party system {#concept_263606 .concept}

The Alibaba Cloud Log Service \(SLS\) supports **Internet logs** for the Alibaba Cloud Firewall Pro, Enterprise, and Flagship Editions. You can import the Internet logs to a third-party system by using the Cloud Firewall log analysis function.

The log analysis function of Cloud Firewall supports exporting logs. You can export the log files to your business systems, such as your security operations and maintenance center.

**Note:** Cloud Firewall supports Internet logs. The Internet log data includes the vulnerability priorities and hit rate of access control rules. Cloud Firewall does not support exporting the event log and operation log.

## Prerequisites {#section_657_3tk_bbx .section}

Before using the log analysis function, you must log on to the [Cloud Firewall console](https://yundunnext.console.aliyun.com/?p=cfwnext) to purchase and enable the log analysis function.

Reference:

-   For more information about purchasing and enabling the log analysis function, see [Enable the log analysis service](../intl.en-US/Logs/Log analysis/Enable the log analysis service.md#).
-   For more information about the log analysis pricing, see [Cloud Firewall log storage specifications and billing methods](#section_4h0_abt_22j).

## Export methods {#section_xn1_vha_hwc .section}

You can use both the Cloud Firewall log analysis function and Alibaba Cloud SLS to export logs.

-   Export a small amount of log data

    You can log on to the Cloud Firewall console, choose **Advanced Functions** \> **Log Analysis** \> **Log Download** to download a log file in CSV or TXT format, and upload the log file to a third-party system.

-   Export a large amount of log data

    You can log on to the SLS console to export log data by using program group programming.

    For more information about exporting log data by using SLS, see [Use a consumer group to consume logs](../../../../../intl.en-US/Real-time subscription and consumption/Consumption by consumer groups/Use a consumer group to consume logs.md#).

    **Note:** If SLS is not activated, when you enable the log analysis function of Cloud Firewall, SLS is activated at the same time.


## Cloud Firewall log storage specifications and billing methods {#section_4h0_abt_22j .section}

The log analysis function of Cloud Firewall provides you with the scalable log storage space. The log storage specifications are charged as follows.

|Log storage duration|Log storage size|Applicable bandwidth|Recommended version|Monthly subscription fee|Annual subscription fee|
|--------------------|----------------|--------------------|-------------------|------------------------|-----------------------|
|180 days|1TB|Applicable to business scenarios with monthly bandwidth not higher than 10 Mbps|Pro Edition|To be released.|To be released.|
|5TB|Applicable to business scenarios with monthly bandwidth not higher than 50 Mbps|Enterprise Edition|To be released.|To be released.|
|20TB|Applicable to business scenarios with monthly bandwidth not higher than Mbps|Flagship Edition|To be released.|To be released.|

For more information about the log storage space, see [Manage log storage](../intl.en-US/Logs/Log analysis/Manage log storage.md#).


# Log analysis billing method {#concept_187712 .concept}

Cloud Firewall Log Analysis service charges fees based on the selected log storage duration and log storage capacity. Log Analysis is charged by monthly and annual subscription.

Enable Activate Log Service and select the log storage period and the log storage size. Then, the price is automatically calculated based on the **log store specification** of your choice.

## Log storage specification {#section_2mt_l1s_ab7 .section}

Different log storage specifications of Cloud Firewall are charged as follows:

|Log storage period|Log storage size|Applicable bandwidth|Recommended version|For Mainland China region instances|
|Monthly subscription fee \(RMB\)|8.5 off annual package fee \(RMB\)|
|------------------|----------------|--------------------|-------------------|-----------------------------------|
|--------------------------------|----------------------------------|
|180 days|1TB|Applicable to business scenarios with monthly bandwidth not higher than 10 Mbps|Pro Edition|To be released.|To be released.|
|5TB|Applicable to business scenarios with monthly bandwidth not higher than 50 Mbps|Enterprise Edition|To be released.|To be released.|
|20TB|Applicable to business scenarios with monthly bandwidth not higher than Mbps|Flagship Edition|To be released.|To be released.|

**Note:** To increase the bandwidth, we recommend that you expand with 1TB log storage for every 10 Mbps increase.

**Upgrade storage capacity**

If you have no log storage left, a notification appears to remind you to expand the storage size. You can use**Upgrade**.

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/161299/155802147645235_en-US.png)

**Notice:** If you fail to upgrade the log storage capacity when the storage capacity is full, Cloud Firewall will stop writing new log data to the exclusive logstore of log analysis service, the stored log data in the logstore is retained. Log data is deleted automatically if it is stored for more than 180 days or is not renewed after the Log Analysis service expires for 7 days. Once the log data is deleted, it cannot be recovered.

## Duration {#section_711_bdm_zvy .section}

The purchase duration of Cloud Firewall log service is bound to the subscription instance of the Cloud Firewall you purchased.

-   **Buy**: When you buy a Cloud Firewall subscription and enable Log Analysis, the price of Log Service is calculated based on the validity of the subscription.
-   **Upgrade**: When you enable Log Service by upgrading an existing Cloud Firewall subscription, the price of Log Service is calculated based on the log storage size.

**Service expiration**

If the purchased Cloud Firewall instance is about to expire, Log Analysis service will also expire.

-   When the service expires, Cloud Firewall stops writing log entries to the exclusive logstore in Log Service.
-   The log entries recorded by Cloud Firewall Log Analysis are retained within seven days after the service expires. If you renew the service within seven days after the service expires, you can continue to use Log Analysis service. Otherwise, all stored log entries are deleted.


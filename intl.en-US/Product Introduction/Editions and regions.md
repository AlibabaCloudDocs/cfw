# Editions and regions

This topic describes the differences between Cloud Firewall editions and supported regions.

## Differences in features and billing between Cloud Firewall editions

|Feature or billable item|Basic Edition|Premium Edition|Enterprise Edition|Ultimate Edition|Description|
|------------------------|-------------|---------------|------------------|----------------|-----------|
|Basic price|Free of charge|USD 420 per month.|USD 1,450 per month.|USD 3,900 per month.|None.|
|Peak Internet bandwidth of protected traffic|Not supported|Valid values: 10 to 2,000. Unit: Mbit/s.|Valid values: 50 to 5,000. Unit: Mbit/s.|Valid values: 200 to 5,000. Unit: Mbit/s.|Extra fee: USD 7 per month for each increase of 1 Mbit/s of bandwidth.|
|Number of protected public IP addresses|Not supported|Valid values: 20 to 1,000.|Valid values: 50 to 2,000.|Valid values: 400 to 4,000.|Extra fee: USD 7 per month for each additional public IP address that you want to protect.|
|Maximum number of access control policies|Not supported|Access control policies for the Internet firewall: 4,000.|-   Access control policies for the Internet firewall: 10,000.
-   Access control policies for VPC firewalls: 10,000.

|-   Access control policies for the Internet firewall: 20,000.
-   Access control policies for VPC firewalls: 20,000.

\(You can submit a [ticket](https://workorder-intl.console.aliyun.com/#/ticket/add/?productId=80) to increase the quota.\)

|If an access control policy involves multiple source CIDR blocks, destination CIDR blocks, or ports, this policy is counted as N policies. N = **Number of source CIDR blocks × Number of destination CIDR blocks × Number of ports**. If a policy involves only one source CIDR block, one destination CIDR block, or one port, this policy is counted as **one** policy.|
|Threat detection by using an intrusion prevention system \(IPS\) and installation of virtual patches|Not supported|Supported.|Supported.|Supported.|None.|
|IPS whitelist|Not supported|Not supported.|Supported.|Supported.|None.|
|Visualization of security group traffic|Not supported|Not supported.|Supported.|Supported.|None.|
|Synchronization of security group policies|Supported|Not supported.|Supported.|Supported.|None.|
|Isolation between VPCs|Not supported|Not supported.|Supported.|Supported.|None.|
|Number of protected VPCs|Not supported|Not supported.|Valid values: 2 to 200.|Valid values: 5 to 500.|Extra fee: USD 300 per month for each additional VPC that you want to protect.|
|Maximum traffic between VPCs that can be protected|Not supported|Not supported.|100 Mbit/s.|1 Gbit/s.|None.|
|Unified VPC protection across Alibaba Cloud accounts \(with Cloud Enterprise Network enabled\)|Not supported|Not supported.|Not supported.|Supported.|None.|
|Log audit \(Logs are stored for seven days by default.\)|Not supported|Provides 5-tuple logs. **Note:** A 5-tuple log contains the information of a source IP address, a source port, a destination IP address, a destination port, and a transport layer protocol.

|Provides 5-tuple logs.|Provides 5-tuple logs.|If you enable the [log analysis](/intl.en-US/Logs/Log analysis/Overview.md) feature, Cloud Firewall stores the logs generated in the last six months and allows you to export the logs.|
|Expert Service|Not supported|Supported.|Supported.|Supported.|None.|
|Cluster deployment|Not supported|Uses shared resources.|Uses shared resources.|Uses dedicated resources.You can submit a [ticket](https://workorder-intl.console.aliyun.com/#/ticket/add/?productId=80) to change the resource specifications.|None.|
|Subscription mode|Free of charge|Shortest subscription period: six months.|Monthly subscription supported.|Monthly subscription supported.|None.|

## VPC firewall limits

A VPC firewall helps you detect and control the traffic between VPCs that are connected by using Express Connect or Cloud Enterprise Network \(CEN\). Different network environments have different limits for enabling VPC firewalls. For more information, see [VPC firewall limits](/intl.en-US/Firewall Settings/VPC Firewall/VPC firewall limits.md).


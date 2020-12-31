# Editions and regions

This topic describes the differences between Cloud Firewall editions and supported regions.

## Differences in features and billing between Cloud Firewall editions

|Feature or billing item|Free trail edition|Premium Edition|Enterprise Edition|Ultimate Edition|Description|
|-----------------------|------------------|---------------|------------------|----------------|-----------|
|Basic price per month|Free of charge.|USD 420 per month|USD 1,450 per month|USD 3,900 per month|N/A.|
|Peak Internet bandwidth of protected traffic|Not supported.|Default value: 10 Mbit/s per month. You can increase the bandwidth.|Default value: 50 Mbit/s per month. You can increase the bandwidth.|Default value: 200 Mbit/s per month. You can increase the bandwidth.|**Extra fee**:USD 7 per month for each increase of 1 Mbit/s of bandwidth.|
|Number of protected public IP addresses|Not supported.|Default value: 20. You can increase the quota.|Default value: 50. You can increase the quota.|Default value: 400. You can increase the quota.|**Extra fee**: USD 7 per month for each additional public IP address that you want to protect.|
|Maximum number of access control policies|Not supported.|-   Access control policies for the Internet firewall: 4,000
-   Access control policies for VPC firewalls: 4,000

|-   Access control policies for the Internet firewall: 10,000
-   Access control policies for VPC firewalls: 10,000

|-   Access control policies for the Internet firewall: 20,000
-   Access control policies for VPC firewalls: 20,000

\(You can[submit a ticket](https://workorder-intl.console.aliyun.com/#/ticket/add/?productId=80) to increase the quota.\)

|If an access control policy involves multiple source CIDR blocks, destination CIDR blocks, or ports, this policy is counted as N policies. N = **Number of source CIDR blocks × Number of destination CIDR blocks × Number of ports**. If a policy involves only one source CIDR block, one destination CIDR block, and one port, this policy is counted as **one** policy.|
|Threat detection by using an intrusion prevention system \(IPS\) and installation of virtual patches|Not supported.|Supported.|Supported.|Supported.|N/A.|
|IPS whitelist|Not supported.|Not supported.|Supported.|Supported.|N/A.|
|Visualization of security group traffic|Not supported.|Not supported.|Supported.|Supported.|N/A.|
|Synchronization of security group policies|Supported.|Not supported.|Supported.|Supported.|N/A.|
|Isolation between VPCs|Not supported.|Not supported.|Supported.|Supported.|N/A.|
|Number of protected VPCs|Not supported.|Not supported.|Default value: 2.You can [submit a ticket](https://workorder-intl.console.aliyun.com/#/ticket/add/?productId=80) to increase the quota.|Default value: 5.You can [submit a ticket](https://workorder-intl.console.aliyun.com/#/ticket/add/?productId=80) to increase the quota.|**Extra fee**:USD 300 per month for each additional VPC that you want to protect.|
|Maximum inter-VPC traffic that can be protected|Not supported.|Not supported.|100 Mbit/s|1 Gbit/s|N/A.|
|Unified VPC protection across Alibaba Cloud accounts \(with Cloud Enterprise Network enabled\)|Not supported.|Not supported.|Not supported.|Supported.|N/A.|
|Log audit \(Logs are stored for seven days by default.\)|Not supported.|Provides quintuple logs. **Note:** A quintuple log contains the information of a source IP address, a source port, a destination IP address, a destination port, and a transport layer protocol.

|Provides quintuple logs.|Provides quintuple logs.|If you enable the [log analysis](/intl.en-US/Logs/Log analysis/Overview.md) feature, Cloud Firewall stores the logs generated in the last six months and allows you to export the logs.|
|Expert service|Not supported.|Supported.|Supported.|Supported.|N/A.|
|Cluster deployment|Not supported.|Uses shared resources.|Uses shared resources.|Uses dedicated resources.You can [submit a ticket](https://workorder-intl.console.aliyun.com/#/ticket/add/?productId=80) to change the resource specifications.|N/A.|
|Subscription mode|Free of charge for trial use.|Shortest subscription period: six months.|Monthly subscription supported.|Monthly subscription supported.|N/A.|

## VPC firewall limits

A VPC firewall helps you detect and control the traffic between VPCs that are connected by using Express Connect or Cloud Enterprise Network \(CEN\). Different network environments have different limits for enabling VPC firewalls. For more information, see [VPC firewall limits](/intl.en-US/Firewall Settings/VPC Firewall/VPC firewall limits.md).


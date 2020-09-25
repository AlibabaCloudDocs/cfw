# Editions and regions

This topic describes the differences between Cloud Firewall editions and supported regions.

## Differences in features and billing between Cloud Firewall editions

|Feature or billing item|Trial Edition|Premium Edition|Enterprise Edition|Ultimate Edition|
|-----------------------|-------------|---------------|------------------|----------------|
|Basic price per month|Free of charge.|USD 420|USD 1,450|USD 3,900|
|Peak Internet bandwidth of protected traffic|Not supported.|Default value: 10 Mbit/s per month. You can increase the bandwidth. **Extra fee**: USD 7 per month for each increase of 1 Mbit/s of bandwidth.

|Default value: 50 Mbit/s per month. You can increase the bandwidth. **Extra fee**: USD 7 per month for each increase of 1 Mbit/s of bandwidth.

|Default value: 200 Mbit/s per month. You can increase the bandwidth. **Extra fee**: USD 7 per month for each increase of 1 Mbit/s of bandwidth. |
|Number of protected public IP addresses|Not supported.|Default value: 20. You can increase the quota. **Extra fee**: USD 7 per month for each additional public IP address that you want to protect.

|Default value: 50. You can increase the quota. **Extra fee**: USD 7 per month for each additional public IP address that you want to protect.

|Default value: 200. You can increase the quota. **Extra fee**: USD 7 per month for each additional public IP address that you want to protect. |
|Maximum number of access control policies **Note:** If an access control policy involves multiple source CIDR blocks, destination CIDR blocks, or ports, this policy is counted as N policies. N = **Number of source CIDR blocks × Number of destination CIDR blocks × Number of ports**. If a policy involves only one source CIDR block, one destination CIDR block, and one port, this policy is counted as **one** policy.

|Not supported.|4,000.|10,000.|20,000. You can [submit a ticket](https://workorder-intl.console.aliyun.com/#/ticket/add/?productId=80) to increase the quota.|
|Threat detection by using an intrusion prevention system \(IPS\) and installation of virtual patches|Not supported.|Supported.|Supported.|Supported.|
|IPS whitelist|Not supported.|Not supported.|Supported.|Supported.|
|Visualization of security group traffic|Not supported.|Not supported.|Supported.|Supported.|
|Synchronization of security group policies|Supported.|Not supported.|Supported.|Supported.|
|Isolation between VPCs|Not supported.|Not supported.|Supported.|Supported.|
|Number of protected VPCs|Not supported.|N/A.|Default value: 2. You can [submit a ticket](https://workorder-intl.console.aliyun.com/#/ticket/add/?productId=80) to increase the quota. **Extra fee**: USD 300 per month for each additional VPC that you want to protect.

|Default value: 5. You can [submit a ticket](https://workorder-intl.console.aliyun.com/#/ticket/add/?productId=80) to increase the quota. **Extra fee**: USD 300 per month for each additional VPC that you want to protect. |
|Maximum inter-VPC traffic that can be protected|Not supported.|N/A.|100 Mbit/s|1 Gbit/s|
|Unified VPC protection across Alibaba Cloud accounts \(with Cloud Enterprise Network enabled\)|Not supported.|Not supported.|Not supported.|Supported.|
|Log audit \(Logs are stored for seven days by default.\) **Note:** If you enable the [log audit](/intl.en-US/Logs/Log analysis/Overview.md) feature, Cloud Firewall stores the logs generated in the last six months and allows you to export the logs.

|Not supported.|Provides quintuple logs. **Note:** A quintuple log contains the information of a source IP address, a source port, a destination IP address, a destination port, and a transport layer protocol.

|Provides quintuple logs.|Provides quintuple logs.|
|Expert service|Not supported.|Supported.|Supported.|Supported.|
|Cluster deployment|Not supported.|Uses shared resources.|Uses shared resources.|Uses dedicated resources. You can [submit a ticket](https://workorder-intl.console.aliyun.com/#/ticket/add/?productId=80) to change resource specifications.|
|Subscription mode|Free trial.|Shortest subscription period: six months.|Monthly subscription supported.|Monthly subscription supported.|

## Regions supported by Cloud Firewall

Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext). In the left-side navigation pane, click Firewall Settings and then the Internet Firewall tab to view the supported regions.

![Regions supported by Cloud Firewall](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/8021507951/p103362.png)

**Note:** Before you purchase Cloud Firewall, make sure that your cloud assets are deployed in the regions supported by Cloud Firewall. Cloud assets include public IP addresses of Elastic Compute Service \(ECS\), Elastic IP addresses \(EIPs\) of Server Load Balancer \(SLB\), High-availability virtual IP addresses \(HAVIP\), EIPs, EIPs of ECS, EIPs of Elastic Network Interface \(ENI\), public IP addresses of SLB, and EIPs of Network Address Translation \(NAT\) Gateway. If your cloud assets are not deployed in regions supported by Cloud Firewall, Cloud Firewall cannot protect these assets even if you have purchased Cloud Firewall. In this case, you must [submit a ticket](https://workorder-intl.console.aliyun.com/#/ticket/add/?productId=80) to apply for a refund.

|Alibaba Cloud account type|Supported region|
|--------------------------|----------------|
|Account registered on the International site \(alibabacloud.com\)|**Regions in China:**-   China \(Beijing\)
-   China \(Zhangjiakou-Beijing Winter Olympics\)
-   China \(Hangzhou\)
-   China \(Shanghai\)
-   China \(Shenzhen\)
-   China \(Hong Kong\) |
|**Regions outside China:**-   Singapore \(Singapore\)
-   Malaysia \(Kuala Lumpur\)
-   Indonesia \(Jakarta\)
-   Germany \(Frankfurt\) |

## VPC firewall limits

A VPC firewall helps you detect and control the traffic between VPCs that are connected by using Express Connect or Cloud Enterprise Network \(CEN\). Different network environments have different limits for enabling VPC firewalls. For more information, see [VPC firewall limits](/intl.en-US/Firewall Settings/VPC Firewall/VPC firewall limits.md).


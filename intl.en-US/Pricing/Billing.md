# Billing

This topic describes the billing of Cloud Firewall. Cloud Firewall has a free trial edition and three paid editions: Premium, Enterprise, and Ultimate.

## Features and billing items of each edition

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

**Note:** Cloud Firewall protects the assets only on Alibaba Cloud, which include ECS instances, Elastic IP addresses, SLB instances, and Bastionhost instances.

## Billing example

A user has 60 public IP addresses and requires a bandwidth of 60 Mbit/s. If the user subscribes to Cloud Firewall in the Enterprise Edition for six months, the user must pay the extra fees of 10 public IP addresses and 10 Mbit/s of bandwidth. The total service fee is USD 9,540, which is the calculation result of \(1,450 + 10 × 7 + 10 × 7\) × 6.

## Billing method

Cloud Firewall uses the subscription billing method. For more information, see [Subscription](/intl.en-US/Pricing/Purchase a Cloud Firewall edition.mdol_vyl_1sf_cfb).

## Billing cycle

The billing cycle starts from the date you purchase your Cloud Firewall instance and ends on the date your Cloud Firewall instance expires.

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

## References

[Purchase a Cloud Firewall edition](/intl.en-US/Pricing/Purchase a Cloud Firewall edition.md)

[Renewal and upgrade](/intl.en-US/Pricing/Renewal and upgrade.md)

[Trial](/intl.en-US/Pricing/Trial.md)

[Cloud Firewall trial and pre-sales consulting]()


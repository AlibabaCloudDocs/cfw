# Billing

This topic describes the billing methods of Cloud Firewall. Cloud Firewall has a free trial edition and three paid editions: Premium, Enterprise, and Ultimate.

## Features and billable items of each edition

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

**Note:** Cloud Firewall protects only Alibaba Cloud assets. The assets include Elastic Compute Service \(ECS\) instances, elastic IP addresses \(EIPs\), Server Load Balancer \(SLB\) instances, and bastion hosts.

## Billing examples

A user has 60 public IP addresses and requires a bandwidth of 60 Mbit/s. If the user subscribes to Cloud Firewall that runs the Enterprise Edition for six months, the total service fee is calculated by using the following formula:\(USD 1,450 + Fee of extra 10 public IP addresses × USD 7 + Fee of extra 10 Mbit/s bandwidth × USD 7\) × 6

## Billing method

Cloud Firewall uses the subscription billing method. For more information, see [Purchase Cloud Firewall](/intl.en-US/Pricing and Service Activation/Purchase Cloud Firewall.mdol_vyl_1sf_cfb).

## Billing cycle

The billing cycle starts from the date you purchase Cloud Firewall and ends on the date Cloud Firewall expires.

## Regions supported by Cloud Firewall

Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext). In the left-side navigation pane, click Firewall Settings and then the Internet Firewall tab to view the supported regions.

![Regions supported by Cloud Firewall](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/8021507951/p103362.png)

**Note:** Before you purchase Cloud Firewall, make sure that your cloud assets are deployed in the regions supported by Cloud Firewall. Cloud assets include the public IP addresses of Elastic Compute Service \(ECS\) instances, elastic IP addresses \(EIPs\) of Server Load Balancer \(SLB\) instances, High-Availability Virtual IP Addresses \(HAVIPs\), EIPs, EIPs of ECS instances, EIPs of Elastic Network Interfaces \(ENIs\), public IP addresses of SLB instances, and EIPs of network address translation \(NAT\) gateways. If your cloud assets are not deployed in the regions supported by Cloud Firewall, Cloud Firewall cannot protect these assets even if you have purchased this service. In this case, submit a [ticket](https://workorder-intl.console.aliyun.com/#/ticket/add/?productId=80) to apply for a refund.

|Alibaba Cloud account type|Supported region|
|--------------------------|----------------|
|Account created on the International site \(alibabacloud.com\)|**Regions in China:**-   China \(Beijing\)
-   China \(Zhangjiakou\)
-   China \(Hangzhou\)
-   China \(Shanghai\)
-   China \(Shenzhen\)
-   China \(Hong Kong\) |
|**Regions outside China:**-   Singapore \(Singapore\)
-   Malaysia \(Kuala Lumpur\)
-   Indonesia \(Jakarta\)
-   Germany \(Frankfurt\)
-   Japan \(Tokyo\) |

## References

[Purchase Cloud Firewall](/intl.en-US/Pricing and Service Activation/Purchase Cloud Firewall.md)

[Renew the subscription to Cloud Firewall](/intl.en-US/Pricing and Service Activation/Renewal and upgrade.md)

[Apply for a free trial of Cloud Firewall](/intl.en-US/.md)

[Product trial and pre-sales consultation]()


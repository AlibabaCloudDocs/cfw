# Release notes

This topic describes the release notes of Cloud Firewall features.

## 2020

|Release date|Category|Feature|Description|Involved edition|Documentation|
|------------|--------|-------|-----------|----------------|-------------|
|2021-02-05|Experience optimization|The Overview page is modified.|The following modules are added to the Overview page: Asset Protection, Protection, Cloud Firewall Tutorial, and Recent Updates.|All paid editions|[Overview](/intl.en-US/Overview/Overview.md)|
|2021-01-28|Experience optimization|The notification feature is upgraded.|The following notification items are added: Protection Against Vulnerabilities, Asset Protection, and Intrusion Prevention.|All paid editions|[Modify notification and contact settings](/intl.en-US/.md)|
|2021-01-28|Experience optimization|Traffic analysis details can be downloaded.|The details of Outbound Connections, Internet Access, and VPC Access can be downloaded to your computer for check and analysis.|All paid editions|[Outbound connections](/intl.en-US/Traffic Analysis/Outbound connections.md) [Internet access](/intl.en-US/Traffic Analysis/Internet access.md)

 [VPC access](/intl.en-US/Traffic Analysis/VPC access.md) |
|2021-01-19|New feature|Intrusions can be blocked by the intrusion prevention system \(IPS\) based on different block modes.|Different block modes are available in Threat Engine Mode to block intrusion attempts based on rule groups.|All paid editions|[Intrusion prevention mode](/intl.en-US/Intrusion prevention/Intrusion prevention.mdsection_tpr_jxp_cfb)|
|2021-01-19|Experience optimization|The Internet firewall is available in the China \(Guangzhou\) region.|The Internet firewall can be enabled for Elastic Compute Service \(ECS\) instances that are deployed in the China \(Guangzhou\) region.|All paid editions|[Regions that are supported by Cloud Firewall](/intl.en-US/Product Introduction/Regions that are supported by Cloud Firewall.md)|
|2020-12-29|New feature|Attack payloads are included in IPS blocking records.|Attack payloads are included in IPS blocking records. This way, you can analyze attack behavior in a more comprehensive manner.|All paid editions|[Traffic blocked by IPS](/intl.en-US/Intrusion prevention/Traffic blocked by IPS.md)|
|2020-12-10|Experience optimization|Access control policies can be located by searching for IP addresses.|Access control policies that use the IP address book or Classless Inter-Domain Routing \(CIDR\) block of a specific IP address can be located by searching for the IP address.|All paid editions|None|
|2020-12-10|Experience optimization|Policy IDs are provided for the Internet firewall.|Policy IDs are provided for the Internet firewall, which helps you identify specific policies by their policy IDs.|All paid editions|[Search for a specific policy based on the policy ID](/intl.en-US/Access control/Access control for outbound and inbound traffic on the Internet firewall.mdsection_nsl_yli_zb2)|
|2020-12-10|New feature|The policy export feature is introduced.|Both inbound and outbound access control policies of the Internet firewall can be exported to your computer.|All paid editions|[Export policies](/intl.en-US/Access control/Access control for outbound and inbound traffic on the Internet firewall.md)|
|2020-12-03|Experience optimization|The types of cloud assets are displayed below the Cloud Address Books option of inbound access control policies.|In the inbound access control policies of the Internet firewall, the types of cloud assets are displayed below the Cloud Address Books option. This way, you can configure access control policies for specific cloud assets.|All paid editions|None|
|2020-12-03|Experience optimization|The display of statistics on brute-force attacks and scanning risks is optimized on the Overview page.|The display of statistics on brute-force attacks and scanning risks is optimized on the Overview page. This way, you can obtain attack status in a more intuitive manner.|All paid editions|None|
|2020-12-03|Experience optimization|The lists on the Access Control page are optimized.|Pagination is supported for the lists on the Access Control page.|All paid editions|None|
|2020-11-17|New feature|Secure forward proxies are supported.|Outbound traffic from NAT Gateway to the Internet can be protected and controlled.|Enterprise Edition and Ultimate Edition|[Use secure forward proxies](/intl.en-US/Firewall Settings/Use secure forward proxies.md)|
|2020-11-19|New feature|Auto-renewal is supported.|Auto-renewal is supported by Cloud Firewall. This feature helps prevent service suspension if you do not renew your service on time.|All paid editions|[Enable the auto-renewal feature](/intl.en-US/Pricing and Service Activation/Renewal and upgrade.md)|
|2020-09-17|New feature|Notification settings are supported.|Notification settings are supported by Cloud Firewall. If Cloud Firewall detects abnormal traffic, compromised hosts, or suspicious outbound connections in your assets, Cloud Firewall sends notifications by text message or email.|All paid editions|[Modify notification and contact settings](/intl.en-US/.md)|
|2020-09-17|New feature|The safeguard mode for major activities is supported.|The Strict Mode switch is added to the Toolbox page.|Enterprise Edition|[t1952831.md\#]()|
|2020-07-30|New feature|The check of security group configurations is supported.|The feature used to check security group configurations is added to the Toolbox page.|All paid editions|[Check security group rules](/intl.en-US/Toolbox/Check security group rules.md)|
|2020-06-04|Experience optimization|The strict mode of access control policies is optimized.|The Strict Mode switch is moved from the Internet Firewall tab of the Access Control page to the Toolbox page.|All paid editions|[Strict mode of the Internet firewall](/intl.en-US/Toolbox/Strict mode of the Internet firewall.md)|
|2020-06-04|New feature|Policy rollback is supported.|The policy rollback feature is added to the Toolbox page.|Enterprise Edition and Ultimate Edition|[Back up and roll back an access control policy](/intl.en-US/Toolbox/Back up and roll back an access control policy.md)|
|2020-04-16|Experience optimization|The Breach Awareness page is introduced.|Intrusion Detection is renamed Breach Awareness. The Breach Awareness page displays the intrusions detected by the IPS.|All paid editions|[Breach awareness](/intl.en-US/Intrusion prevention/Breach awareness.md)|
|2020-03-19|New feature|Enterprise policy groups are supported.|Enterprise policy groups are supported by internal firewalls.|Enterprise Edition and Ultimate Edition|[Access control on an internal firewall between ECS instances](/intl.en-US/Access control/Access control on an internal firewall between ECS instances.md)|
|2020-03-19|New feature|The strict mode of access control policies is supported.|The strict mode is supported by the Internet firewall.|All paid editions|[Strict mode of the Internet firewall](/intl.en-US/Toolbox/Strict mode of the Internet firewall.md)|
|2020-02-21|New feature|Mining activities over outbound connections are displayed.|Mining activities are displayed on the Outbound Connections page.|All paid editions|[Outbound connections](/intl.en-US/Traffic Analysis/Outbound connections.md)|
|2020-02-21|New feature|The most commonly encountered vulnerabilities are displayed.|The most commonly encountered vulnerabilities are displayed.|All paid editions|None|
|2020-02-21|New feature|The alerting feature is optimized.|Cloud Firewall is connected with Cloud Monitor to display alerts.|All paid editions|None|
|2020-02-21|New feature|Internal firewalls are optimized.|The operations logs of internal firewalls are provided.|Enterprise Edition and Ultimate Edition|None|

## 2019

|Release date|Description|Involved edition|Documentation|
|------------|-----------|----------------|-------------|
|2019-12|Default allow policies are supported. You can change default inbound policies from Deny to Allow for security groups.|All paid editions|[Default allow policies for security groups](/intl.en-US/Access control/Default allow policies for security groups.md)|
|2019-12|If Destination Type of an access control policy is set to Domain Name, Cloud Firewall resolves domain names and displays resolution results.|All paid editions|[Configure access control policies for domain names](/intl.en-US/Access control/Configure access control policies for domain names.md)|
|2019-12|The page on which you create a VPC firewall is updated.|All paid editions|[Create a VPC firewall](/intl.en-US/Firewall Settings/VPC Firewall/Create a VPC firewall.md)|
|2019-10|Log reports are supported. You can subscribe to reports and view the traffic data collected by using the log analysis feature.|All paid editions|[Log reports](/intl.en-US/Logs/Log analysis/Log reports.md)|
|2019-09|Intelligent policies can be delivered to protect your networks and hosts against security threats.|All paid editions|[Intelligent policies](/intl.en-US/Traffic Analysis/Intelligent policies.md)|
|2019-05|Region-based blocking is implemented to allow access only from specified regions, which prevents unauthorized logons and brute-force attacks.|All paid editions|[Access control for outbound and inbound traffic on the Internet firewall](/intl.en-US/Access control/Access control for outbound and inbound traffic on the Internet firewall.md)|
|2019-01|Internet access control is supported. Cloud Firewall analyzes access relationships among services and displays analysis results without the need for configuration.|Enterprise Edition|[Internet access](/intl.en-US/Traffic Analysis/Internet access.md)|

## 2018

|Release date|Description|Involved edition|Documentation|
|------------|-----------|----------------|-------------|
|2018-08|The IPS whitelist feature is introduced. This feature allows you to create IPS whitelists to allow access only from trusted sources.|All paid editions|[Intrusion prevention](/intl.en-US/Intrusion prevention/Intrusion prevention.md)|


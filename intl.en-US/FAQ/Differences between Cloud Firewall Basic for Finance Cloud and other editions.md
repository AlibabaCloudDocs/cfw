# Differences between Cloud Firewall Basic for Finance Cloud and other editions {#concept_yt5_zhs_xgb .concept}

You can upgrade Cloud Firewall Basic to Cloud Firewall Pro or Enterprise in the following situations:

-   You want to know the EIPs and ports that are enabled for your businesses in the cloud, and the risks of enabling these IP addresses and ports.
-   You need to save a log that contains records over the last six months for security regulation and compliance requirements.
-   You need to control network access based on domain names. You want to control requests sent from your instances to the Internet and only allow requests destined for the specified domain names and IP addresses.
-   You need to control network access based on the applications that use the FTP and MQTT protocols.
-   In addition to Finance Cloud in the China \(Hangzhou\) region, you also need to use Cloud Firewall to protect resources in other regions.

## Differences between Cloud Firewall Basic for Finance Cloud and other editions {#section_app_dg5_xgb .section}

|Function|Description|Basic for Finance Cloud in the China \(Hangzhou\) region|Pro|Enterprise|
|--------|-----------|--------------------------------------------------------|---|----------|
|Firewall|Access control based on IP addresses and ports.|√|-|-|
|Access control based on applications.|X.|√|√|
|Access control based on domain names.|X.|√|√|
|External connection detection.|X.|√|√|
|Intrusion prevention.|Basic IPS detection.|√|√|√|
|Virtual patches.|√|√|√|
|Threat intelligence.|√|√|√|
|Network access activities.|Internet access activities.|X.|√|√|
|External connections.|X.|√|√|
|Intrusion prevention activities|X.|√|√|
|IPS analysis.|X.|√|√|
|All access activities.|X|√|√|
|Logs|Logs include the security log, access log, and operation log. Newly created log entries are kept for up to six months.|X.|√|√|
|Micro-segmentation.|Network topology visualization and business topology visualization.|X.|X.|√|
|Micro-segmentation \(access control in the east-west direction\).|X.|X.|√|
|Others.|Supported regions.|The China \(Hangzhou\) region of Finance Cloud.|Only one region is supported.|Up to three regions are supported.|
|Performance.|Bandwidth \(Internet border firewall throughput\).|-|Default: 10 Mbit/s. Upgradable.|Default: 50 Mbit/s. Upgradable.|
|Maximum number of ECS instances supported by micro-segmentation.|Micro-segmentation is not supported.|Micro-segmentation is not supported.|Default: 50 ECS instances. Upgradable.|
|Maximum number of EIPs supported by each firewall.|-|20 EIPs.|100 EIPs.|
|Maximum number of policies.|200 policies.|1,000 policies.|2,000 policies.|


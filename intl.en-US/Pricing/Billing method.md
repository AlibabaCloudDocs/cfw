# Billing method {#concept_twk_1lk_bfb .concept}

Cloud Firewall has three editions: Advanced, Enterprise, and Flagship.

These editions provide different features. For more information, see [Features](../../../../reseller.en-US/Product Introduction/Features.md#table_qsv_slr_cfb).

**Billing of the Cloud Firewall service**

**Note:** Currently, only the users with ECS instances based in Malaysia or Singapore can purchase the Cloud Firewall.

|Feature and billing item|Advanced Edition|Enterprise Edition|Flagship Edition|
|------------------------|----------------|------------------|----------------|
|Basic price/month|420 USD/month|1450 USD/month|3900 USD/month|
|Number of supported Alibaba Cloud assets \(ECS, EIP, and SLB instances\)|The micro-isolation feature is not supported, and the number of ECS instances is not limited.|50 ECS instances by default, which can be scaled out **Extra charge**: 3.8 USD/month for each additional ECS instance

 |200 ECS instances by default, which can be scaled out **Extra charge**: 3.8 USD/month for each additional ECS instance

 |
|Bandwidth \(Internet firewall throughput\)|10 Mbps/month by default, which can be increased **Extra charge**: 15.5 USD/month/Mbps for increased bandwidth

 |50 Mbps/month by default, which can be increased **Extra charge**: 15.5 USD/month/Mbps for increased bandwidth

 |Mbps/month by default, which can be increased **Extra charge**: 15.5 USD/month/Mbps for increased bandwidth

 |
|Number of enabled public IP addresses|Support 20 public IPs by default. **Extra charge**: Support one more public IP for each additional 1 Mbit/s bandwidth

 |Support 100 public IPs by default. **Extra charge**: Support one more public IP for each additional 1 Mbit/s bandwidth

 |Support 400 public IPs by default. **Extra charge**: Support one more public IP for each additional 1 Mbit/s bandwidth

 |
|Number of supported policies|1,000|2,000|5,000|
|Threat detection and virtual patching of IPS|Supported|Supported|Supported|
|IPS whitelist|Not supported|Supported|Supported|
|Security group and business topology|Not supported|Supported|Supported|
|Logs \(default storage duration: 7 days\) **Note:** If you need log duration to be extended to 6 months, you can buy the Log Analysis service of Cloud Firewall.

 |Logs collecting 5-tuple information. The log storage capacity of Log Analysis is 80 USD/T \(1000G\).

 |Logs collecting 5-tuple information. The log storage capacity of Log Analysis is 80 USD/T \(1000G\).

 |Logs collecting 5-tuple information. The log storage capacity of Log Analysis is 80 USD/T \(1000G\).

 |
|Number of supported regions|Support 1 region by default. **Extra charge**: Support one more region for each additional 50 Mbit/s bandwidth

 |Support 3 regions by default. **Extra charge**: Support one more region for each additional 50 Mbit/s bandwidth

 |Support multiple regions by default.|
|Cluster deployment|Shared resources|Shared resources|Exclusive resources|

**Note:** Cloud Firewall protects Alibaba Cloud assets including ECS, EIP, and intranet SLB. It currently does not support non-Alibaba Cloud servers.

## Billing example {#section_ktc_zzz_ygb .section}

Assume that an Enterprise Edition user has 60 Alibaba Cloud assets with the bandwidth being 60 Mbit/s. Compared to the default number of supported Alibaba Cloud assets and default bandwidth, the user uses 10 additional ECS instances and 10 Mbit/s increased bandwidth. If this user subscribes to the Cloud Firewall service for six months, the service fee \(unit: USD\) is calculated as follows: \(1,500 USD + 4 USD x 10 + 16 USD × 10\) × 6.

## Billing method {#section_gbn_fbc_zdb .section}

Month or annual subscription.

For more information, see [Subscription](reseller.en-US/Pricing/Subscription.md#ol_vyl_1sf_cfb).

## Billing period {#section_hbn_fbc_zdb .section}

You are billed for the validity period specified in your subscription.

## Related {#section_ouh_zjn_m3i .section}

[Subscription](reseller.en-US/Pricing/Subscription.md#)

[Renewal and upgrade](reseller.en-US/Pricing/Renewal and upgrade.md#)

[Trial](reseller.en-US/Pricing/Trial.md#)

[Cloud Firewall trial and pre-sales consulting](../../../../reseller.en-US/FAQ/Cloud Firewall trial and pre-sales consulting.md#)


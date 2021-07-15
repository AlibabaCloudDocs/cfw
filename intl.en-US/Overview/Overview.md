# Overview

The Overview page of the Cloud Firewall console displays the overall protection capabilities and statistics on your Cloud Firewall. The statistics include unhandled events, protected assets, security protection data, traffic trends, scenario-specific data, and recent updates. On the Overview page, you can obtain the overall security status of your network assets.

## Go to the Overview page

Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext). In the left-side navigation pane, click **Overview**. The **Overview** page appears, as shown in the following figure.

![Overview page](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/8012806261/p78161.png)

The **Overview** page consists of seven sections. You can click the following links to view the individual sections:

-   [Unhandled Event](#section_j1g_sld_4rv) \(marked by 1\)
-   [Asset Protection](#section_wj3_hqh_w7i) \(marked by 2\)
-   [Protection](#section_u4d_ei7_b9e) \(marked by 3\)
-   [Security Policies](#section_o8w_i7t_m65) \(marked by 4\)
-   [Traffic Trends](#section_fev_jef_sfq) \(marked by 5\)
-   [Scenario Data](#section_hlh_2sx_yvk) \(marked by 6\)
-   [Recent Updates](#section_xxc_jsu_gk2) \(marked by 7\)

In the upper-right corner of the **Overview** page, you can view the edition and remaining validity period of your Cloud Firewall. You can also perform the following operations:

-   Click **Bandwidth Upgrade**, **Upgrade**, **Renew**, or **Auto Renewal** to perform specific operations. For more information, see [Upgrade and renew](/intl.en-US/Overview/Upgrade and renewal.md).
-   Click **More** to view the details of your Cloud Firewall. The details include **Protected Internet Traffic**, **Recent Peak Traffic**, **Public IP Address Quota**, **Protected VPCs**, **Audit Logs Stored**, and **Multi-account Quota**.

![More](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/8012806261/p238333.png)

## Unhandled Event

This section displays the protection situation of your assets. In this section, you can view **Breached Hosts**, **Detected Vulnerabilities**, **Open Ports**, and **Risk Outbound Connections** that Cloud Firewall detects.

![Unhandled Event](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/8012806261/p132997.png)

In this section, you can perform the following operations:

-   Specify a time range for query: In the upper-right corner of the section, click the time drop-down list and select a specific time range. The valid values are **Last 1 Day** and **Last 7 Days**.
-   Handle an exception event: Move the pointer over a specific type of exception event and click **Handle Now**. On the page that appears, you can view and handle the exception events of this type. For example, click **Handle Now** in **Risk Outbound Connections**. The **Outbound Connections** page appears, and you can handle exception events of this type.

    For more information about how to handle different types of exception events, see the following topics:

    -   [Breach awareness](/intl.en-US/Intrusion Prevention/Breach awareness.md)
    -   [Vulnerability prevention](/intl.en-US/Intrusion Prevention/Vulnerability prevention.md)
    -   [Internet access](/intl.en-US/Traffic Analysis/Internet access.md)
    -   [Outbound connections](/intl.en-US/Traffic Analysis/Outbound connections.md)

## Asset Protection

This section displays the protection status of your assets. In this section, you can view **Internet Firewall**, **VPC Firewalls**, and **Internal Firewalls** to check the number of the public IP addresses that are protected by specific firewalls and the number of the public IP addresses that are not protected by specific firewalls.

![Asset Protection](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/8012806261/p238289.png)

In the upper-right corner of this section, select **Auto-renewal by Month** to enable Cloud Firewall to continuously protect your network assets.

If an asset is not protected, you can enable the required firewall on the **Firewall Settings** page of the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext). For more information, see [Enable or disable Internet Firewall](/intl.en-US/Firewall Settings/Enable or disable Internet Firewall.md) and [Enable or disable VPC Firewall](/intl.en-US/Firewall Settings/VPC Firewall/Enable or disable VPC Firewall.md).

## Protection

This section displays the numbers of times that specific modules are triggered to protect your assets. In this section, you can view **Total Attacks Blocked**, **Intrusions Blocked**, **Requests Blocked**, and **Vulnerability Exploits Blocked**.

![Enabled protection capabilities](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/8012806261/p133011.png)

In this section, you can perform the following operations:

-   Specify a time range for query: In the upper-right corner of the section, click the time drop-down list and select a specific time range. The valid values are **Last 1 Day** and **Last 7 Days**.
-   View details: Click **Show** in the lower-right corner to view the statistics on different protection modules.

    For more information about the protection modules, see the following topics:

    -   [Intrusion prevention](/intl.en-US/Intrusion Prevention/Intrusion prevention.md)
    -   [Overview of access control policies](/intl.en-US/Access Control/Overview of access control policies.md)
    -   [Vulnerability prevention](/intl.en-US/Intrusion Prevention/Vulnerability prevention.md)

## Security Policies

This section displays the statistics on access control policies. In this section, you can view **Intelligent Policies to be Delivered** and **Total Access Control Policies**. You can also view the change in Total Access Control Policies from the last seven days.

![Security Policies](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/8012806261/p286820.png)

On the **Access Control** page, you can view and deliver the intelligent policies that are recommended by Cloud Firewall. For more information, see [Apply intelligent policies](/intl.en-US/Access Control/Apply intelligent policies.md).

In the upper-right corner of this section, you can click **View Best Practices** to view the best practices of Cloud Firewall.

## Traffic Trends

This section displays the trends in the overall traffic of your assets that are protected by Cloud Firewall, as well as the changes in the sessions whose inbound or outbound traffic is blocked by Cloud Firewall.

![Traffic Trends](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/0117685161/p78162.png)

In this section, you can perform the following operations:

-   Specify a time range for query: In the upper-right corner of the section, click the time drop-down list and select a specific time range. The valid values are **Last 1 Day** and **Last 7 Days**.
-   View a specific trend: Switch between the **Traffic Trends**, **Blocking Trends of Inbound Traffic**, and **Blocking Trends of Outbound Traffic** tabs to view the specific trend.

## Scenario Data

This section displays the information about brute-force attacks and scanning risks that Cloud Firewall detects on your assets.

![Scenario Data](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/0117685161/p78163.png)

In this section, you can perform the following operations:

-   Specify a time range for query: In the upper-right corner of the section, click the time drop-down list and select a specific time range. The valid values are **Last 1 Day** and **Last 7 Days**.
-   View the data of a specific scenario: Switch between the **Brute Force** and **Scan** tabs to view specific data.
    -   **Brute Force**: displays the statistics on brute-force attacks and the rankings of attacked applications and assets. The statistics include **Attacks**, **Blocking**, **Applications**, and **Assets**.
    -   **Scan**: displays the statistics on scanning risks and the rankings of scanned applications and assets. The statistics include **Attacks**, **Blocking**, **Applications**, and **Assets**.

## Recent Updates

This section displays the update records of **Virtual Patches**, **Rules**, and **Features** of Cloud Firewall.

![Recent Updates](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/0117685161/p238323.png)

You can switch between the **Virtual Patches**, **Rules**, and **Features** tabs to view specific update records.


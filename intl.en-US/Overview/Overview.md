# Overview

The Overview page of the Cloud Firewall console displays the overall protection capabilities and statistics of your Cloud Firewall. The statistics include unhandled events, protected assets, security protection data, traffic trends, and scenario data. On the Overview page, you can obtain the overall security status of your network assets.

## Access the Overview page

Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext)[Cloud Firewall console](https://partners-yundun.console.aliyun.com/?p=cfwnext). In the left-side navigation pane, click **Overview**. The **Overview** page appears, as shown in the following figure.

![Overview page](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/6486685161/p78161.png)

The **Overview** page consists of seven sections. You can click the following links to view the individual sections:

-   [Unhandled Event](#section_j1g_sld_4rv) \(marked by 1\)
-   [Asset Protection](#section_wj3_hqh_w7i) \(marked by 2\)
-   [Protection](#section_u4d_ei7_b9e) \(marked by 3\)
-   [Cloud Firewall Tutorial](#section_iq6_0hp_bf8) \(marked by 4\)
-   [Traffic Trend](#section_fev_jef_sfq) \(marked by 5\)
-   [Scenario Data](#section_hlh_2sx_yvk) \(marked by 6\)
-   [Recent Updates](#section_xxc_jsu_gk2) \(marked by 7\)

In the upper-right corner of the **Overview** page, you can view the edition and validity period of your Cloud Firewall. You can also perform the following operations:

-   Click **Bandwidth Upgrade**, **Upgrade**, **Renew**, or **Auto Renewal** to perform specific operations. For more information, see [Upgrade and renew](/intl.en-US/Overview/Upgrade and renewal.md).
-   Click **More** to view the details of your Cloud Firewall. The details include **Protected Internet Traffic**, **Recent Peak Traffic**, **Public IP Address Quota**, **Protected VPCs**, and **Audit Logs Stored**.

![More](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/6486685161/p238333.png)

## Unhandled Event

This section displays the protection situation of your assets. In this section, you can view **Breached Hosts**, **Detected Vulnerabilities**, **Unprotected Open Ports**, and **Risk Outbound Connections** that Cloud Firewall detects.

![Unhandled Event](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/6486685161/p132997.png)

In this section, you can perform the following operations:

-   Specify a time range for query: In the upper-right corner of the section, click the time drop-down list and select a specific time range. The valid values of the time drop-down list are **Last 1 Hour**, **Last 1 Day**, and **Last 7 Days**.
-   Handle an exception event: Move the pointer over a specific type of exception event and click **Handle Now**. On the page that appears, you can view and handle the exception events of this type. For example, click **Handle Now** in **Risk Outbound Connections**. The **Outbound Connections** page appears, and you can handle exception events of this type.

    For more information about how to handle different types of exception events, see the following topics:

    -   [Breach awareness](/intl.en-US/Traffic Analysis/Breach awareness.md)
    -   [Vulnerability prevention](/intl.en-US/Intrusion prevention/Vulnerability prevention.md)
    -   [Internet access](/intl.en-US/Traffic Analysis/Internet access.md)
    -   [Outbound connections](/intl.en-US/Traffic Analysis/Outbound connections.md)

## Asset Protection

This section displays the protection status of your assets. In this section, you can view **Internet Firewall**, **VPC Firewalls**, and **Internal Firewalls** to check whether your public IP addresses are protected by specific firewalls.

![Asset Protection](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/6486685161/p238289.png)

If a public IP address is not protected, you can enable the required firewall on the **Firewall Settings** page of the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext)[Cloud Firewall console](https://partners-yundun.console.aliyun.com/?p=cfwnext). For more information, see [Enable or disable Internet Firewall](/intl.en-US/Firewall Settings/Enable or disable Internet Firewall.md) and [Enable or disable VPC Firewall](/intl.en-US/Firewall Settings/VPC Firewall/Enable or disable VPC Firewall.md).

## Protection

This section displays the numbers of times that specific modules are triggered to protect your assets. In this section, you can view **Total Attacks Blocked**, **Intrusions Blocked**, **Requests Blocked**, and **Vulnerability Exploits Blocked**.

![Enabled protection capabilities](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/6486685161/p133011.png)

In this section, you can perform the following operations:

-   Specify a time range for query: In the upper-right corner of the section, click the time drop-down list and select a specific time range. The valid values of the time drop-down list are **Last 1 Hour**, **Last 1 Day**, and **Last 7 Days**.
-   View details: Click **Show** to view the statistics on other protection modules.

    For more information about the protection modules, see the following topics:

    -   [Traffic blocked by IPS](/intl.en-US/Traffic Analysis/Traffic blocked by IPS.md)
    -   [Overview of access control policies](/intl.en-US/Access control/Overview of access control policies.md)
    -   [Vulnerability prevention](/intl.en-US/Intrusion prevention/Vulnerability prevention.md)

## Cloud Firewall Tutorial

This section provides a link to the tutorial for the best practices of Cloud Firewall.

![Cloud Firewall Tutorial](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/4117685161/p238321.png)

You can click **Get Started** to view the tutorial.

## Traffic Trend

This section displays the trends in the overall traffic of your assets that are protected by Cloud Firewall, as well as the sessions whose inbound or outbound traffic is blocked by Cloud Firewall.

![Traffic Trend](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/0117685161/p78162.png)

In this section, you can perform the following operations:

-   Specify a time range for query: In the upper-right corner of the section, click the time drop-down list and select a specific time range. The valid values of the time drop-down list are **Last 1 Hour**, **Last 1 Day**, and **Last 7 Days**.
-   View a specific trend: Switch between the **Traffic Trend**, **Blocking Trends of Inbound Traffic**, and **Blocking Trends of Outbound Traffic** tabs to view the specific trend.

## Scenario Data

This section displays the information about brute-force attacks and scanning risks that Cloud Firewall detects on your assets.

![Scenario Data](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/0117685161/p78163.png)

In this section, you can perform the following operations:

-   Specify a time range for query: In the upper-right corner of the section, click the time drop-down list and select a specific time range. The valid values of the time drop-down list are **Last 1 Hour**, **Last 1 Day**, and **Last 7 Days**.
-   View a specific type of information: Switch between the **Brute Force** and **Scan** tabs to view specific information.
    -   **Brute Force**: displays the statistics on brute-force attacks and the rankings of applications and attacked assets. The applications are used to launch attacks. The statistics include **Attacks**, **Blocking**, **Applications**, and **Assets**.
    -   **Scan**: displays the statistics on scanning risks and the rankings of applications and scanned assets. The applications are used to launch scan attacks. The statistics include **Attacks**, **Blocking**, **Applications**, and **Assets**.

## Recent Updates

This section displays the records of virtual patch updates, rule updates, and feature updates of Cloud Firewall.

![Recent Updates](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/0117685161/p238323.png)

You can switch between the **Virtual Patches**, **Rules**, and **Features** tabs to view specific update records.


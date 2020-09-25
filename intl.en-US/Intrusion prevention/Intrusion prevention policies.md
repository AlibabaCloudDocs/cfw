# Intrusion prevention policies

The built-in threat detection engine of Cloud Firewall defends against intrusions and common cyber attacks in real time. It also provides virtual patches to enhance the precision of threat detection and intelligently block intrusion attempts.

You can use the intrusion prevention feature of Cloud Firewall to set the mode of the threat detection engine. You can also customize the basic protection and virtual patches as needed to accurately identify and block intrusions.

## Modes of the threat detection engine

The threat detection engine supports the following modes:

-   **Monitoring Mode**: If you select this option, the threat detection engine monitors malicious traffic and sends alerts when detecting malicious traffic.

    **Note:** **Monitoring Mode** is selected by default for the intrusion prevention feature after you activate Cloud Firewall.

-   **Traffic Control Mode**: If you select this option, the threat detection engine intercepts malicious traffic to block intrusion attempts.

## Advanced settings

The intrusion prevention feature of Cloud Firewall provides **Advanced Settings**. You can customize the intrusion prevention whitelist, threat intelligence, basic protection, and virtual patches to implement a high-precision intrusion prevention system.

![Advanced settings of Cloud Firewall](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/6450305751/p57002.png)

-   Whitelist

    The intrusion prevention module of Cloud Firewall does not block the traffic of IP addresses in the whitelist. The source and destination IP addresses that are added to the whitelist are regarded as trusted IP addresses and their traffic is allowed to pass Cloud Firewall.

-   Threat intelligence

    The threat intelligence feature synchronizes the malicious IP addresses that are detected by Alibaba Cloud to Cloud Firewall, providing up-to-date protection. Malicious IP addresses include IP addresses that initiate malicious access traffic, scanning, and brute-force attacks. Enabling this feature provides up-to-date information about threat sources.

-   Basic protection

    The basic protection feature provides basic intrusion prevention capabilities, such as protecting against brute-force attacks and command execution vulnerability attacks, as well as managing and controlling the connection from infected hosts to a command and control \(C&C\) server. This feature provides basic protection for your assets.

-   Virtual patches

    You can use virtual patches to defend against the most common high-risk vulnerabilities without installing the patches in your system.


## Procedure

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext#/overview).

2.  In the left-side navigation pane, choose **Security Policies** \> **Intrusion Prevention**.

3.  On the **Intrusion Prevention** page that appears, you can perform the following operations to protect your network.

    -   In the **Threat Engine Settings** section, select **Monitoring Mode** or **Traffic Control Mode**.

        **Note:** **Monitoring Mode** is selected by default for the intrusion prevention feature after you activate Cloud Firewall. After **Traffic Control Mode** is selected, the threat intelligence, basic protection, and virtual patch modules can perform threat blocking. If Traffic Control Mode is not selected, the intrusion prevention module only monitors various types of threats and malicious traffic.

    -   In the **Advanced Settings** section, click **Whitelist** to add trusted IP addresses to the whitelist. After the whitelist is configured, the intrusion prevention feature of Cloud Firewall allows traffic from the IP addresses in the whitelist.

        You can add the trusted source IP addresses, destination IP addresses, or address books for inbound and outbound traffic to the whitelist.

        ![Whitelist](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/6450305751/p57012.png)

    -   Set **Threat Intelligence**. After Threat Intelligence is turned on, Cloud Firewall scans for and detects threat intelligence, and blocks malicious behavior based on the threat intelligence.

        **Note:** We recommend that you enable threat intelligence.

    -   Set **Basic Protection**. After Basic Policies is turned on, Cloud Firewall provides basic protection for your assets, such as blocking brute-force attacks and command execution vulnerability attacks.

        **Note:** We recommend that you enable basic protection.

        In the **Basic Protection** section, click **Customize**. In the **Customize Basic Protection Policies** dialog box that appears, you can customize one or more basic protection policies.

        ![Customize basic protection policies](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/7450305751/p57010.png)

    -   Set **Virtual Patches**. After Patches is turned on, Cloud Firewall provides installation-free, real-time protection against the most common vulnerabilities in your assets.

        **Note:** If Patches is turned off, virtual patches cannot be automatically updated. We recommend that you enable all virtual patches.

        In the **Virtual Patches** section, click **Customize**. In the **Customize Virtual Patches Policies** dialog box that appears, you can customize one or more basic virtual patch policies.

        ![Customize virtual patch policies](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/5924586851/p57009.png)



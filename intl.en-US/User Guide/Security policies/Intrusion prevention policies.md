# Intrusion prevention policies {#concept_ocy_lxd_dfb .concept}

With the built-in IPS, Cloud Firewall defends against intrusions and common attacks in real time, and provides virtual patches for precise threat detection to intelligently block intrusions.

Cloud Firewall supports the following intrusion prevention features:

-   **Threat Intelligence**: Cloud Firewall scans for and detects threat intelligence, and blocks malicious behavior from command-and-control servers in advance based on received threat intelligence.
-   **Basic Rules**: Cloud Firewall detects malware and intercepts communication with command-and-control servers or backdoors.
-   **Virtual Patching**: Cloud Firewall provides virtual patches to defend against exploits of popular high-risk vulnerabilities in real time.

## IPS running mode {#section_tpr_jxp_cfb .section}

IPS supports the following running modes:

-   **Observation Mode**: If you select this option, IPS monitors for malicious traffic and sends alarms when detecting it.

    **Note:** By default, IPS runs in **Observation Mode** mode once you subscribe to the Cloud Firewall service.

-   **Interception Mode**: If you select this option, IPS intercepts malicious traffic to block intrusions.

## Basic defense {#section_z35_jc2_dfb .section}

IPS provides basic intrusion prevention capabilities to intercept password cracking, command execution vulnerabilities, and connections from infected servers to command-and-control servers.

IPS supports the following basic intrusion prevention modes:

-   **Basic Rules**: If this mode is enabled, IPS provides basic intrusion prevention based on built-in intrusion prevention rules.
-   **Threat Intelligence**: If this mode is enabled, IPS can perceive threat sources across the entire Alibaba Cloud network in advance. IPS learns malicious IP addresses \(for example, those of malicious visitors, scanners, and crackers\) on the entire network and precisely intercepts their intrusions. \[DO NOT TRANSLATE\]

## Virtual patching {#section_dxb_lc2_dfb .section}

You can use virtual patches to defend against popular high-risk vulnerabilities without installing the patches in your system.

## Procedure {#section_atq_lzd_dfb .section}

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext#/overview).
2.  In the left-side navigation pane, choose **Security Policies** \> **Intrusion Prevention**. The **Intrusion Prevention** page is displayed.
3.  In the **Mode Selection** area, click **Observation Mode** or **Interception Mode**.

    **Note:** We recommend that you click Interception Mode.

4.  In the **Basic Defense** area, turn on or off the **Basic Rules** or **Threat Intelligence** switch.

    **Note:** We recommend that you turn on both the Basic Rules and Threat Intelligence switches.

5.  In the **Virtual Patching**, enable or disable the virtual patching function.

    **Note:** We recommend that you enable the virtual patching function.

6.  Select the required virtual patches as follows: Click **Custom** in the **Virtual Patching** area to go to the **Virtual Patch Management** dialog box.
7.  Click **Enable** or **Disable** to enable or disable a specified patch.

    **Note:** Disabled patches cannot be automatically updated. We recommend that you enable all virtual patches.



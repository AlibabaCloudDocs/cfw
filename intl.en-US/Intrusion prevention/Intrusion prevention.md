# Intrusion prevention

Cloud Firewall uses a built-in intrusion prevention system \(IPS\) to defend against intrusions and common cyberattacks. It provides virtual patches against vulnerabilities to intelligently block intrusion attempts.

The intrusion prevention feature allows you to configure the working mode of the IPS. You can also customize the threat intelligence, basic protection, intelligent defense, and virtual patch functions based on your business requirements to accurately identify and block intrusion attempts.

**Note:** Intrusion prevention policies take effect only after you enable the Internet Firewall feature. For more information, see [Enable or disable Internet Firewall](/intl.en-US/Firewall Settings/Enable or disable Internet Firewall.md).

## Limits

Premium Edition, Enterprise Edition, and Ultimate Edition of Cloud Firewall support intrusion prevention. The free trial edition does not support this feature. If you are using the free trial edition and want to use this feature, upgrade the current edition to a paid edition first.

Premium Edition of Cloud Firewall does not allow you to customize the virtual patch and basic protection functions. Enterprise Edition and Ultimate Edition do not have this limit.

## Intrusion prevention mode

Intrusion prevention supports the following modes:

-   **Monitoring Mode**: The IPS only sends alerts after it detects malicious traffic.

    **Note:** **Monitoring Mode** is selected by default after you activate Cloud Firewall. The threat intelligence, basic protection, and virtual patch functions block threats only after you select **Traffic Control Mode**. If you do not select **Traffic Control Mode**, functions of the intrusion prevention feature only monitor threats and malicious traffic.

-   **Traffic Control Mode**: The IPS blocks malicious traffic to prevent intrusions.

## Advanced settings

In the **Advanced Settings** section, you can configure a whitelist and customize the threat intelligence, intelligent defense, basic protection, and virtual patch functions to achieve precise intrusion prevention.

![Advanced settings of intrusion prevention](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/5924586851/p77719.png)

You can perform the following operations in the Advanced Settings section:

-   Configure a whitelist

    Cloud Firewall trusts the source and destination IP addresses in a whitelist and does not block their traffic.

    In the **Advanced Settings** section, click **Whitelist** to add trusted IP addresses to a whitelist. Cloud Firewall allows traffic of IP addresses in the whitelist.

    **Note:** Only Enterprise Edition and Ultimate Edition of Cloud Firewall allow you to configure a whitelist.

    You can add the trusted source IP addresses, destination IP addresses, or address books of both inbound and outbound traffic to the whitelist.

-   Enable threat intelligence

    The threat intelligence function synchronizes malicious IP addresses detected across Alibaba Cloud to Cloud Firewall. Malicious IP addresses include IP addresses that initiate malicious traffic, scanning, or brute-force attacks. This function provides up-to-date information about threat sources.

    After you turn on **Threat Intelligence**, Cloud Firewall scans for threat intelligence, and blocks malicious behavior initiated from command-and-control \(C&C\) servers based on the received threat intelligence. We recommend that you enable threat intelligence.

-   Enable basic protection

    The basic protection function defends your network against common intrusions, such as brute-force attacks and command execution vulnerabilities, and manages connections from infected hosts to a C&C server. We recommend that you enable basic protection.

    After you turn on **Basic Policies**, Cloud Firewall detects common threats by default. If such a detection mechanism does not meet your requirements, click **Customize** for **Basic Protection**. In the **Customize Basic Protection Policies** dialog box, customize basic defense policies. You can only change actions of basic defense policies. The actions include Monitor, Block, and Disable.

    ![Customize basic protection policies](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/5924586851/p77751.png)

    **Note:** Only Enterprise Edition and Ultimate Edition of Cloud Firewall allow you to customize basic defense policies.

-   Enable intelligent defense

    The intelligent defense function identifies attacks and generates alerts in real time based on massive data about attacks on the cloud.

    After you turn on **Intelligent Defense**, Cloud Firewall learns the massive data about attacks from the cloud to improve the threat and attack detection accuracy. We recommend that you enable intelligent defense.

    **Note:** Intelligent defense is available only in monitoring mode.

-   Enable virtual patches

    This function provides hot patches at the network layer to protect your business against high-risk vulnerabilities and emergency vulnerabilities that can be remotely exploited. This helps intercept vulnerability exploits in real time and prevents business interruption during vulnerability fixing. You do not need to install virtual patches on your server. After you enable this function, Cloud Firewall defends your assets against common high-risk vulnerabilities and emergency vulnerabilities in real time. If this function is disabled, Cloud Firewall does not automatically update patches for your assets. We recommend that you enable virtual patches.

    **Note:** Only Enterprise Edition and Ultimate Edition of Cloud Firewall allow you to customize virtual patch policies.

    Click **Customize** for **Virtual Patches**. In the **Customize Virtual Patches Policies** dialog box, configure basic virtual patch policies.

    ![Customize virtual patch policies](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/5924586851/p57009.png)

    **Note:** In the **Customize Virtual Patches Policies** dialog box, some policies are marked with **Highly Focused**. This indicates frequent attacks across the entire network. You must pay attention to such attacks and perform troubleshooting in time.


## Rule base update

The **Rule Base Update** tab displays information about the updates of security intelligence, virtual patches, and basic IPS policies.

In the upper-right corner of the **Rule Base Update** tab, click **Learn More** to view all updates.

![Rule base update](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/6924586851/p77753.png)


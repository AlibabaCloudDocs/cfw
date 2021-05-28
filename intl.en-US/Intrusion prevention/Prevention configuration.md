# Prevention configuration

Cloud Firewall uses a built-in threat detection engine to defend against intrusions and common cyberattacks in real time. Cloud Firewall also provides virtual patching against threats to intelligently block intrusion attempts.

The prevention configuration feature allows you to configure the working mode of the threat engine. You can also customize the threat intelligence, basic protection, intelligent defense, and virtual patching modules based on your business requirements to effectively identify and block intrusion attempts.

**Note:** Intrusion prevention policies take effect only after you enable the Internet firewall. For more information, see [Enable or disable Internet Firewall](/intl.en-US/Firewall Settings/Enable or disable Internet Firewall.md).

## Limits

The Premium Edition, Enterprise Edition, and Ultimate Edition of Cloud Firewall support the prevention configuration feature. The free trial edition does not support this feature. If you are using the free trial edition and want to use this feature, you must upgrade your Cloud Firewall to the Premium Edition or higher.

The Premium Edition of Cloud Firewall does not allow you to customize the virtual patching or basic protection module. Enterprise Edition and Ultimate Edition do not have this limit.

## Working modes of the threat engine

The threat engine supports the following modes:

-   **Monitor Mode**: If you enable this mode, Cloud Firewall monitors traffic and sends alerts when it detects malicious traffic.
-   **Block Mode**: If you enable this mode, Cloud Firewall intercepts malicious traffic and blocks intrusion attempts. You can also select the following levels for this mode based on your business requirements:

    -   Loose: blocks attacks in a loose way by using rules that prevent a high rate of false positives. This level is suitable for business that requires the false positive rate to be minimized.
    -   Medium: blocks attacks in a standard way by using common rules. This level is suitable for daily operations and maintenance \(O&M\).
    -   Strict: blocks attacks in a strict way by using all rules. This level is suitable for business that requires the false negative rate to be minimized, such as major events or cybersecurity protection activities launched by Chinese government departments. The activities are rehearsals for network attacks and protection. This level may cause a higher false positive rate than the Medium level.
    **Note:** After Cloud Firewall is activated, **Block Mode** is enabled by default. Cloud Firewall automatically determines the level based on your traffic condition. The threat intelligence, basic protection, and virtual patching modules block threats only after you enable **Monitor Mode**. If you do not enable **Monitor Mode**, the modules only monitor threats and malicious traffic.


## Advanced settings

In the **Advanced Settings** section, you can configure whitelists and customize the threat intelligence, intelligent defense, basic protection, and virtual patching modules to implement precise intrusion prevention.

You can perform the following operations in the Advanced Settings section:

-   Configure whitelists

    In the **Advanced Settings** section, click **Whitelist** to add trusted IP addresses to specific whitelists. After you configure the whitelists, Cloud Firewall trusts the source and destination IP addresses in the whitelists and does not block their traffic.

    **Note:** Only the Enterprise Edition and Ultimate Edition of Cloud Firewall allow you to configure whitelists.

    You can add the trusted source IP addresses, destination IP addresses, or address books of both inbound and outbound traffic to the whitelists.

    ![Whitelist](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/4642951261/p77749.png)

-   Enable or disable threat intelligence

    The threat intelligence module synchronizes malicious IP addresses detected across Alibaba Cloud to Cloud Firewall, and then implements precise intrusion prevention. The malicious IP addresses are used to initiate malicious access, scans, or brute-force attacks. This module provides up-to-date information about threat sources.

    After you turn on **Threat Intelligence**, Cloud Firewall scans for threat intelligence, and blocks malicious behavior initiated from central control systems based on the threat intelligence. We recommend that you enable threat intelligence.

-   Enable or disable basic protection

    The basic protection module protects your network against common intrusions, such as brute-force attacks and attacks that exploit command execution vulnerabilities. The module also manages connections from infected hosts to a command-and-control \(C&C\) server. We recommend that you enable basic protection.

    After you turn on **Basic Policies**, Cloud Firewall detects common threats by default. If this detection mechanism does not meet your requirements, click **Customize** for **Basic Protection**. In the **Customize Basic Protection Policies** dialog box, customize basic protection policies. You can change only the actions of basic protection policies. The actions include Monitor, Block, and Disable.

    **Note:** Only the Enterprise Edition and Ultimate Edition of Cloud Firewall allow you to customize basic protection policies.

-   Enable or disable intelligent defense

    The intelligent defense module identifies attacks and generates alerts in real time based on a large amount of data about attacks on the cloud.

    After you turn on **Intelligent Defense**, Cloud Firewall learns a large amount of data about attacks on the cloud to improve the accuracy of threat and attack detection. We recommend that you enable intelligent defense.

    **Note:** Intelligent defense is available only for Monitor Mode.

-   Enable or disable virtual patching

    The virtual patching module provides hot patches at the network layer to protect your business against high-risk vulnerabilities and urgent vulnerabilities that can be remotely exploited. This helps intercept vulnerability exploits in real time and prevents business interruption during vulnerability fixing. You do not need to install virtual patches on your server. After you enable this module, Cloud Firewall protects your assets against common high-risk vulnerabilities and urgent vulnerabilities in real time. If this module is disabled, Cloud Firewall does not automatically update patches for your assets. We recommend that you enable virtual patching.

    **Note:** Only the Enterprise Edition and Ultimate Edition of Cloud Firewall allow you to customize virtual patching policies.

    Click **Customize** for **Virtual Patches**. In the **Customize Virtual Patches Policies** dialog box, configure basic virtual patching policies.

    ![Customize virtual patching policies](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/5924586851/p57009.png)

    **Note:** In the **Customize Virtual Patches Policies** dialog box, some policies are marked with **Highly Focused**. This indicates frequent attacks across the entire network. You must pay attention to such attacks and perform troubleshooting in time.


## Rule base update

The **Rule Base Update** tab displays information about the updates of security intelligence, virtual patches, and IPS policies.

In the upper-right corner of the **Rule Base Update** tab, click **Learn More** to view all updates of Cloud Firewall.

![Rule Base Update tab](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/6924586851/p77753.png)


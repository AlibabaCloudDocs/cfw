---
keyword: [Cloud Firewall, security policies, intrusion prevention, threat detection engine, real-time intrusion prevention]
---

# Enable intrusion prevention

Cloud Firewall provides an intrusion prevention system \(IPS\) to defend against intrusions in real time.

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext).

2.  In the left-side navigation pane, choose **Intrusion Prevention** \> **Prevention Configuration**.

3.  In the **Threat Engine Mode** section, configure the engine based on the following descriptions:

    -   **Block Mode**: If you enable this mode, Cloud Firewall intercepts malicious traffic and blocks intrusion attempts. You can also select the following levels for this mode based on your business requirements:

        -   Loose: blocks attacks in a loose way by using rules that prevent a high rate of false positives. This level is suitable for business that requires the false positive rate to be minimized.
        -   Medium: blocks attacks in a standard way by using common rules. This level is suitable for daily operations and maintenance \(O&M\).
        -   Strict: blocks attacks in a strict way by using all rules. This level is suitable for business that requires the false negative rate to be minimized, such as major events or cybersecurity protection activities launched by Chinese government departments. The activities are rehearsals for network attacks and protection. This level may cause a higher false positive rate than the Medium level.
        **Note:** After Cloud Firewall is activated, **Block Mode** is enabled by default. Cloud Firewall automatically determines the level based on your traffic condition. The threat intelligence, basic protection, and virtual patching modules block threats only after you enable **Monitor Mode**. If you do not enable **Monitor Mode**, the modules only monitor threats and malicious traffic.

    -   Turn on **Threat Intelligence**. This allows Cloud Firewall to receive real-time threat intelligence from the entire network.
    -   In the **Basic Protection** section, click **Customize**. In the Customize Basic Protection Policies dialog box, select basic protection rules and specify actions. The rules are used to defend against various attacks, such as brute-force attack and unauthorized command execution.
    -   Turn on **Intelligent Defense** section. This allows Cloud Firewall to identify unknown attacks based on AI technologies and large amounts of historical attack data. This feature is supported only in **Monitoring** Mode.
    -   In the **Virtual Patches** section, turn on **Patches**. This allows Cloud Firewall to obtain patches that do not require installation. The patches defend against the latest vulnerabilities.
    **Note:** To view intrusion prevention details, choose **Traffic Analysis** \> **Traffic Blocked by IPS**.



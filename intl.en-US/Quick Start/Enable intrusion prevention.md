---
keyword: [Cloud Firewall, security policies, intrusion prevention, threat detection engine, real-time intrusion prevention]
---

# Enable intrusion prevention

Cloud Firewall provides an intrusion prevention system \(IPS\) to defend against intrusions in real time.

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext).

2.  In the **Threat Engine Settings** section, make the following configurations:

    -   Select **Traffic Control Mode** to block malicious traffic.

        **Note:** By default, **Monitoring Mode** is selected. In this mode, Cloud Firewall only monitors malicious traffic and reports alarms, but does not block the traffic.

    -   Enable **Threat Intelligence** to receive real-time threat intelligence from the entire network.
    -   In the **Basic Protection** section, click **Customize** to configure basic protection policies against different attacks such as password cracking and unauthorized command execution.
    -   In the **Virtual Patches** section, enable **Patches** to obtain installation-free patches that help defend against the latest vulnerabilities.
    **Note:** You can view intrusion prevention details by choosing **Traffic Analysis** \> **Traffic Blocked by IPS**.



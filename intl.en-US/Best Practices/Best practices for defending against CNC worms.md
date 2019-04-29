# Best practices for defending against CNC worms {#concept_hg1_tht_dfb .concept}

Worms are a major threat to current businesses on the cloud. They exploit server vulnerabilities to spread over the network and do various malicious operations on infected servers. This poses serious threats to the assets and businesses of users. Cloud Firewall provides layered defense against the attack chains of worms, and can detect and intercept a variety of worms and their variants. Additionally, Cloud Firewall can update and expand its capability in real time based on threats on the cloud. This enables Cloud Firewall to detect and intercept the latest worms.

## Harms of worms {#section_g3p_n3t_dfb .section}

Worms mainly cause the following harm:

-   Business interruption: Worms may modify configurations or stop services on infected servers, causing risks such as server breakdown and business interruption.
-   Information stealing: Worms for stealing information compress data on infected servers and send the compressed data back to attackers. This may cause serious information leakage or resource abuse.
-   Blocking by regulators: Worms send a large number of packets when they spread. When the number of packets sent from an IP address exceeds the threshold, a regulator may block this IP address. This directly causes business interruption.
-   Monetary or data losses: Ransomware worms encrypt files on infected servers for ransom, causing monetary or data losses.

## Cloud Firewall solution {#section_qgt_djt_dfb .section}

Cloud Firewall provides layered defense against the attack chains of worms, and can detect and intercept a variety of worms and their variants. Additionally, Cloud Firewall can update and expand its capability in real time based on threats on the cloud. This enables Cloud Firewall to detect and intercept the latest worms.

Typical worms include:

-   **DDG**: spreads by exploiting Redis vulnerabilities and through brute-force attacks, and uses the computing resources on infected servers for mining cryptocurrency.
-   **WannaCry**: spreads by exploiting the EternalBlue vulnerability of the Windows operating system and infects servers for ransom.
-   **BillGates**: spreads by exploiting application vulnerabilities and through brute-force attacks, and builds a zombie network of infected servers for DDoS attacks.

**Typical case: DDG worm**

DDG is an active worm that spreads by exploiting Redis vulnerabilities and through brute-force attacks. Infected servers are added to a zombie network for mining cryptocurrency.

**Impact scope of the DDG**

-   Servers that use weak SSH passwords
-   Redis or other database servers with vulnerabilities

**Major harm of the DDG**

-   Business interruption: The DDG mines cryptocurrency on infected servers, which occupies a large amount of computing resources on the servers. This may affect service availability and cause business interruption.
-   Blocking by regulators: The DDG sends a large number of packets when it spreads. When the number of packets sent from an IP address exceeds the threshold, a regulator may block this IP address.

**Defense against the DDG attack chain**

Cloud Firewall provides real-time detection and defense against the DDG attack chain to block both the attack and spreading chains of the worm.

Cloud Firewall provides the following intrusion prevention features:

-   **Threat Intelligence**: Cloud Firewall scans for and detects threat intelligence, and blocks malicious behavior from command-and-control servers in advance based on received threat intelligence.
-   **Basic Protection**: Cloud Firewall detects malware and intercepts communication with command-and-control servers or backdoors.
-   **Virtual Patches**: Cloud Firewall provides virtual patches to defend against exploits of popular high-risk vulnerabilities in real time.

## Procedure {#section_agl_5kt_dfb .section}

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext#/overview).
2.  In the console, choose **Security Policies** \> **Intrusion Prevention**. The **Intrusion Prevention** page is displayed.
3.  Select **Traffic Control Mode**.

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21415/155653779112041_en-US.png)

4.  In the **Basic Protection** area, turn on the **Basic Policies** and **Threat Intelligence** switches.

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21415/155653779112042_en-US.png)

5.  In the **Virtual Patches** area, turn on the **Patches** switch.![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21415/155653779112043_en-US.png)


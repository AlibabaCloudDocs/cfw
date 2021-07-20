# Best practices to defend against mining worms

This topic describes how Cloud Firewall defends against mining worms from the perspectives of prevention, detection, and damage control. In this topic, a cloud-based environment is used.

The 2018 Cryptocurrency Mining Hijacker Report released by the Alibaba Cloud security team shows that the occurrence of common zero-day vulnerabilities was accompanied by the outbreak of mining worms. Mining worms occupy system resources, which may cause service interruption. Some mining worms, such as Xbash, may also be bundled with ransomware. This type of mining worm can result in economic and data loss for enterprises.

## How do mining worms spread?

The Alibaba Cloud security team concludes that mining worms in the cloud exploit the following network vulnerabilities to spread:

-   Common vulnerabilities

    Mining worms exploited common vulnerabilities in network applications, such as configuration errors and weak passwords, to continuously scan the Internet, launch attacks, and compromise hosts.

    The following table lists common vulnerabilities that are exploited by active mining worms.

    |Common vulnerability|Mining worm family|
    |--------------------|------------------|
    |SSH, RDP, and Telnet vulnerabilities, which can be exploited to launch brute-force attacks|MyKings and RDPMiner|
    |Write of crontab commands to Redis|DDG, Watchdogs, Kworkerd, and 8220 Mining Group|
    |Command execution based on user-defined functions \(UDFs\) in MySQL and SQL Server|BuleHero, MyKings, and ProtonMiner|
    |Command execution in Apache CouchDB|8220 Mining Group|

-   Zero-day and N-day vulnerabilities

    Mining worms also exploited zero-day and N-day vulnerabilities to compromise a large number of hosts before the vulnerabilities are fixed.

    The following table lists common zero-day and N-day vulnerabilities that are exploited by active mining worms.

    |Zero-day or N-day vulnerability|Mining worm family|
    |-------------------------------|------------------|
    |Arbitrary code execution in ThinkPHP V5 series

Arbitrary code execution in Apache ActiveMQ \(CVE-2015-5254\)

|iBus|
    |Remote command execution in Confluence \(CVE-2019-3396\)|Watchdogs \(ksoftirqds and Kerberods\)|
    |Remote code execution \(RCE\) in Nexus Repository Manager 3 \(CVE-2019-7238\)

Arbitrary code execution in ThinkPHP V5 series

|Watchbogs|
    |WebLogic \(CVE-2017-10271\)

RCE in Drupal \(CVE-2018-7600\)

Deserialized command execution in JBoss 5.x and JBoss 6.x \(CVE-2017-12149\)

|8220 Mining Group|
    |MS17-010 EternalBlue \(CVE-2017-0143\)|MyKings|
    |Arbitrary code execution in ThinkPHP V5 series

RCE in Tomcat \(CVE-2017-12615\)

Vulnerability in the WLS Security component of WebLogic \(CVE-2017-10271\)

|Bulehero|
    |MS17-010 EternalBlue \(CVE-2017-0143\)|WannaMine|
    |Arbitrary code execution in ThinkPHP V5 series|Sefa|
    |Unauthorized access in Hadoop YARN

RCE in Drupal \(CVE-2018-7600\)

Command execution in Elasticsearch \(CVE-2014-3120\)

Vulnerability in the WLS Security component of WebLogic \(CVE-2017-10271\)

|ProtonMiner|
    |RCE in Tomcat \(CVE-2017-12615\)

Deserialized command execution in JBoss 5.x and JBoss 6.x \(CVE-2017-12149\)

Vulnerability in the WLS Security component of WebLogic \(CVE-2017-10271\)

|Satan|


## How does Cloud Firewall defend against mining worms?

Cloud Firewall detects and blocks malicious inbound and outbound network traffic in the cloud in real time to defend against mining worms.

-   Defense against mining worms that exploit common vulnerabilities

    Some mining worms launch brute-force attacks by exploiting vulnerabilities such as SSH and RDP vulnerabilities. To defend against these worms, Cloud Firewall provides the basic protection feature. This feature supports common methods to detect brute-force attacks. For example, the feature calculates the threshold for the logon retry attempts and limits the IP addresses from which the number of logon retry attempts exceeds the threshold. The feature also analyzes user access habits and frequency to ensure that normal access requests are allowed and abnormal requests are denied based on behavior models.

    This feature takes advantage of the big data capabilities provided by Alibaba Cloud and generates precise defense rules based on the malicious attack samples accumulated in attack and defense by the Alibaba Cloud security team. This way, the feature can protect your assets more precisely against other worms that exploit common vulnerabilities, such as write of crontab commands to Redis and UDF-based command execution in databases.

    You can enable basic protection to defend against mining worms that exploit common vulnerabilities.

    To enable basic protection, perform the following steps:

    1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext#/overview).
    2.  In the left-side navigation pane, choose **Intrusion Prevention** \> **Prevention Configuration**.
    3.  On the **Prevention Configuration** page, turn on the switches for **Threat Intelligence** and **Basic Protection** in the **Advanced Settings** section.
    4.  In the left-side navigation pane, choose **Intrusion Prevention** \> **Intrusion Prevention** to view the detailed blocking logs in the **Detailed Data** section.

        ![IPSzu'duan](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/9386506261/p46789.png)

-   Defense against mining worms that exploit zero-day and N-day vulnerabilities

    If common zero-day and N-day vulnerabilities are not fixed at the earliest opportunity, these vulnerabilities are likely to be exploited by mining worms. Cloud Firewall analyzes attack traffic by using honeypots deployed across the network and obtains vulnerability intelligence from the Alibaba Cloud Crowdsourced Security Testing platform. This way, Cloud Firewall can promptly detect zero-day and N-day vulnerabilities, obtain the proofs of concept \(POCs\) and exploits of these vulnerabilities, and generate virtual patches in advance.

    You can enable virtual patching to defend against mining worms that exploit zero-day and N-day vulnerabilities.

    To enable virtual patching, perform the following steps:

    1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext#/overview).
    2.  In the left-side navigation pane, choose **Intrusion Prevention** \> **Prevention Configuration**.
    3.  On the **Prevention Configuration** page, turn on the switch for **Virtual Patches** in the **Advanced Settings** section.
    4.  Click **Customize** below the switch for **Virtual Patches**. In the **Customize Virtual Patches Policies** dialog box, view or manage the virtual patches that are enabled.

        ![Defense against zero-day and N-day vulnerabilities ](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/1357476261/p46790.jpg)


## How does Cloud Firewall detect mining worms?

Detection principle

Even if the Internet firewall is enabled to prevent intrusions, hosts may still be vulnerable to mining worms. Mining worms can spread from a development machine to a production network over a VPN. If the system images and Docker images used for O&M are inserted with mining viruses, a large number of hosts may be compromised.

Cloud Firewall uses Network Traffic Analysis \(NTA\) to provide the breach awareness feature. This feature can detect host intrusion events in a timely and efficient manner.

Cloud Firewall uses a powerful threat intelligence network to identify the mining pool addresses of common cryptocurrencies and the common communication protocols of mining pools, and detect the downloads of mining trojans. In addition, Cloud Firewall can identify the mining behavior of hosts in real time and promptly generate alerts.

You can turn on **Auto Blocking** on the **Breach Awareness** page to enable Cloud Firewall to detect mining worms and block the communication between mining trojans and mining pools on the network.

To turn on Auto Blocking, perform the following steps:

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext#/overview).
2.  In the left-side navigation pane, choose **Intrusion Prevention** \> **Breach Awareness**.
3.  On the **Breach Awareness** page, find the required event and click **Block** in the Actions column. In the Block dialog box, turn on **Auto Blocking**.

    ![Mining worm detection ](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/1357476261/p46792.jpg)

    You can find the faulty process on the host and handle the event based on the external address displayed on the **Details** page.


## How do I use Cloud Firewall to immediately control the damages of mining worms?

If a host is compromised by mining worms, Cloud Firewall can use the following methods to prevent the spread of these worms and reduce economic and data loss. The methods are to block malicious file downloads, intercept the communication between command and control \(C&C\) servers and mining worms, and enable enhanced access control for critical business.

-   Block malicious file downloads

    In most cases, after hosts are compromised by mining worms, the hosts download malicious files. Basic protection is integrated with malicious file detection and dynamically updates the unique characteristics codes and fuzzy hashes of malicious files for common mining worms. After the mining worms intrude into your host, your host may further download updated malicious payloads. In this case, basic protection performs security checks on the files downloaded to your host. The checks include file restoration and characteristics matching. If an attempt to download a malicious file is detected, an alert is generated, and the download is blocked.

    ![Basic protection](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/1357476261/p46794.jpg)

    You can turn on the switch for **Basic Protection** on the **Prevention Configuration** page to block malicious file downloads.

-   Intercept communication between C&C servers and mining worms

    After C&C servers are compromised by mining worms, the C&C servers may leak sensitive data or receive malicious instructions from mining worms. In this case, basic protection intercepts the communication between the worms and C&C servers by using the following methods:

    -   Basic protection dynamically monitors and analyzes the data related to mining worms across the network and the communication traffic of the C&C servers. Then, basic protection dynamically extracts the characteristics of unusual communication traffic and forms a mechanism to identify the communication between the mining worms and C&C servers. This way, basic protection ensures the prompt detection of attacks.
    -   Basic protection learns historical access information and establishes a model to detect unusual traffic and explore potential mining worm information.
    -   Basic protection uses big data visualization to map access behavior to all IP addresses and uses machine learning to detect suspicious IP addresses and access domains. In addition, a threat intelligence library for C&C servers is formed based on network-wide attack data. This way, basic protection matches host communication traffic with the information in the library to block malicious traffic between C&C servers and mining worms.
    The following figure shows the communication interception records between a C&C server and mining worms. The communication is intercepted by basic protection based on threat intelligence.

    ![Intercept communication between C&C servers and mining worms](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/1357476261/p46796.jpg)

    You can turn on the switch for **Basic Protection** on the **Prevention Configuration** page to intercept the communication between C&C servers and mining worms.

-   Enable enhanced access control for critical business

    To ensure critical business, enterprises may need to open services or ports to the Internet. However, Internet-based scans and attacks pose security threats to the assets of enterprises, which makes fine-grained control on external access challenging. Outbound connections that are initiated from an Elastic Compute Service \(ECS\) instance, elastic IP address, or internal network are usually valid. In these scenarios, the number of domain names or IP addresses is controllable. Cloud Firewall implements access control on these domain names and IP addresses to prevent mining trojans from being inserted into compromised ECS instances by using suspicious domain names and block communication between trojans and C&C servers.

    Cloud Firewall allows you to configure access control rules for source IP addresses and domain names, including wildcard domain names. For critical business, you can configure fine-grained access control policies for outbound connections. For example, you can open critical ports only to specific domain names or IP addresses. Fine-grained access control policies effectively prevent the downloads and spread of mining worms. The policies also prevent mining worms from surviving and eliciting malicious actions.

    For example, a total of six IP addresses are used for outbound connections on an internal network, all NTP services are identified as Alibaba Cloud services, and the IP address of the DNS server is 8.8.8.8. In this case, you can configure rules to allow outbound connections only from the six IP addresses based on the security suggestions provided by Cloud Firewall. The rules prevent other outbound connections, such as malicious downloads and outbound C&C connections, without affecting normal business access.

    ![Security suggestions provided by Cloud Firewall](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/2357476261/p46797.jpg)

    To configure the rules, perform the following steps: In the left-side navigation pane of the Cloud Firewall console, choose **Access Control** \> **Access Control**. On the Access Control page, click the **Internet Firewall** tab and then the **Outbound Policies** tab. Then, configure rules to allow outbound connections only from the authorized IP addresses.


Mining worms spread on a large scale because of the persistence of common application vulnerabilities on the Internet, frequent occurrence of zero-day vulnerabilities, and highly efficient monetization of mining activities. Customers whose business is deployed on the cloud can transparently access Cloud Firewall to protect their applications against various attacks on the Internet. Cloud Firewall relies on strong cloud computing power to perceive the latest attack threats and connects to a threat intelligence network to provide optimal security protection from mining worms. Cloud Firewall can also be scaled out as your business grows. This way, you can focus more on your business expansion.


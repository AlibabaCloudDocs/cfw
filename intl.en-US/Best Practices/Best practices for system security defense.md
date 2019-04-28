# Best practices for system security defense {#concept_ppp_zwx_yfb .concept}

System security is a key factor in maintaining secure and stable business operations. As the battle between cyberattacks and defense is heating up, more and more attack forms emerge, such as large-scale automated attacks, worms, ransomware, fraudulent cryptocurrency mining, and Advanced Persistent Threats \(APTs\). This brings great challenges to secure system running.

A system installed with default settings has the following security flaws, making it vulnerable to intrusions:

-   The system is not properly configured.
    -   Unnecessary open ports: Unnecessary services and applications are opened, and exposed to attacks.
    -   Weak passwords: They are vulnerable to brute-force attacks, resulting in easy system intrusions.
    -   Improper policy configuration: System security policies are not configured or their strength is weak.
-   System vulnerabilities exist or necessary patches are not installed.
    -   Command execution vulnerability: This vulnerability allows arbitrary command execution, causing system intrusions.
    -   Denial of Service \(DoS\) vulnerability: The system under DoS attacks rejects normal service requests, resulting in business interruption.
    -   Information leakage vulnerability: Sensitive or confidential data is disclosed.

## Typical case: remote code execution vulnerability in Samba {#section_rcf_v1y_yfb .section}

Samba is the software that implements the Server Message Block \(SMB\) protocol on Linux and UNIX operating systems. It allows computers to share resources such as files and printers with each other.

The Samba server software was reported to have a remote code execution vulnerability. This vulnerability allows a malicious client to upload a shared library to a writable shared directory, and then cause the server to load and execute the library.

CVE: CVE-2017-7494

**Impact scope:** 

-   Linux or UNIX operating system on which Samba is installed
-   Samba versions earlier than 4.6.4, 4.5.10, and 4.4.14

**Major harm:** 

-   Command execution: Servers are breached and information is disclosed due to remote code execution.
-   Business interruption: A worm, named SambaCry, can spread by exploiting this vulnerability. This worm mines cryptocurrency on infected servers, which occupies a large amount of computing resources on the servers. This may affect service availability and cause business interruption.

## Typical case: remote code execution vulnerability in SMB Server {#section_knt_vby_yfb .section}

SMB Server is a server protocol component that is installed on the Windows operating system by default. SMB Server was reported to have a remote code execution vulnerability. This vulnerability allows a remote attacker to execute code by sending crafted packets to SMBv1 Server.

CVE: CVE-2017-0143

**Impact scope:** 

-   Microsoft Windows Server 2008 R2 SP1
-   Microsoft Windows Server 2008 SP2
-   Microsoft Windows Server 2012 R2
-   Microsoft Windows server 2012 Gold
-   Microsoft Windows Server 2016

**Major harm** 

-   Command execution: Servers are breached and information is disclosed due to remote code execution.
-   Data loss: Worms, such as WannaCry, can spread by exploiting this vulnerability. Such worms encrypt files on infected servers for ransom and cause information leakage.

## How to use Cloud Firewall for system intrusion prevention? {#section_p3w_myx_yfb .section}

Alibaba Cloud Security team is continuously tracking and studying system vulnerabilities and their preventive measures, and has accumulated rich experience in attack defense. The defense rules formulated based on this experience greatly enhance the system security defense capability of Cloud Firewall.

To ensure normal system running, Cloud Firewall provides multi-point defense against all risks that the system faces.

-   **Brute-force attack**: The threat intelligence feature of Cloud Firewall can detect attack threats on the Internet and block scanning or intrusion behavior in advance.
-   **System vulnerabilities**: Cloud Firewall provides intrusion prevention against high-risk vulnerabilities of operating systems.
-   **Other attacks**: The basic rules feature of Cloud Firewall can detect other system attacks, such as a reverse shell and system file leakage, and block them in real time.

## Procedure {#section_agl_5kt_dfb .section}

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext#/overview).
2.  In the console, choose **Security Policies** \> **Intrusion Prevention**. The **Intrusion Prevention** page is displayed.
3.  In the **Modes** area, click **Traffic Control Mode**.

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/66337/155647264445848_en-US.png)

4.  In the **Basic Protection** area, turn on the **Basic Policies** and **Threat Intelligence** switches.

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/66337/155647264445849_en-US.png)

5.  In the **Virtual Patches** area, turn on the **Patches** switch.

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/66337/155647264445850_en-US.png)

    Click **Virtual Patches** to open the virtual patches configuration list. You can enable/disable a certain patch.

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/66337/155647264445851_en-US.png)

    **Note:** When the **Patches** switch is turned on in **Virtual Patches** module, all the patches on Virtual Patches list will be enabled automatically.



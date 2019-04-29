# Best practices for database security defense {#concept_wtd_hgc_nfb .concept}

The Intrusion Prevention feature of Cloud Firewall can defend against common database intrusions.

## Database security defense requirements {#section_qqw_mf5_nfb .section}

A database is a system for managing and storing data resources in an enterprise. The database stores a lot of valuable and sensitive information, so it is often the primary target of hackers. Database security is vital to normal business operations and enterprise development.

A database faces the following main security threats:

-   Brute-force attack

    Upon successful brute-force attacks, the database is directly compromised.

-   Database application vulnerabilities

    For example, database CVE vulnerabilities may cause DoS attacks to database applications, malicious command execution, and information leakage.

-   Malicious command execution and file reading or writing

    For example, attackers can execute malicious commands and read or write files by calling high-risk stored procedures or functions.

-   Information stealing and illegal export of database

    Attackers sell stolen data or defraud other people, causing business losses.


## Cloud Firewall solution {#section_vyw_b35_nfb .section}

The Intrusion Prevention feature of Cloud Firewall can defend most databases against intrusions. The databases include:

-   MySQL
-   Microsoft SQL Server
-   Redis
-   PostgreSQL
-   Memcache
-   MongoDB
-   Oracle

**How to use Cloud Firewall for database intrusion prevention**

The Alibaba Cloud Security team is continuously tracking and studying database vulnerabilities and their preventive measures, and has accumulated rich experience in attack defense. The defense rules formulated based on this experience greatly enhance the database security defense capability of Cloud Firewall.

To ensure normal database running, Cloud Firewall provides multi-point defense against all risks that the database faces.

-   Brute-force attack

    Threat intelligence: The threat intelligence feature of Cloud Firewall can detect attack threats on the Internet and block scanning or intrusion behavior in advance.

-   Database application vulnerabilities

    Virtual patches: The virtual patches feature of Cloud Firewall provides intrusion prevention against high-risk vulnerabilities of databases.

-   Malicious command execution and file reading or writing

    Basic protection: The basic protection feature of Cloud Firewall can block malicious operations in real time, including system file operations, Webshell writing, and stored procedure or user defined function \(UDF\) invocation.

-   Information stealing and illegal export of database

    High-risk SQL blocking: The basic rules feature of Cloud Firewall can block the database export operation in real time to prevent information from being stolen.


## Procedure {#section_agl_5kt_dfb .section}

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext#/overview).
2.  In the console, choose **Security Policies** \> **Intrusion Prevention**. The **Intrusion Prevention** page is displayed.
3.  In the **Mode Selection** area, click **Interception Mode**.

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21415/155653809912041_en-US.png)

4.  In the **Basic protection** area, turn on the **Basic Policies** and **Threat Intelligence** switches.

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21415/155653809912042_en-US.png)

5.  In the **Virtual Patches** area, turn on the **Patches** switch.![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21415/155653810012043_en-US.png)


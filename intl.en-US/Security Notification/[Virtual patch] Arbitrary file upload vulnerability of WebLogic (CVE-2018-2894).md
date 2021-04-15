# \[Virtual patch\] Arbitrary file upload vulnerability of WebLogic \(CVE-2018-2894\)

Alibaba Cloud's Cloud Firewall has been able to defend against the arbitrary file upload vulnerability of WebLogic.

WebLogic is an application server launched by Oracle Corporation, which is a piece of middleware based on the Java EE architecture. The WebLogic Java application server is used to develop, integrate, deploy, and manage large distributed web applications, network applications, and database applications.

The configuration page of ws\_utc, a WebLogic web service test client, has an issue of unauthorized access. The path to the configuration page is /ws\_utc/config.do. Attackers can access this configuration page, use a valid WebLogic web path to replace the JKS Keystores file path, and upload malicious JSP Trojan files.

Rule-based defense: Cloud Firewall has been able to defend against this vulnerability.

Scope of impact:

-   WebLogic 10.3.6.0
-   WebLogic 12.1.3.0
-   WebLogic 12.2.1.2
-   WebLogic 12.2.1.3

Rule type: Command execution

Risk level: High


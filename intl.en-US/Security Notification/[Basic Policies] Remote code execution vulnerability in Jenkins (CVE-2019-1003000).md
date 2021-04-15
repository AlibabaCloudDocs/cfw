# \[Basic Policies\] Remote code execution vulnerability in Jenkins \(CVE-2019-1003000\)

Jenkins is an open-source program written in Java. It can be used as a continuous integration server. The Script Security and Pipeline plug-in is a security plug-in of Jenkins and can be integrated into various functional plug-ins of Jenkins.

Alibaba Cloud Security has discovered that the exploitation methods of the remote code execution vulnerability in Jenkins Script Security and Pipeline \(CVE-2019-1003000\) have been revealed on the Internet. Users with overall or read permissions can bypass sandbox protections and execute arbitrary code in Jenkins.

Vulnerability description: [**Jenkins Security Advisory 2019-01-08**](https://jenkins.io/security/advisory/2019-01-08/)

Policy: Command execution

Risk level: High

Impacted plug-ins:

-   Declarative Plug-in versions earlier than 1.3.4.1
-   Groovy Plug-in versions earlier than 2.61.1
-   Script Security Plug-in versions earlier than 1.5.0

Policy-based protection: Cloud Firewall provides basic firewall policies to fix this vulnerability. We recommend that you enable [Intrusion Prevention](/intl.en-US/Intrusion prevention/Intrusion prevention.md) to use the basic policies.


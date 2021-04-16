# \[Basic rule\] Remote code execution vulnerabilities in multiple versions of ThinkPHP 5.1 series and 5.2 series

On January 15, 2019, Alibaba Cloud Security team detected remote code execution vulnerabilities in all versions of ThinkPHP 5.1 series and 5.2 series under certain conditions.

These vulnerabilities are caused by a flaw in the process of handling methods of the Request class by the ThinkPHP 5.0 framework. Hackers exploit these vulnerabilities to create special requests to obtain webshell directly.

In the past two months, multiple high-risk command execution vulnerabilities in the ThinkPHP5 framework have been continuously disclosed. Cloud Firewall has launched rules for defending against these vulnerabilities. Cloud Firewall can monitor and intercept the attacks exploiting these vulnerabilities in real time.

Rule type: Web attack

Risk Level: High

Scope of impact: All versions of ThinkPHP 5.1 series and 5.2 series

Rule-based defense: Cloud Firewall has been able to defend against these vulnerabilities. We recommend that you enable [intrusion prevention policies](/intl.en-US/Intrusion prevention/Intrusion prevention.md) in the Cloud Firewall console.


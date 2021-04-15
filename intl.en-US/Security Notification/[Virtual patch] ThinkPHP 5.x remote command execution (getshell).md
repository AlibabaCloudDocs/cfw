# \[Virtual patch\] ThinkPHP 5.x remote command execution \(getshell\)

Cloud Firewall has been able to defend against ThinkPHP 5.x remote command execution \(getshell\) attacks.

ThinkPHP is a simple, fast, and compatible lightweight PHP development framework, which Chinese websites use widely, especially in the e-commerce, financial services, and online gaming industries.

On December 10, 2018, the ThinkPHP team released a patch to fix a remote code execution vulnerability caused by the ThinkPHP v5 framework's insufficient checks on controllers. That vulnerability can be widely used to execute any code and commands remotely. Security checks on controller names in the ThinkPHP v5 framework are insufficient. If no forced routing has been configured, hackers can exploit the vulnerability to create special requests to run code remotely and get server privileges.

Scope of impact: ThinkPHP v5.0 series earlier than 5.0.23 and ThinkPHP v5.1 series earlier than 5.1.31

Rule type: Web attack

Risk level: High

Rule-based defense: Cloud Firewall has been able to defend against such attacks. We recommend that you enable [intrusion prevention policies](/intl.en-US/Intrusion prevention/Intrusion prevention.md) in the Cloud Firewall console.


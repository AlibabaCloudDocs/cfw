# **\[Basic rule\] Remote code execution vulnerabilities in ThinkPHP versions earlier than 5.0.24**

ThinkPHP is a simple, fast, and compatible lightweight PHP development framework, which Chinese websites use widely, especially in the e-commerce, financial service, and online gaming industries.

On January 11, 2019, ThinkPHP team officially released a security update that disclosed a high-risk security vulnerability: Attackers can create special malicious requests to obtain server privileges directly.

These vulnerabilities are caused by a flaw in the process of handling methods of the Request class by the ThinkPHP 5.0 framework. Hackers exploit these vulnerabilities to create special requests to obtain webshell directly.

ThinkPHP versions from 5.0.0 to 5.0.23 are affected.

Rule-based defense: Cloud Firewall has been able to defend against these vulnerabilities.

Scope of impact: ThinkPHP v5.0 series versions earlier than 5.0.24

Rule type: Web attack

Risk level: High


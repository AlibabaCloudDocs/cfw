# \[Virtual patch\] Nginx security issues cause servers' vulnerability to DoS attacks

Nginx has been experiencing security issues recently, which may cause more than 14 million servers to be vulnerable to DoS attacks. The vulnerabilities that cause the security issues are in the HTTP/2 and MP4 modules.

Two security vulnerabilities were identified in Nginx HTTP/2 implementation. Nginx compiled with the ngx\_http\_v2\_module \(not compiled by default\) is affected if the http2 option of the listen directive is used in a configuration file.This may cause excessive memory consumption \(CVE-2018-16843\) and CPU usage \(CVE-2018-16844\).

To take advantage of these two vulnerabilities, an attacker can send a specially crafted HTTP/2 request, which results in excessive CPU usage and memory usage, eventually triggering a DoS status. All Nginx servers that are running unpatched versions are vulnerable to DoS attacks.

Scope of impact:

-   CVE-2018-16843 and CVE-2018-16844: Mainline versions 1.9.5 - 1.15.5
-   CVE-2018-16845: Mainline versions 1.1.3+ and 1.0.7+

Rule type: DoS attack

Risk level: High

Rule-based defense: Cloud Firewall has been able to use the virtual patch feature to defend against such attacks. For more information about the virtual patch feature, see [Virtual patching](/intl.en-US/Intrusion prevention/Intrusion prevention.md).

For more information about the alert, see [Nginx security issues cause over 14 million servers to be vulnerable to DoS attacks](https://yq.aliyun.com/articles/666605).


# \[Threat intelligence\] DDG mining botnet attack

DDG is a Monero-mining botnet that targets Redis servers through brute-force attacks against SSH and unauthorized access vulnerability. The latest DDG version is 3014.

Recently, Alibaba Cloud Security team detects an increase in the number of DDG mining botnet attacks. Once an attack succeeds, DDG executes the crontab command on the controlled servers to perform regularly update and run. Update source: hxxp://149.56.106.215:8000/i.sh

Download URLs:

-   hxxp://149.56.106.215:8000/i.sh
-   hxxp://149.56.106.215:8000/static/3014/ddgs.i686
-   hxxp://149.56.106.215:8000/static/3014/ddgs.x86\_64

Malicious IP address: 149.56.106.215

Event: DDG worm from a command-and-control server

Risk level: High

Cloud Firewall has been able to defend against such attacks. We recommend that you enable [intrusion prevention policies](/intl.en-US/Best Practices/Best practices for defending against CNC worms.md) in the Cloud Firewall console.


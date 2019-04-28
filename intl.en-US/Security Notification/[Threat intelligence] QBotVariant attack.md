# \[Threat intelligence\] QBotVariant attack {#concept_kz2_zjz_5fb .concept}

In May 2018, the Alibaba Cloud Security team detected worm samples written based on the QBot open-source code. Further investigation revealed that this was indeed a new QBot family member, which the team named QBotVariant. QBotVariant is capable of performing DDoS attacks, leveraging backdoors and downloaders, and conducting brute-force cracking. Infected servers become part of the QBotVariant botnet. QBotVariant can spread widely on the Internet and cause great harm.

QBotVariant exploits the REST API unauthorized access vulnerability of Hadoop YARN and uses hard-coded weak passwords to perform brute-force cracking. Once a server is infected, it becomes a botnet member that attacks other servers, and its bandwidth is consumed by its new "master." Furthermore, this infection may result in consequences such as data leakage and data loss.

Event: Worm attack

Risk level: High

Cloud Firewall has been able to defend against such attacks. We recommend that you enable [intrusion prevention policies](../../../../intl.en-US/User Guide/Security policies/Intrusion prevention policies.md#ol_ez3_mzd_dfb) in the Cloud Firewall console.

For more information, see [Some malicious URLs and QBotVariant details](https://yq.aliyun.com/articles/667970).


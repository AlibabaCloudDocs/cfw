# \[Basic rule\] Malicious file writing vulnerability of PostgreSQL

Alibaba Cloud's Cloud Firewall has been able to defend against the malicious file writing vulnerability of PostgreSQL.

PostgreSQL is a powerful, open-source object-relational database that runs on multiple operating systems. The PostgreSQL function `Lo_export` can be called to export large objects to a file. Once an attacker obtains PostgreSQL database privileges, the attacker can use the `Lo_import` and `Lo_export` functions to import malicious library files and execute system commands.

Rule type: Command execution

Risk level: High

Scope of impact: PostgreSQL databases

Rule-based defense: Cloud Firewall has been able to defend against this vulnerability. We recommend that you enable [intrusion prevention policies](/intl.en-US/Intrusion prevention/Intrusion prevention.md) in the Cloud Firewall console.


# \[Basic rule\] Update of Bash reverse shell detection rules

Cloud Firewall has updated the Bash reverse shell detection rules.

A lot of cyberattacks are launched by exploiting reverse shells. Such attacks often occur during the maintenance stage. Once an attacker obtains certain system command execution privileges, the attacker can use a reverse shell to open an interactive command execution window and then intrude into the system to steal data. When Cloud Firewall detects a reverse shell attack to your server, indicating that your server is at risk of intrusion, it blocks the reverse shell creation and command execution. This helps reduce the risks that the attack may bring.

Rule type: Reverse shell

Risk level: High

Rule-based defense: Cloud Firewall has been able to defend against such attacks. We recommend that you enable [intrusion prevention policies](/intl.en-US/Intrusion prevention/Intrusion prevention.md) in the Cloud Firewall console.


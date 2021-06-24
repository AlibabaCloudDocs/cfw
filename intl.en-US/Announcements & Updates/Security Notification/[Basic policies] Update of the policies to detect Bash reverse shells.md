# \[Basic policies\] Update of the policies to detect Bash reverse shells

The policies of Cloud Firewall to detect Bash reverse shells are updated. You can use the updated policies to accurately block attacks.

Reverse shells are common cyberattacks. In most cases, reverse shells are used if an attacker wants to continue to launch attacks. After an attacker obtains some permissions to execute commands in a system, the attacker can use reverse shells to establish interactive shell sessions to implement intrusions and information theft. If Cloud Firewall detects reverse shells on your server, your server has experienced an intrusion. In this case, Cloud Firewall blocks the establishment of reverse shell connections and related command execution to reduce risks.

Risk level: high

Rule-based defense: A virtual patch is available in the Cloud Firewall console to defend against this vulnerability.

Rule type: reverse shell


# \[Basic rule\] Malicious MySQL UDF execution {#concept_sdv_brc_tfb .concept}

MySQL allows users to specify user-defined functions \(UDFs\). Attackers who have MySQL database privileges can exploit this vulnerability to import custom UDFs from malicious library files to execute system commands.

This vulnerability mainly affects opened MySQL application servers. It may cause risks such as unauthorized control over servers, data leakage, ransom, cryptocurrency mining, and Distributed Denial of Service \(DDoS\) attacks to external systems.

Rule-based defense: Cloud Firewall has been able to defend against this vulnerability. We recommend that you enable [intrusion prevention policies](../../../../intl.en-US/Best Practices/Best practices for defending against CNC worms.md#ol_axk_vkt_dfb) in the Cloud Firewall console.

Scope of impact: MySQL databases

Rule type: Command execution

Risk level: High


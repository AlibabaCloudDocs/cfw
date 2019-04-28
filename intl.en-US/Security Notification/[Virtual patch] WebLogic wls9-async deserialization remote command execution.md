# \[Virtual patch\] WebLogic wls9-async deserialization remote command execution {#concept_186202 .concept}

On April 17, 2019, Yundun emergency response center of Alibaba Cloud detected the vulnerability named as "Oracle WebLogic wls9-async deserialization remote command execution vulnerability" disclosed by China National Vulnerability Database \(CNVD\). Attackers can exploit this vulnerability to remotely execute commands without authorization.

The default wls9\_async\_response package in some WebLogic versions provides asynchronous communication services for WebLogic Server. Because the War package has a defect in deserializd information processing, attackers can send specially crafted malicious HTTP requests to obtain the permissions of the target server and remotely execute commands without authorization.

Scope of impact: Oracle WebLogic 10. X and Oracle WebLogic 12.1.3

Risk level: High risk

Rule-based defense: A virtual patch is available in the Cloud Firewall console to defend against this vulnerability.


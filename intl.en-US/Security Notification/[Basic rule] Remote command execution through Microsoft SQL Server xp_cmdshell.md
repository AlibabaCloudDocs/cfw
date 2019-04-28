# \[Basic rule\] Remote command execution through Microsoft SQL Server xp\_cmdshell {#concept_v3r_pdc_dfb .concept}

SQL Server is a relational database management system introduced by Microsoft Corporation. The extended stored procedure xp\_cmdshell of SQL Server is used to run system commands. The xp\_cmdshell option enables system administrators to control whether to spawn a Windows command shell and pass it in a string for execution. Any output is returned as rows of text.

Malicious users sometimes attempt to elevate their privileges by using xp\_cmdshell to run system commands.

Rule-based defense: Cloud Firewall has been able to defend against remote command execution through SQL Server xp\_cmdshell.

Scope of impact: Microsoft SQL Server

Rule type: Command execution

Risk level: High


# Enable Intrusion Prevention {#concept_vpn_csh_cfb .concept}

Cloud Firewall is embedded with IPS to defend against intrusions in real time.

## Procedure {#section_css_2g3_cfb .section}

1.  Select the Intrusion Prevention Mode.

    -   **Monitoring Mode**: Enable monitoring mode to monitor malicious traffic and generate alarms.
    -   **Traffic Control Mode**: Enable traffic control mode to block the malicious traffic.
    **Note:** After you subscribe to the Cloud Firewall service, **Monitoring Mode** is enabled for IPS by default.

2.  In the **Basic Protection** module, turn on or off the **Basic Policies** switch to enable or disable the built-in basic intrusion prevention rules. The basic rules can intercept intrusions such as password cracking and command execution vulnerability.
3.  Turn on or off the **Threat Intelligence** switch to enable or disable the function of collecting network-wide threat intelligence.
4.  In the **Virtual Patches** Module, turn on or off the **Patches** switch to enable or disable the installation-free virtual patch function for preventing exploitation of high-risk vulnerabilities.

**Note:** After the configuration, you can view the details on different intrusion prevention activities in the **IPS Analysis** area on Traffic Analysis page.


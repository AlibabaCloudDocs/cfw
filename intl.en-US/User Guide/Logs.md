# Logs {#concept_z4k_xk4_cfb .concept}

All traffic passing through Cloud Firewall is recorded on the **Logs** page. Logs on this page are classified into traffic logs, event logs, and operation logs. You can use logs to audit your network traffic in real time and process it accordingly. By default, Cloud Firewall logs are stored for six months.

## Event logs {#section_lh4_wsq_cfb .section}

**Event logs** record event information including the event detection time, threat type, direction \(inbound or outbound\), source IP address, destination IP address, application type, severity, and action status.

![](images/11767_en-US.png)

You can specify the source IP address, destination IP address, threat type, action, or other information to search for an event log.****

You can also specify a custom time range to search for relevant event logs.

**Note:** The custom time range must be within the last six months.

## Traffic logs {#section_mb2_xsq_cfb .section}

**Traffic logs** record traffic information including the access start time and end time, direction \(inbound or outbound\), source IP address, destination IP address, application type, source port number, application, protocol, action status, byte count, and packet count.

![](images/11768_en-US.png)

You can specify the source IP address, destination IP address, application, or other information to search for a traffic log.****

You can also specify a time range to search for relevant traffic logs.

**Note:** The custom time range must be within the last six months.

To search for traffic logs more precisely, you can click **Show Advanced Search** next to the search bar and specify advanced criteria such as **Direction**, **Rule Source**, **Port**, and **Asset Region**.

![](images/36889_en-US.png)

For the traffic that matches an access control policy or IPS policy, the name of the matching policy is displayed in the **Rule Name** column of the traffic log. For the traffic that does not match any policies, the **Rule Name** column is empty.

## Operation logs {#section_ss2_xsq_cfb .section}

**Operation logs** record the execution time, type, severity, and details about each operation in Cloud Firewall.

![](images/11769_en-US.png)

You can select a value from the **Severity** drop-down list on the **Operation Log** tab to search for the operation logs at the specified severity.

You can also specify a time range to search for relevant operation logs. The custom time range must be within the last six months.


# View Cloud Firewall logs {#concept_z4k_xk4_cfb .concept}

All traffic passing through Cloud Firewall is recorded on the **Log Audit** page. The logs are classified into traffic logs, event logs, and operation logs. You can use the logs to audit your network traffic in real time and take actions accordingly. By default, Cloud Firewall logs are retained for six months.

## Event logs {#section_lh4_wsq_cfb .section}

The **event logs** record the information of each event, including the event detection time, threat type, traffic direction \(inbound or outbound\), source IP address, destination IP address, application type, severity, and policy action.

You can specify the source IP address, destination IP address, threat type, action, or other information to search for an **event log**.

You can also specify a time range to search for relevant event logs.

**Note:** The custom time range must be within the previous six months.

## Traffic logs {#section_mb2_xsq_cfb .section}

The **traffic logs** record traffic information including the access start time and end time, direction \(inbound or outbound\), source IP address, destination IP address, application type, source port number, application, protocol, policy action, byte count, and packet count.

You can specify the source IP address, destination IP address, application, or other information to search for a **traffic log**.

You can also specify a time range to search for relevant traffic logs.

**Note:** The custom time range must be within the previous six months.

To search for traffic logs more precisely, you can click **Show Advanced Search** next to the search bar and specify advanced conditions such as **Direction**, **Policy Source**, **Port**, and **Region**.

For the traffic that matches an access control policy or IPS policy, the name of the matching policy is displayed in the **Policy Name** column of the traffic log. For the traffic that does not match any policy, the **Policy Name** column is empty.

## Operation logs {#section_ss2_xsq_cfb .section}

The **operation logs** record the time, type, severity, and details about each operation in Cloud Firewall.

You can select a value from the **Severity** drop-down list on the **Operation Logs** tab page to search for the operation logs of the specified severity.

You can also specify a time range to search for relevant operation logs. The custom time range must be within the previous six months.


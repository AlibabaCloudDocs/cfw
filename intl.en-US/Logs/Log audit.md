# Log audit

All the traffic that passes through Cloud Firewall is recorded as logs and displayed on the **Log Audit** page. The logs are classified into traffic logs, event logs, and operations logs. You can use the logs to audit your network traffic in real time and take measures accordingly. By default, the log audit feature retains logs for seven days.

Cloud Firewall also provides the log analysis feature, which can retain logs for six months. If your business must meet classified protection requirements, we recommend that you enable the log analysis feature. For information about the billing method of the log analysis feature, see [Billing](/intl.en-US/Logs/Log analysis/Billing.md).

## Event logs

The Event Logs tab displays the logs of events on the Internet firewall and VPC firewalls. You can click the **Internet Firewall** or **VPC Firewall** tab to view information about event logs. The information includes the time an event was detected, the threat type, source IP address, destination IP address, application, severity, and policy action.

![Event logs](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/3779486851/p77773.png)

On the **Event Logs** tab, you can specify the source IP address, destination IP address, threat type, policy action, or time range to search for event logs.

**Note:** The time range must be within the last seven days.

## Traffic logs

The Traffic Logs tab displays the logs of traffic on the Internet firewall and VPC firewalls. You can click the **Internet Firewall** or **VPC Firewall** tab to view information about traffic logs. The information includes the start time and end time of traffic, source IP address, destination IP address, application type, source port, application, protocol, policy action, number of bytes, and number of packets.

![Traffic logs](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/3779486851/p77775.png)

On the **Traffic Logs** tab, you can specify the source IP address, destination IP address, application, or time range to search for traffic logs.

**Note:** The time range must be within the last seven days.

To more precisely search for traffic logs, click **Show Advanced Search** in the upper-right corner and specify search conditions such as **Direction**, **Policy Source**, **Port**, and **Region**.

![Advanced search](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/3779486851/p77779.png)

**Note:** If traffic hits an access control policy or IPS policy, the name of the policy is displayed in the **Policy Name** column of the traffic log entry. For traffic that does not hit a policy, the **Policy Name** column is displayed as a hyphen \(-\).

## Operation logs

The **Operation Logs** tab displays the time, type, severity, and other details about each operation performed on Cloud Firewall.

![Operation logs](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/6041523261/p77776.png)

On the **Operation Logs** tab, you can select an option from the **Severity** drop-down list to obtain operations logs of a specific severity.

You can also specify a time range within the last seven days to search for operations logs.


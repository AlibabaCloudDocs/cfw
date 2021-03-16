# Log fields

Cloud Firewall logs record both inbound and outbound traffic. Each log entry contains multiple fields. You can use these fields to search and analyze logs.

|Field name|Description|Example|
|:---------|:----------|:------|
|\_\_time\_\_|The time when the operation is performed.|2018-02-27 11:58:15|
|\_\_topic\_\_|The topic of the log entry. The value is fixed as `cloudfirewall_access_log`, which indicates that the log entry records traffic controlled by Cloud Firewall.|cloudfirewall\_access\_log|
|log\_type|The type of the log entry. The value is fixed as `internet_log`, which indicates the log entry records Internet traffic.|internet\_log|
|aliuid|The ID of the Alibaba Cloud account.|1233333333\*\*\*\*|
|app\_name|The application to which the traffic belongs. The valid values include `HTTPS`, `NTP`, `SIP`, `SMB`, `NFS`, `DNS`, and `Unknown`.|HTTPS|
|direction|The direction of the traffic. Valid values: -   `in`: inbound traffic to your Elastic Compute Service \(ECS\) instances from other ECS instances in the internal network or from servers on the Internet.
-   `out`: outbound traffic from your ECS instances to other ECS instances in the internal network or to servers on the Internet.

|in|
|domain|The domain name of the traffic.|www.aliyun.com|
|dst\_ip|The destination IP address of the traffic.|1.XX.XX.1|
|dst\_port|The destination port of the traffic.|443|
|end\_time|The time when the session ends. This value is a UNIX timestamp. Unit: seconds.|1555399260|
|in\_bps|The rate of inbound traffic. Unit: bit/s.|11428|
|in\_packet\_bytes|The total number of bytes in inbound traffic.|2857|
|in\_packet\_count|The total number of packets in inbound traffic.|18|
|in\_pps|The packet throughput of inbound traffic. Unit: packet/s.|9|
|ip\_protocol|The IP protocol of the traffic. Valid values: `TCP` and `UDP.`|TCP|
|out\_bps|The rate of outbound traffic. Unit: bit/s.|27488|
|out\_packet\_bytes|The number of bytes in outbound traffic.|6872|
|out\_packet\_count|The number of packets in outbound traffic.|15|
|out\_pps|The packet throughput of outbound traffic. Unit: packet/s.|7|
|region\_id|The region ID of the traffic. For more information about region IDs, see [Regions that are supported by Cloud Firewall](/intl.en-US/Product Introduction/Regions that are supported by Cloud Firewall.md).|cn-beijing|
|rule\_result|The processing result of the traffic that matches the access control policy. Valid values: -   `pass`: Cloud Firewall allows the traffic.
-   `alert`: Cloud Firewall allows the traffic and generates an alert.
-   `drop`: Cloud Firewall drops the traffic, which indicates that the traffic cannot pass Cloud Firewall.

|pass|
|src\_ip|The source IP address of the traffic.|1.XX.XX.1|
|src\_port|The source port of the traffic.|47915|
|start\_time|The time when the session starts. This value is a UNIX timestamp. Unit: seconds.|1555399258|
|start\_time\_min|The time when the session starts. The value of this field is rounded up to the next minute. This value is a UNIX timestamp. Unit: seconds.|1555406460|
|tcp\_seq|The TCP serial number.|3883676672|
|total\_bps|The total rate of inbound and outbound traffic. Unit: bit/s.|38916|
|total\_packet\_bytes|The total number of bytes in inbound and outbound traffic. Unit: byte.|9729|
|total\_packet\_count|The total number of packets in inbound and outbound traffic.|33|
|total\_pps|The total packet throughput of inbound and outbound traffic. Unit: packet/s.|16|
|vul\_level|The risk level of the vulnerability. Valid values: -   `1`: low-risk vulnerabilities
-   `2`: medium-risk vulnerabilities
-   `3`: high-risk vulnerabilities

|1|
|url|The URL of the Internet website that your ECS instance accesses.|http://www.test.com/index.html|
|src\_private\_ip|The private IP address of the source ECS instance in outbound traffic.|192.168.0.0|
|acl\_rule\_id|The ID of the access control list \(ACL\) rule that matches the traffic.|073a1475-6e11-43e2-8b28-98cee9c688c0|
|ips\_rule\_id|The ID of the intrusion prevention system \(IPS\) rule that matches the traffic.|073a1475-6e11-43e2-8b28-98cee9c688c0|
|ips\_ai\_rule\_id|The ID of the AI rule that matches the traffic.|073a1475-6e11-43e2-8b28-98cee9c688c0|
|ips\_rule\_name|The Chinese name of the IPS rule that matches the traffic.|Mining activities of hosts|
|ips\_rule\_name\_en|The English name of the IPS rule that matches the traffic.|Mining behavior on the host|
|attack\_type\_name|The Chinese name of the attack type that is detected in the traffic.|Mining activities|
|attack\_type\_name\_en|The English name of the attack type that is detected in the traffic.|Mining Behavior|


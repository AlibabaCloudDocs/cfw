# Fields in the log entry {#concept_ttq_kd4_hhb .concept}

Cloud firewall records the inbound and outbound traffic logs, including multiple log fields. You can perform query and analysis based on specific fields.

|Field Name|Description|Example|Comments|
|:---------|:----------|:------|--------|
|\_\_time\_\_|Time of the operation in Cloud Firewall|2018-02-27 11:58:15|-|
|\_\_topic\_\_|Log topic|cloudfirewall\_access\_log|Log topic is unique, which is cloudfirew for Cloud Firewall.|
|Log\_type|Log types|Internet\_log|Internet\_log refers to the Internet Traffic Log.|
|aliuid|User's Alibaba Cloud UID|12333333333333|-|
|app\_name|Protocol of the access traffic|HTTPS|Possible values include HTTPS, NTP, SIP, SMB, NFS, and DNS. Unknown values are Unknown.|
|direction|Traffic direction|in| -   in: traffic goes to the ENI
-   out: traffic goes from the ENI

 |
|domain|Domain name|www.aliyun.com|-|
|dst\_ip|Destination IP|1.1.1.1|-|
|dst\_port|Destination port|443|-|
|end\_time|Session end time|1555399260|Unit: Seconds \(Unix timestamp\)|
|In\_bps|Bps of inbound traffic|11428|Unit: bps|
|In\_packet\_bytes|Total number of bytes of inbound traffic|2857|-|
|In\_packet\_count|Total number of packet of inbound traffic|18|-|
|In\_pps|Pps of inbound traffic|9|Unit: pps|
|Ip\_protocol|IP protocol type|TCP|Protocol name. TCP and UDP protocol are supported.|
|Out\_bps|Bps of outbound traffic|27488|Unit: bps|
|Out\_packet\_bytes|Total number of bytes of outbound traffic|6872|-|
|Out\_packet\_count|Total number of packet of outbound traffic|15|-|
|Out\_pps|Pps of outbound traffic|7|Unit: pps|
|region\_id|Region to which the access traffic belongs|cn-beijing|-|
|Rule\_result|Result of matching with the rules|pass23|The result of matching with the rules. The values are: -   Pass: The traffic is allowed to pass through Cloud Firewall.
-   Alert: Cloud Firewall detects threats in the traffic.
-   Discard: The traffic is not allowed to pass through Cloud Firewall.

 |
|src\_ip|Source IP|1.1.1.1|-|
|src\_port|The port of the host from which traffic data is sent|47915|-|
|start\_time|Session start time|1555399258|Unit: Seconds \(Unix timestamp\)|
|Start\_time\_min|Session start time, which is an integer in minutes|1555406460|Unit: Seconds \(Unix timestamp\)|
|Tcp\_seq|TCP serial number|3883676672|-|
|Total\_bps|Total bps of both inbound and outbound traffic|38916|Unit: bps|
|Total\_packet\_bytes|Total number of bytes of both inbound and outbound traffic|9729|Unite: byte|
|Total\_packet\_count|Total number of packets of both inbound and outbound traffic|33|-|
|Total\_pps|Total number of pps of both inbound and outbound traffic|16|Unit: pps|
|Src\_private\_ip|Private IP of the source host|1.1.1.1| |
|Vul\_level|Vulnerability Risk level|High|Vulnerability Risk level: -   1: Low
-   2: Moderate
-   3: High

 |


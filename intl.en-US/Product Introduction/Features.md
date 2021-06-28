# Features

Cloud Firewall is an industry-leading cloud security solution that provides firewalls as a service. It manages both north-south and east-west traffic and provides features, such as traffic monitoring, precise access control, and real-time intrusion prevention, to protect your networks.

## Cloud Firewall features

The following table describes Cloud Firewall features and the editions that provide these features.

**Note:**

-   Cross \(×\): Cloud Firewall does not support this feature.
-   Tick \(√\): Cloud Firewall supports this feature.

|Scenario|Feature|Description|Basic Edition|Premium Edition|Enterprise Edition|Ultimate Edition|References|
|--------|-------|-----------|-------------|---------------|------------------|----------------|----------|
|Access traffic analysis and attack detection of on-cloud networks|Overview|Provides an overview of defense features that are enabled and disabled and shows statistics on access traffic and detected security risks in the last seven days.|×|√|√|√|[Overview](/intl.en-US/Overview/Overview.md)|
|Access control|Internet Firewall|Supports two-way access control over north-south traffic and supports domain name-based access control to strictly control the traffic of outbound connections.|×|√|√|√|[Access control for outbound and inbound traffic on the Internet firewall](/intl.en-US/Access Control/Access control for outbound and inbound traffic on the Internet firewall.md)|
|VPC Firewall|Controls traffic between virtual private clouds \(VPCs\).|×|×|√|√|[Access control on VPC firewalls](/intl.en-US/Access Control/Access control on VPC firewalls.md)|
|Internal Firewall|Isolates east-west traffic among your Elastic Compute Service \(ECS\) instances on an internal network.|×|×|√|√|[Access control on an internal firewall between ECS instances](/intl.en-US/Access Control/Access control on an internal firewall between ECS instances.md)|
|Real-time monitoring and analysis of network traffic|Outbound Connections|Monitors outbound connections of cloud assets in real time.|×|√|√|√|[Outbound connections](/intl.en-US/Traffic Analysis/Outbound connections.md)|
|Internet Access|Collects and analyzes the statistics on access traffic of on-cloud networks.|×|√|√|√|[Internet access](/intl.en-US/Traffic Analysis/Internet access.md)|
|VPC Access|Monitors the traffic between VPCs in real time, which allows you to dynamically obtain the VPC traffic data and identify and handle suspicious traffic at the earliest opportunity.|×|×|√|√|[VPC access](/intl.en-US/Traffic Analysis/VPC access.md)|
|Breach Awareness|Provides details about intrusion events that are detected by the intrusion prevention system \(IPS\) and the solutions to handle the intrusion events.|×|√|√|√|[Breach awareness](/intl.en-US/Intrusion Prevention/Breach awareness.md)|
|Traffic Blocked by IPS|Provides statistics on access traffic that is blocked by Cloud Firewall.|×|√|√|√|[Intrusion prevention](/intl.en-US/Intrusion Prevention/Intrusion prevention.md)|
|All Access Activities|Allows you to query traffic that passes through Cloud Firewall based on conditions.|×|√|√|√|[All access activities](/intl.en-US/Traffic Analysis/All access activities.md)|
|Intrusion prevention|Vulnerability Prevention|Detects vulnerabilities that can be exploited by network attacks and defends against these vulnerabilities.|×|√|√|√|[Vulnerability prevention](/intl.en-US/Intrusion Prevention/Vulnerability prevention.md)|
|Intrusion prevention|-   Intelligently detects and blocks intrusions in real time. Analyzes the network traffic blocked by Cloud Firewall and IPS.
-   Synchronizes all malicious IP addresses of sources that are detected across Alibaba Cloud and defends against potential threats. The sources include malicious visitors, scanners, and command and control \(C&C\) servers.
-   Integrates the intrusion prevention policies used for attack and defense on Alibaba Cloud to ensure high accuracy in threat detection.
-   Supports installation-free virtual patches for business systems. Protects against common vulnerabilities and high-risk zero-day and N-day vulnerabilities.

|×|√|√|√|[Prevention configuration](/intl.en-US/Intrusion Prevention/Prevention configuration.md)|
|Log management|Log Audit|Provides log audit and behavior backtracking.-   Provides event logs to show threats or intrusions detected and blocked by the intrusion prevention module in real time.
-   Provides traffic logs to record the traffic that passes through Cloud Firewall. When a threat occurs, you can view traffic logs to analyze traffic, identify its source, and check whether configured access control policies take effect.
-   Provides system operation logs to record all configurations and operations on Cloud Firewall.

|×|√|√|√|[Log audit](/intl.en-US/Logs/Log audit.md)|
|Log Analysis|Automatically collects, stores, and analyzes inbound and outbound traffic logs in real time and supports real-time monitoring and alerting based on specific metrics. This ensures timely responses if exceptions occur in critical business. Logs can be stored for up to six months.|×|√|√|√|[Activate Log Service](/intl.en-US/Logs/Log analysis/Enable the Log Analysis feature.md)|
|Common tools for network traffic detection|Toolbox|Provides the policy rollback feature.|×|√|√|√|[Back up and roll back an access control policy](/intl.en-US/Toolbox/Back up and roll back an access control policy.md)|
|Provides the packet capture feature to help you fully understand network traffic that passes through Cloud Firewall.|×|√|√|√|[Create a packet capture task](/intl.en-US/Toolbox/Create a packet capture task.md)|
|Allows you to check security group configurations and check whether the requirements of classified protection are met.|√|√|√|√|[Check security group rules](/intl.en-US/Toolbox/Check security group rules.md)|
|Business visualization|Custom Groups|Allows you to create custom groups to build relationships between the applications of your cloud assets and application groups or business groups.|×|√|√|√|[Create application groups and business groups](/intl.en-US/Business Visualization/Create application groups and business groups.md)|


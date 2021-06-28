# VPC firewall limits

This topic describes the limits of Virtual Private Cloud \(VPC\) firewalls.

|Item|Description|Suggestion|
|----|-----------|----------|
|Number of protected VPCs|By default, VPC Firewall can be enabled for 15 VPCs in the same region of a cloud enterprise network \(CEN\). You can increase the quota to 20.|None.|
|Each region can have up to 20 VPCs. A VPC firewall that is added by Cloud Firewall consumes this quota. After VPC Firewall is enabled, Cloud Firewall adds a VPC for each region involved. To view the newly added VPC, log on to the [VPC console](https://vpcnext.console.aliyun.com/vpc) and go to the VPCs page. The VPC named Cloud\_Firewall\_VPC is the newly added VPC. If a region already has 20 VPCs, VPC Firewall cannot be enabled for this region.|If the VPC quota is used up, log on to the [VPC console](https://vpcnext.console.aliyun.com/vpc) and go to the Quota Management page to increase the VPC quota. If the VPC quota has reached the upper limit, submit a ticket or contact after-sales service in the specified DingTalk group.|
|The total number of VPCs and regions for which VPC Firewall is enabled is less than or equal to 32.|None.|
|VPC custom routes|The number of custom routes increases after you enable VPC Firewall. If the number of custom routes in your VPC route table reaches the upper limit, you cannot enable VPC Firewall. For more information, see [Add a custom route entry]().|Increase the VPC quota. Log on to the [VPC console](https://vpcnext.console.aliyun.com/vpc), go to the Quota Management page, and then increase the maximum number of custom routes allowed for each route table within your Alibaba Cloud account.

**Note:** Do not modify or delete custom routes that are added by Cloud Firewall. If you modify or delete these routes, VPC firewalls cannot protect inbound traffic to ECS instances. |
|CEN-related limits|If two VPCs in a CEN are created by different Alibaba Cloud accounts, Cloud Firewall must be authorized to access both VPCs. Otherwise, VPC Firewall cannot be enabled for the CEN.|Before you enable VPC Firewall, you must use the Alibaba Cloud accounts to separately log on to the Cloud Firewall console and complete the authorization. For more information, see [Create a VPC firewall for a CEN](/intl.en-US/Firewall Settings/VPC Firewall/Create a VPC firewall.md).|
|Make ensure that VPC Firewall is available in all the regions in the CEN. Otherwise, VPC Firewall cannot be enabled for the CEN.|None.|
|VPC firewall users in a CEN cannot publish routes to a network with a 32-bit subnet mask. If such routes are published and VPC Firewall is enabled, the connections to this network are interrupted.|We recommend that you change the subnet mask length to less than or equal to 30 bits before you enable VPC Firewall.|
|Traffic that is not between VPCs|Cloud Firewall does not protect the following mutual access traffic because it does not pass Cloud Firewall:-   Mutual access traffic between Virtual Border Routers \(VBRs\)
-   Mutual access traffic between Cloud Connect Networks \(CCNs\)
-   Mutual access traffic between VBRs and CCNs

|You can submit a ticket or contact after-sales service in the specified DingTalk group for product consultation.|
|Server Load Balancer \(SLB\) and ApsaraDB RDS-related limits|When you enable or disable VPC Firewall for SLB or ApsaraDB RDS, the persistent connections may fail. If the backend server of an SLB instance has custom forwarding rules, such as SNAT rules, DNAT rules, or routing rules, mutual access traffic between cloud services and the Internet passes different VPCs.|The following suggestions are provided:-   Before you enable or disable VPC Firewall, make sure that the port used for health checks of the SLB instance does not overlap with the ports specified by the custom forwarding rules for the backend servers of the instance. This prevents network latency and network jitter.
-   Configure the keep-connection-alive and reconnection mechanisms on the client. |
|If a public IP address is used as private in your network topology after Cloud Firewall is enabled, access to SLB and ApsaraDB RDS is interrupted.|We recommend that you develop a network plan based on the standards and do not use a public IP address as private.|


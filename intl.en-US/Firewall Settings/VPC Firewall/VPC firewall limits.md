# VPC firewall limits

This topic describes the limits of Virtual Private Cloud \(VPC\) firewalls.

|Item|Description|Solution|
|----|-----------|--------|
|Number of protected VPCs|If you enable VPC Firewall for a Cloud Enterprise Network \(CEN\), up to 15 VPCs can be added to a Basic Edition transit router of the CEN, and up to 100 VPCs can be added to an Enterprise Edition transit router of the CEN. The VPCs must reside in the same region as the CEN. **Note:** The total number of VPCs that you can add to a Basic Edition or Enterprise Edition transit router includes the VPC that is automatically created when you enable VPC Firewall. The created VPC is the VPC named Cloud\_Firewall\_VPC on the VPCs page of the [VPC console](https://vpcnext.console.aliyun.com/vpc).

|None.|
|Each region can have up to 20 VPCs. A VPC firewall that is added by Cloud Firewall consumes this quota. After VPC Firewall is enabled, Cloud Firewall automatically creates a VPC for each region involved. The newly created VPC is the VPC named Cloud\_Firewall\_VPC on the VPCs page of the [VPC console](https://vpcnext.console.aliyun.com/vpc). If a region has 20 VPCs, VPC Firewall cannot be enabled for this region.|If the VPC quota is used up, log on to the [VPC console](https://vpcnext.console.aliyun.com/vpc) and go to the Quota Management page to increase the VPC quota. If the VPC quota reaches the upper limit, submit a [ticket](https://workorder-intl.console.aliyun.com/console.htm#/ticket/createIndex) or contact after-sales service in the specified DingTalk group.|
|The total number of VPCs and regions for which VPC Firewall is enabled is less than or equal to 32.|None.|
|VPC custom routes|After you enable VPC Firewall, the number of custom routes increases. If the number of custom routes in your VPC route table reaches the quota, you cannot enable VPC Firewall.|Increase the VPC quota. Log on to the [VPC console](https://vpcnext.console.aliyun.com/vpc), go to the Quota Management page, and then increase the maximum number of custom routes allowed for each route table within your Alibaba Cloud account.

**Note:** Do not modify or delete custom routes that are added by Cloud Firewall. If you modify or delete these routes, VPC firewalls cannot protect inbound traffic to ECS instances. |
|CEN-related limits|If two VPCs in a CEN are created by different Alibaba Cloud accounts, Cloud Firewall must be authorized to access both VPCs. Otherwise, VPC Firewall cannot be enabled for the CEN.|Before you enable VPC Firewall, you must use the Alibaba Cloud accounts to separately log on to the Cloud Firewall console and complete the authorization. For more information, see [Create a VPC firewall for a CEN](/intl.en-US/Firewall Settings/VPC Firewall/Create a VPC firewall.md).|
|Make sure that VPC Firewall is available in all the regions in the CEN. Otherwise, VPC Firewall cannot be enabled for the CEN.|None.|
|VPC firewall users in a CEN cannot publish routes to a network with a 32-bit subnet mask. If routes with a 32-bit subnet mask are published and VPC Firewall is enabled, the connections to this network are interrupted.|Before you enable VPC Firewall, we recommend that you change the subnet mask length to less than or equal to 30 bits.|
|Take note of the following limits on Enterprise Edition transit routers in CEN:-   After you create a VPC firewall in **automatic mode**, you must contact after-sales service to add the newly created VPC that is named Cloud\_Firewall\_VPC to the whitelist of a CEN. Then, you can enable VPC Firewall.
-   After you create a VPC firewall in **manual mode**, you must contact after-sales service to add the newly created VPC to the whitelist of a CEN. Then, you can enable VPC Firewall.

|To add a VPC to the whitelist of a CEN, submit a [ticket](https://workorder-intl.console.aliyun.com/console.htm#/ticket/createIndex) or contact after-sales service in the specified DingTalk service group.|
|Traffic that is not between VPCs|Cloud Firewall does not protect the following mutual access traffic because it does not pass Cloud Firewall:-   Mutual access traffic between Virtual Border Routers \(VBRs\)
-   Mutual access traffic between Cloud Connect Networks \(CCNs\)
-   Mutual access traffic between VBRs and CCNs

|You can submit a [ticket](https://workorder-intl.console.aliyun.com/console.htm#/ticket/createIndex) or contact after-sales service in the specified DingTalk group for product consultation.|
|Server Load Balancer \(SLB\) and ApsaraDB RDS-related limits|When you enable or disable VPC Firewall for SLB or ApsaraDB RDS, the persistent connections may fail. If the backend server of an SLB instance has custom forwarding rules, such as SNAT rules, DNAT rules, or routing rules, mutual access traffic between cloud services and the Internet passes different VPCs.|The following suggestions are provided:-   Before you enable or disable VPC Firewall, make sure that the port used for health checks of the SLB instance does not overlap with the ports specified by the custom forwarding rules for the backend servers of the instance. This prevents network latency and network jitter.
-   Configure the keep-connection-alive and reconnection mechanisms on the client. |
|If a public IP address is used as private in your network topology after Cloud Firewall is enabled, access to SLB and ApsaraDB RDS is interrupted.|We recommend that you develop a network plan based on the standards and do not use a public IP address as private.|


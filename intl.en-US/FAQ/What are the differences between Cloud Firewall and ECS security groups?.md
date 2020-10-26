# What are the differences between Cloud Firewall and ECS security groups?

A security group is a virtual internal firewall provided by Elastic Compute Service \(ECS\) to control the traffic between ECS instances.

Cloud Firewall provides the Internet firewall to control the traffic at the Internet boundaries, VPC firewalls to control the traffic between VPCs, and internal firewalls to control the traffic between ECS instances.

Internal firewalls provided by Cloud Firewall use the technology of security groups. The policies that are configured on the **Internal Firewall** tab of the **Access Control** page in the [Cloud Firewall console](https://yundunnext.console.aliyun.com/?&p=cfwnext#/security/access/internal) are automatically synchronized with the policies that are configured on the Security Groups page in the [ECS console](https://ecs-cn-zhangjiakou.console.aliyun.com/?#/securityGroup/region/cn-zhangjiakou).

## Unique features of Cloud Firewall

-   Application-based access control. For example, you can allow HTTP traffic so that HTTP services can run on any port.
-   Domain name-based access control. For example, you can allow ECS instances to send requests only to \*.aliyun.com.
-   Address books. You can add multiple IP addresses, ports, or ECS instances with the same tag to an address book for centralized management.
-   Intrusion prevention. Cloud Firewall provides preemptive measures against common system vulnerabilities and brute-force attacks.
-   The monitor mode of access control policies.
-   Complete traffic logs and real-time traffic analysis.

## Enhanced features of Cloud Firewall

Cloud Firewall provides the following enhancements to security groups:

-   If no policy in a policy group is set to allow, the ECS instances in the policy group cannot communicate with each other.

    **Note:** After all policies in a policy group are deleted, the policy group is considered as a policy group to which no policies have been added.

-   You can publish multiple policies at a time.
-   The number of policies configured for internal firewalls \(rules in ECS security groups\) is limited. You can configure access control policies for VPC firewalls to ensure security. You can [submit a ticket](https://workorder-intl.console.aliyun.com/console.htm#/ticket/createIndex) to increase the quota of access control policies for VPC firewalls.


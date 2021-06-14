# FAQ about access control policies

## How do I determine the priority of an access control policy?

The priorities of access control policies determine the order in which the policies take effect. Cloud Firewall automatically determines the priorities of access control policies. By default, a smaller value indicates a higher priority. You can manually adjust the priority of a policy. For more information, see [Change the priority of an access control policy](/intl.en-US/Access control/Change the priority of an access control policy.md).

If you have configured multiple access control policies, Cloud Firewall matches policies against the traffic that arrives at **Cloud Firewall** based on the priorities of the policies. If Cloud Firewall matches a policy, Cloud Firewall no longer checks other policies. If an Allow policy is matched, the traffic is allowed. If a Deny policy is matched, the traffic is blocked.

-   For access control policies of the Internet firewall for inbound and outbound traffic, a smaller value indicates a higher priority.

    **Note:** The priority of each access control policy is unique.

-   For access control policies of internal firewalls, a smaller value indicates a higher priority. This also applies to the rules of security groups.

    The priorities range from 1 to 100. Different access control policies can have the same priority. If multiple policies have the same priority, **Deny** policies take precedence over other policies.


## What do I do if the number of policy groups or policies for an internal firewall reaches the upper limit?

By default, you can create a maximum of 100 policy groups and 100 policies in each group. The policies include those synchronized from Elastic Compute Service \(ECS\) security groups to Cloud Firewall and those created in the Cloud Firewall console. If you require more policies, we recommend that you delete unnecessary policies or submit a [ticket](https://workorder-intl.console.aliyun.com/console.htm#/ticket/createIndex) for Alibaba Cloud technical support.

## What are the differences between common policy groups and enterprise policy groups?

Policy groups configured on an internal firewall between Elastic Compute Service \(ECS\) instances are classified into common and enterprise policy groups.

-   A common policy group applies to the basic security groups of ECS instances and functions as a virtual firewall to provide the Stateful Packet Inspection \(SPI\) and packet filtering capabilities. You can use a common policy group to isolate security domains on the cloud. You can configure access control policies to allow or block inbound and outbound traffic between ECS instances in a common policy group.
-   An enterprise policy group applies to the advanced security groups of ECS instances and supports more ECS instances than a common policy group. You can configure access control policies for an unlimited number of private IP addresses. Enterprise policy groups are best suited to enterprises that require efficient operations and maintenance \(O&M\) on large-scale networks.

The following table lists the differences between common and enterprise policy groups.

|Feature|Common policy group|Enterprise policy group|
|-------|-------------------|-----------------------|
|VPC|Supported.|Supported.|
|Policy priority configuration|Supported.|Supported.|
|Authorization of other policy groups|Supported.|Supported.|
|Custom Allow policy|Supported.|Supported.|
|Custom Deny policy|Supported.|Not supported. Enterprise policy groups block all traffic by default.|
|Number of private IP addresses allowed|2000|65536|
|Communication between ECS instances in the same policy group|Supported.|Not supported. You must add access control policies for the ECS instances to the policy group.|

## Why is an error returned after I click Apply to allow the traffic of a security group?

The security groups associated with the IP address of the ECS instance do not support the default Allow policy due to the following reasons:

-   Advanced security groups do not support default allow policies. For more information, see [Advanced security groups](/intl.en-US/Security/Security groups/Advanced security groups.md). If a VPC contains an advanced security group, default allow policies are also not supported for other security groups in the VPC.
-   Default allow policies can be configured only for security groups associated with public IP addresses or EIPs of ECS instances. They cannot be configured for Internet SLB instances.
-   To better protect your assets, we recommend that you do not apply default allow policies to IP addresses with the Internet firewall disabled. You must enable the firewall for IP addresses to which you have applied default allow policies. Otherwise, these IP addresses may be exposed to the Internet.

## When I apply the default Allow policy, the system prompts a conflict that cannot be resolved. Why?

The priorities of the access control rules that you want to apply to an ECS security group conflict with those specified for the rules of another ECS security group in the same virtual private cloud \(VPC\).

You can click the One-click Apply icon to apply the default Allow policy only when no conflicts exist between the priorities of rules in different ECS security groups in the same VPC.

## Why is the One-click Apply icon unavailable?

Conflicts exist between the priorities of rules in different ECS security groups. You can apply the default Allow policy only after you resolve the conflicts between the priorities of rules in the security groups that are associated with the IP address of the ECS instance. For more information, see [Default allow policies for security groups](/intl.en-US/Access control/Default allow policies for security groups.md).

## Why is an error returned when I click the One-click Apply icon?

An error is returned because the number of access control rules created for the required security group exceeds the upper limit.

By default, you can create a maximum of 100 policy groups and 100 policies in each group. The policies include those synchronized from Elastic Compute Service \(ECS\) security groups to Cloud Firewall and those created in the Cloud Firewall console. If you require more policies, we recommend that you delete unnecessary policies or submit a [ticket](https://workorder-intl.console.aliyun.com/console.htm#/ticket/createIndex) for Alibaba Cloud technical support.


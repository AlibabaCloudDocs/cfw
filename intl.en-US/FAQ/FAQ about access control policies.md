# FAQ about access control policies

## How can I determine the priority of an access control policy?

The priorities of access control policies determine the order of the policies to be matched against network traffic.

-   For access control policies of the Internet firewall for inbound and outbound traffic, a small value indicates a high priority.

    The traffic that arrives at **Cloud Firewall** is matched against policies with priorities 1 to 8 in sequence. If the traffic hits an allow policy, the traffic is allowed. If the traffic hits a deny policy, the traffic is denied. The priority for each access control policy must be unique.

    For more information, see [Change the priority of an access control policy](/intl.en-US/Access control/Change the priority of an access control policy.md).

-   For access control policies of internal firewalls, a small value indicates a high priority, which is the same as security group rules.

    The priorities range from 1 to 100. Different access control policies can have the same priority. For policies with the same priority, **deny** policies take precedence over allow policies.


## What do I do if the number of policy groups or policies for an internal firewall reaches the upper limit?

By default, you can create a maximum of 100 policy groups and 100 policies in each group. The policies include those synchronized from Elastic Compute Service \(ECS\) security groups to Cloud Firewall and those created in the Cloud Firewall console. If you need more policies, we recommend that you delete unnecessary policies or submit a [ticket](https://workorder-intl.console.aliyun.com/console.htm#/ticket/createIndex) for Alibaba Cloud technical support.

## What are the differences between common policy groups and enterprise policy groups?

Policy groups for an internal firewall that controls the traffic between ECS instances are classified into common policy groups and enterprise policy groups.

-   A common policy group is equivalent to an ECS security group. A common policy group functions as a virtual firewall to detect the connection status and filter data packets. It can be used to divide security zones on the cloud. You can configure access control policies to allow or deny inbound and outbound traffic between ECS instances in a common policy group.
-   An enterprise policy group is equivalent to an advanced ECS security group. An enterprise policy group supports more ECS instances than a common policy group. You can configure access control policies for an unlimited number of private IP addresses. Enterprise policy groups are best suited to enterprises that require efficient O&M on large-scale networks.

The following table lists the features of common and enterprise policy groups.

|Feature|Common policy group|Enterprise policy group|
|-------|-------------------|-----------------------|
|VPC|Supported.|Supported.|
|Policy priority configuration|Supported.|Not supported.|
|Authorization to other policy groups|Supported.|Not supported.|
|Custom allow policy|Supported.|Supported.|
|Custom deny policy|Supported.|Not supported. Enterprise policy groups deny all traffic by default.|
|Number of private IP addresses allowed|2,000|65,536|
|Communication between ECS instances in the same policy group|Supported.|Not supported. You must add access control policies for the ECS instances to the policy group.|

## Why is an error returned after I click Apply to allow traffic of a security group?

The security group associated with the public IP address does not support the default allow policy due to the following reasons:

-   Advanced security groups do not support default allow policies. For more information, see [Advanced security group](/intl.en-US/Security/Security groups/Advanced security group.md). If a VPC contains an advanced security group, default allow policies are also not supported for other security groups in the VPC.
-   Default allow policies can be configured only for security groups associated with public IP addresses or EIPs of ECS instances. They cannot be configured for Internet SLB instances.
-   To better protect your assets, we recommend that you do not apply default allow policies to IP addresses with the Internet firewall disabled. You must enable the firewall for IP addresses to which you have applied default allow policies. Otherwise, these IP addresses may be exposed to the Internet.

## Why am I unable to handle the configuration conflict that occurred when the default allow policy is applied?

The priorities of the access control rules you want to apply to an ECS security group conflict with the rules for another ECS security group in the same VPC.

You can apply the default allow policy with one click only if priorities of access control rules for all ECS security groups in the VPC do not have conflicts.

## Why is the One-click Apply icon unavailable?

ECS security groups have rule priority conflicts. You can apply the default allow policy only after the priority conflicts between the access control rules for ECS security groups are handled. For more information, see [Default allow policies for security groups](/intl.en-US/Access control/Default allow policies for security groups.md).

## Why is an error returned when I click One-click Apply?

The cause is that the number of access control rules created for a security group exceeds the upper limit.

By default, you can create a maximum of 100 policy groups and 100 policies in each group. The policies include those synchronized from Elastic Compute Service \(ECS\) security groups to Cloud Firewall and those created in the Cloud Firewall console. If you need more policies, we recommend that you delete unnecessary policies or submit a [ticket](https://workorder-intl.console.aliyun.com/console.htm#/ticket/createIndex) for Alibaba Cloud technical support.


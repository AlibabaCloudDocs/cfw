# Access control over the internal firewall between ECS instances {#concept_lxf_5k4_cfb .concept}

Cloud Firewall supports access control over the internal firewall. You can configure access control policies to restrict unauthorized access between ECS instances.

The internal firewall integrates the features of the ECS security group module. The access control policies that you configure on the Internal Firewall page in Cloud Firewall are automatically synchronized to the security group module of ECS.

**Note:** To view the policy groups that you have configured on the Internal Firewall page, specify **Source** as Custom, and click **Search**.

## Benefits of internal firewall {#section_v00_wn6_rjs .section}

-   You can publish multiple policies at the same time.
-   You can create policy groups based on templates.

    The templates are as follows:

    -   default-accept-login: Allow all inbound traffic that passes through port 22 and port 3389 by default.
    -   default-drop-all: Deny all traffic in the policy group by default.
    -   default-accept-all: Allow all traffic in the policy group by default.
-   Security groups can be automatically created based on application groups.

**Note:** By default, you can create up to 100 policy groups and 100 policies between ECS instances. The policies include those created in the ECS security group module and synchronized to Cloud Firewall and those created on the Internal Firewall page in Cloud Firewall. If you want to create more policies than allowed, we recommend that you delete unnecessary policies or submit a ticket for technical support.

## Procedure {#section_9av_68m_tlu .section}

Create a policy group, and then configure **inbound** or **outbound** access control policies.

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext#/overview).
2.  In the left-side navigation pane, choose **Security Policies** \> **Access Control** \> **Internal Firewall**.

    ![主机边界防火墙](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21269/156897215511761_en-US.png)

3.  In the upper-right corner, click **Create Policy Group**. In the Create Policy Group dialog box, configure the policy group.

    ![新建策略](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21269/156897215511762_en-US.png)

    The configuration items of a policy group are described as follows:

    |Item|Description|Configuration note|
    |----|-----------|------------------|
    |**Name**|The name of the policy group. The name must be from 1 to 128 characters in length.|Enter a policy group name.|
    |**VPC**|The VPC network to which the policy group is applied.|In the **VPC** drop-down list, select a VPC network . **Note:** You can select only one VPC network.

 |
    |**Instance ID**|The IDs of instances in the selected VPC network.|In the **Instance ID** drop-down list, select instance IDs. **Note:** You can select multiple instance IDs.

 |
    |**Description**|A description of the policy group. The description must be from 2 to 256 characters in length.|Enter a description of the policy group.|
    |**Template**|The policy group template.|In the **Template** drop-down list, select a template. The templates are as follows:     -   default-accept-login: Allow all inbound traffic that passes through port 22 and port 3389 by default.
    -   default-drop-all: Deny all traffic in the policy group by default.
    -   default-accept-all: Allow all traffic in the policy group by default.
 |

4.  Click **Submit**.

    You can locate the new policy group on the Internal Firewall page, and **configure**, **publish**, **modify**, or **delete** this policy group.

    **Note:** You can modify or delete a policy group. When you modify a policy group, you can only modify the related instances and the policy group description. After you delete a policy group, the access control policies between ECS instances in this policy group are automatically deleted and become invalid.

5.  Click **Configure Policy** in the **Actions** column to create access control policies.

    **Note:** You can create multiple policies in a policy group. By default, you can create up to 100 policy groups and 100 policies. If you want to create more policies than allowed, we recommend that you delete unnecessary policies or submit a ticket for technical support.

    ![配置策略](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21269/156897215611763_en-US.png)

6.  On the Policies page, click the **Inbound** or **Outbound** tab, and click **Create Policy** in the upper-right corner.

    ![管理策略](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21269/156897215611764_en-US.png)

7.  In the Create Policy dialog box, configure the policy.

    ![配置策略参数](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21269/156897215611765_en-US.png)

    The policy configuration items are as follows:

    |Item|Description|Configuration note|
    |----|-----------|------------------|
    |**Network Type**|The type of the network to which this policy is applied.|The default value is Internal, indicating that the policy is applied to traffic between ECS instances.|
    |**Direction**|The direction of traffic controlled by this policy.|Options:     -   Inbound: Apply the policy to traffic from other instances to the specified instance.
    -   Outbound: Apply the policy to traffic from the specified instance to other instances.
 |
    |**Policy Type**|Indicates whether to allow or deny the traffic passing through the internal firewall.|Options:     -   Allow: Allow the traffic between ECS instances.
    -   Deny: Deny the traffic between ECS instances.
 |
    |**Protocol Type**|The protocol of the traffic.|In the **Protocol Type** dialog box, select a protocol. Options:     -   TCP
    -   UDP
    -   ICMP
    -   ANY indicates any protocol. You can select ANY if you do not know which protocol is used.
 |
    |**Port Range**|The ports that are controlled by this policy.|Enter a port range. For example, 22/22.|
    |**Priority**|The priority of this policy.|Enter a priority number. **Note:** The priority number must be an integer from 1 to 100. If two policies have the same priority number, the **Deny** policy has the higher priority. If two **Allow** policies have the same priority number, both policies take effect at the same time.

 |
    |**Source Type**|The type of the traffic source controlled by this policy.|Options:     -   CIDR Block: The policy controls the traffic from a CIDR block.
    -   Policy Group: The policy controls the traffic from multiple ECS instances in a policy group.
    -    **Note:** For a policy created in the ECS security group module, you cannot select Policy Group as the source type.

 |
    |**Source**|The traffic source controlled by this policy. Enter a CIDR block or addresses of instances in a policy group.|Specify the traffic source based on the selected **source type**.     -   If the source type is set to CIDR Block, enter a CIDR block. You can specify only one CIDR block.
    -   If the source type is set to Policy Group, click the **Source** drop-down list, and select a policy group. This sets multiple instances in the specified policy group as the traffic source.

**Note:** You can select only one policy group as the **source**.

 |
    |**Destination**|The destination of the traffic.|Options:     -   All ECS Instances: Apply this policy to all ECS instances.
    -   CIDR Block: Specify an IP address or a CIDR block. The policy is applied to the traffic received by the specified addresses.
 |
    |**Description**|A description of the policy.|Enter a policy description. The description must be from 2 to 256 characters in length.|

8.  Click **Submit**.

    On the Policies page, you can view, modify, or delete the inbound or outbound policies.

    ![编辑删除](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21269/156897215647929_en-US.png)

    **Note:** After you delete a policy, the traffic control rule specified in this policy becomes invalid. After you delete a policy, you can still view this policy in the list but cannot perform any operation on it.

9.  On the Internal Firewall page, find the policy group to be applied. Click **Publish** in the **Actions** column. The policies take effect and are synchronized to the ECS security group module.

    ![发布](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21269/156897215647931_en-US.png)

    **Note:** To apply a policy and synchronize it to the ECS security group module, you must publish it first. To view the policies that are created on the Internal Firewall page in Cloud Firewall and synchronized to the ECS security group module, log on to the ECS console, and choose **Security Groups** \> **Security Groups**.

    ![安全组](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21269/156897215747930_en-US.png)


## Differences between the internal firewall and ECS security groups {#section_r21_d8e_czu .section}

The internal firewall in Cloud Firewall can control the traffic between ECS instances.

For more information about the differences between the internal firewall and ECS security groups, see[Differences between Cloud Firewall and Security groups](../../../../reseller.en-US/FAQ/Differences between Cloud Firewall and Security groups.md#)


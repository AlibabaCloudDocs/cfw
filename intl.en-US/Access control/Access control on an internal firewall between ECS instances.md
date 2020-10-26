# Access control on an internal firewall between ECS instances

Internal firewalls can control inbound and outbound traffic between ECS instances to block unauthorized access. The access control policies you configured and published for internal firewalls in the Cloud Firewall console are synchronized to ECS security groups.

Access control policies for internal firewalls outperform rules of ECS security groups in the following aspects:

-   You can publish multiple policies at a time.
-   If no policy is set to allow in a policy group, the ECS instances in the policy group cannot communicate with each other.
-   Access control policies can be set to monitor mode.
-   Cloud Firewall creates security groups based on application groups.
-   You can manage access control policies in the Cloud Firewall console without the need to switch between different regions of ECS instances.

By default, you can create up to 100 policy groups and 100 policies in each group. The policies include those synchronized from ECS security groups to Cloud Firewall and those created in the Cloud Firewall console. If you need more policies, we recommend that you delete unnecessary policies in time or configure access control policies for VPC firewalls.

**Note:** For information about the differences between internal firewalls and ECS security groups, see [What are the differences between Cloud Firewall and ECS security groups?](/intl.en-US/FAQ/What are the differences between Cloud Firewall and ECS security groups?.md).

Before you configure access control policies for an internal firewall, you must create a policy group, which contains default access control policies. Then, you can configure fine-grained inbound and outbound access control policies in the policy group. After you configure access control policies in the policy group, you must publish the policies, so that they can be synchronized to ECS security groups and take effect. The procedure consists of three steps:

1.  [Create a policy group](#section_9av_68m_tlu).
2.  [Configure a policy in a policy group](#section_pcz_vbn_299).
3.  [Publish a policy in a policy group](#section_y7n_b3v_00e).

## Policy group types

Policy groups are classified into common and enterprise policy groups. The following table describes the differences between the two policy group types.

|Policy group type|Supported policy|Policy priority|Scenario|
|:----------------|----------------|:--------------|:-------|
|Common policy group|-   Default policies, including:
    -   **default-accept-login**: allows inbound traffic destined for TCP ports 22 and 3389 and all outbound traffic.
    -   **default-accept-all**: allows all inbound and outbound traffic.
    -   **default-drop-all**: denies all inbound and outbound traffic.
-   Custom policies

|The default priority is 1. You can change the priority.The priority ranges from 1 to 100. A smaller value indicates a higher priority.

|Business that requires fine-grained network control on a moderate number of network connections.|
|Enterprise policy group|-   Default allow policies, including:
    -   **default-accept-login**: allows inbound traffic destined for TCP ports 22 and 3389 and all outbound traffic.
    -   **default-accept-all**: allows all inbound and outbound traffic.
-   Custom policies

|The priority is 1 and cannot be changed.|Business that requires efficient O&M.|

## Create a policy group

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext).

2.  In the left-side navigation pane, choose **Security Policies** \> **Access Control**.

3.  On the Access Control page, click the **Internal Firewall** tab. Then, click **Create Policy Group** in the upper-right corner.

4.  In the Create Policy Group dialog box, configure the required parameters.

    ![Create Policy Group](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/9347249851/p11762.png)

    |Parameter|Description|
    |---------|-----------|
    |**Policy Group Type**|Valid values:     -   **Common Policy Group**: suitable for business that requires fine-grained network control on a moderate number of network connections.
    -   **Enterprise Policy Group**: suitable for business that requires efficient O&M. |
    |**Name**|Enter an name of the policy group. We recommend that you enter an informative name for easy identification. |
    |**VPC**|Select a VPC to which you want to apply the policy group from the **VPC** drop-down list. **Note:** A policy group can be applied to only one VPC. |
    |**Instance ID**|Select one or more ECS instances to which you want to apply the policy group from the **Instance ID** drop-down list. **Note:** The Instance ID drop-down list only contains ECS instances within the selected **VPC**. |
    |**Description**|Enter a description for the policy group.|
    |**Template**|Select a template that you want to use from the **Template** drop-down list.     -   **default-accept-login**: allows inbound traffic destined for TCP ports 22 and 3389 and all outbound traffic.
    -   **default-accept-all**: allows all inbound and outbound traffic.
    -   **default-drop-all**: denies all inbound and outbound traffic.

**Note:** Enterprise policy groups do not support the **default-drop-all** template. |

5.  Click **Submit**.

    The created policy group is displayed on the Internal Firewall tab. You can perform the following operations on the policy group:

    -   **Configure Policy**: Customize policies to implement fine-grained access control.
    -   **Publish**: Synchronize the access control policies in the policy group to ECS security groups.
    -   **Modify**: Change the ECS instances specified in the policy group and modify the policy group description.
    -   **Delete**: Delete the policy group.

        **Warning:** After you delete a policy group, its access control policies are also deleted. Exercise caution when you perform this operation.

        If you want to delete policy groups that are no longer required, set the policy group source to **Custom** to obtain all custom policy groups and determine whether to delete them.

        ![Filter custom policy groups](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/9347249851/p94768.png)


## Configure a policy in a policy group

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext).

2.  In the left-side navigation pane, choose **Security Policies** \> **Access Control**.

3.  On the Access Control page, click the **Internal Firewall** tab, find the required policy group, and then click **Configure Policy** in the Actions column.

4.  On the Configure Policy page, click **Create Policy** in the upper-right corner.

5.  In the Create Policy dialog box, configure the required parameters.

    ![Parameters used to create a policy](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/9347249851/p11765.png)

    |Parameter|Description|
    |---------|-----------|
    |**Network Type**|The default value is **Internal** and cannot be changed. This value indicates that the policy is applied to ECS instances.|
    |**Direction**|Valid values:     -   **Inbound**: traffic from other ECS instances to the ECS instances specified in the policy group.
    -   **Outbound**: traffic from the ECS instances specified in the policy group to other ECS instances. |
    |**Policy Type**|Valid values:     -   **Allow**: allows traffic that hits the policy.
    -   **Deny**: denies traffic that hits the policy. If the traffic is denied, data packets are discarded without responses. If two policies have the same configuration but different policy types, the policy whose type is **Deny** takes effect.****

**Note:** Enterprise policy groups do not support the **Deny** policy type. |
    |**Protocol Type**|Select a traffic protocol from the **Protocol Type** drop-down list.     -   **TCP**
    -   **UDP**
    -   **ICMP**
    -   **ANY** \(Select ANY if you do not know the traffic protocol.\) |
    |**Port Range**|The destination port of traffic controlled by the policy, for example, 22/22.|
    |**Priority**|The priority of the policy. The priority must be an integer within the range of 1 to 100. A smaller value indicates a higher priority. Different policies can have the same priority. If an allow policy and a deny policy have the same priority, the **deny** policy takes precedence.

**Note:** The priorities of policies in an enterprise policy group are fixed to **1** and cannot be changed. The value 1 indicates the highest priority. |
    |**Source Type** and **Source**|For an **inbound** policy, configure the source type and source of traffic. Valid source types:

    -   **CIDR Block**

If you select this type, you can enter only one CIDR block as the traffic source.

    -   **Policy Group**

If you select this type, you must select a policy group as the traffic source. Traffic from all ECS instances in the policy group is controlled.

**Note:** Enterprise policy groups do not support the **Policy Group** type. |
    |**Destination**|For an **inbound** policy, select the destination of traffic. Valid values:     -   **All ECS Instances**: all ECS instances specified in the policy group.
    -   **CIDR Block**: If you select this option, you must enter a destination CIDR block. The ECS instances that correspond to this CIDR block are the destination of traffic. |
    |**Select Source**|For an **outbound** policy, select the source of traffic. Valid values:    -   **All ECS Instances**: all ECS instances specified in the current policy group.
    -   **CIDR Block**: If you select this option, you must enter a destination CIDR block. The ECS instances that correspond to this CIDR block are the source of traffic. |
    |**Destination Type** and **Destination**|For an **outbound** policy, configure the destination type and traffic destination. Valid destination types:

    -   **CIDR Block**

If you select this option, you can enter only one CIDR block as the traffic destination.

    -   **Policy Group**

If you select this option, you must select a policy group. Traffic whose destination is an ECS instance specified in the policy group is controlled.

**Note:** Enterprise policy groups do not support the **Policy Group** option. |
    |**Description**|Enter a description for the policy.|

6.  Click **Submit**.

    The created policy is displayed in the policy list. You can **edit** or **delete** policies.

    **Warning:** After you delete a policy, its access control configuration becomes invalid. Exercise caution when you delete a policy. A deleted policy is retained in the list, but you cannot perform operations on it.


## Publish a policy in a policy group

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext).

2.  In the left-side navigation pane, choose **Security Policies** \> **Access Control**.

3.  On the Access Control page, click the **Internal Firewall** tab, find the required policy group, and then click **Publish** in the **Actions** column.

    ![Publish policies](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/0447249851/p77669.png)

4.  In the **Publish Policy** dialog box, confirm **policy changes**, set **Remarks**, and then click **OK**.

    ![Publish policies](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/0447249851/p94777.png)

    The policies take effect on ECS security groups after you publish them. You can log on to the ECS console and choose **Network & Security** \> **Security Groups** to view the policies you published in the Cloud Firewall console. The default policy name is **Cloud\_Firewall\_Security\_Group**.

    ![ECS security groups](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/0447249851/p77670.png)


## Video tutorial on how to configure an internal firewall



## References

[Why does Cloud Firewall provide three types of firewalls?](/intl.en-US/FAQ/Protection scope of Cloud Firewall.md)

[What are the differences between Cloud Firewall and ECS security groups?](/intl.en-US/FAQ/What are the differences between Cloud Firewall and ECS security groups?.md)

[t275154.md\#]()


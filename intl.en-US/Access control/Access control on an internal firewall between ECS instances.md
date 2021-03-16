# Access control on an internal firewall between ECS instances

Internal firewalls can control inbound and outbound traffic between ECS instances to block unauthorized access. The access control policies you configured and published for internal firewalls in the Cloud Firewall console are synchronized to ECS security groups.

Access control policies for internal firewalls outperform rules of ECS security groups in the following aspects:

-   You can publish multiple policies at a time.
-   If no policy is set to allow in a policy group, the ECS instances in the policy group cannot communicate with each other.
-   You can set access control policies to the monitor mode.
-   Cloud Firewall creates security groups based on application groups.
-   You can manage access control policies in the Cloud Firewall console without the need to switch between different regions of ECS instances.

By default, you can create up to 100 policy groups and 100 policies in each group. The policies include those synchronized from ECS security groups to Cloud Firewall and those created in the Cloud Firewall console. If you need more policies, we recommend that you delete unnecessary policies in time or configure access control policies for VPC firewalls.

**Note:** For information about the differences between internal firewalls and ECS security groups, see [What are the differences between Cloud Firewall and ECS security groups?](/intl.en-US/FAQ/What are the differences between Cloud Firewall and ECS security groups?.md).

Before you configure access control policies for an internal firewall, you must create a policy group, which contains default access control policies. Then, you can configure fine-grained inbound and outbound access control policies in the policy group. After you configure access control policies in the policy group, you must publish the policies, so that they can be synchronized to ECS security groups and take effect. The procedure consists of three steps:

1.  [Create a policy group](#section_9av_68m_tlu).
2.  [Configure a policy in a policy group](#section_pcz_vbn_299).
3.  [Publish a policy in a policy group](#section_y7n_b3v_00e).

## Policy group types

Policy groups are classified into common and enterprise policy groups. The following list describes the scenarios of the two policy groups.

-   A common policy group takes effect on the basic security groups of ECS instances. It functions as a virtual firewall to monitor connection status and filter data packets, and can be used to isolate security domains on the cloud. You can configure access control policies to allow or deny inbound and outbound traffic between ECS instances in a common policy group.
-   An enterprise policy group takes effect on the advanced security groups of ECS instances. It supports more ECS instances than a common policy group. You can configure access control policies for a large number of private IP addresses. Enterprise policy groups are ideal for enterprises that require efficient O&M on large-scale networks.

The following table describes the differences between the two policy groups.

|Feature|Common policy group|Enterprise policy group|
|-------|-------------------|-----------------------|
|VPC|Supported|Supported|
|Policy priority configuration|Supported|Not supported|
|Authorization of other policy groups|Supported|Not supported|
|Custom policy configuration to allow traffic|Supported|Supported|
|Custom policy configuration to deny traffic|Supported|Not supported \(Enterprise policy groups deny all traffic by default.\)|
|Number of private IP addresses|2,000|65,536|
|Communication between ECS instances in the same policy group|Not supported \(You must manually create policies to **allow** the communication.\)|Not supported \(You must manually create policies to **allow** the communication.\)|

## Create a policy group

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext)[Cloud Firewall console](https://partners-yundun.console.aliyun.com/?p=cfwnext).

2.  In the left-side navigation pane, click **Access Control**.

3.  On the Access Control page, click the Internal Firewall tab.

4.  In the upper-right corner of the Internal Firewall tab, click **Create Policy Group**.

5.  In the Create Policy Group dialog box, configure the following parameters.

    ![Create Policy Group](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/9347249851/p11762.png)

    |Parameter|Description|
    |---------|-----------|
    |**Policy Group Type**|Select a type for the policy group. Valid values:     -   **Common Policy Group**: suitable for business that requires fine-grained network control on a moderate number of network connections.
    -   **Enterprise Policy Group**: suitable for business that requires efficient O&M. |
    |**Name**|Enter a name for the policy group. We recommend that you enter an informative name for easy identification. |
    |**VPC**|Select a VPC to which you want to apply the policy group from the **VPC** drop-down list. **Note:** A policy group can be applied to only one VPC. |
    |**Instance ID**|Select one or more ECS instances to which you want to apply the policy group from the **Instance ID** drop-down list. **Note:** The Instance ID drop-down list only contains ECS instances within the selected **VPC**. |
    |**Description**|Enter a description for the policy group.|
    |**Template**|Select a template that you want to use from the **Template** drop-down list.     -   **default-accept-login**: allows inbound traffic destined for TCP ports 22 and 3389 and all outbound traffic.
    -   **default-accept-all**: allows all inbound and outbound traffic.
    -   **default-drop-all**: denies all inbound and outbound traffic.

**Note:** Enterprise policy groups do not support the **default-drop-all** template. |

6.  Click **Submit**.

    The created policy group is displayed on the Internal Firewall tab. You can perform the following operations on the policy group:

    -   **Configure Policy**: Customize policies to implement fine-grained access control.
    -   **Publish**: Synchronize the access control policies in the policy group to ECS security groups.
    -   **Modify**: Change the ECS instances specified in the policy group and modify the policy group description.
    -   **Delete**: Delete the policy group.

        **Warning:** After you delete a policy group, its access control policies become invalid. Exercise caution when you perform this operation. A deleted policy is retained in the list, but you cannot perform operations on it.

        If you want to delete policy groups that are no longer required, set the policy group source to **Custom** to obtain all custom policy groups and determine whether to delete them.

        ![Filter custom policy groups](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/9347249851/p94768.png)


## Configure a policy in a policy group

After you create a policy group, you must configure a policy for the policy group.

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext)[Cloud Firewall console](https://partners-yundun.console.aliyun.com/?p=cfwnext).

2.  In the left-side navigation pane, click **Access Control**.

3.  On the Access Control page, click the Internal Firewall tab.

4.  On the Internal Firewall tab, find the required policy group and click **Configure Policy** in the **Actions** column.

5.  In the upper-right corner of the Configure Policy page, click **Create Policy**.

6.  In the Create Policy dialog box, configure the following parameters.

    ![Create Policy dialog box](../images/p184097.png)

    |Parameter|Description|
    |---------|-----------|
    |**Network Type**|The default value is **Internal** and cannot be changed. This value indicates that the policy is applied to ECS instances.|
    |**Direction**|The direction of traffic to which the policy applies. Valid values:     -   **Inbound**: traffic from other ECS instances to the ECS instances specified in the policy group.
    -   **Outbound**: traffic from the ECS instances specified in the policy group to other ECS instances. |
    |**Policy Type**|The type of the policy. Valid values:     -   **Allow**: allows traffic that hits the policy.
    -   **Deny**: denies traffic that hits the policy. If the traffic is denied, data packets are discarded without responses. If two policies have the same configuration but different policy types, the policy whose type is **Deny** takes effect.

**Note:** Enterprise policy groups do not support the **Deny** policy type. |
    |**Protocol Type**|The protocol of traffic to which the policy applies. Valid values:     -   **TCP**
    -   **UDP**
    -   **ICMP**
    -   **ANY** \(If you do not know the traffic protocol, select ANY.\) |
    |**Port Range**|The destination port of traffic controlled by the policy. Example: 22/22.|
    |**Priority**|The priority of the policy. The priority must be an integer within the range of 1 to 100. A smaller value indicates a higher priority. Different policies can have the same priority. If an allow policy and a deny policy have the same priority, the **deny** policy takes precedence. |
    |**Source Type** and **Source**|The source of traffic. If you set Direction to **Inbound**, you must specify these parameters. You can specify Source based on the value of Source Type. Valid source types:

    -   **CIDR Block**

If you select this type, you must enter a source CIDR block in **Source**. You can enter only one CIDR block.

    -   **Policy Group**

If you select this type, you must select a policy group from the **Source** drop-down list as the traffic source. Traffic from all ECS instances in the policy group is controlled.

**Note:** Enterprise policy groups do not support the **Policy Group** type. |
    |**Destination**|The destination of traffic. If you set Direction to **Inbound**, you must specify this parameter. Valid values:     -   **All ECS Instances**: all ECS instances specified in the policy group.
    -   **CIDR Block**: If you select this option, you must enter a destination CIDR block. The ECS instances that correspond to this CIDR block are the destination of traffic. |
    |**Select Source**|The type of the traffic source. If you set Direction to **Outbound**, you must specify this parameter. Valid values:    -   **All ECS Instances**: all ECS instances specified in the current policy group.
    -   **CIDR Block**: If you select this option, you must enter a destination CIDR block. The ECS instances that correspond to this CIDR block are the source of traffic. |
    |**Destination Type** and **Destination**|The destination type and traffic destination. If you set Direction to **Outbound**, you must specify these parameters. Valid destination types:

    -   **CIDR Block**

If you select this type, you must enter a destination CIDR block. You can enter only one CIDR block.

    -   **Policy Group**

If you select this type, you must select a policy group. Traffic destined for all ECS instances in the policy group is controlled.

**Note:** Enterprise policy groups do not support the **Policy Group** type. |
    |**Description**|The description for the policy.|

7.  Click **Submit**.

    The created policy is displayed in the policy list. You can **edit** or **delete** policies.

    **Warning:** After you delete a policy, its access control configuration becomes invalid. Exercise caution when you delete a policy. A deleted policy is retained in the list, but you cannot perform operations on it.


## Publish a policy in a policy group

To apply a created policy, you must publish the policy. Then, the policy can control inbound or outbound traffic.

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext)[Cloud Firewall console](https://partners-yundun.console.aliyun.com/?p=cfwnext).

2.  In the left-side navigation pane, click **Access Control**.

3.  On the Access Control page, click the **Internal Firewall** tab, find the required policy group, and then click **Publish** in the **Actions** column.

    ![Publish policies](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/0447249851/p77669.png)

4.  In the **Publish Policy** dialog box, confirm **policy changes**, set **Remarks**, and then click **OK**.

    ![Publish policies](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/0447249851/p94777.png)

    The policies take effect on ECS security groups only after you publish them. You can log on to the ECS console and choose **Network & Security** \> **Security Groups** to view the policies you published in the Cloud Firewall console. By default, the policy that you create in the Cloud Firewall console is named **Cloud\_Firewall\_Security\_Group**.

    ![ECS security groups](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/0447249851/p77670.png)


## 主机边界防火墙配置视频教程



## References

[Why does Cloud Firewall provide three types of firewalls?](/intl.en-US/FAQ/Protection scope of Cloud Firewall.md)

[What are the differences between Cloud Firewall and ECS security groups?](/intl.en-US/FAQ/What are the differences between Cloud Firewall and ECS security groups?.md)

[t275154.md\#]()


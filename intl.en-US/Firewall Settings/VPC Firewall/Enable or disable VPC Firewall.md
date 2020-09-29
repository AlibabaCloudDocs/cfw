# Enable or disable VPC Firewall

The VPC Firewall feature can detect and collect statistics on traffic between connected VPCs. This feature helps you detect attacks and perform troubleshooting. You can enable or disable this feature in the Cloud Firewall console.

-   A Cloud Enterprise Network \(CEN\) or Express Connect instance is purchased and two VPCs have been connected by using the instance. For more information, see [Interconnect two VPCs under the same account](/intl.en-US/Peering connections/Interconnect two VPCs under the same account.md).
-   A VPC firewall is created. You must create a VPC firewall before you enable the VPC Firewall feature. For more information, see [Create a VPC firewall](/intl.en-US/Firewall Settings/VPC Firewall/Create a VPC firewall.md).

After the VPC Firewall feature is enabled, you can log on to the Cloud Firewall console and choose **Traffic Analysis** \> **VPC Access** in the left-side navigation pane to view information about traffic between VPCs.

After the VPC Firewall feature is enabled, a security group named Cloud\_Firewall\_Security\_Group and an allow policy appear on the **Security Groups** page of the [ECS console](https://ecs.console.aliyun.com/?securityGroup/region/cn-shenzhen#/securityGroup/region/cn-shenzhen). The allow policy is also referred to as an **authorization policy**, which is used to allow inbound traffic from a VPC firewall to ECS instances. To go to the Security Groups page, log on to the ECS console and click **Network & Security** in the left-side navigation pane.

**Note:** Do not delete the security group Cloud\_Firewall\_Security\_Group and the allow policy. Otherwise, the inbound traffic from the VPC firewall to ECS instances cannot be protected by the VPC firewall.

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext).

2.  In the left-side navigation pane, click **Firewall Settings**.

3.  On the Firewall Settings page, click the **VPC Firewall** tab.

4.  On the VPC Firewall tab, click the **Express Connect** or **CEN** tab based on your VPC connection type.

5.  Find the required Cloud Firewall instance and turn on or turn off **Firewall Settings**.

    If a large number of Cloud Firewall instances exist, we recommend that you use the filter or search function to find the required Cloud Firewall or VPC.

    ![Firewall Settings](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/8463068951/p59034.png)

6.  Wait for a few seconds until the VPC Firewall feature is enabled or disabled.


-   After you turn on Firewall Settings, **Firewall Status** becomes **Enabling**. If Firewall Status becomes **Enabled**, the VPC Firewall feature is enabled.
-   After you turn off Firewall Settings, **Firewall Status** becomes **Disabling**. If Firewall Status becomes **Disabled**, the VPC Firewall feature is disabled.

After the VPC Firewall feature is enabled, traffic between VPCs is collected and analyzed. You can view the statistics and analysis results on the VPC Access page. To go to the VPC Access page, log on to the Cloud Firewall console, and choose **Traffic Analysis** \> **VPC Access** in the left-side navigation pane. For more information about VPC access traffic, see [VPC access](/intl.en-US/Traffic Analysis/VPC access.md).


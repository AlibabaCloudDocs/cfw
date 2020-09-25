# Check security group rules

Improper configuration of security group rules may bring security risks. The security check function of Cloud Firewall allows you to check risky security group rules for your ECS instances and provides troubleshooting suggestions. This improves security and efficiency of security groups. This topic describes how to use the security check function in the Cloud Firewall console.

The Premium Edition, Enterprise Edition, and Ultimate Edition of Cloud Firewall support the security check function.

A security group is a virtual firewall that is used to protect ECS instances in Alibaba Cloud. The security check function supports both basic and advanced security groups. For more information, see [Overview](/intl.en-US/Security/Security groups/Overview.md).

For information about the check items, see [t1917836.md\#section\_n2a\_ed3\_vqv](/intl.en-US/Precautions/Security group checks.md).

## Procedure

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext).

2.  In the left-side navigation pane, click **Toolbox**.

3.  In the left-side navigation page, click Toolbox. In the **Security Check** section, click **Go to check**.

    ![Security Check](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/9951488951/p140304.png)

4.  On the Security Check page, click **Obtain Latest Check Results**.

    The check may take 1 to 5 minutes.

    ![Security Check](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/8104649951/p133949.png)

    **Note:** The latest check results are obtained based on the static analysis of security group rules and may not cover all port risks. You can view complete check results about port exposure on the [t64125.md\#](/intl.en-US/Traffic Analysis/Internet access.md) page.

5.  In the **Check Result Details** section, view the details of detected security group risks.

    ![](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/8104649951/p133950.png)

    You can view the **Risk Level**, **Check Item**, **Risky Security Groups/Servers**, and **Check Item Status** of a security group.

    **Note:** You can turn on or off **Check Item Status**.

6.  Fix the issue of a check item.

    1.  Find the target check item, and click **View Details** in the Actions column.

        You can also click the number in the **Risky Security Groups/Servers** column to go to the Details page.

    2.  On the Details page, find the target security group, and click **Fix Issue** in the Actions column.

        ![Details](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/8104649951/p133951.png)

        You can also click the security group ID in the **Risky Security Group ID/Name** column to go to the Security Groups page of the [ECS console](https://ecs.console.aliyun.com) and fix the issue.

        **Note:** Improper configuration of security group rules may bring severe risks. The Details page provides **suggestions** to fix the issue. We recommend that you modify the risky security group rules based on the **suggestions**.


## Related operations

If you use the Free Edition of Cloud Firewall, after you click **Fix Issue**, you can select **Upgrade now** or **Manually fix issue**.

![Upgrade your Cloud Firewall to intelligently fix the issues and get advanced features](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/0061488951/p140430.png)

-   **Upgrade now**: You can purchase the Premium Edition or a higher edition and use the **Security Check** function to fix risky security group rules. We recommend that you select this option. You can use Cloud Firewall to centrally manage access control policies of security groups and public IP addresses. This reduces assets exposure and improves efficiency of security management.
-   **Manually fix issue**: You are redirected to the Security Groups page of the [ECS console](https://ecs.console.aliyun.com). You can manually fix the risky security group rules. For more information, see [Modify security group rules](/intl.en-US/Security/Security groups/Manage security group rules/Modify security group rules.md).


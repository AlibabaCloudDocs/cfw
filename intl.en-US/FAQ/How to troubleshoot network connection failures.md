# How to troubleshoot network connection failures

## Symptom

After you enable the Clouf Firewall, the following issues may occur:

1.  You cannot log on to your ECS instance.
2.  You cannot access the service running on your instance.
3.  Your ECS instances cannot access external networks.

## Troubleshoot the Internet firewall

-   Verify the Internet firewall is enabled for your asset. If it is disabled, skip this step.![](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/9681329951/p38808.png)
-   Check the access records on the **Logs** \> **Access Log** tab page.![](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/9681329951/p38809.png)
    -   If no relevant record is found, this means that the request is dropped before it reaches the firewall.
    -   If you find the record of the request and the action is **Discard**, this means that the request is blocked by the internal firewall. Find the relevant event on the **Logs** \> **Event Log** tab page, and then confirm the module that performs the **Discard** action according to the information in the **Criterion** column.![](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/9681329951/p38810.png)
        -   If the **Criterion** shows **Access Control**, then you must check the configuration of the relevant access control policy.
        -   If the column shows **Basic Protection**, **Virtual Patches**, or **Threat Intelligence**, then you must go to the **Security Policies** \> **Intrusion Prevention** tab page to disable the relevant module.
    -   If you find the record of the request and the action is **Allow** or **Monitor**, this means that the request is not blocked by the Internet firewall. You must troubleshoot the internal firewall and security groups.

## Troubleshoot the internal firewall and security group

Log on to the [ECS console](https://ecs.console.aliyun.com/#/home), click the ECS instance where the connection failure occurs, and click **Security Groups** in the left-side navigation pane. Verify the **Action** of the rules in the security group is set to **Allow**.

![](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/9681329951/p38814.png)

If the issue still exists, [submit a ticket](https://selfservice.console.aliyun.com/ticket/category/cfw/today).


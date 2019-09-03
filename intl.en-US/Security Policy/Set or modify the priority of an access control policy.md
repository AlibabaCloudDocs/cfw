# Set or modify the priority of an access control policy {#concept_kws_vx2_nfb .task}

Each access control policy in Cloud Firewall is automatically assigned with a default priority. You can click **Move** in the **Actions** column to modify the priority of a policy.

The priorities of policies determine the order in which the policies take effect. Each access control policy has a unique priority. The number 1 indicates the highest priority.

The larger the priority number, the lower the priority.

The maximum number of policies varies with the edition of Cloud Firewall. Therefore, the priority number range also changes with the Cloud Firewall edition.

-   In Pro Edition, you can configure up to 1,000 access control policies. The priority ranges from 1 to 1,000.
-   In Enterprise Edition, you can configure up to 2,000 access control policies. The priority ranges from 1 to 2,000.
-   In Ultimate Edition, you can configure up to 5,000 access control policies. The priority ranges from 1 to 5,000.

**Note:** A new policy has the lowest priority by default. That is, this policy is assigned with the largest priority number.

## Procedure {#section_mgt_1y2_nfb .section}

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext#/overview).
2.  In the left-side navigation pane, choose **Security Policies** \> **Access Control** \> **Internet Firewall**.
3.  On the **Outbound Policies** or **Inbound Policies** tab page, locate the access control policy of which the priority needs to be modified. Click **Move** in the **Actions** column.

    ![Move](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/24037/156749177313959_en-US.png)

4.  Modify the priority in the displayed dialog box.

    ![Priority](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/24037/156749177313960_en-US.png)

5.  Click **OK**.

**Note:** After you modify the priority of a policy, the priorities of policies with lower priorities decrease accordingly.


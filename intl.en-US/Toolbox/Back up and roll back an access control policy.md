# Back up and roll back an access control policy

Cloud Firewall allows you to back up and roll back access control policies for both inbound and outbound traffic on the Internet firewall. This ensures that your access control policies can be restored to a normal status in a timely manner.

You can roll back access control policies in Cloud Firewall Enterprise and Ultimate Editions, but not in the Premium Edition.

Each Alibaba Cloud account can have up to 12 policy backups at a time. If you already have 12 policy backups, you must delete a backup before you create another backup. For information about how to delete a backup, see [What to do next](#section_vli_7rh_iue). There is no limit to the number of times you can create backups in a day.

Rolling back an access control policy that is in use replaces it with a policy that you have backed up. To ensure that access control policies function correctly, we recommend that you follow these steps to roll back a policy that is in use:

1.  Back up the policy.
2.  Roll back the policy during off-peak hours with all firewall switches turned off.
3.  After the policy is rolled back, turn on the firewall switches one by one and verify that your business access is normal.

**Note:** Only access control policies of the Internet firewall can be rolled back. Those of VPC firewalls and internal firewalls cannot be rolled back.

## Back up an access control policy

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext).

2.  In the left-side navigation pane, click **Toolbox**.

3.  On the Toolbox page, click **View Backup**.

    ![Roll back an access control policy](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/2893068951/p113734.png)

4.  On the Policy Backup and Rollback page, click **New Backup**.

    ![Policy Backup and Rollback](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/2893068951/p113737.png)

5.  In the Backup Policy dialog box, enter a description of the policy backup and click **OK**.

    ![Backup Policy dialog box](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/2893068951/p113740.png)

    The following table describes the parameters for creating a backup.

    |Parameter|Description|
    |---------|-----------|
    |**Backup Time**|The time the access control policy for both inbound and outbound traffic on the Internet Firewall is backed up.|
    |**Description**|The description of the policy backup. **Note:** You can enter a maximum of 256 characters for the description. You can determine which policy to roll back based on the description and backup time. Therefore, enter an informative description. |
    |**Policies**|The number of access control policies for both inbound and outbound traffic on the Internet Firewall created by the current Alibaba Cloud account.|

    You can view the new backup on the Policy Backup and Rollback page.

    ![Policy Backup and Rollback](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/2893068951/p113745.png)


## Roll back an access control policy

Before you roll back an access control policy, ensure that a backup file is available for the rollback.

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext).

2.  In the left-side navigation pane, click **Toolbox**.

3.  On the Toolbox page, click **View Backup**.

    ![Roll back an access control policy](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/2893068951/p113734.png)

4.  On the Policy Backup and Rollback page, find the policy that you want to roll back and click **Use Backup** in the Actions column.

    ![Use Backup](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/2893068951/p113781.png)

    **Note:**

    -   The policy is rolled back in seconds.
    -   If the number of policies under your Alibaba Cloud account is large or if many users are rolling back policies at the same time, a timeout error may occur. We recommend that you only use your Alibaba Cloud account yourself to roll back policies. If a policy rollback times out, the system displays a message. Follow the prompts to resolve the issue.
    -   If a policy rollback fails, the access control policy remains unchanged.

## What to do next

To delete a policy backup, follow these steps: Navigate to the Policy Backup and Rollback page, find the target policy, and click **Delete Backup** in the Actions column.


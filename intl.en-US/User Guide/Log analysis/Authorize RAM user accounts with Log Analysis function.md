# Authorize RAM user accounts with Log Analysis function {#task_oy2_sj4_hhb .task}

If you want to use Cloud Firewall's Log Analysis function with a RAM user account, you must first use your Alibaba Cloud account to authorize this RAM user account with the Log Analysis functions of Cloud Firewall.

The following permissions are required for enabling and using Cloud Firewall's Log Analysis function.

|Operations|Required account|
|:---------|:---------------|
|Enable the Log Analysis function. You only need to perform this operation once.|Alibaba Cloud account|
|Authorize Cloud Firewall to write the log data into the dedicated Logstore of Log Analysis in real time. You only need to perform this operation once.| -   Alibaba Cloud account
-   A RAM user account with `AliyunLogFullAccess` permission
-   A RAM user account with the customized permission of log writing

 |
|Use the Log Analysis function.| -   Alibaba Cloud account
-   A RAM user account with `AliyunLogFullAccess` permission
-   A RAM user account with the customized permissions

 |

You can grant permissions to a RAM user account as needed.

|Scenarios|Grant a RAM user account permissions|Procedure|
|---------|------------------------------------|---------|
|Grant a RAM user account full permission to Log Service.|The `AliyunLogFullAccess` policy specifies full permission to Log Service.|For more information, see [RAM user management](../../../../reseller.en-US/Access control RAM/Grant a RAM user the permissions to access Log Service.md#).|
|After you use your Alibaba Cloud account to enable the Cloud Firewall log analysis function and complete the authorization, grant the RAM user account the permission to view logs.|The `AliyunLogReadOnlyAccess` policy specifies the read-only permission.|For more information, see [RAM user management](../../../../reseller.en-US/Access control RAM/Grant a RAM user the permissions to access Log Service.md#).|
|Grant the RAM user account the permissions to enable and use the Cloud Firewall log analysis function. Do not grant other permissions to Log Service.|Create a custom authorization policy, and apply the policy to the RAM user account.|For more information, see the following procedure.|

1.  Log on to the [RAM console](https://partners-intl.console.aliyun.com/#/ram).
2.  Open the Create Custom Policy tab page on the Policies page.
3.  In the upper-right corner of the page, click **Create Authorization Policy**.
4.  Click **Blank Template**, enter the **Policy Name** and the following **Policy Content** into this template. 

    **Note:** Replace `${Project}` and `${Logstore}` in the following policy with the Log Service Project name and Logstore name dedicated for Cloud Firewall, respectively.

    ``` {#codeblock_7ku_kl4_tvp}
    
    
    
    {
      "Version": "1",
      "Statement": [
          {
          "Action": "log:GetProject",
          "Resource": "acs:log:*:*:project/${Project}",
          "Effect": "Allow"
        },
        {
          "Action": "log:CreateProject",
          "Resource": "acs:log:*:*:project/*",
          "Effect": "Allow"
        },
        {
          "Action": "log:ListLogStores",
          "Resource": "acs:log:*:*:project/${Project}/logstore/*",
          "Effect": "Allow"
        },
        {
          "Action": "log:CreateLogStore",
          "Resource": "acs:log:*:*:project/${Project}/logstore/*",
          "Effect": "Allow"
        },
        {
          "Action": "log:GetIndex",
          "Resource": "acs:log:*:*:project/${Project}/logstore/${Logstore}",
          "Effect": "Allow"
        },
        {
          "Action": "log:CreateIndex",
          "Resource": "acs:log:*:*:project/${Project}/logstore/${Logstore}",
          "Effect": "Allow"
        },
        {
          "Action": "log:UpdateIndex",
          "Resource": "acs:log:*:*:project/${Project}/logstore/${Logstore}",
          "Effect": "Allow"
        },
        {
          "Action": "log:CreateDashboard",
          "Resource": "acs:log:*:*:project/${Project}/dashboard/*",
          "Effect": "Allow"
        },
        {
          "Action": "log:UpdateDashboard",
          "Resource": "acs:log:*:*:project/${Project}/dashboard/*",
          "Effect": "Allow"
        },
        {
          "Action": "log:CreateSavedSearch",
          "Resource": "acs:log:*:*:project/${Project}/savedsearch/*",
          "Effect": "Allow"
        },
        {
          "Action": "log:UpdateSavedSearch",
          "Resource": "acs:log:*:*:project/${Project}/savedsearch/*",
          "Effect": "Allow"
        }
      ]
    }
    ```

    ![策略](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/154325/156586037343270_en-US.png)

5.  Click **Create Authorization Policy**.
6.  Go to the Users page, locate the RAM user account, and click **Authorize**.
7.  Select the custom authorization policy that you created, and then click **OK**. The authorized RAM user account then can enable and use the Log Analysis function. However, this RAM user account is not authorized to use other functions of Log Service.


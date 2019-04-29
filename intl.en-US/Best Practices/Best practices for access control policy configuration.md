# Best practices for access control policy configuration {#concept_w5r_hnn_vgb .concept}

This topic describes the best practice for configuring access control policy.

## How network access control works {#section_upx_pnn_vgb .section}

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/126848/155653730338982_en-US.png)

-   **Internet Firewall**:
    -   How it works: Internet Firewall controls the traffic between internet and cloud assets.
    -   Portal: **Outbound Policies** and **Inbound Policies** in **Security Policies** \> **Access Control** tab page.
    -   Default Policy: Both inbound and outbound traffic are allowed to pass through by default.
-   **Internal firewall/security group**:
    -   How it works: A Security Group \(also a virtual internal firewall\) is deployed on each ECS instance to control the internal network traffic of ECS instances.
    -   Portal: **Security Policies** \> **Access Control** \> **Internal Firewall**.

        **Note:** Only Cloud Firewall Enterprise/Flagship edition supports this function. Cloud Firewall Pro users must configure the security groups in ECS console.

    -   Default policy: Only outbound traffic is allowed to pass through by default, and inbound traffic is blocked.

## Procedure {#section_b3c_qnn_vgb .section}

1.  Tune the configuration of Inbound policies of Internet Firewall.

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/126848/155653730438987_en-US.png)

    When you perform this task, follow these guidelines:

    -   **Allow all the necessary ports** 

        For ports that must be opened to the Internet, such as HTTP port 80 and HTTPS port 443, set these ports as **Allow** in Inbound Policies configuration.

    -   **Strictly allow some ports in high risk** 

        For ports that are used only for operations and maintenance, and ports that may pose high risks, such as SSH port 22 and MySQL port 3306, allow them to communicate with the necessary source IP. You can use the address book function to simplify your configuration.

    -   **Deny the risky ports** 

        For the risky ports, such as SMB port 445, set them as **Deny**in access control policy configuration.

    -   Create a policy with both the source and destination set to **Any**, and then set the policy action to **Monitor**. After this policy is created, check the **access log** to make sure that the network traffic is received, and then change the policy action to **Deny**.
2.  Set all the the inbound traffic of Internal Firewall to **Allow**.

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/126848/155653730438988_en-US.png)

    When you perform this task, follow these guidelines:

    Go to the **Security Policies** \> **Access Control** \> **Internal Firewall** tab page, select the policy group that contains all test ECS instances, create a policy to allow the network traffic sent to the test ECS instances from 0.0.0.0./0. By default, the internal firewall and security group forbid all inbound traffic to pass through. Therefore, you must create a policy to allow the inbound traffic to pass through.

     **** 

    **Note:** The **Security Policies** \> **Access Control** \> **Internal Firewall** tab page is only available to Cloud Firewall Enterprise and Flagship editions. Cloud Firewall Advanced users must complete this task in Security Group configuration of ECS console.

3.  Verify the policies.

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/126848/155653730445993_en-US.png)

    Go to **Log** \> **Access Log** to verify the network traffic that is permitted, denied, and monitored. Based on the access log and the actual test results, verify the policies are executed as expected.

4.  Tune the Internet Firewall policies.![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/126848/155653730438987_en-US.png) 

    Make sure that the Internet Firewall policies do not have any false positives, and then change the action of the Any-Any policies from **Monitor** to **Deny**. Make sure that you understand the risks of this operation before you perform this task.

5.  Allow the inbound traffic to pass through the Internal Firewall on all ECS instances.

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/126848/155653730546000_en-US.png)

    When you perform this task, follow these guidelines:

    -   Go to **Security Policies** \> **Access Control** \> **Internal Firewall**, add a policy to all policy groups to allow all network traffic sent from 0.0.0.0/0.
    -   After you complete this task, you no longer need to create a new policy for new ECS instances that join the security groups. However, if you add an ECS instance to a newly created security group, then you must create a default inbound policy in the group to allow all inbound traffic.
6.  Verify the availability of all businesses.

    Go to **Log** \> **Access Log** and verify the network traffic that is permitted, denied, and monitored. Based on the access log and the actual test results, verify the policies are executed as expected.

7.  Configure Internet Firewall outbound policies.

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/126848/155653730546001_en-US.png)

    When you perform this task, follow these guidelines:

    -   When you need to establish external connections, you can go to **Security Policies** \> **Access Control** \> **Internet Firewall** \> **Outbound Policies** tab page to create policies.
    -   We recommend that you only allow network traffic destined for the specified domain names or IP addresses, such as the end point of an external API.
    -   By default, all network traffic destined for the Internet are not allowed to pass through the Internet Firewall. You can monitor your businesses a short period of time to make sure that they need external connections before creating a policy.


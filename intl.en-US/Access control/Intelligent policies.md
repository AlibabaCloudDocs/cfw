# Intelligent policies

Cloud Firewall uses machine learning to analyze traffic passing through the Internet firewall. Cloud Firewall recommends intelligent policies for destination IP addresses or domain names based on your IP address assets, access history, and external connections. You can apply the intelligent policies based on your business needs. Intelligent policies help you control the exposure of assets to the Internet and block outbound traffic to malicious IP addresses and domain names. This reduces your business risks.

Cloud Firewall automatically generates intelligent policies only for assets protected by the Internet firewall.

Cloud Firewall offers three types of intelligent policies: **high\_risk\_service**, **Block Unused Ports**, and **botnet prevention**.

![Intelligent policy types](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/4387686851/p75076.png)

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext).

2.  In the left-side navigation pane, choose**Security Policies** \> **Access Control**.

3.  On the Internet Firewall tab, click **Outbound Policies** or **Inbound Policies**.

4.  Click **Intelligent Policy**.

    The Intelligent Policy Recommendation page appears, which displays the inbound and outbound policies recommended for the public IP address.

    ![Intelligent Policy Recommendation](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/4387686851/p75074.png)

5.  View policy details.

    1.  On the Intelligent Policy Recommendation page, find the target policy, and click **View Details** in the Actions column.

        **Note:** If there are too many recommended policies, you can filter them based on **Recommendation Type** and **Destination**.

    2.  On the Intelligent Policy Details page, view all policies recommended by Cloud Firewall for the public IP address and the reasons why these policies are recommended.

        **Note:** To reduce the exposure of your assets to the Internet, we recommend that you allow access to the open ports that provide services for an open public IP address on the Internet firewall and deny access to other ports.

        ![Intelligent Policy Details](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/5387686851/p75085.png)

6.  Use one of the following methods to apply an intelligent policy:

    **Note:** Before you apply a policy, make sure that you understand its meaning and possible service impacts.

    -   In the list of recommended intelligent policies, select one or more policies and click **Apply Selected**.
    -   In the list of recommended intelligent policies, find the target policy and click **Apply Policy** in the Actions column.
    -   On the Intelligent Policy Details page, click **Apply Policy**.

An intelligent policy takes effect after it is applied. On the Access Control page, you can view, modify, and delete applied access policies. For more information, see [Outbound and inbound traffic control on the Internet firewall](/intl.en-US/Access control/Outbound and inbound traffic control on the Internet firewall.md).


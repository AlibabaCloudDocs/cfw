# Apply intelligent policies

Cloud Firewall provides the AI intelligent policy feature, which is based on machine learning technology. Cloud Firewall recommends intelligent policies based on your IP address assets, access history, and outbound connections. Intelligent polices can be applied to the Internet firewall to control access to each destination IP address or domain name. Intelligent policies help minimize the exposure of your assets to the Internet and block outbound traffic to malicious IP addresses and domain names. This reduces risks to your business.

Cloud Firewall automatically learns your traffic from the last 30 days and recommends multiple intelligent policies based on the traffic risks it identifies. You must promptly view the details of the recommended policies in the Cloud Firewall console and determine whether to apply the intelligent policies.

## Limits

Cloud Firewall automatically generates intelligent policies only for the **Internet firewall**.

You must manually create access control policies for internal and VPC firewalls. For more information, see [Access control on an internal firewall between ECS instances](/intl.en-US/Access control/Access control on an internal firewall between ECS instances.md) and [Access control for outbound and inbound traffic on the Internet firewall](/intl.en-US/Access control/Access control for outbound and inbound traffic on the Internet firewall.md).

## Procedure

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext)[Cloud Firewall console](https://partners-yundun.console.aliyun.com/?p=cfwnext).

2.  In the left-side navigation pane, click **Access Control**.

3.  On the **Internet Firewall** tab, click **Outbound Policies** or **Inbound Policies** based on your business requirements.

    ![Entry into intelligent policies](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/9773685161/p238272.png)

4.  Find the **Intelligent Policy** section and click **View Recommended Policy**.

5.  In the **Intelligent Policy Recommendation** panel, select and apply intelligent policies.

    ![Intelligent Policy Recommendation](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/9773685161/p75074.png)

    The **Intelligent Policy Recommendation** panel lists the inbound and outbound access control policies that Cloud Firewall recommends for all your public IP addresses. You can click **View Details** in the Actions column to view all the intelligent policies that Cloud Firewall recommends for the public IP address and also **Recommendation Reason**. If a large number of policies are recommended, you can filter them by **Recommendation Type** and **Destination**.

    **Note:** We recommend that you allow access to the open ports that provide services for an open public IP address on the Internet firewall and deny access to other ports. This reduces the exposure of your assets to the Internet.

    ![Intelligent Policy Details](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/5387686851/p75085.png)

    You can select one of the following methods to apply intelligent policies to your assets:

    **Warning:** Before you apply an intelligent policy, make sure that you understand its meaning and the possible impacts on services.

    -   In the list of recommended intelligent policies, select one or more policies and click **Apply Selected**.
    -   In the list of recommended intelligent policies, find the required policy and click **Apply Policy** in the **Actions** column.

An intelligent policy takes effect immediately after it is applied.

On the **Access Control** page, you can view, modify, and delete the access control policies that are applied. For more information, see [Access control for outbound and inbound traffic on the Internet firewall](/intl.en-US/Access control/Access control for outbound and inbound traffic on the Internet firewall.md).


# Create a VPC firewall

You can use a VPC firewall to detect and control the traffic between two VPCs. If your VPCs are connected by using an Express Connect or if they belong to the same Cloud Enterprise Network \(CEN\), you can create a VPC firewall for the Express Connect or CEN. Cloud Firewall can be used to analyze and control traffic between two VPCs only after a VPC firewall is created and enabled.

You have purchased a CEN or Express Connect instance, and have connected two VPCs by using the instance. For more information, see [Interconnect two VPCs under the same account](/intl.en-US/Peering connections/Interconnect two VPCs under the same account.md).

The VPC Firewall feature is available in Cloud Firewall Enterprise and Ultimate Editions. A VPC firewall can be created only between two VPCs that are connected by using an [Express Connect](/intl.en-US/Product Introduction/What is Express Connect?.md) or a [CEN]().

## Create a VPC firewall for a CEN

Cloud Firewall of the **Ultimate Edition** can be used to protect VPCs that are connected by using a CEN and are created by using different Alibaba Cloud accounts. If you want to enable VPC Firewall for such VPCs, Cloud Firewall must be authorized to access the cloud assets under both accounts. Otherwise, you cannot create a VPC firewall for the CEN, and the message **It is not allowed to be created because of the existing unauthorized network instance** is displayed on the **CEN** tab. To go to this tab, log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext), click **Firewall Settings** in the left-side navigation pane, click the **VPC Firewall** tab, and then click the CEN tab.

To authorize Cloud Firewall to access cloud assets of an Alibaba Cloud account, perform the following operations:

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext) by using the account.
2.  On the welcome page of Cloud Firewall, get started as instructed.
3.  On the Cloud Resource Access Authorization page, click **Confirm Authorization Policy**.

**Note:** If you want to enable VPC Firewall for a CEN, note the following items:

-   VPC firewalls can be used to protect VPCs that are deployed in different regions or created by different Alibaba Cloud accounts. If your VPC is connected with a VPC that is created by another Alibaba Cloud account, you can enable VPC Firewall to protect these VPCs even if Cloud Firewall Premium, Enterprise, or Ultimate Edition is not enabled for the VPC that is created by another Alibaba Cloud account.
-   VPC Firewall can be enabled for a maximum of 10 VPCs in a region of a CEN. If you want to increase the quota, [submit a ticket](https://workorder-intl.console.aliyun.com/console.htm#/ticket/createIndex).
-   VPC firewalls can protect traffic between VPCs, between a VPC and a Virtual Border Router \(VBR\), and between a VPC and a Cloud Connect Network \(CCN\), but cannot protect traffic between VBRs, between CCNs, or between a CCN and a VBR.

To create a VPC firewall for a CEN, perform the following operations:

**Note:** When you create, enable, disable, or delete a VPC firewall, the system automatically modifies custom routes in your VPC route table, causing a short network interruption. If you need to perform batch operations on VPC firewalls or frequently enable and disable VPC firewalls, we recommend that you perform such operations during off-peak hours to prevent the impact on your business.

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext).

2.  In the left-side navigation pane, click **Firewall Settings**.

3.  On the Firewall Settings page, click the VPC Firewall tab.

4.  On the VPC Firewall tab, click the **CEN** tab.

5.  Find the CEN instance for which you want to create a VPC firewall and click **Create** in the Actions column.

    If a large number of CEN instances exist, you can filter CEN instances by region, CEN instance name, network instance name, or Cloud Firewall configuration status. For example, you can set the Cloud Firewall configuration status to **Unconfigured** and click **Search** to query all CEN instances for which Cloud firewalls are not configured.

    ![Cloud Firewall unconfigured](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/8463068951/p72469.png)

6.  In the Create VPC Firewall dialog box, configure the required parameters.

    The following table describes the parameters used to create a VPC firewall for a CEN.

    |Parameter|Description|
    |---------|-----------|
    |**Instance Name**|Enter a name for the VPC firewall. We recommend that you enter a unique name that indicates the specific business to make it easy to identify the VPC firewall.|
    |**Connection Type**|Specify the type of the connection between VPCs or between a VPC and an on-premises data center. In this scenario, the value is fixed to **CEN**.|
    |**Network Instance**|Confirm the region and the network instance, and specify **Destination CIDR Blocks**. You can click **Add Destination CIDR Block** next to **Destination CIDR Blocks** to add CIDR blocks. |
    |**IPS Mode**|Select the work mode of the intrusion prevention system \(IPS\). Valid values:     -   **Monitoring Mode**: If you select this option, Cloud Firewall monitors traffic and sends alerts when it detects malicious traffic.
    -   **Traffic Control Mode**: If you select this option, Cloud Firewall intercepts malicious traffic and blocks intrusion attempts.
**Note:** This setting is applied to all VPCs that belong to the CEN. |
    |**Intrusion Prevention**|Select the intrusion prevention policies that you want to enable. Valid values:     -   **Monitoring Mode** or **Traffic Control Mode**. In monitoring mode, traffic that hits intrusion prevention rules is monitored but not blocked. In traffic control mode, traffic that hits intrusion prevention rules is blocked. You can select only one of the two modes.
    -   **Basic Policies**: This feature provides basic intrusion prevention capabilities such as protection against brute force attacks and attacks that exploit command execution vulnerabilities. It also allows you to manage and control the connections from infected hosts to a command and control \(C&C\) server.
    -   **Virtual Patches**: This feature defends against the most common high-risk application vulnerabilities in real time.
**Note:** This setting is applied to all VPCs that belong to the CEN. |
    |**Enable VPC Firewall**|After the VPC firewall is enabled, traffic from the CEN to the configured destination CIDR blocks is protected by Cloud Firewall. If you do not require the VPC firewall to be automatically enabled after it is created, turn off this switch.|

7.  Click **Submit** and confirm the submission.

    The VPC firewall is created. If you turn on Enable VPC Firewall when you configure the VPC firewall, the VPC firewall is enabled automatically. When the VPC firewall takes effect, **Firewall Status** of the VPC firewall changes to **Enabled**.

    ![CEN with Cloud Firewall enabled](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/8463068951/p72475.png)


**Note:** After a VPC firewall is enabled, a security group named Cloud\_Firewall\_Security\_Group is automatically added and an access control policy is created to allow traffic to the VPC firewall. Do not modify or delete this security group and the access control policy.

## Create a VPC firewall for an Express Connect

If you want to enable VPC Firewall for an Express Connect, note the following items:

-   VPC firewalls can control traffic between VPCs that are deployed in the same region, but cannot control traffic between VPCs that are deployed in different regions or are created by using different Alibaba Cloud accounts.
-   VPC firewalls cannot control traffic between a VPC and a VBR.

To create a VPC firewall for an Express Connect, perform the following operations:

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext).

2.  In the left-side navigation pane, click **Firewall Settings**.

3.  On the Firewall Settings page, click the **VPC Firewall** tab.

4.  On the VPC Firewall tab, click the **Express Connect** tab.

5.  Find the Express Connect for which you want to create a VPC firewall and click **Create** in the Actions column.

    If a large number of Express Connects exist, you can filter them by region, VPC instance, or Cloud Firewall configuration status. For example, you can set the Cloud Firewall configuration status to **Unconfigured** and click **Search** to query all Express Connects for which Cloud firewalls are not configured.

6.  In the Create VPC Firewall dialog box, configure the required parameters. The following table describes the parameters used to create a VPC firewall for an Express Connect.

    |Parameter|Description|
    |---------|-----------|
    |**Instance Name**|Enter a name for the VPC firewall. We recommend that you enter a unique name that indicates the specific business to make it easy to identify the VPC firewall.|
    |**Connection Type**|Specify the type of the connection between VPCs or between a VPC and an on-premises data center. In this scenario, the value is fixed to **Express Connect**.|
    |**VPC**|Confirm the region and name of the VPC, and configure **Route Table** and **Destination CIDR Block**.     -   Route Table

When you create a VPC, the system automatically creates a default route table. You can add system routes to the route table to manage VPC traffic. VPC allows you to create multiple route tables as required. For more information, see [Overview](/intl.en-US/Route tables/Route table overview.md).

When you create a VPC firewall in the Cloud Firewall console, Cloud Firewall automatically reads your VPC route tables. Express Connect supports multiple route tables. When you create a VPC firewall for an Express Connect, you can view multiple VPC route tables and can select the route tables that you want to protect.

    -   Destination CIDR Block

After you select a route table from the Route Table drop-down list, the default destination CIDR block of the route table is displayed in the Destination CIDR Block section. If you need to protect traffic to other CIDR blocks, you can modify this destination CIDR block. You can add multiple CIDR blocks that are separated with commas \(,\). |
    |**Peer VPC**|Confirm the region and name of the peer VPC, and configure **Peer Route Table** and **Peer Destination CIDR Blocks**. For more information about route tables and destination CIDR blocks, see the **VPC** configuration description.|
    |**Intrusion Prevention**|Select the intrusion prevention policies that you want to enable. Valid values:     -   **Monitoring Mode** or **Traffic Control Mode**. In monitoring mode, traffic that hits intrusion prevention rules is monitored but not blocked. In traffic control mode, traffic that hits intrusion prevention rules is blocked. You can select only one of the two modes.
    -   **Basic Policies**: This feature provides basic intrusion prevention capabilities such as protection against brute force attacks and attacks that exploit command execution vulnerabilities. It also allows you to manage and control the connections from infected hosts to a command and control \(C&C\) server.
    -   **Virtual Patches**: This feature defends against the most common high-risk application vulnerabilities in real time. |
    |**Enable VPC Firewall**|After you turn on Enable VPC Firewall, a VPC firewall is enabled automatically after it is created. If you do not require the VPC firewall to be automatically enabled after it is created, turn off this switch.|

7.  Click **Submit** and confirm the submission.

    The VPC firewall is created. If you turn on Enable VPC Firewall when you configure the VPC firewall, the VPC firewall is enabled automatically. When the VPC firewall takes effect, **Firewall Status** of the VPC firewall changes to **Enabled**.

    ![Cloud Firewall enabled](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/8463068951/p72476.png)


After a VPC firewall is created, you can perform the following operations as required:

-   On the VPC Firewall tab, click **Modify** or **Delete** to modify or delete the created VPC firewall.
-   On the VPC Firewall tab, enable or disable the VPC firewall. For more information, see [Enable or disable VPC Firewall](/intl.en-US/Firewall Settings/VPC Firewall/Enable or disable VPC Firewall.md).
-   In the left-side navigation pane, choose **Security Policies** \> **Access Control**. On the Access Control page, click the VPC Firewall tab. On the VPC Firewall tab, configure VPC firewall policies to control traffic between VPCs. For more information, see [Access control on VPC firewalls](/intl.en-US/Access control/Access control on VPC firewalls.md).

After a VPC firewall is enabled, VPC access traffic is collected and analyzed. You can view the statistics and analysis results on the VPC Access page. To go to this page, choose **Traffic Analysis** \> **VPC Access** in the left-side navigation pane. For more information, see [VPC access](/intl.en-US/Traffic Analysis/VPC access.md).


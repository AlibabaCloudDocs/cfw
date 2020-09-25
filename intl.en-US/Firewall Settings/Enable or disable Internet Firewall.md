# Enable or disable Internet Firewall

The Internet Firewall feature allows you to detect traffic between the Internet and public IP addresses in Alibaba Cloud. After Cloud Firewall is activated, you can enable or disable this feature for specific public IP addresses under your Alibaba Cloud account. After you enable Internet Firewall for your IP address, you can use Cloud Firewall to analyze and control the traffic between the Internet and on-cloud hosts.

The public IP address quota does not exceed the threshold. The public IP address quota refers to the maximum number of public IP addresses that the Internet firewall can protect. Different Cloud Firewall editions have different public IP address quotas. For more information, see [Features](/intl.en-US/Product Introduction/Features.md). You can increase the bandwidth of Cloud Firewall to increase the quota. For more information, see [Renewal and upgrade](/intl.en-US/Pricing/Renewal and upgrade.md).

## Procedure

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext).

2.  In the left-side navigation pane, click **Firewall Settings**.

3.  On the Internet Firewall tab, enable or disable Internet Firewall for specific public IP addresses.

    You can enable or disable this feature for individual public IP addresses, or for all public IP addresses under the current Alibaba Cloud account with one click.

    **Note:** By default, Internet Firewall is disabled for all IP addresses after Cloud Firewall is activated. We recommend that you enable this feature for all IP addresses. After it is enabled, traffic passes through the Internet firewall. However, the default action of access control policies is **Allow**, so your business is not affected.

    You can perform the following operations on the Internet Firewall tab to enable or disable Internet Firewall.

    -   To enable or disable Internet Firewall for all public IP addresses, follow these steps:
        1.  In the Public IP section, click **Batch**.

            ![Enable or disable Internet Firewall](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/5463068951/p72297.png)

        2.  In the Batch dialog box, click **Enable** or **Disable**.

            You can also select **Enable Protection** next to **New Assets** and click Enable. Then, Internet Firewall is enabled for new public IP addresses added under the current Alibaba Cloud account by default.

            ![Batch management](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/5463068951/p53973.png)

    -   To enable or disable Internet Firewall for one or more public IP addresses, follow these steps:
        1.  In the IP address list at the lower section of the page, find the target public IP addresses.

            You can filter the target IP addresses by using **Asset Type**, **Region**, and **Firewall Status**. Alternatively, you can search for the target IP addresses by using **Instance ID/IP**.

        2.  Select the target IP addresses and click **Enable Firewall** or **Disable Firewall** at the lower section of the page. Alternatively, find the target IP address and click **Enable Firewall** or **Disable Firewall** in the Actions column.

            ![Select IP addresses](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/5463068951/p32275.png)

            Due to the network restrictions, Internet Firewall cannot be enabled for some public IP addresses of SLB instances. For such IP addresses, the Enable Firewall button is dimmed. When you move your pointer over this button, a message **"You cannot enable Cloud Firewall for this IP address because the network where the SLB instance is located does not support Cloud Firewall."** appears. We recommend that you use another security service, such as Web Application Firewall, to protect these public IP addresses.

            ![Failed to enable Internet Firewall](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/5463068951/p127298.png)


After you enable Internet Firewall, wait until **Firewall Status** becomes **Enabled**, which indicates that this feature has been enabled. After you disable Internet Firewall, wait until Firewall Status becomes **Disabled**, which indicates that this feature has been disabled. It may take several seconds for the firewall status to be updated.

-   [Overview](/intl.en-US/Traffic Analysis/Overview.md)
-   [Outbound and inbound traffic control on the Internet firewall](/intl.en-US/Access control/Outbound and inbound traffic control on the Internet firewall.md)

**Related topics**  


[Functions of Internet Firewalls]()

[Why do I fail to enable the Internet firewall?]()

[What are the impacts of disabling the Internet firewall?](/intl.en-US/FAQ/What are the impacts of disabling the Internet firewall?.md)


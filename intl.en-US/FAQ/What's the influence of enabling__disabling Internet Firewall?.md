# What's the influence of enabling/disabling Internet Firewall? {#concept_jkv_cpw_tgb .concept}

This topic describes the impacts of enabling and disabling the Internet Firewall.

The following figure shows the configuration of Internet Firewall.

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/124495/155652046438959_en-US.png)

Disabling the Internet Firewall may have the following impacts:

-   On the **Overview** \> **Security Analysis** tab page, the **Overall Protection Levels** of your assets may be changed to **Low**. Less assets are protected, as shown under **Asset Protection**.

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/124495/155652046445898_en-US.png)

-   On the **Overview** \> **Network Activities** tab page, some network traffic analysis charts may fail to display the data.
-   If you have configured inbound or outbound policies, these policies will become invalid after the Internet Firewall is disabled. You can find the policy**hits** of the affected server stays unchanged. This means the policy no longer takes effect.
-   After you disable the Internet Firewall, network traffic no longer pass through the Cloud Firewall to reach its destination. This means that the intrusion prevention function no longer takes effect.

    Even if the IPS is set to the **Monitor** mode, IPS no longer detects network traffic on the instance, and the **Traffic Control** mode of IPS is invalid then.

-   After the Internet Firewall is disabled, Network traffic statistics generated are not displayed on the **Logs** \> **Access Log** tab page.

For more information, see [Enable or disable the Cloud Firewall service](../../../../intl.en-US/User Guide/Enable or disable the Cloud Firewall service.md#).


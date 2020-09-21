---
keyword: [one-click activation, enable firewall, Cloud Firewall, firewall, Firewall Settings]
---

# Activate Cloud Firewall

After you purchase Cloud Firewall, it does not automatically start protection. You can activate or deactivate this service on the Firewall Settings page. After you activate this service, you can use it without the need to perform complex configurations.

## Limits

Cloud Firewall Enterprise Edition and Ultimate Edition support VPC firewalls. The free trial edition and Premium Edition do not support VPC firewalls. For more information, see [Editions and regions](/intl.en-US/Product Introduction/Editions and regions.md).

For the items that you must pay attention to when you enable VPC firewalls, see [VPC firewall limits](/intl.en-US/Firewall Settings/VPC Firewall/VPC firewall limits.md).

## Procedure

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext).

2.  In the left-side navigation pane, click **Firewall Settings**.

3.  On the Firewall Settings page, activate Cloud Firewall.

    ![Firewall Settings](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/7853289951/p77240.png)

    **Note:** Only Cloud Firewall Enterprise Edition and Ultimate Edition support VPC firewalls. If you are using the free trial edition or Premium Edition, the VPC Firewall tab does not appear on the Firewall Settings page.

    You can enable the **Internet firewall** or **VPC firewalls**.

    -   To enable the **Internet firewall**, perform the following steps:
        1.  On the Firewall Settings page, click the Internet Firewall tab.
        2.  On the Internet Firewall tab, perform the following operations:
            -   Click **Batch**. In the dialog box that appears, select Enable Protection and click **Enable** to enable the Internet firewall for all assets.
            -   Select the assets for which you want to enable the Internet firewall and click **Enable Firewall** in the lower-left corner.
    -   To enable **VPC firewalls**, perform the following steps:
        1.  On the Firewall Settings page, click the VPC Firewall tab.
        2.  On the VPC Firewall tab, find the asset for which you want to enable VPC firewalls and turn on the switch in the **Firewall Settings** column.
    You can view the firewall status of assets by specifying **Asset Type**, **Region**, and **Firewall Status**.



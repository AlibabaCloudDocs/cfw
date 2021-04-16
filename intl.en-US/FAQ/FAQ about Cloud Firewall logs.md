# FAQ about Cloud Firewall logs

This topic provides answers to some commonly asked questions about Cloud Firewall logs.

## Can traffic logs on Cloud Firewall be exported to a third-party system?

Yes. Cloud Firewall Premium Edition, Enterprise Edition, and Ultimate Edition provides the log analysis feature that can be used with Alibaba Cloud Log Service, also known as Simple Log Service \(SLS\). The log analysis feature allows you to view and export **Internet traffic logs**.

You can use this feature to export traffic logs to your business system, such as your security O&M center.

**Note:** Internet traffic logs contain data such as the vulnerability priorities and hit results of access control rules.

For information about how to export logs, see [Import Cloud Firewall Internet logs to a third-party system](/intl.en-US/Best Practices/Import Cloud Firewall Internet logs to a third-party system.md).

## How do I know the remaining log storage capacity of Cloud Firewall?

If you have purchased Cloud Firewall Premium Edition, Enterprise Edition, or Ultimate Edition, and have enabled the log analysis feature, you can view the used and remaining log storage capacity in the upper-right corner of the Log Analysis page. To go to this page, choose [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext)**Logs** \> **Log Analysis** in the left-side navigation pane.

![Log analysis](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/7034631061/p143225.png)

**Note:** The free trial edition of Cloud Firewall does not support the log analysis feature, so the log storage capacity is not displayed.

## Why is the log storage capacity not displayed in the Cloud Firewall console?

The free trial edition of Cloud Firewall does not support the log analysis feature. If you are using the free trial edition of Cloud Firewall, the log storage capacity is not displayed. For information about how to enable the log analysis feature, see [t154091.dita\#concept\_pzr\_rxj\_hhb](/intl.en-US/Logs/Log analysis/Enable the Log Analysis feature.md).


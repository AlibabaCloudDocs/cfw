# Purchase a Cloud Firewall edition

This topic describes how to purchase a paid Cloud Firewall edition. Paid Cloud Firewall editions support only the subscription billing method. When you purchase an edition, you must select the service edition, specifications, and subscription period based on your business requirements, and complete the payment.

## Procedure

1.  Go to the [Cloud Firewall buy page](https://common-buy.aliyun.com/?&commodityCode=vipcloudfw#/buy) by using your Alibaba Cloud account.

2.  Configure the following parameters as required.

    |Parameter|Description|
    |---------|-----------|
    |**Current Version**|The edition of Cloud Firewall that you want to purchase. Valid values:    -   **Premium Edition**
    -   **Enterprise Edition**
    -   **Premium Edition**
Different editions support different features. You can click an edition and view its features in the **Features** section. For more information, see [Features](/intl.en-US/Product Introduction/Features.md).

For pricing information about each edition, see [Billing](/intl.en-US/Pricing/Billing.md). |
    |**Protected Public IP Addresses**|The number of public IP addresses that the Internet firewall can protect. Valid values:    -   **Premium Edition**: 20 to 1000
    -   **Enterprise Edition**: 50 to 2000
    -   **Ultimate Edition**: 400 to 4000 |
    |**Protected Internet Traffic**|The maximum inbound or outbound Internet traffic that Cloud Firewall can protect. Unit: Mbit/s Valid values:    -   **Premium Edition**: 10 to 1000
    -   **Enterprise Edition**: 50 to 2000
    -   **Ultimate Edition**: 200 to 4000
We recommend that you set this parameter to the Internet bandwidth of your business.

If the specification does not meet your business requirements, [submit a ticket](https://workorder-intl.console.aliyun.com/console.htm#/ticket/createIndex) to apply for scale-out. |
    |**Protected VPCs**|The number of VPCs that VPC firewalls can protect.Only **Enterprise Edition** and **Ultimate Edition** support VPC firewalls. This parameter is required only after you select **Enterprise Edition** or **Ultimate Edition** for Current Version. Valid values:

    -   **Enterprise Edition**: 2 to 200
    -   **Ultimate Edition**: 5 to 500 |
    |**Log Audit**|Specifies whether to enable the Log Audit \(Log Analysis\) feature.By default, Cloud Firewall retains logs of the last seven days. If you want to save logs of more than seven days or meet specific classified protection requirements, we recommend that you enable the Log Audit feature.

The Log Audit feature supports the storage of logs generated in the last six months, which meets classified protection requirements. For more information, see [Overview](/intl.en-US/Logs/Log analysis/Overview.md). |
    |**Log Storage**|The log storage capacity of the Log Audit feature. Unit: GB. Valid values:    -   **Premium Edition**: 1000 to 100000
    -   **Enterprise Edition**: 3000 to 100000
    -   **Ultimate Edition**: 5000 to 100000
This parameter appears only after you select **Yes** for **Log Audit**.

If you want to store logs of six months and set Protected Internet Traffic to 10 Mbit/s, we recommend that you purchase 1,000 GB of storage capacity.

For information about the billing rules of the Log Audit feature, see [Log analysis billing method](/intl.en-US/Logs/Log analysis/Log analysis billing method.md). |
    |**Expert Service**|Specifies whether to enable the expert service.The expert service allows you to consult experts about configuration access and policy optimization over DingTalk. We recommend that you purchase the expert service for major business events to achieve high security. |
    |**Duration**|The subscription duration.You can select **Auto-renewal**. |

3.  Click **Buy Now** and complete the payment.

    After you complete the payment, you can view the Cloud Firewall edition and remaining validity period in the upper-right corner of the **Overview** page in the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext)。

    ![Edition and remaining validity period](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/7631860061/p136987.png)


## Related operations

-   Renew the subscription

    To renew the subscription to prolong the validity period of the current Cloud Firewall edition, perform the following steps: Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext), click **Renew** in the upper-right corner of the **Overview** page, and then complete the renewal operation as prompted. For more information, see [Renewal](/intl.en-US/Pricing/Renewal and upgrade.md).

-   Upgrade the Cloud Firewall edition

    To upgrade your Cloud Firewall to a higher edition, perform the following steps: Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext), click **Upgrade** in the upper-right corner of the **Overview** page, and then complete the upgrade as prompted. For more information, see [Upgrade](/intl.en-US/Pricing/Renewal and upgrade.md).

-   Downgrade the Cloud Firewall edition

    If you have subscribed to Cloud Firewall and want to downgrade it to a lower edition, [submit a ticket](https://workorder-intl.console.aliyun.com/console.htm#/ticket/createIndex) to unsubscribe from the current edition and then subscribe to the lower edition.



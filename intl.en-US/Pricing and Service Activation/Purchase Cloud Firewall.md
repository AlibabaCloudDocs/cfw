# Purchase Cloud Firewall

Cloud Firewall supports only the subscription billing method. To purchase Cloud Firewall, select the service edition, specifications, and duration based on your business requirements, and complete the payment.

## Procedure

1.  Log on to the [Cloud Firewall buy page](https://common-buy-intl.alibabacloud.com/?&commodityCode=cfw_pre_intl) with your Alibaba Cloud account.

2.  Configure the parameters for purchasing Cloud Firewall.

    |Parameter|Description|
    |---------|-----------|
    |**Current Version**|The edition of Cloud Firewall that you want to purchase. Valid values: **Premium Edition**, **Enterprise Edition**, and **Ultimate Edition**.Different editions have different features. You can click an edition and view its features in the **Features** section. For more information, see [Features](/intl.en-US/Product Introduction/Features.md).

For pricing information about each edition, see [Billing](/intl.en-US/Pricing and Service Activation/Billing.md). |
    |**Protected Public IP Addresses**|The number of public IP addresses that can be protected by the Internet firewall. Valid values for each edition:    -   **Premium Edition**: 20 to 1000
    -   **Enterprise Edition**: 50 to 2000
    -   **Ultimate Edition**: 400 to 4000 |
    |**Protected Internet Traffic**|The peak bandwidth of Internet traffic that can be protected by Cloud Firewall. Unit: Mbit/s. Valid values for each edition:    -   **Premium Edition**: 10 to 1000
    -   **Enterprise Edition**: 50 to 2000
    -   **Ultimate Edition**: 200 to 4000
**Note:** We recommend that you set this parameter to the Internet bandwidth of your business.

If the specification does not meet your business requirements, [submit a ticket](https://workorder-intl.console.aliyun.com/console.htm#/ticket/createIndex) to apply for a scale-out. |
    |**Protected VPCs**|The number of VPCs that can be protected by Cloud Firewall.This feature is available only in **Enterprise Edition** and **Ultimate Edition**. Therefore, you can configure this parameter only when you select **Enterprise Edition** or **Ultimate Edition** for Current Version. Valid values for each edition:

    -   **Enterprise Edition**: 2 to 200
    -   **Ultimate Edition**: 5 to 500 |
    |**Log Audit**|Specifies whether to enable the Log Audit \(Log Analysis\) feature.By default, Cloud Firewall retains logs of the last seven days. If you want to store logs of more than seven days or meet specific classified protection requirements, we recommend that you enable the Log Audit feature.

The Log Audit feature allows Cloud Firewall to store logs of the last six months, which meets classified protection requirements. For more information, see [Overview](/intl.en-US/Logs/Log analysis/Overview.md). |
    |**Log Storage**|The log storage capacity of the Log Audit feature. Unit: GB. Valid values for each edition:    -   **Premium Edition**: 1000 to 100000
    -   **Enterprise Edition**: 3000 to 100000
    -   **Ultimate Edition**: 5000 to 100000
This parameter is required only after you select **Yes** for **Log Audit**.

**Note:** If you want to store logs of six months and set Protected Internet Traffic to 10 Mbit/s, we recommend that you purchase 1,000 GB of storage capacity.

For information about the billing rules of the Log Audit feature, see [Billing](/intl.en-US/Logs/Log analysis/Billing.md). |
    |**Expert Service**|Specifies whether to enable the expert service.The expert service allows you to consult experts about configuration access and policy optimization over DingTalk. We recommend that you purchase the expert service for major business events to achieve high security. |
    |**Duration**|The subscription duration.You can select **Auto-renewal** as required. |

3.  Click **Buy Now** and complete the payment.

    After you complete the payment, you can view the Cloud Firewall edition and remaining validity period in the upper-right corner of the **Overview** page in the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext).


## Related operations

|Operation|Description|Step|
|---------|-----------|----|
|**Renew**|Renew the subscription to prolong the validity period of the current Cloud Firewall edition.|Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext), click **Renew** in the upper-right corner of the **Overview** page, and then complete the renewal operation as prompted. For more information, see [Renew the subscription](/intl.en-US/Pricing and Service Activation/Renewal and upgrade.md). |
|**Upgrade**|Upgrade to a more advanced edition.|Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext), click **Upgrade** in the upper-right corner of the **Overview** page, and then complete the upgrade operation as prompted. For more information, see [Upgrade the Cloud Firewall edition](/intl.en-US/Pricing and Service Activation/Renewal and upgrade.md). |
|**Downgrade**|Downgrade to a less advanced edition.|[submit a ticket](https://workorder-intl.console.aliyun.com/console.htm#/ticket/createIndex) to cancel the subscription and place a new order to buy the edition that you required. |
|**Auto Renewal**|Allow automatic fee deduction and renewal nine days before Cloud Firewall expires.|Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext), click **Auto Renewal** in the upper-right corner of the **Overview** page, and then complete the renewal operation as prompted. For more information, see [Enable the auto-renewal feature](/intl.en-US/Pricing and Service Activation/Renewal and upgrade.md). |


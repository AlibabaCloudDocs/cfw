# FAQ

## Can Cloud Firewall protect public SLB instances?

Alibaba Cloud provides public and internal SLB instances. Some public SLB instances cannot be protected by Cloud Firewall due to network architecture reasons. We recommend that you deploy internal SLB instances and associate EIPs with the internal SLB instances. For information about how to associate an EIP with an SLB instance, see [Associate an Elastic IP address with an SLB instance](/intl.en-US/User Guide/Instance/Associate an EIP with an SLB instance.md).

**Note:** For a public SLB instance that is in use and is not protected by Cloud Firewall, we recommend that you do not change the network type of the instance by yourself. If you need any help, contact SLB technical support.

## What are the protected bandwidth quotas of Cloud Firewall in different editions?

Cloud Firewall can protect your Internet traffic and traffic between VPCs. Cloud Firewall in different editions have different protected bandwidth quotas:

-   For Internet traffic, the default protected bandwidth quota per month is 10 Mbit/s in Premium Edition, 50 Mbit/s in Enterprise Edition, and 200 Mbit/s in Ultimate Edition.
-   For traffic between VPCs, the default protected bandwidth quota per month is 100 Mbit/s in Enterprise Edition and 1 Gbit/s in Ultimate Edition. No protection is provided in Premium Edition.

For more information, see [Features and billing items of each edition](/intl.en-US/Pricing/Billing.md).


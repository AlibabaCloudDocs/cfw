# FAQ about bandwidth supported by Cloud Firewall

## What are the protected bandwidth quotas of Cloud Firewall in different editions?

Cloud Firewall can protect your Internet traffic and traffic between VPCs. Cloud Firewall in different editions have different protected bandwidth quotas:

-   For Internet traffic, the default protected bandwidth quota per month is 10 Mbit/s in Premium Edition, 50 Mbit/s in Enterprise Edition, and 200 Mbit/s in Ultimate Edition.
-   For traffic between VPCs, the default protected bandwidth quota per month is 100 Mbit/s in Enterprise Edition and 1 Gbit/s in Ultimate Edition. No protection is provided in Premium Edition.

For more information, see [Features and billing items of each edition](/intl.en-US/Pricing/Billing.md).

## Which types of traffic consume the protected bandwidth quota of Cloud Firewall?

Internet traffic consumes the protected bandwidth quota of Cloud Firewall. However, the mutual access traffic between VPCs does not consume the quota. For example, if an elastic IP address \(EIP\) is under a DDoS attack, the traffic to the EIP consumes the protected bandwidth quota no matter whether Cloud Firewall blocks the attack. This is because the traffic is considered Internet traffic.

## What do I do if the bandwidth of my business traffic exceeds the protected bandwidth quota of Cloud Firewall?

If the bandwidth of your business traffic exceeds the protected bandwidth quota, Cloud Firewall protects only the traffic within the quota. We recommend that you perform the following operations:

-   In the Cloud Firewall console, observe the traffic trends displayed on the Overview page and the VPC traffic information displayed on the **VPC Access** page under **Traffic Analysis**. Locate suspicious IP addresses based on Cloud Firewall logs and handle the risks.
-   If the bandwidth of your business traffic exceeds the protected bandwidth quota, Cloud Firewall sends a notification email to you. Check emails in time and handle issues based on the information provided in the email.

    **Note:** The notification email is sent no later than the day after your business traffic exceeds the protected bandwidth quota.

-   Upgrade the Cloud Firewall edition to increase the protected bandwidth quota. For more information, see [Renewal and upgrade](/intl.en-US/Pricing/Renewal and upgrade.md).


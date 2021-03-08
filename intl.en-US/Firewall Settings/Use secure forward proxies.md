# Use secure forward proxies

Cloud Firewall provides secure forward proxies to protect traffic that passes through a network address translation \(NAT\) gateway to the Internet. If you use a secure forward proxy, the traffic that is destined for the Internet passes through the secure forward proxy and then the NAT gateway. This way, you can protect the traffic that is destined for the Internet from an internal network.

A secure forward proxy is a virtual firewall. After you create a secure forward proxy, traffic that passes through the NAT gateway is automatically directed to the secure forward proxy.

**Note:** If a destination network address translation \(DNAT\) entry is created, you cannot use a secure forward proxy.

## Prerequisites

A NAT gateway is created, and a source network address translation \(SNAT\) rule is configured. For more information, see [Create a SNAT entry to access the Internet](/intl.en-US/User Guide/Create a SNAT entry to access the Internet.md).

## Regions and Cloud Firewall editions that support secure forward proxies

Cloud Firewall Enterprise Edition and Ultimate Edition support secure forward proxies.

Secure forward proxies are now available in the China \(Beijing\), China \(Hangzhou\), China \(Shanghai\), China \(Shenzhen\), and China \(Chengdu\) regions. If your Cloud Firewall is deployed on ECS instances that reside in the China \(Shanghai\) or China \(Chengdu\) region, you can create secure forward proxies in the Cloud Firewall console. If your Cloud Firewall is deployed on ECS instances that reside in the other three regions, you must submit a [submit a ticket](https://workorder-intl.console.aliyun.com/console.htm#/ticket/createIndex) to create secure forward proxies.

## Procedure

When you create a secure forward proxy, a transient connection error of 20 seconds may occur due to the change of your route to a NAT gateway. We recommend that you create the secure forward proxy during off-peak hours.

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext).

2.  On the Secure Forward Proxy page, click **Create Secure Forward Proxy**.

3.  In the Create Secure Forward Proxy dialog box, configure the following parameters.

    |Parameter|Description|
    |---------|-----------|
    |**Name**|The custom name of the forward proxy rule. The name can contain letters and special characters.|
    |**Region**|Secure forward proxies are now available in the China \(Beijing\), China \(Hangzhou\), China \(Shanghai\), China \(Shenzhen\), and China \(Chengdu\) regions. If your Cloud Firewall is deployed on ECS instances that reside in the China \(Shanghai\) or China \(Chengdu\) region, you can create secure forward proxies in the Cloud Firewall console. If your Cloud Firewall is deployed on ECS instances that reside in the other three regions, you must submit a [submit a ticket](https://workorder-intl.console.aliyun.com/console.htm#/ticket/createIndex) to create secure forward proxies. |
    |**VPC**|The VPC of the NAT gateway whose outbound traffic requires protection.|
    |**VPC CIDR Block**|The CIDR block of the VPC.|
    |**NAT Gateway**|The route for your traffic to access the Internet through the NAT gateway. After you select a route, the original route is closed and the traffic is directed to the secure forward proxy.|

    After you create a secure forward proxy, the secure forward proxy is automatically enabled. Then, the traffic is directed to the secure forward proxy.

    On the Secure Forward Proxy page, you can modify or delete existing secure forward proxies, and download the data of these proxies.

    **Note:** If your Cloud Firewall expires and is not renewed, your secure forward proxies are released. Then, the traffic is directed to the original route destined for the Internet. This may interrupt your services. To prevent interruptions to your services, renew your Cloud Firewall before expiration. For more information, see [Renew subscription](/intl.en-US/Pricing and Service Activation/Renewal and upgrade.md).


## References

-   View outbound connections for elastic IP addresses \(EIPs\) that are associated with NAT gateways

    On the Outbound Connections page, choose **Outbound traffic** \> **Assets** and view outbound connections for EIPs and public IP addresses that are associated with NAT gateways. For more information, see [Outbound connections](/intl.en-US/Traffic Analysis/Outbound connections.md).

-   View Internet access activities that are initiated by using EIPs associated with NAT gateways

    On the **Open Public IP Addresses** tab of the Internet Access page, view Internet access activities that are initiated by using EIPs associated with NAT gateways. For more information, see [Internet access](/intl.en-US/Traffic Analysis/Internet access.md).

-   View traffic logs for EIPs that are associated with NAT gateways

    On the **Traffic Logs** tab of the Log Audit page, view traffic logs based on the conditions that you specify. For more information, see [Traffic logs](/intl.en-US/Logs/Log audit.md).



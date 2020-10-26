# FAQ about the Internet firewall

## What is the function of the Internet firewall?

If the Internet firewall is disabled, the traffic of public IP addresses is forwarded to internal firewalls or security groups and then to the destination ECS instances.

If the Internet firewall is enabled, the traffic of public IP addresses is redirected to the Internet firewall before it is forwarded to internal firewalls or security groups and then to the destination ECS instances. If you enable the Internet firewall but do not configure access control policies for Cloud Firewall or policies for the intrusion prevention system \(IPS\), Cloud Firewall detects traffic and generates alerts for suspicious traffic but does not block any traffic.

The following figure shows both the route of network traffic when the Internet firewall is enabled and when it is disabled:

![](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/124627/156689959138816_en-US.png)

## Is network traffic affected when you enable the Internet firewall?

Enabling Internet Firewall or VPC Firewall has no impact on network traffic.

## What are the impacts of disabling the Internet firewall?

The following figure shows the Internet Firewall tab.

![Firewall Settings](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/0781329951/p88614.png)

Disabling the Internet firewall may have the following impacts:

-   On the Internet Access page, some traffic analysis charts have no data. To go to this page, choose **Traffic Analysis** \> **Internet Access** in the left-side navigation pane.
-   If you have created outbound or inbound access control policies, these policies become invalid. The **hits** of these policies remain unchanged.
-   Network traffic does not pass Cloud Firewall. Intrusion prevention is not implemented.

    Even if Intrusion Prevention Mode is set to **Monitoring Mode**, the IPS no longer detects network traffic on the server. **Traffic Control Mode** is also invalid.

-   The Traffic Logs tab does not display the traffic data generated after the Internet firewall is disabled. To go to this tab, choose **Logs** \> **Log Audit** in the left-side navigation pane, and click the Traffic Logs tab.
-   Network traffic does not pass Cloud Firewall, so traffic data cannot be captured. The Packet Capture page does not display the IP packet information. To go to this page, choose **Tools** \> **Packet Capture** in the left-side navigation pane. For more information, see [Packet capture](/intl.en-US/Toolbox/Packet capture.md).

For information about how to enable or disable the Internet firewall, see [Enable or disable Internet Firewall](/intl.en-US/Firewall Settings/Enable or disable Internet Firewall.md).

## Why do I fail to enable the Internet firewall?

**Symptom**

On the Internet Firewall tab of the Firewalls page, when you click **Enable Firewall** in the Actions column for some assets, the system prompts a message **You cannot enable Cloud Firewall for this IP address because the network where the SLB instance is located does not support Cloud Firewall.**

![Failed to enable Internet Firewall](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/5463068951/p127298.png)

**Causes**

The Internet firewall cannot be enabled because the network where the Server Load Balancer \(SLB\) instance is located does not support the Internet firewall. The specific cause is one of the following reasons:

-   A limit is imposed on the network architecture of the SLB instance.
-   The assets do not have public IP addresses.

**Solution**

If your assets are deployed only on a private SLB instance, associate an elastic IP address \(EIP\) with the private SLB instance to redirect the traffic to Cloud Firewall. For more information, see [Associate an Elastic IP address with an SLB instance](/intl.en-US/User Guide/Instance/Associate an EIP with an SLB instance.md).

## Which types of public IP addresses can be protected by the Internet firewall?

The Internet firewall can protect the following types of public IP addresses:

-   EIPs of Elastic Network Interfaces \(ENIs\). EIPs can be associated with ECS instances of the VPC type, private SLB instances in the VPC type, ENIs, and Network Address Translation \(NAT\) gateways.
-   Public IP addresses of ECS instances
-   EIPs of SLB instances of the VPC type
-   Public IP addresses of bastion hosts


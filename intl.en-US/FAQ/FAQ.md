# FAQ

## Is Cloud Firewall applicable to the classic network?

The Internet firewall and intrusion prevention system \(IPS\) are applicable to the classic network. The microsegmentation feature is applicable to access control over east-west traffic in VPCs. However, this feature is not applicable to the classic network

## Is Cloud Firewall available in regions outside China?

Yes, in addition to regions in mainland China and the China \(Hong Kong\) region, Cloud Firewall is available in Malaysia \(Kuala Lumpur\), Singapore \(Singapore\), and Indonesia \(Jakarta\) regions.

## Can Cloud Firewall protect public SLB instances?

Alibaba Cloud provides public and internal SLB instances. Some public SLB instances cannot be protected by Cloud Firewall due to network architecture reasons. We recommend that you deploy internal SLB instances and associate EIPs with the internal SLB instances. For information about how to associate an EIP with an SLB instance, see [Associate an Elastic IP address with an SLB instance](/intl.en-US/User Guide/Instance/Associate an EIP with an SLB instance.md).

**Note:** For a public SLB instance that is in use and is not protected by Cloud Firewall, we recommend that you do not change the network type of the instance by yourself. If you need any help, contact SLB technical support.

After you activate Cloud Firewall, the traffic first goes through the firewall. The destination IP address, which is an elastic IP address \(EIP\), of the traffic is then translated into an IP address of a private SLB instance by using destination network address translation \(DNAT\).

## Can Cloud Firewall control traffic from private IP addresses to the Internet?

Cloud Firewall only controls traffic to the Internet from EIPs or public IP addresses obtained by using DNAT. It cannot control outbound traffic from private IP addresses.

If you want to control the traffic from a private IP address, bind an EIP to the private IP address and configure access control policies for this EIP.

## Can Cloud Firewall control IPsec traffic?

The Internet firewall cannot be used to control decrypted IPsec traffic.

You can use east-west traffic control policies of Cloud Firewall to control decrypted IPsec traffic.

## Can Cloud Firewall protect traffic on Express Connect?

Yes, Cloud Firewall can protect traffic on Express Connect.

-   Cloud Firewall can protect only traffic between VPCs that are connected by using Express Connect in the same region. It cannot protect traffic between a VPC and a VBR that are connected by using Express Connect.
-   Cloud Firewall can protect traffic between two VPCs in different regions, as well as a VPC and a VBR, that are connected by using a Cloud Enterprise Network \(CEN\).

**Note:** If you need Cloud Firewall to protect traffic between two VPCs in different regions, or between a VPC and a VBR, migrate the traffic of Express Connect to a CEN. For more information, see [Migrate a VPC in a peering connection to a CEN instance]().

## Traffic from unknown applications accounts for a large proportion of all traffic. Does this occur because Cloud Firewall cannot identify the applications that generate traffic in the Internet?

The possible reasons include:

-   A large amount of traffic is generated in the Internet and the traffic does not comply with standard protocols. Therefore, Cloud Firewall cannot identify the traffic type.
-   The destination server blocks network traffic and returns a large number of RST packets. These packets are carried in inbound or outbound traffic, which causes a large proportion of traffic from unknown applications.

**Note:** You can choose **Log Audit** \> **Traffic Logs** or **Log Audit** \> **Event Logs** in the left-side navigation pane to check the source and purpose of the traffic with unknown applications, and determine whether the traffic is normal.

You can view the details of unknown applications on the following pages in the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext):

-   Unknown application types on the Internet Access page
-   Unknown attacked applications on the Traffic Blocked by IPS page
-   Unknown applications in the **Rankings of Visits by Traffic** section on the All Access Activities page

## Why is there a large proportion of traffic with unknown ISPs on the All Access Activities page under Traffic Analysis?

This occurs because a large amount of inbound traffic comes from regions outside China. Cloud Firewall marks the ISPs of such traffic as unknown. To view the regions and ISPs of specific IP addresses, choose **Log Audit** \> **Traffic Logs** in the left-side navigation pane.


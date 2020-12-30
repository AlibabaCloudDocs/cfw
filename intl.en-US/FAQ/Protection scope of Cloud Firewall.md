# Protection scope of Cloud Firewall

## What cloud assets or traffic can Cloud Firewall protect?

Cloud Firewall can protect the following cloud assets or traffic:

-   Internet traffic: traffic from public IP addresses of Elastic Compute Service \(ECS\) instances, elastic IP addresses \(EIPs\) of Server Load Balancer \(SLB\) instances, highly available virtual IP addresses \(HAVIPs\), EIPs, EIPs of ECS instances, EIPs of Elastic Network Interfaces \(ENIs\), some public IP addresses of SLB instances, and EIPs of network address translation \(NAT\) gateways.

    **Note:** Alibaba Cloud provides public and private SLB instances. Some public SLB instances cannot be protected by Cloud Firewall due to network architecture reasons. We recommend that you deploy private SLB instances and associate EIPs with the private SLB instances. For information about how to associate an EIP with an SLB instance, see [Associate an Elastic IP address with an SLB instance](/intl.en-US/Classic Load Balancer/User Guide/Instance/Associate an EIP with an SLB instance.md).

-   Traffic between VPCs: traffic between VPCs that are connected by using a CEN or Express Connect

## Is Cloud Firewall applicable to the classic network?

The Internet firewall and intrusion prevention system \(IPS\) are applicable to the classic network. Internal firewalls are applicable to VPCs, but are not applicable to the classic network.

## Is Cloud Firewall available in regions outside China?

Yes, in addition to regions in mainland China and the China \(Hong Kong\) region, Cloud Firewall is available in Malaysia \(Kuala Lumpur\), Singapore \(Singapore\), Indonesia \(Jakarta\), and Germany \(Frankfurt\) regions. For more information, see [t2012355.md\#]().

## Can Cloud Firewall protect public SLB instances?

Alibaba Cloud provides public and private SLB instances. Some public SLB instances cannot be protected by Cloud Firewall due to network architecture reasons. We recommend that you deploy private SLB instances and associate EIPs with the private SLB instances. For information about how to associate an EIP with an SLB instance, see [Associate an Elastic IP address with an SLB instance](/intl.en-US/Classic Load Balancer/User Guide/Instance/Associate an EIP with an SLB instance.md).

**Note:** For a public SLB instance that is in use and is not protected by Cloud Firewall, we recommend that you do not change the network type of the instance by yourself. If you need any help, contact SLB technical support.

After you activate Cloud Firewall, the traffic first goes through the firewall. The destination IP address, which is an elastic IP address \(EIP\), of the traffic is then translated into an IP address of an internal-facing SLB instance by using destination network address translation \(DNAT\).

## Can Cloud Firewall control traffic from private IP addresses to the Internet?

Cloud Firewall controls only traffic to the Internet from EIPs or public IP addresses obtained by using DNAT. It cannot control outbound traffic from private IP addresses.

If you want to control the traffic from a private IP address, bind an EIP to the private IP address and configure access control policies for this EIP.

## Can Cloud Firewall control IPsec traffic?

The Internet firewall cannot be used to control decrypted IPsec traffic.

You can use east-west traffic control policies of Cloud Firewall to control decrypted IPsec traffic.

## Can Cloud Firewall protect traffic on Express Connect or CEN?

Yes, Cloud Firewall can protect traffic on Express Connect and Cloud Enterprise Network \(CEN\).

-   Cloud Firewall can protect only traffic between VPCs that are connected by using Express Connect in the same region. It cannot protect traffic between a VPC and a Virtual Border Router \(VBR\) that are connected by using Express Connect.
-   Cloud Firewall can protect traffic between two VPCs in different regions, as well as a VPC and a VBR, that are connected by using a CEN.

**Note:** If you need Cloud Firewall to protect traffic between two VPCs in different regions, or between a VPC and a VBR, migrate the traffic of Express Connect to a CEN. For more information, see [t630439.md\#]().

## Why does Cloud Firewall provide three types of firewalls?

Cloud Firewall provides three types of firewalls: Internet firewall, VPC firewall, and internal firewall.

The Internet firewall is deployed at the boundary of the Internet to manage public IP addresses. Internal firewalls works in the same way as security groups to manage communications between ECS instances. The following figure shows how the Internet firewall and internal firewalls work and where they are deployed in the network topology.

![Internet firewall and internal firewalls](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/7681329951/p38798.png)

VPC firewalls are used to protect traffic between VPCs and are deployed at the boundaries of VPCs to manage the traffic over Express Connect. The following figure shows how a VPC firewall works and where it is deployed in the network topology.

![VPC firewalls](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/7681329951/p38893.png)

You can use all of the three types of firewalls to refine your network access control strategy and build three protection systems: Internet traffic protection, VPC protection, and instance protection.

-   Cloud Firewall provides centralized access control, including inbound and outbound policies, to support more precise control over network traffic. Cloud Firewall also provides application-specific and domain name-specific access control policies for you to centrally manage VPCs and regions. You can use the monitor mode and address books to tune your access control policies.
-   For network traffic that requires microsegmentation, Cloud Firewall provides distributed access control. Cloud Firewall is developed based on the capabilities of security groups and offers visualized analysis of internal network traffic, which allows you to tune policies for traffic between ECS instances. The monitor mode, blocked traffic analysis, and threat intelligence features will be soon available.

Cloud Firewall allows you to configure firewalls based on network boundaries to build multiple logical protection systems. This makes your maintenance work much easier. If you only want to detect the Internet traffic, you only need to configure inbound and outbound policies on the Internet firewall. If you want to protect your instances, you can configure access control policies for east-west traffic on internal firewalls.


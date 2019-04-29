# Differences between Cloud Firewall and Security groups {#concept_hqd_wtw_tgb .concept}

This topic describes the major differences between Cloud Firewall and Security groups of ECS.

A security group is a distributed virtual firewall provided by ECS. It controls the traffic between ECS instances.

Cloud Firewall consists of the Internet firewall, VPC firewall, and internal firewall. These firewalls are used to provide protection for the Internet traffic, VPC networks, and ECS instances.

## Unique features of Cloud Firewall {#section_jyz_fdf_vgb .section}

Compared with security groups, Cloud Firewall supports the following unique features:

-   Supports access control on applications. For example, you can set HTTP as **Allow** in access control policy configuration, so that HTTP services can run on any port.
-   Supports access control based on domain names. For example, you can allow all ECS instances to send requests to \*.aliyun.com only.
-   Support address books. You can add multiple IP addresses, ports, or ECS instances with the same tags to an address book and use this address book in access control configuration. This simplifies your configuration.
-   Supports intrusion prevention system \(IPS\). You can use IPS to detect and fix common system vulnerabilities.
-   Prevents brute force password cracking.
-   Monitor and overall logs for blocked traffic analysis.

## Enhanced features of Cloud Firewall {#section_p52_gdf_vgb .section}

Compared with Security groups of ECS, certain features have been enhanced in Cloud Firewall. The internal firewall is based on the capabilities of security groups. You can go to the **Access Control -\> Internal Firewall** tab page to create policies or go to the **security group** page in ECS console to create rules. The policies and rules in both Cloud Firewall and ECS Security groups are automatically synchronized.

The following features of Cloud Firewall are enhanced:

-   You can release multiple policies at the same time.
-   Policy group templates are supported.
-   Security groups can be automatically created based on application groups.
-   By default, ECS instances in the same security group cannot communicate with each other.

## Internet firewall, VPC firewall, and internal firewall {#section_xgg_gdf_vgb .section}

Cloud Firewall consists of the Internet firewall, VPC firewall, and internal firewall. These firewalls are used to provide protection for the Internet traffic, VPC networks, and ECS instances.

The Internet firewall is deployed at the border between Internet and internal network, and monitors the traffic with public IP addresses.

The internal firewall works in the same way as security groups to manage the traffic between ECS instances.

The following figure shows how the Internet firewall and internal firewall work and where they are deployed in the network topology:

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/124497/155651814138798_en-US.png)

The VPC firewall is deployed at the border of the VPC networks to manage the traffic forwarded through Express Connect. The following figure shows how the VPC firewall works and where it is deployed in the network topology:

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/124497/155651814138893_en-US.png)

You can use all of the three types of firewalls to precisely control your network access activities and build three protection systems: Internet traffic protection, VPC network protection, and instance protection.

-   Cloud Firewall provides centralized access control, including inbound and outbound policies, to support more precise control of network traffic. Cloud Firewall also provides application-specific and domain name-specific access control policies for you to centrally manage VPCs and regions. You can use the **monitor** mode and address books to tune your access control policies.
-   For network traffic that requires micro-segmentation, Cloud Firewall provides distributed access control. Currently, Cloud Firewall is based on the capabilities of security groups. It offers visualized analysis of internal network traffic, allowing you to tune internal policies. The monitor mode, blocked network traffic analysis, and threat intelligence features will be soon available.

Cloud Firewall allows you to configure firewalls based on network borders to build multiple logical protection systems. This makes your maintenance work much easier. If you only need to protect the external traffic, then you can configure Internet border firewall policies \(inbound and outbound policies\) in the **south-north** direction. If you need to protect your ECS instances, you can configure internal firewall policies \(internal policies\) for ECS instances.


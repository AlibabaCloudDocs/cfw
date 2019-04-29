# FAQs {#concept_mdz_5gr_cfb .concept}

## Does Cloud Firewall apply to classic networks? {#section_dzj_zgr_cfb .section}

The north-south access control and IPS features of Cloud Firewall apply to classic networks. However, its micro-isolation feature oriented for east-west access applies only to VPCs, but not classic networks.

## Does Cloud Firewall apply to international sites outside China? {#section_kcv_1hr_cfb .section}

The current version applies only to sites in Mainland China and Hong Kong, but not international sites outside China.

## Can Cloud Firewall control the access traffic tunneled through Internet SLBs? {#section_x3w_1hr_cfb .section}

Cloud Firewall temporarily cannot protect the inbound traffic tunneled through Internet SLBs due to a certain network architecture issue. To work around this issue, we recommend that you deploy Destination Network Address Translation \(DNAT\) and intranet SLBs. In this way, the inbound traffic flows through Cloud Firewall, DNAT \(or EIP\), and intranet SLBs in sequence.

## Can Cloud Firewall control outbound access from private addresses to the Internet? {#section_yvx_dhr_cfb .section}

Cloud Firewall only controls outbound access for public IP addresses DNATed from private IP addresses or for EIP addresses bound to private IP addresses. It cannot directly control outbound access from private IP addresses.

Recommended workaround: Bind an independent EIP to the private IP address for which you want to control outbound access. Then configure access control policies on this EIP.

## Can Cloud Firewall control IPsec traffic? {#section_ily_dhr_cfb .section}

North-south traffic control policies of Cloud Firewall cannot be used to control decrypted IPsec traffic.

Recommended workaround: Regard the decrypted IPsec traffic as east-west traffic, and use east-west traffic control policies of Cloud Firewall to control the traffic.

## Can Cloud Firewall control the access traffic tunneled through Express Connect? {#section_jcz_dhr_cfb .section}

Currently, Cloud Firewall does not support this function. You can configure [security groups](../../../../intl.en-US/Security/Security groups/Create a security group.md#) to control the access traffic tunneled through Express Connect.

## Can Cloud Firewall control the access traffic tunneled through bastion hosts? {#section_nqs_wkb_yfb .section}

Currently, Cloud Firewall does not support this function.

## The traffic of the Unknown application type accounts for a large proportion of all inbound network traffic. Is this because Cloud Firewall cannot identify specific requests from the Internet? {#section_fkx_b2k_1gb .section}

There is a large amount of inbound scanning traffic from the Internet, most of which does not comply with any standard protocol. Cloud Firewall cannot identify this type of traffic and marks the traffic as unknown.

You can view logs under **Logs** \> **Access Log** or **Logs** \> **Event Log** to determine the specific sources and uses of such unknown traffic.

## On the Full Activity Search tab of the Network Traffic Analysis page, why is there a large percentage of traffic with unknown carriers in the Top Access Traffic area? {#section_qsp_22k_1gb .section}

For inbound traffic from and outbound traffic to carriers outside China, Cloud Firewall only identifies the countries to which the carriers belong and marks the carriers as unknown. You can view logs under **Logs** \> **ccess Logs** to determine the regions and carriers to which the specific IP addresses belong.

## The traffic of the Unknown application type accounts for a large proportion of all outbound network traffic. Is this because Cloud Firewall cannot identify this type of traffic? {#section_crz_tqz_2hb .section}

Outbound traffic may be blocked by destination servers, which then send back RST packets. These packets are recorded as outbound traffic. If there are a large number of RST packets, the traffic of the Unknown application type accounts for a large proportion of all outbound traffic. You can view logs under **Logs** \> **Traffic Logs** to determine whether exceptions occur in outbound traffic.


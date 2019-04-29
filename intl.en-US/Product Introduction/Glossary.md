# Glossary {#concept_mcl_ldc_5gb .concept}

## Internet Firewall {#section_o1r_vdc_5gb .section}

An Internet Firewall monitors and centrally manages the traffic between the Internet and your cloud assets. An Internet Firewall works as follows:

 ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/124630/155654000338818_en-US.png) 

The built-in Intrusion Prevention module of an Internet Firewall allows you to detect victim servers, block external connections started by your servers, and view the connections among cloud services. An Internet firewall is delivered based on the SaaS model. You can quickly enable the firewall without complex network configurations or firewall installation using an image file. Internet Firewalls are deployed in a cluster by default and support smooth scale-up.

## VPC Firewall {#section_otd_ggc_5gb .section}

A VPC firewall is a distributed firewall that monitors the traffic between two VPC networks. A VPC firewall works as follows:

 ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/124630/155654000338820_en-US.png) 

A VPC Firewall can be deployed between two VPC networks that are connected by Express Connect or are bound to the same CEN instance of the VPC network. A VPC Firewall is not created by default. You must specify two VPC networks to create a VPC Firewall.

## Security Group/Internal Firewall {#section_hct_kgc_5gb .section}

A Security Group is a distributed virtual internal firewall provided by ECS. It provides port status monitoring and packet filtering. You can use Security Group to configure access control among ECS instances. A Security Group is set for a group of ECS instances from the same region. These instances have the same security requirements and trust each other. When you create an ECS instance, you must specify at least one Security Group.

The Internal Firewall provided by Cloud Firewall IS based on Security Groups. To configure Internal Firewall policies, you can choose **Cloud Firewall** \> **Internal Firewall** or go to the Security Group configuration page in the **ECS console**. The configurations are automatically synchronized between the two platforms.

## External connections {#section_wb5_lgc_5gb .section}

Cloud Firewall analyzes the external connections started by your ECS instances. You can detect suspicious servers by monitoring the external connections data.

## Intrusion detection {#section_vcw_pgc_5gb .section}

The intrusion detection module monitors the network traffic and detects suspicious events. The module sends alerts on or directly deals with the suspicious events. Cloud Firewall integrates the intrusion detection and prevention capabilities of Alibaba Cloud that have been built over the last ten years. Cloud Firewall performs real-time data collection and analysis on the traffic passing through the firewalls. You can detect victim servers and block suspicious network activities by using Cloud Firewall.

## Open application, open port, and open public IP address {#section_ihq_qgc_5gb .section}

An open application is an application that is exposed to the Internet. For example, HTTP and SSH.

An open port is a port that is exposed to the Internet. For example, port 80 and port 22.

An open public IP address is the public IP address of an asset that is exposed to the Internet.

Cloud Firewall can identify the following types of public IP addresses:

-   EIP addresses, which can be bound to ECS instances in VPC networks, SLB instances in VPC networks, ENI instances, or NAT gateways.
-   NatPublicIp, the public IP addresses allocated to ECS instances.

## Application group {#section_odb_5gc_5gb .section}

In the east-west business visualization module, an application group is a set of applications that provide the same or similar services. For example, you can add all ECS instances that are deployed with MySQL to a database application group.

## Business group {#section_l4y_5gc_5gb .section}

In the east-west business visualization module, a business group contains all application groups related to a specific business. For example, a Web portal business group contains the Web application groups and the database application groups.

## Vulnerable application group, vulnerable business group {#section_bls_vgc_5gb .section}

A vulnerable application group is a set of applications with a specific open vulnerable port, such as port 445. Each vulnerable port corresponds to a vulnerable application group.

A vulnerable business group is a set of vulnerable application groups.

You can use vulnerable business groups and application groups to find out which ECS instances have open vulnerable ports or have accessed vulnerable ports.

Cloud Firewall automatically creates vulnerable business groups and adds vulnerable businesses to the groups.

## Independent business group, dependent business group {#section_npp_wgc_5gb .section}

In the east-west traffic visualization module, these concepts reflect the access relationships between two business groups. For example, if business group A accesses the resources in business group B, business group B is the independent group, and business group A is the dependent group.

## First visit traffic {#section_vjm_xgc_5gb .section}

The first visit traffic refers to the traffic from the source IP address to the destination IP address during the first visit within the specified period. You can analyze the cause of the first visit based on the time of the first visit, the source and destination IP addresses, and other information. The first visit traffic can be generated by intrusions or the activation of services.

## Address book {#section_mpv_xhc_5gb .section}

Cloud Firewall allows you to create address books of IP addresses or port numbers. This enables more efficient firewall configuration. You can reference an address book to quickly configure all the IP addresses or ports in this address book.

Cloud Firewall supports the following types of address books:

-   IP address books
-   Port address books
-   ECS tag address books. After you specify a group of ECS tags, Cloud Firewall automatically adds the public IP addresses of ECS instances with these tags to the specific ECS tag address book.

The following rules apply to address books:

-   Cloud Firewall has built-in global address books. You cannot modify or delete these address books.

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/124630/155654000446007_en-US.png)

-   An IP address or port number can be added to multiple address books.
-   Changes of IP addresses or port numbers in address books automatically apply to the access control policies.


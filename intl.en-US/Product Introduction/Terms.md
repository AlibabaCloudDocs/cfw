# Terms

This topic introduces the common terms in Cloud Firewall.

## Internet firewall

The Internet firewall monitors and manages the traffic between the Internet and your cloud assets in a centralized manner. The Internet firewall is deployed between the Internet and your servers. The following figure shows how the Internet firewall works.

![Internet firewall](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/124630/156689664538818_en-US.png)

The built-in intrusion prevention module of the Internet firewall allows you to detect compromised servers, block outbound connections initiated by your servers, and view the relationships among cloud services. You can enable the Internet firewall to protect your assets with a few clicks. You are not required to configure access to networks or install images. The Internet firewall is deployed in a cluster and can be smoothly scaled up and out.

## VPC firewall

A VPC firewall is a distributed firewall that monitors the traffic between two virtual private clouds \(VPCs\). A VPC firewall is deployed between two VPCs. The following figure shows how a VPC firewall works.

![VPC firewall](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/124630/156689664638820_en-US.png)

A VPC firewall must be deployed between two VPCs that are connected by Express Connect or are bound to the same Cloud Enterprise Network \(CEN\) instance. VPC firewalls are not automatically created. You must specify two VPCs to create a VPC firewall.

## security group and internal firewall

A security group is a distributed virtual internal firewall provided by Elastic Compute Service \(ECS\). It supports port status monitoring and packet filtering. You can use a security group to control access to ECS instances. A security group is a group of ECS instances in the same region. These instances have the same security requirements and trust each other. When you create an ECS instance, you must specify at least one security group for this instance.

An internal firewall implements the security group feature at the underlying layer. You can configure policies on the Internal Firewall tab of the Access Control page in the Cloud Firewall console or configure security groups in the **ECS console**. The configurations are automatically synchronized.

## outbound connection

Cloud Firewall analyzes the outbound connections initiated by your servers in Alibaba Cloud to detect suspicious servers.

## breach awareness

The breach awareness module monitors network traffic and detects suspicious events. The module sends alerts on or directly deals with the detected suspicious events. Cloud Firewall integrates the intrusion detection and prevention capabilities of Alibaba Cloud that are built over more than a decade. Cloud Firewall collects and analyzes the traffic that passes through Cloud Firewall in real time. You can use Cloud Firewall to detect compromised servers and block suspicious network activities.

## open application, open port, and open public IP address

An open application is an application that is exposed to the Internet, such as an HTTP or SSH application.

An open port is a port that is exposed to the Internet, such as port 80 or 22.

An open public IP address is the public IP address of an asset that is exposed to the Internet.

Cloud Firewall can identify the following types of public IP addresses:

-   Elastic IP addresses \(EIPs\). EIPs can be associated with the ECS instances of the VPC type, internal-facing Server Load Balancer \(SLB\) instances of the VPC type, elastic network interfaces \(ENIs\), or Network Address Translation \(NAT\) gateways.
-   Public NAT IP addresses of ECS instances.

## application group

In the east-west business visualization module, an application group is a collection of applications that provide the same or similar services. For example, you can add all ECS instances that are deployed with MySQL to a database application group.

An application is the smallest unit of east-west business visualization in Cloud Firewall. By default, an application serves as a collection of all open ports on an ECS instance. You can create an application by cloning the application of a specific port.

## business group

In the east-west business visualization module, a business group contains all application groups related to specific business. For example, a web portal business group contains web application groups and database application groups.

## vulnerable application group and vulnerable business group

A vulnerable application group is a collection of applications that have open vulnerable ports, such as port 445. Each vulnerable port corresponds to a vulnerable application group.

A vulnerable business group is a collection of vulnerable application groups.

You can use vulnerable business groups and application groups to identify the ECS instances that have open vulnerable ports or have accessed vulnerable ports.

Cloud Firewall automatically creates vulnerable business groups and adds vulnerable business to the groups.

## independent business group and dependent business group

In the east-west traffic visualization module, these terms reflect the access relationships between two business groups. For example, if Business Group A accesses the resources in Business Group B, Business Group B is the independent group, and Business Group A is the dependent group.

## first visit traffic

First visit traffic refers to the traffic from a source IP address to a destination IP address during the first visit within a specific period of time. You can identify the cause of the first visit traffic based on information including the time of the first visit and the source and destination IP addresses. The first visit traffic can be generated by intrusions or applications that are newly published.

## address book

Cloud Firewall allows you to create address books of IP addresses or port numbers. This allows you to implement flexible access control based on IP addresses or ports. When you configure an access control policy, you can use an address book to specify all the IP addresses or ports in the address book at a time.

Cloud Firewall supports the following types of address books:

-   IP address book: allows you to specify a set of IP addresses.
-   Port address book: allows you to specify a set of ports.
-   Domain name address book: allows you to specify a set of domain names.
-   Cloud address book: allows you to specify a set of IP addresses or domain names.

The following rules apply to address books:

-   Cloud Firewall has built-in global address books. You cannot modify or delete these address books.
-   One IP address or port number can be added to multiple address books.
-   If you change the IP addresses or port numbers in an address book, the changes automatically take effect for access control policies.


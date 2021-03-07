# What are the differences between common policy groups and enterprise policy groups?

Policy groups configured on an internal firewall between ECS instances are classified into common and enterprise policy groups.

-   A common policy group takes effect on the basic security groups of ECS instances. It functions as a virtual firewall to monitor connection status and filter data packets, and can be used to isolate security domains on the cloud. You can configure access control policies to allow or deny inbound and outbound traffic between ECS instances in a common policy group.
-   An enterprise policy group takes effect on the advanced security groups of ECS instances. It supports more ECS instances than a common policy group. You can configure access control policies for a large number of private IP addresses. Enterprise policy groups are ideal for enterprises that require efficient O&M on large-scale networks.

The following table lists the differences between common and enterprise policy groups.

|Feature|Common policy group|Enterprise policy group|
|-------|-------------------|-----------------------|
|VPC|Supported|Supported|
|Policy priority configuration|Supported|Not supported|
|Authorization of other policy groups|Supported|Not supported|
|Custom policy configuration to allow traffic|Supported|Supported|
|Custom policy configuration to deny traffic|Supported|Not supported \(Enterprise policy groups deny all traffic by default.\)|
|Number of private IP addresses|2,000|65,536|
|Communication between ECS instances in the same policy group|Not supported \(You must manually create policies to **allow** the communication.\)|Not supported \(You must manually create policies to **allow** the communication.\)|


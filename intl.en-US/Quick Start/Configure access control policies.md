# Configure access control policies

Cloud Firewall allows you to configure policies to specify the ports exposed to the Internet and control access between your ECS instances and the Internet. You can configure access control policies for inbound, outbound, and internal traffic.

## Procedure

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext).
2.  In the left-side navigation pane, choose **Security Policies** \> **Access Control**.
3.  On the Internet Firewall tab, click **Create Policy**.
4.  In the Create Outbound Policy dialog box that appears, [configure parameters](/intl.en-US/Access control/Access control for outbound and inbound traffic on the Internet firewall.md) to add a policy.

    -   Source Type: Select IP or Address Book.
    -   Source: Specify the traffic source. If the source type is IP, enter an IP address or CIDR block in this field.
    -   Destination Type: Specify the type of the traffic destination.
    -   Destination: Specify the traffic destination.
    -   Protocol: Select TCP, UDP, ICMP, or ANY.
    -   Port Type: Select Ports or Address Book.
    -   Ports: Specify the ports to which you want to apply this policy.
    -   Application: Select an application to which this policy applies.
    -   Policy Action: Select **Allow**, **Monitor**, or **Deny**.
    -   Description: Enter a description that helps identify this policy.
    -   Priority: Specify the priority of this policy, which defaults to Lowest.
    You can add multiple IP addresses to an address book to simplify the policy configuration. In the upper-right corner of the Access Control page, click **Address Books** to add, modify, or delete address books used in access control policies.

    On the Outbound Policies tab, you can modify, delete, or move a policy.

    **Note:** We recommend that you set the policy actions of all outbound policies to **Deny** except for those required in necessary external connections.

5.  Click **OK**.


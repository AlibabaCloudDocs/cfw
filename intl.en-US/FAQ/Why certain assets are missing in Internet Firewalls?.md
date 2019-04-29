# Why certain assets are missing in Internet Firewalls? {#concept_tbd_kcc_5gb .concept}

For those cloud products don't support enable Cloud Firewall, or the asset is only assigned with a private IP, then the Internet Firewall is unavailable to these asset, and you cannot find them in Internet Firewall setting list.

The Internet Firewall is unavailable to the cloud assets in the following situations:

-   The asset is assigned with the public IP which is not supported by Internet Firewall, such as an SLB public IP address.
-   The asset is assigned with only the private IP address.
-   The asset is not owned by the account that has purchased Cloud Firewall.

The public IP supported by Internet Firewall are as follows:

-   EIPs. You can bind EIPs to your ECS instances in VPC network, SLB instances in VPC network, ENIs, and NAT gateways.
-   ECS public IP addresses \(NatPublicIP\).


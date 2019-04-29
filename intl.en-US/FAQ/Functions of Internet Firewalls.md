# Functions of Internet Firewalls {#concept_fvm_qzb_5gb .concept}

You can enable the Internet Firewall for a single or multiple public IP addresses.

The following figure shows the routes of the network traffic when the Internet Firewall is enabled and disabled.

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/124627/155652701438816_en-US.png)

-   When the Internet Firewall is disabled, the internet traffic with public IP is forwarded to the Internal Firewall or Security Group and then to the target ECS instances, without the need to pass through the Internet Firewall.
-   When the Internet Firewall is enabled, the internet traffic with public IP is forwarded to the Internet Firewall for monitoring and filtering, then passed through Internal Firewall or Security Group and finally to the target ECS instances.


# What are the meanings of the tags of domain names on the Outbound Connections page?

The tags are automatically added by Cloud Firewall based on the Internet information in domain names or destination IP addresses. The tags include **New**, **Periodic**, **Malicious download**, **Popular website**, **Ore pooled**, and **Threat Intelligence**.

![Outbound Connections page](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/0580631061/p147097.png)

-   **New**: Cloud Firewall identifies a domain name for the first time.
-   **Periodic**: Your assets periodically communicate with a domain name or destination IP address.
-   **Malicious download**, **Ore pooled**, or **Threat Intelligence**: Cloud Firewall considers the outbound connection risky. Check whether the risk exists. If the risk exists, we recommend that you configure an access control policy. For more information, see [Outbound and inbound traffic control on the Internet firewall](/intl.en-US/Access control/Outbound and inbound traffic control on the Internet firewall.md).
-   **Popular website**: A domain name is frequently accessed by your server or business.


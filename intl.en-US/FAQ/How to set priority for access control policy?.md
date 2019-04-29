# How to set priority for access control policy? {#concept_ctc_tww_tgb .concept}

The priority of access control policies determines the order of the policies to be validated against the network traffic.

-   Internet firewall

    For inbound and outbound policies of the Internet border firewall, the greater the value, the lower the priority.

    As shown in the following figure, when a request reaches the **Cloud Firewall**, it is matched against the policies with priorities from 1 to 8. If the request matches an **Allow** policy, then it is **allowed** to pass through. If it matches a **Deny** policy, then this request/traffic is blocked.

    **Note:** The priorities of the Internet firewall policies must be unique.

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/124619/155650961538802_en-US.png)

-   Internal firewall

    The priority of internal firewall policies are similar to that of security groups. The greater the value, the lower the priority. For internal firewall policies, valid priority values are from 1 to 100. Different policies can be assigned with the same priority. For policies assigned with the same priority, **Deny** policies are applied first.



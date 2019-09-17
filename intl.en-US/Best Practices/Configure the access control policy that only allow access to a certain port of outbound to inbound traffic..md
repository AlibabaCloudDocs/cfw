# Configure the access control policy that only allow access to a certain port of outbound to inbound traffic. {#concept_c5m_qtb_kgb .task}

The outbound-inbound traffic and inbound-outbound traffic of Alibaba cloud firewall refer to Internet-oriented traffic, known as north-south traffic. You can customize the access control policy for north-south traffic via Alibaba cloud firewall access control feature, to precisely control the access traffic and to protect your network security.

For example, an ECS \(host\) IP address is 10.1.1.1, and the EIP is 200.2.2.2, you shall set that only the TCP 80 port of the host can be accessed by outbound to inbound traffic.

**Note:** Elastic IP Address \(EIP\) is a public IP address resource that can be independently purchased and owned. For more information of EIP, refer to [What are Elastic IP Addresses](../../../../reseller.en-US/Product Introduction/What are Elastic IP Addresses.md#).

## Steps {#section_f4z_qvb_kgb .section}

Access control of outbound-inbound traffic and inbound-outbound traffic allows simplified configuration process of customized IP address book. It can effectively reduce the number of policies and improve configuration efficiency.

1.  On Alibaba cloud firewall console, position to **Outbound-inbound traffic** tab in **Access control** tab.
2.  Configure the TCP 80 port of host that allows to be accessed by outboard-inbound traffic.
    -   In the new outbound-inbound policy, select **IP** for **Origin type**, and enter `0.0.0.0/0` for **Access origin**.
    -   For **Destination type**, select **IP**. Enter `200.2.2.2/32`as **Destination**.
    -   For **Protocol type**, select **TCP**.
    -   For **Destination port**, enter `80/80`.
    -   For **Application**, select **ANY**.
    -   For **Action**, select **Release**.
    -   Enter **description**. We recommend that you enter a description of the policy and its purpose.
3.  Configure the outbound-inbound access control policy that rejects all external traffic to the host.
    -   In the new outbound-inbound policy, for **Origin type**, select **IP** , and for **Access origin** enter `0.0.0.0/0`.
    -   For **Destination type**, select **IP**. Enter `0.0.0.0/0`as **Destination**.
    -   For **Protocol type**, select **ANY**.
    -   For **Destination port**, enter `0/0` to refer to all ports.
    -   For **Application**, select **ANY**.
    -   For **Action**, select **Reject**.
    -   Enter **description**. A description of the policy and its objective are recommended here.
4.  Once the policy configuration is complete, confirm the first **Release port 80** Policy priority is higher than the Second Configuration **Reject all traffic** of policy.

    **Note:** To adjust priority of the policy, refer to [Set or modify the priority of an access control policy](../../../../reseller.en-US/Security Policy/Set or modify the priority of an access control policy.md#).


## What to do next {#section_qlc_41c_kgb .section}

Once the access control policy configuration is complete, you can use the number of hits in **Access control** page to observe the condition of hits. In **Traffic log** page, you can view hits done by the policy.

![traffic log](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/92815/156868573060749_en-US.png)


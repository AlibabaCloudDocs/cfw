# Configure the access control policy that only allow access to a certain domain of inbound-outbound traffic.

The outbound-inbound traffic and inbound-outbound traffic of Alibaba cloud firewall refer to Internet-oriented traffic, known as north-south traffic. You can customize the access control policy for north-south traffic via Alibaba cloud firewall access control feature, to precisely control the access traffic and to protect your network security.

## Background information

For example, an ECS \(host\) IP address is 10.1.1.1, and the EIP is 200.2.2.2, you shall set inbound-outbound traffic so that the host can only access the domain of www.abc.com.

**Note:** Elastic IP Address \(EIP\) is a public IP address resource that can be independently purchased and owned. For more information of EIP, refer to [What is an EIP?](/intl.en-US/.md).

## Steps

1.  On Alibaba cloud firewall console, position to **Inbound-outbound traffic** tab in **Access control** tab.
2.  Configure inbound-outbound traffic so that the host can only access www.abc.com.
    -   In the new inbound-outbound policy, for **Origin type**, select **IP** and for **Access origin**, enter `200.2.2.2/32`.
    -   For **Destination type**, select **Domain name**, and for **Destination**, enter www.abc.com.

        **Note:** For **Destination type**, select **Domain name** without protocol type configuration.

    -   For **Destination port**, enter `0/0`.
    -   For **Application**, according to domain type, select **HTTP** or **HTTPS**.
    -   For **Action**, select **Release**.
    -   Enter **description information**. We recommend that you enter a description of the policy and its purpose.
3.  Configure inbound-outbound traffic to release DNS resolution.
    -   In the new inbound-outbound policy, for **Origin type**, select **IP** and for **Access origin**, enter `200.2.2.2/32`.
    -   For **Destination type**, select **IP**, and for **Destination**, enter 0.0.0.0/0.
    -   For **Protocol type**, select **UDP**.
    -   For **Destination port**, enter`53/53`.
    -   For **Application**, select **ANY**.
    -   For **Action**, select **Release**.
    -   Enter **description information**. We recommend that you enter a description of the policy and its purpose.
4.  Set traffic except the release policy to **Reject**.
    -   In the new inbound-outbound policy, for **Origin type**, select **IP**, and for **Access origin**, enter `0.0.0.0/0`.
    -   For **Destination type**, select **IP**, and for **Destination**, enter `0.0.0.0/0`.
    -   For **Protocol type**, select **ANY**.
    -   For **Destination port**, enter `0/0`.
    -   For **Application**, select **ANY**.
    -   For **Action**, select **Reject**.
    -   Enter **description information**. We recommend that you enter a description of the policy and its purpose.
5.  After the policy configuration is complete, confirm that priorities of the first **release www.abc.com domain** policy and the second **release DNS** policy are higher than the third **Reject all traffic** policy.

    **Note:** To adjust priority of the policy, refer to [Change the priority of an access control policy](/intl.en-US/Access control/Change the priority of an access control policy.md).


## What to do next

Once the access control policy configuration is complete, you can use the number of hits in **Access control** page to observe the condition of hits. In **Traffic log** page, you can view hits done by the policy.

![traffic log](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/93164/156868598860753_en-US.png)


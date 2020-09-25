# Intelligent policy delivery

Cloud Firewall provides the intelligent policy feature targeted at Internet access and external connections. With this feature, Cloud Firewall provides security policies to isolate high-risk services \(inbound traffic\) and prevent worms from spreading \(outbound traffic\), and recommends ACL policies to help you defend against security threats to networks and hosts.

## Isolation of high-risk services

The **intelligent policy** feature of Cloud Firewall provides you with the optimal ACL policy based on detected security threats in Internet access traffic. For example, if high-risk services such as SSH and RDP are enabled on IP address assets that are exposed to the Internet and are at risk of being cracked or intruded, the **intelligent policy** feature will recommend a policy. This policy allows only Internet requests sent by users in normal logon status and in commonly used logon areas, and rejects requests from other logon areas to reduce the risk of network attacks.

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext#/overview).

2.  Choose **Traffic Analysis** \> **Internet Access** \> **Open Public IP Addresses**.

3.  Find the target public IP address and click **Intelligent Policy** in the **Actions** column corresponding to the public IP address.

    On the **Intelligent Policy** page that appears, the **Recommended Intelligent Policy** section is displayed. The recommended intelligent policy specifies the **allow** or **deny** action on user IP addresses and ports.

4.  On the **Intelligent Policy** page, perform the following operations.

    -   Click **Show** to view the reason for recommending the intelligent policy.

        For example, you can see that a large number of malicious IP addresses have tried to access the SSH service of the user IP address.

    -   Click **Deliver Policy**. Choose **Security Policies** \> **Access Control** \> **Internet Firewall** \> **Inbound Policies** to view the configured defense policy.

        **Note:** Before clicking **Deliver Policy**, make sure that you understand the meaning of the recommended policy and the possible impact of this policy on your business.

        You can click **Modify**, **Delete**, **Insert**, and **Move** to perform corresponding operations on the delivered policy.


## Worm prevention

When your host suffers from worm attacks, it will be controlled by the malicious code of the worm and send requests to domain names of malicious websites. If Cloud Firewall detects that your host has initiated an external connection request, Cloud Firewall recommends a policy to you to prevent the host from accessing malicious domain names, downloading malicious programs, being controlled, and being attacked by cryptocurrency mining malware.

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext#/overview).

2.  Choose **Traffic Analysis** \> **External Connections** \> **External Domains**.

3.  Find the target external domain name, and click **Intelligent Policy** in the **Recommended Operation** column corresponding to the external domain name.

    On the **Intelligent Policy** page that appears, the **Recommended Intelligent Policy** section is displayed. The recommended intelligent policy specifies the allow or deny action on external connections.

4.  On the **Intelligent Policy** page, perform the following operations.

    -   Click **Show** to view the reason for recommending the intelligent policy.

        For example, you can see that your host has sent many malicious requests.

    -   Click **Deliver Policy**. Choose **Security Policies** \> **Access Control** \> **Internet Firewall** \> **Inbound Policies** to view the configured defense policy.

        **Note:** Before clicking **Deliver Policy**, make sure that you understand the meaning of the recommended policy and the possible impact of this policy on your business.

        You can click **Modify**, **Delete**, **Insert**, and **Move** to perform corresponding operations on the delivered policy.



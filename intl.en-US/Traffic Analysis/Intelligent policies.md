# Intelligent policies

Cloud Firewall provides intelligent ACL policies for Internet access and external connections. These policies isolate high-risk services for inbound traffic, prevent the spread of worm viruses in outbound traffic, and defend your networks and hosts against security threats.

## Isolate high-risk services

**Intelligent policies** provide you with optimal ACL policies based on security threats detected in Internet access traffic. For example, if high-risk services, such as SSH and RDP, are enabled for IP addresses exposed to the Internet, the recommended policies only allow Internet requests sent by hosts that exhibits normal logon status and from common source locations. This reduces risks of network attacks.

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext).

2.  In the left-side navigation pane, choose **Traffic Analysis** \> **Internet Access**.

3.  On the Internet Access page, click **Open Public IP Addresses**.

    ![Open public IP addresses](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/2309751161/p77567.png)

4.  Find the target public IP address and click **Intelligent Policy** in the **Actions** column.

    ![Intelligent policy](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/2309751161/p59678.png)

    The **Intelligent Policy** page displays policies recommended for the public IP address, including both **Allow** and **Deny** policies.

    ![Recommended intelligent policy](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/2309751161/p59685.png)

5.  On the **Intelligent Policy** page, you can perform the following operations:

    -   Click **Show** to view the reason why a policy is recommended.

        The following figure shows that a large number of malicious IP addresses have tried to access the SSH service of your IP address.

        ![Recommendation reason](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/3309751161/p59686.png)

    -   Choose **Deliver Policy** \> **Submit**. The recommended policy takes effect immediately. You can view delivered policies by choosing **Security Policies** \> **Access Control** \> **Internet Firewall** \> **Inbound Policies**.

        **Note:** Before you click **Deliver Policy** to deliver a recommended policy, make that you understand its content and possible service impacts.

        You can perform **Modify**, **Delete**, **Insert**, and **Move** operations on a delivered policy.


## Prevent worm attacks

Worm attacks control your host by using malicious code and cause it to send requests to the domain name of a malicious website. After Cloud Firewall detects that your host has initiated an external connection request, a recommended policy takes effect to prevent access to malicious domain name, downloads of malicious programs, virus-control over the host, and attacks by using cryptocurrency mining malware.

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext).

2.  In the left-side navigation pane, choose **Traffic Analysis** \> **Outbound Connections**.

3.  On the External Connections page, click **External Domains**.

    The page displays the external domain name list.

4.  Find the target external domain name and click **Intelligent Policy** in the **Recommended Operation** column.

    The **Intelligent Policy** page displays **Deny** policies recommended by Cloud Firewall for an IP address based on its external connections.

5.  On the **Intelligent Policy** page, you can perform the following operations:

    -   Click **Show** to view the reason why an intelligent policy is recommended.

        The following figure shows that the host has sent many requests to malicious destinations.

        ![inoutcelue](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/8286234261/p285165.png)

    -   Choose **Deliver Policy** \> **Submit**. The recommended policy takes effect immediately. You can view delivered policies by choosing **Security Policies** \> **Access Control** \> **Internet Firewall** \> **Outbound Policies**.

        ![checkinout](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/9286234261/p285175.png)

        **Note:** Before you click **Deliver Policy** to deliver a recommended policy, make sure that you understand its content and possible service impacts.

        You can perform the **Modify**, **Delete**, **Insert**, and **Move** operations on a delivered policy.



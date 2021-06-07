# Configure access control policies

Cloud Firewall allows you to configure access control policies for inbound, outbound, and internal traffic. This can reduce the risk of intrusion into your assets.

## Procedure

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext).
2.  In the left-side navigation pane, click **Access Control**.
3.  On the **Access Control** page, configure access control policies for the Internet firewall, an internal firewall, or a VPC firewall.

    You can add multiple IP addresses to an address book. This simplifies the procedure to configure access control policies. You can also click **Address Books** to add, modify, or delete IP addresses. For more information about address book management, see [Manage address books](/intl.en-US/Access control/Manage address books.md).

    -   If you want to control outbound traffic, click the **Internet Firewall** tab to create **outbound policies**.

        **Note:**

        -   We recommend that you configure the actions of outbound policies to **Deny**. This does not apply if the policies are used to allow necessary outbound connections.
        -   If the source addresses in outbound policies are internal IP addresses, you must configure a secure forward proxy. Otherwise, the outbound policies do not take effect. For more information about how to configure a secure forward proxy, see [Use secure forward proxies](/intl.en-US/Firewall Settings/Use secure forward proxies.md).
        ![Outbound Policies](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/1671303261/p263065.png)

    -   If you want to control inbound traffic, click the **Internet Firewall** tab to create **inbound policies**.

        ![Inbound Policies](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/1671303261/p263069.png)

    -   If you want to control traffic between VPCs, click the **VPC Firewall** tab to create **VPC firewall** policies.

        **Note:** The VPC Firewall feature is supported only for Cloud Firewall Enterprise Edition and Ultimate Edition.

        ![VPC Firewall tab](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/1671303261/p263071.png)



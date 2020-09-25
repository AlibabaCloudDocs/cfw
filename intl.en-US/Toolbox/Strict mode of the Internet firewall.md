# Strict mode of the Internet firewall

The strict mode of the Internet firewall blocks traffic that matches an access control policy but contains an application unknown to Cloud Firewall. Cloud Firewall identifies applications based on packet characteristics. If Cloud Firewall fails to identify the application in the traffic, it allows the traffic by default. If you want to discard traffic with unknown applications, you can enable the strict mode.

The strict mode only takes effect on traffic that matches an access control policy, regardless of whether the policy action is allow, deny, or monitor. If the traffic does not match any access control policy, the traffic is allowed even if its application is unknown.

Before you enable the strict mode on the Internet firewall, we recommend that you configure access control policies. For more information, see [Outbound and inbound traffic control on the Internet firewall](/intl.en-US/Access control/Outbound and inbound traffic control on the Internet firewall.md).

## Enable or disable the strict mode

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext).

2.  In the left-side navigation pane, choose **Security Policies** \> **Access Control**.

3.  In the upper-right corner of the **Internet Firewall** tab, click **Advanced Settings**.

    ![Advanced Settings](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/5893068951/p94528.png)

4.  In the Advanced Settings dialog box that appears, enable or disable **Internet Firewall-Strict Mode** and click **OK**.

    ![Internet Firewall - Strict Mode](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/5893068951/p94502.png)

    After the strict mode is enabled, all traffic that matches an access control policy and contains unknown applications is discarded. You can view logs of discarded traffic on the Log Audit page.


## View logs of discarded traffic

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext).

2.  In the left-side navigation pane, choose **Logs** \> **Log Audit**.

3.  Navigate to **Traffic Logs** \> **Internet Firewall** and click **Show Advanced Search**. Then, set **Application** to **Unknown** and **Policy Source** to **Access Control** and click **Search**.

    ![Logs of traffic with unknown applications](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/5893068951/p94537.png)

4.  View the logs of traffic discarded in strict mode. The policy names of these logs are **unknown\_app\_deny\_all**. You can view the time, source IP addresses, destination IP addresses, and destination ports of the discarded traffic.

    If normal traffic is discarded, we recommend that you add the application information to the request packets or disable the strict mode.



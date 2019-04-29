# Security Analysis {#concept_ljj_mk4_cfb .concept}

In Security Analysis page, you can view the **Overall protection level** of hosts and scores of the four protection items in real time. Stricter configuration of the four protection items means a higher overall protection level and stronger protection for your assets.

**Overall protection levels** include high \(H\), medium \(M\), and low \(L\). The four protection items are:

-   Security Policies
-   Risk Management
-   IPS settings
-   Asset protection

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21267/155647188411751_en-US.png)

## Security Policies {#section_qz4_545_5fb .section}

The **Security Policies** modules displays the percentage of the assets for which access control policies are configured in all your assets. The access control policies include those for outbound traffic to the Internet \(in-out traffic\) and those for inbound traffic from the Internet \(out-in traffic\).

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21267/155647188445842_en-US.png)

Click in this area to go to the **Access Control** page. On the **Inbound Traffic** and **Outbound Traffic** tab pages, you can configure access policies. The stricter the access policies are configured, the higher the score of this protection item.

## Unresolved risks {#section_mh4_xr5_5fb .section}

The **Unresolved Risks** area displays the number of abnormal activities that have not been resolved within the last **30 days** and the corresponding risk levels.

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21267/155647188445843_en-US.png)

Click in this area to go to the **Intrusion Detection** tab page of the Network Traffic Analysis page, you can view and process threat activities detected by Cloud Firewall. The earlier the intrusions are handled, the higher the score.

The **IPS Settings** area displays the status of all IPS features on Cloud Firewall.

IPS features include:

-   Interception mode or observation mode
-   Basic rules
-   Threat intelligence
-   Virtual patching

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21267/155647188445844_en-US.png)

Click in this area to go to the **Intrusion Prevention** page. On this page, you can enable or disable the interception mode, basic policies, threat intelligence, and virtual patches features of IPS.

For more information, see [Intrusion prevention policies](intl.en-US/User Guide/Security policies/Intrusion prevention policies.md#).

**Note:** You can quickly determine whether an IPS feature is enabled based on the protection status icon displayed in the lower part of the **IPS Settings** area. ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21267/155647188435248_en-US.png) indicates **Protecting**, while ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21267/155647188435249_en-US.png) indicates **Protection disabled**.

## Asset protection {#section_hyk_ws5_5fb .section}

The **Asset Protection** module displays the number of assets that have been protected by Cloud Firewall.

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21267/155647188545845_en-US.png)

Click in this area to go to the **Firewall** page. On this page, you can enable or disable Cloud Firewall protection for your assets. The more assets are protected by Cloud Firewall, the higher the score of this protection item.

For more information, see [Turn on or off the Cloud Firewall switch](intl.en-US/User Guide/Enable or disable the Cloud Firewall service.md#).

## Inbound/Outbound Internet Traffic {#section_c65_jzi_8ba .section}

The Inbound or Outbound Internet Traffic module displays trend charts for inbound traffic from and outbound traffic after Cloud Firewall protection is enabled. You can view the trends of total sessions and intercepted sessions, and locate the time point when a session is intercepted. Then, you can check whether an abnormal event occurs at the time point on the [IPS Blocking Analysis](intl.en-US/User Guide/Network traffic analysis/IPS analysis.md#) or [Operation Logs](intl.en-US/User Guide/Logs.md#section_ss2_xsq_cfb) page.

After **Cloud Firewall protection** is enabled, click **Yesterday**, **Today**, or **Seven Days** in the upper-right corner of the **Internet Inbound or Outbound Protection Trends** area to view data in the specified time range.

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21267/155647188545846_en-US.png)

You can view the following protection data for inbound or outbound traffic:

-   **Average Block Percentage**: displays the percentage of the inbound or outbound sessions intercepted by IPS or access control in all sessions in the specified time range.
-   **Relative Change of Average Blocked Sessions**: displays the change rate of the average number of intercepted sessions in the specified time range compared with the average number in the previous time range. The change rate is calculated as follows: \(Number of intercepted sessions in the current time range - Number of intercepted sessions in the previous time range\)/Number of intercepted sessions in the previous time range
-   Click a certain time on the trend chart to view the total number of sessions, number of intercepted sessions, interception percentage, and interception change rate until that time point.

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/21267/155647188545847_en-US.png)


**Note:** The **Internet Inbound or Outbound Protection Trends** area can display traffic protection trends only after **Cloud Firewall protection** is enabled. We recommend that you click **Protect All** on the Firewall page to enable Cloud Firewall protection for all assets.

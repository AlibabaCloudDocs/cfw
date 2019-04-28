# Internet access {#concept_sfl_snx_5fb .concept}

The **Internet access** tab page in the Cloud Firewall console provides an overview of normal and abnormal inbound traffic details of your assets.

You can view the open applications, ports, public IP addresses, cloud products info, inbound internet traffic, and the internet access list with details.

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/64125/155645112545775_en-US.png)

## Procedure {#section_69l_rgi_u4o .section}

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext#/overview).
2.  In the left-side navigation pane, go to **Traffic Analysis** \> **Internet Access** to check your assets' internet access activities.

    You can perform the follows operations on Internet Access page:

    -   Monitor the overview on internet access traffic, including the amounts of open applications, open ports, open public IP addresses, and cloud products.

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/64125/155645112845791_en-US.png)

        In the overview area of internet access, risky event number and total number of each item are displayed. Click the **Risky**![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/64125/155645112845792_en-US.png)or **All**![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/64125/155645112845793_en-US.png)button to go to the detailed internet access list.

    -   Monitor the inbound internet traffic, including the average traffic and peak traffic.

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/64125/155645112845799_en-US.png)

        In Inbound Internet Traffic module, you can monitor traffic rate within the selected time range.

        Click the **time** on the timeline, you can see the corresponding rankings for the most visited IPs of the inbound traffic. You can choose to display top 10, 20 or 50 inbound IPs by clicking the **Rankings of IP Addresses by Traffic** drop-down list.

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/64125/155645112845800_en-US.png)

    -   Monitor the Top 10/20/50 internet access traffic with the relevant IP address, request/response rate, and logs recorded by Cloud Firewall.

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/64125/155645112845817_en-US.png)

        Click **View Logs**, **Access Log** in Logsis displayed, and automatically filtered with Inbound direction. You can check the details on the inbound traffic, including the time of access, source/destination IP and port, access application, protocol, bytes/packets of the access traffic, and applied access control policy.

    -   Monitor the detailed inbound traffic list, including the open applications, protocols, open ports, open public IP addresses and inbound traffic of the cloud products.

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/64125/155645112845820_en-US.png)

        In **Action** column, click **View Details** to open the details page of internet access traffic.



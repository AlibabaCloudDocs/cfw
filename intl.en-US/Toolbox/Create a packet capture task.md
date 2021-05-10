# Create a packet capture task

This topic describes how to create a packet capture task. You can use the packet capture feature to capture network data packets for specific IP addresses and ports, and analyze the packets. This feature allows you to locate network exceptions, analyze attacks, and identify the security risks of network communications.

## Limits

Enterprise Edition and Ultimate Edition of Cloud Firewall support the packet capture feature. Basic Edition and Premium Edition of Cloud Firewall do not support this feature. The following list describes the quota of packet capture tasks per Alibaba Cloud account:

-   If you use Enterprise Edition of Cloud Firewall, the quota is 20 per day.
-   If you use Ultimate Edition of Cloud Firewall, the quota is 50 per day.

## Procedure

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext).

2.  In the left-side navigation pane, click **Toolbox**.

3.  In the left-side navigation pane, choose **Settings** \> **Toolbox**.

4.  On the Toolbox page, click **Capture Now** in the Packet Capture section.

5.  On the Packet Capture page, click **Create Packet Capture Task**.

    ![Create a packet capture task](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/6011460261/p269088.png)

6.  In the Create Packet Capture Task dialog box, configure the parameters and click **OK**.

    ![Create a packet capture task](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/3893068951/p63542.png)

    |Parameter|Description|
    |---------|-----------|
    |**Task Name**|The name of the packet capture task. We recommend that you enter information such as the purpose of the task.|
    |**Maximum Bytes**|The maximum number of bytes in a packet that can be captured. If the number of bytes in a packet exceeds this number, the packet is discarded.|
    |**Duration \(s\)**|The maximum duration for the packet capture task. Unit: seconds.|
    |**Protocol**|The protocol type for packet capture. Valid values:    -   All
    -   TCP
    -   UDP
    -   ICMP |
    |**Address Type**|The type of the IP address configuration.     -   IP: Only the packets that are sent to or from a specific IP address are captured. You can enter only one IP address.
    -   IP Address Pair: Only the packets that are transmitted between a specific IP address and its peer IP address are captured. You can enter only one source IP address and one destination IP address. |
    |**IP**|The IP address based on which packets are captured.|
    |**Ports**|The port based on which packets are captured.|
    |**Peer IP**|The peer IP address based on which packets are captured. **Note:** This parameter is required only when Address Type is set to IP Address Pair. |
    |**Peer Port**|The peer port based on which packets are captured. **Note:** This parameter is required only when Address Type is set to IP Address Pair. |


You can go to the Packet Capture page to view the newly created task and the status of the task.


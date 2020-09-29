# Packet capture

This topic describes how to create a packet capture task. You can enable the packet capture feature to capture network data packets for specified IP addresses and ports and analyze the packets. This feature helps you locate faults, analyze attacks, and identify security risks of network communications.

## Limits

Enterprise Edition and Ultimate Edition of Cloud Firewall support the packet capture feature. The free trial edition and Premium Edition do not support this feature. Each Alibaba Cloud account has a quota of 200 packet captures per day.

## Procedure

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext).

2.  In the left-side navigation pane, click **Toolbox**.

3.  On the Toolbox page, click **Capture Now** in the Packet Capture section.

    ![Packet Capture](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/7179531061/p142816.png)

4.  On the Packet Capture page, click **Create Packet Capture Task**.

    ![Packet capture](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/7179531061/p142822.png)

5.  In the Create Packet Capture Task dialog box, configure the required parameters and click **OK**.

    ![Create a packet capture task](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/3893068951/p63542.png)

    |Parameter|Description|
    |---------|-----------|
    |**Task Name**|The name of the packet capture task. We recommend that you enter information such as the task purpose.|
    |**Maximum Bytes**|The maximum number of bytes in a packet that can be captured. If the number of bytes in a packet exceeds this number, the packet is discarded.|
    |**Duration \(s\)**|The maximum duration for the packet capture task. Unit: seconds.|
    |**Protocol**|The protocol type for packet capture. Valid values:    -   All
    -   TCP
    -   UDP
    -   ICMP |
    |**Address Type**|The IP address type.     -   IP: Only packets came from or sent to a specified IP address are captured. You can enter only one IP address.
    -   IP Address Pair: Only packets that transmitted between specified source and destination IP addresses are captured. You can enter only one source IP address and one destination IP address. |
    |**IP**|The IP address that is specified for packet capture.|
    |**Ports**|The port that is specified for packet capture.|
    |**Peer IP**|The peer IP address that is specified for packet capture.**Note:** This parameter is required only when Address Type is set to IP Address Pair. |
    |**Peer Port**|The peer port that is specified for packet capture.**Note:** This parameter is required only when Address Type is set to IP Address Pair. |


You can go to the Packet Capture page to view the newly created packet capture task and the task status.


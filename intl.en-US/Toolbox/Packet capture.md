# Packet capture

This topic describes how to create a packet capture task. You can use the packet capture function to analyze the security of data packets sent by a specific source and identify network security risks.

## Procedure

1.  Log on to the [Cloud Firewall console](https://yundun.console.aliyun.com/?p=cfwnext#/overview).

2.  Choose **Tools** \> **Packet Capture**.

3.  Click **Create Task**.

    ![Create a packet capture task](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/3893068951/p63540.png)

4.  In the Create Packet Capture Task dialog box that appears, configure the task parameters.

    |Parameter|Description|
    |---------|-----------|
    |Task Name|The name of the packet capture task. We recommend that you use information such as the task purpose to facilitate task management.|
    |Maximum Bytes|The maximum size of a captured data packet in bytes. If the data packet size exceeds the specified value, the packet is discarded.|
    |Time Limit \(s\)|The maximum time for capturing packets. Unit: seconds.|
    |Protocol|The type of the protocol used to capture packets. Valid values: All, TCP, UDP, and ICMP.|
    |Address Type|The IP address type.     -   IP: The IP address to be filtered. Only data packets that contain the IP address are captured.
    -   IP Address Pair: The IP address pair to be filtered. Only data packets that contain the IP address pair are captured. |
    |IP|The IP address to be filtered.|
    |Port|The port number to be filtered.|
    |Peer IP|The peer IP address. **Note:** This parameter is specified only when **Address Type** is set to IP Address Pair. |
    |Peer Port|The peer port number. **Note:** This parameter is specified only when **Address Type** is set to IP Address Pair. |

    ![Create a packet capture task](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/3893068951/p63542.png)

5.  Click **OK**.


Choose **Tools** \> **Packet Capture**. On the page that appears, you can view the created packet capture task and the task status.


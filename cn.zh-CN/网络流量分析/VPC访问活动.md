# VPC访问活动

云防火墙的VPC访问活动模块为您展示VPC专有网络之间的流量信息，帮助您实时获取VPC网络流量信息，及时发现和排查异常流量，从而更快地发现和检测出攻击。VPC访问活动页面中展示的信息包括VPC间流量访问TOP排行、VPC间会话TOP排行、流量访问的开放端口和资产信息等。

您必须先开启VPC边界防火墙开关，**VPC访问活动**页面才会展示对应的流量分析数据。

关于如何开启VPC边界防火墙开关，请参见[开启防火墙](/cn.zh-CN/快速入门/开启防火墙.md)。

## 操作步骤

1.  登录[云防火墙控制台](https://yundun.console.aliyun.com/?p=cfwnext)。

2.  在左侧导航栏，选择**网络流量分析** \> **VPC访问活动**。

3.  在**VPC访问活动**页面右上角，设置查询时间范围。

    您可以直接从下拉列表中选择以下时间范围：**最近1小时**、**最近24小时**、**最近7日**，也可以自定义查询最近7日范围内任何时间段的数据。

    ![设置时间范围](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/4250432161/p237768.png)

4.  在**VPC访问活动**页面上方，设置要查看的目标VPC和已开启的VPC边界防火墙。

    ![设置VPC](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/4250432161/p237771.png)

5.  查看满足条件的VPC访问活动数据。

    您可以查看以下数据：

    -   **VPC间流量**：查看VPC专有网络入方向、出方向流量的峰值和均值数据，及对应的入方向、出方向流量数据趋势。
    -   **流量Top排行**：查看流量排名前10、20或50的流量数据和相关信息，包括流量的IP地址、流入和流出数据。
    -   **VPC间会话TOP排行**：查看VPC间会话的流量排行数据和相关信息，包括流量排行、IP会话、IP会话数、流量和端口数据。

        在**VPC间会话TOP排行**列表中，单击**查看占比**栏的**查看**，可以查看该会话中端口占比的详细数据。

    -   **开放端口占比**：查看所有开放端口占比信息。
    -   **开放端口**和**资产**明细：查看VPC间流量日志详情列表，包括VPC间流量访问的开放端口和资产的基本信息。

        您可以单击列表右上方的![下载 ](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/4335322161/p237696.png)图标，将VPC开放端口、VPC资产列表（CSV格式）下载到本地计算机进行查看和分析。

        ![VPC流量信息](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/4250432161/p58398.png)



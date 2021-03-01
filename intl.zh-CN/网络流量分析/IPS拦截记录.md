# IPS拦截记录

IPS拦截记录页面为您实时展示云防火墙拦截流量的源区域、目的IP、阻断应用、阻断来源和阻断事件详情等信息。本文介绍了IPS拦截页面展示的信息和相关操作。

## 前提条件

您需要先在入侵防御开关页面开启**基础规则**开关，云防火墙才能拦截这些流量并展示在IPS拦截记录中。

![基础规则开关](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/3417068951/p77756.png)

## 概述

**IPS拦截记录**页面为您展示了互联网拦截和VPC拦截的流量数据的详细信息，您可切换到互联网拦截或VPC拦截页签查看对应事件详情。

**说明：** 云防火墙高级版不支持展示VPC拦截页面。

![IPS拦截页面](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/3417068951/p81782.png)

## 互联网拦截页面

在互联网拦截页面，您可查看最近1小时、1天、7天、1个月内和自定义时间范围内出方向或入方向的阻断活动情况。可设置的自定义时间范围为3个月内。

![IPS拦截记录页面](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/3417068951/p77498.png)

互联网拦截页面具体包含以下模块：

-   **被阻断的源区域TOP**：展示了被云防火墙IPS功能阻断的出方向或入方向流量的来源或目的区域。
-   **阻断目的IP**：展示了被云防火墙IPS功能阻断的出方向或入方向流量的目的IP地址信息。

    单击阻断目的IP地址右侧的**查看日志**可跳转到云防火墙日志审计页面。您可在日志列表中查看该目的IP地址的目的端口、应用类型、动作等详细信息。

-   **被阻断的应用TOP**：展示了被云防火墙IPS功能阻断的出方向或入方向流量占比前5的应用类型。
-   **阻断来源TOP**：展示了云防火墙各个IPS功能模块阻断的流量占比。
-   **详细数据**：展示了所有阻断事件的详细信息，包括事件的风险级别、事件数量、源IP地址和目的IP地址等信息。

    ![阻断事件详情列表](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/3417068951/p77510.png)

    在**详细数据**模块，您可以执行以下操作：

    -   在搜索栏通过筛选风险级别、判断来源、方向和时间范围等定位到具体事件。
    -   单击**动作**栏的**详情**可打开阻断事件的详情页面，查看事件描述、攻击载荷等详细信息。

        ![IPS拦截详情页](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/7285300161/p211164.png)


## VPC拦截页面

VPC拦截页面展示了云防火墙拦截到的VPC网络之间的异常事件信息。您可以查看指定时间段内VPC拦截事件的名称、风险级别、攻击类型、攻击载荷等详细信息。

![VPC拦截](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/3417068951/p77595.png)

在VPC拦截页签，您可根据需要执行以下操作：

-   选择风险级别、防御状态、攻击类型和时间等条件后，单击**搜索**，查看符合设定条件的事件信息。
-   定位到目标事件，单击动作栏下的**详情**，查看当前事件的事件描述、规则ID、防御状态等详细信息。

    ![VPC拦截事件详情](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/3417068951/p77596.png)


## 相关文档

-   [云防火墙支持防护的范围](/intl.zh-CN/常见问题/云防火墙支持防护的范围.md)
-   [入侵防御开关](/intl.zh-CN/入侵防御/入侵防御开关.md)


# IPS阻断分析 {#concept_int_klb_kfb .concept}

云防火墙**IPS阻断分析**页面为您实时展示云防火墙阻断流量的源区域、目的IP、阻断应用、阻断来源和阻断事件详情等信息。

您可查看主机1小时、1天、7天、1个月内和自定义时间范围内的阻断活动情况。可设置的自定义时间范围为6个月内。

**IPS阻断分析**页面包含以下数据：

-   **方向**：被阻断流量的方向，云防火墙支持出/入方向流量检测。
-   **时间范围**：可筛选不同的时间段，定位到特定时间段内的IPS阻断流量数据。
-   **被阻断的源区域TOP**：显示被阻断流量的源区域地理位置分布图、阻断数量最高的前9名地区的地区名称和百分比。
-   **阻断目的IP**：显示阻断数量排名前5名的阻断流量的目的IP址。
-   **被阻断的应用TOP**：显示阻断数量排名前5名的阻断应用名称及其占比数。
-   **阻断来源TOP**：显示阻断数量排名前5名的阻断来源名称及其占比数。
-   **阻断事件列表**：显示阻断事件的详细信息。您可通过来源、出入方向、防御状态和自定义时间范围来搜索阻断事件。

## 操作步骤 {#section_x5y_g32_kfb .section}

1.  登录[云防火墙控制台](https://yundun.console.aliyun.com/?p=cfwnext#/overview)。
2.  单击导航栏**网络流量分析**打开网络流量分析页面。
3.  单击**IPS阻断分析**打开IPS阻断分析页面，查看1小时、1天、7天、1个月内或自定义时间范围内的出/入方向阻断活动情况。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/22641/154529253113416_zh-CN.png)

    在**方向**模块中单击**入方向**或**出方向**，显示对应时间范围内入方向/出方向被阻断流量相关的数据。

4.  在**阻断活动**页面查看排名前九的阻断源区域信息及占比、阻断目的IP地址、占比排名前四的被阻断应用和阻断来源类型。

## 查看被阻断的源区域TOP {#section_ajt_kbl_2gb .section}

您可在**被阻断的源区域TOP**区域查看被云防火墙IPS功能阻断的出/入方向流量排名前9的来源区域及其占比。

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/22641/154529253234685_zh-CN.png)

## 查看阻断目的IP {#section_hyy_kbl_2gb .section}

您可在**阻断目的IP**区域查看被云防火墙IPS功能阻断的出/入方向流量的目的IP地址信息。

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/22641/154529253234697_zh-CN.png)

单击阻断目的IP地址栏右侧的**查看日志**可跳转到云防火墙**日志**页面。您可在日志列表中查看该目的IP地址的目的端口、应用类型、动作类型等详细信息。

## 查看被阻断的应用TOP {#section_inz_kbl_2gb .section}

您可在**被阻断的应用TOP**区域查看被云防火墙IPS功能阻断的出/入方向流量占比最高的应用类型。

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/22641/154529253234701_zh-CN.png)

## 查看阻断来源TOP {#section_uk1_lbl_2gb .section}

您可在**被阻断的应用TOP**区域查看云防火墙各个IPS功能模块阻断的流量占比。

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/22641/154529253234705_zh-CN.png)

## 查看阻断事件详情列表 {#section_ntj_nbl_2gb .section}

您可在**IPS阻断分析**页面的阻断事件列表中查看所有阻断事件的详细信息，包括事件的风险级别、事件数量、防御状态、源/目的IP地址等信息。![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/22641/154529253234737_zh-CN.png)

-   您可在搜索栏通过筛选风险级别、来源、方向和时间范围等定位到单个事件。![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/22641/154529253234711_zh-CN.png)
-   单击**动作**栏的**详情**可打开阻断事件的详情页面，查看事件描述等详细信息。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/22641/154529253234714_zh-CN.png)


**说明：** 云防火墙检测到**高危**等级的告警事件后，请及时确认您已开启[入侵防御策略](cn.zh-CN/用户指南/安全策略/入侵防御策略.md#)。


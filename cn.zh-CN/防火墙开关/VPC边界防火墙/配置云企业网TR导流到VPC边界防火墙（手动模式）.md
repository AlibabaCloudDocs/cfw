# 配置云企业网TR导流到VPC边界防火墙（手动模式）

使用了云企业网转发路由器（TR）后，您需要配置云企业网TR与VPC边界防火墙之间的互访路由，实现VPC边界防火墙对该TR连接的两个VPC之间的流量进行防护。本文介绍如何打通云企业网转发路由器与VPC边界防火墙之间的网络。

**说明：** 完成了以下前提条件之后，您会拥有：3个VPC实例、3个Vswitch、1个弹性网卡（在ECS控制台**网络与安全** \> **弹性网卡**页面，系统默认分配名称为cfw-bonding-eni的网卡）。

1.  已在云企业网控制台创建了云企业网实例，且创建了连接云企业网网络实例用于连接两个专有网络VPC（本文中分别以`VPC-01`和`VPC-02`为例）。

    相关内容，请参见[创建云企业网实例]()。

2.  已在专有网络控制台手动创建了VPC边界防火墙的VPC实例（本文中以`Cfw-TR-manual-VPC`为例），且为该VPC实例创建了路由表、交换机。
3.  已在云防火墙控制台的**VPC边界防火墙**页面，创建了VPC边界防火墙。创建该VPC边界防火墙时，**专有网络**选择`Cfw-TR-manual-VPC`（需要创建3个交换机，其中2个交换机提供给TR网络实例连接使用，本文示例中命名分别为`TR-Vswitch-01`和`TR-VSwitch-02`，1个交换机提供给创建VPC防火墙的时候使用，本文示例中命名为`Cfw-Vswitch`）。

    相关内容，请参见[为云企业网创建VPC边界防火墙](/cn.zh-CN/防火墙开关/VPC边界防火墙/创建VPC边界防火墙.md)。


## 适用对象

云防火墙可以防护通过云企业网转发路由器打通的网络实例之间的流量，网络实例包括VPC、VBR、CCN，并为网络实例提供自动引流模式和手动引流模式。

本文档仅针对VPC边界防火墙手动引流模式的配置，适用于对多个VPC（相同地域）之间互访流量的防护。

自动引流模式下，由云防火墙自动完成由VPC到VPC边界防火墙的引流配置，无需您手动操作。

**说明：** 云防火墙支持防护云企业网TR流量的功能正在公测中。如果您需要使用该功能，请联系云防火墙售后人员开启白名单。未开启白名单的情况下，在云防火墙控制台的**VPC边界防火墙**页面，为云企业网TR企业版实例创建防火墙的按钮会置灰，并提示您先申请加入白名单。

## 步骤一：在云企业网TR中添加防火墙VPC的网络实例连接

本步骤建立VPC实例`Cfw-TR-manual-VPC`与云企业网TR企业版之间的连接。

1.  登录[云企业网管理控制台](https://cen.console.aliyun.com/)。

2.  在**云企业网实例**页面，定位到需要引流到云防火墙VPC边界防火墙的云企业网实例，并单击实例ID。

    ![云企业网实例ID](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/1940221261/p273784.png)

3.  在该云企业网实例页面**基本信息**页签中，单击**操作**列的**创建网络实例连接**或单击页面上方VPC基础信息右侧的![添加图标](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/9713413261/p281962.png)图标。

4.  在**连接网络实例**页面，设置`Cfw-TR-manual-VPC`和云企业网TR之间的连接信息。

    以下是创建网络连接实例时，关键的配置项说明。

    |配置项|如何设置|
    |---|----|
    |**实例类型**|通过云企业网连接的网络实例的类型。此处选择专有网络（VPC）。|
    |**地域**|通过云企业网连接的网络实例的地址。此处需要与创建`Cfw-TR-manual-VPC`时指定的地域保持一致。|
    |**网络实例**|通过云企业网连接的网络实例。此处选择`Cfw-TR-manual-VPC`的实例ID。|
    |**交换机**|网络连接实例可绑定的交换机。**主交换机**选择`TR-Vswitch-01`，**备交换机**`TR-VSwitch-02`。|

    其他配置项的说明，请参见[使用企业版转发路由器创建VPC连接]()。


## 步骤二：为两个VPC创建云企业网连接网络实例

您需要为`VPC-01`和`VPC-02`分别创建连接网络实例，将两个VPC加载到该云企业网中。

相关内容，请参见[使用企业版转发路由器创建VPC连接]()。

## 步骤三：为VPC-01和VPC-02创建路由

本步骤为云企业网和VPC边界防火墙之间的流量创建路由。

1.  登录[云企业网管理控制台](https://cen.console.aliyun.com/)。

2.  在**云企业网实例**页面，定位到需要引流到云防火墙VPC边界防火墙的云企业网实例，并单击实例ID。

    ![云企业网实例ID](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/1940221261/p273784.png)

3.  在该云企业网实例页面的转发路由器列表中，单击**路由表**列下的数字，打开**转发路由器路由表**页签。

    ![路由表列下的路由表数量](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/1016303261/p274280.png)

4.  单击**转发路由器路由表**页签左侧的**创建路由表**。

5.  在**创建路由表**对话框中，配置路由表的信息。

    **转发路由器**选择默认的路由器。本文示例中路由表名称设置为`Cfw-TR-RouteTable`。

    新增的路由表`Cfw-TR-RouteTable`用于转发`VPC-01`和`VPC-02`到VPC边界防火墙`Cfw-TR-manual-VPC`之间的流量。

6.  选定`Cfw-TR-RouteTable`路由表，单击**创建路由条目**。

7.  在**添加路由条目**对话框中，配置路由条目的信息。

    配置项说明：

    -   **目的地址**：选择默认地址段`0.0.0.0/0`。
    -   **是否为黑洞路由**：选择默认选项`否`。
    -   **下一跳连接**：选择防火墙VPC实例`Cfw-TR-manual-VPC`。
    本操作完成后，来自云企业网自定义路由表`Cfw-TR-RouteTable`的流量会默认指向VPC防火墙。

8.  在**转发路由器路由表**页签中，单击左侧路由表列表中的系统路由表，然后在**路由表详情**页面，单击**关联转发**。

9.  在**关联转发**页签中，删除下一跳为`VPC-01`和`VPC-02`的关联转发。

10. 在**转发路由器路由表**页签中，单击左侧路由表列表中的`Cfw-TR-RouteTable`路由表。

11. 在**路由表详情**页面中，单击**关联转发**，然后单击**创建关联转发**。

12. 在**添加关联转发**页面，**关联转发**选择`VPC-01`和`VPC-02`，单击**确定**保存该关联转发设置。

    本操作完成后，两个VPC的流量关联转发到`Cfw-TR-RouteTable`。

13. 在**转发路由器**页面中，单击左侧路由器列表中的系统路由表。

14. 在系统路由表的**路由表详情**页签中，单击**路由学习**页签。

15. 在**路由学习**页签中，创建两条路由学习，**关联连接**分别选择`VPC-01`和`VPC-02`。

    本操作会为系统路由表创建路由学习，自动同步`VPC-01`和`VPC-02`的路由。

    路由学习创建完成后，您可以在**路由条目页签**中看到自动学习的路由信息。

    ![自动学习的路由条目](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/1016303261/p274286.png)

16. 在当前的系统路由表的**路由表详情**页面中，单击**关联转发**页签。

17. 在**关联转发**页签中，单击**创建关联转发**。

18. 在**添加关联转发**对话框中，选择`Cfw-TR-manual-VPC`。


本步骤完成后，云企业网路由配置完成，流量牵引到VPC边界防火墙的VPC实例上。

## 步骤四：添加VPC路由表到云防火墙实例

本步骤将防火墙VPC实例的路由引流到云防火墙实例上。

1.  登录专有网络VPC控制台。

2.  在**路由表**页面，新建一个路由表，**专有网络**选择`Cfw-TR-manual-VPC`，名称设置为`VPC-CFW-RouteTable`。

3.  进入刚创建的路由表`VPC-CFW-RouteTable`，单击**已绑定交换机**。

4.  单击**绑定交换机**，选择交换机为`Cfw-Vswitch`。

5.  在**路由表条目**列表中，选择**自定义**页签。

6.  单击**添加自定义路由条目**，配置路由条目信息。

    关键配置项说明：

    -   **目标网段**：选择`0.0.0.0/0`。
    -   **下一跳类型**：选择`转发路由器`。
    -   **转发路由器**：选择默认项，即VPC防火墙的网络实例连接。
    本操作完成后会创建子网路由表，VPC边界防火墙出方向的流量会通过子网路由表转发到云企业网转发路由器TR。

7.  在路由表列表页面，选择防火墙VPC实例`Cfw-TR-manual-VPC`的系统路由表。

8.  在**路由条目**列表 ，单击**自定义页签**。

9.  单击**添加自定义路由条目**，配置路由条目信息。

    关键配置项说明：

    -   **目标网段**：选择0.0.0.0/0。
    -   **下一跳类型**：选择辅助弹性网卡。
    -   **辅助弹性网卡**：选择Cfw-bonding-eni。
    本步骤完成后，来自防火墙VPC实例的流量会牵引到云防火墙实例上。


## 步骤五：测试转发配置是否成功

访问[流量日志](/cn.zh-CN/日志/日志审计.md)，查看是否有来自该云企业网的流量日志。如果有相关流量日志，代表转发配置成功。


# 开启或关闭VPC边界防火墙

VPC边界防火墙能够检测和统计已连通的VPC间的通信流量数据，帮助您发现和排查异常攻击。您可以在云防火墙控制台开启或关闭VPC边界防火墙。

-   已购买了云企业网或高速通道实例，并且已使用云企业网或高速通道完成了两个VPC之间的网络互连。详细操作请参见[同账号VPC互连](/intl.zh-CN/专有网络对等连接（关闭新购）/同账号VPC互连.md)。
-   已创建VPC边界防火墙。您必须先完成创建VPC边界防火墙，才能开启或关闭VPC边界防火墙开关。更多信息，请参见[创建VPC边界防火墙](/intl.zh-CN/防火墙开关/VPC边界防火墙/创建VPC边界防火墙.md)。

只有开启VPC边界防火墙后，您才可以在**网络流量分析** \> **VPC访问活动**页面查看VPC网络间的相互访问流量。

开启VPC边界防火墙后，[ECS控制台](https://ecs.console.aliyun.com/?securityGroup/region/cn-shenzhen#/securityGroup/region/cn-shenzhen)**网络与安全** \> **安全组**页面会自动添加名称为Cloud\_Firewall\_Security\_Group的安全组和放行策略（即**授权策略**），用于放行VPC边界防火墙到ECS的入方向流量。

**说明：** Cloud\_Firewall\_Security\_Group的安全组和放行策略不可以删除，否则会导致VPC边界防火墙到ECS的入方向流量无法受到VPC边界防火墙的防护。

![自动创建安全组VPC防火墙放行规则](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/zh-CN/9246298951/p129283.png)

1.  登录[云防火墙控制台](https://yundun.console.aliyun.com/?p=cfwnext)。

2.  在左侧导航栏单击**防火墙开关**。

3.  在防火墙开关页面，单击**VPC边界防火墙**页签。

4.  在VPC边界防火墙页面，根据VPC的网络连通类型，单击**高速通道**或**云企业网**页签。

5.  定位到要操作的云防火墙实例，开启或关闭其**防火墙开关**。

    如果云防火墙实例过多，建议您使用列表上方的筛选和搜索功能，快速定位到要操作的云防火墙或VPC实例。

    ![VPC实例开关](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/zh-CN/9246298951/p59034.png)

6.  等待云防火墙开启或关闭完成，该过程一般需要数秒。


-   开启防火墙开关后，**防火墙状态**变为**开启中**，等到状态更新为**已开启**，则表示成功开启VPC边界防火墙。
-   关闭防火墙开关后，**防火墙状态**变为**关闭中**，等到状态更新为**未开启**，则表示成功关闭VPC边界防火墙。

开启VPC边界防火墙开关后，当您的VPC网络中出现互访流量时，您可以在**网络流量分析** \> **VPC访问活动**页面查看VPC访问流量的数据统计和分析结果。关于VPC访问流量的更多信息，请参见[VPC访问活动](/intl.zh-CN/网络流量分析/VPC访问活动.md)。


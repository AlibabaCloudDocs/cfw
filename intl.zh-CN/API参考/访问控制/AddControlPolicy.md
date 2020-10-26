# AddControlPolicy

调用AddControlPolicy添加访问控制策略。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cloudfw&api=AddControlPolicy&type=RPC&version=2017-12-07)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|AddControlPolicy|要执行的操作。

 取值：**AddControlPolicy**。 |
|AclAction|String|是|accept|访问控制策略中设置的流量通过云防火墙的方式。取值：

 -   **accept**：放行
-   **drop**：拒绝
-   **log**：观察 |
|ApplicationName|String|是|HTTP|访问控制策略支持的应用类型。取值：

 -   **FTP**
-   **HTTP**
-   **HTTPS**
-   **Memcache**
-   **MongoDB**
-   **MQTT**
-   **MySQL**
-   **RDP**
-   **Redis**
-   **SMTP**
-   **SMTPS**
-   **SSH**
-   **SSL**
-   **VNC**
-   **ANY**（表示所有类型的应用）

 **说明：** 支持的应用类型取值与协议类型（Proto）取值存在依赖关系。Proto为TCP协议时，ApplicationName支持选择以上所有应用类型中的任意一种；Proto为UDP、ICMP和ANY协议类型时，ApplicationName仅支持选择ANY。 |
|Description|String|是|放行所有TCP流量。|访问控制策略的描述信息。 |
|Destination|String|是|1.2.3.4/24|访问控制策略中的目的地址。取值：

 -   当DestinationType为net时，Destination为目的CIDR。

例如：1.2.3.4/24

-   当DestinationType为group时，Destination为目的地址簿名称。

例如：db\_group

-   当DestinationType为domain时，Destination为目的域名。

例如：\*.aliyuncs.com

-   当DestinationType为location时，Destination为目的区域。

例如： \["BJ11", "ZB"\] |
|DestinationType|String|是|net|访问控制策略中的目的地址类型。取值：

 -   **net**：目的网段（CIDR地址）
-   **group**：目的地址簿
-   **domain**：目的域名
-   **location**：目的区域 |
|Direction|String|是|in|访问控制策略的流量方向。取值：

 -   **in**：外对内流量访问控制
-   **out**：内对外流量访问控制 |
|NewOrder|String|是|-1|访问控制策略生效的优先级。优先级数字从1开始顺序递增，优先级数字越小，优先级越高。

 **说明：** **－1**表示优先级最低。 |
|Proto|String|是|TCP|访问控制策略中流量访问的协议类型。取值：

 -   **ANY**（任何协议）
-   **TCP**
-   **UDP**
-   **ICMP** |
|Source|String|是|1.2.3.0/24|访问控制策略中的源地址。取值：

 -   当SourceType为net时，Source为源CIDR地址。

例如：1.2.3.0/24

-   当SourceType为group时，Source为源地址簿名称。

例如：db\_group

-   当SourceType为location时，Source为源区域。

例如\["BJ11", "ZB"\] |
|SourceType|String|是|net|访问控制策略中的源地址类型。取值：

 -   **net**：源网段（CIDR）
-   **group**：源地址簿
-   **location**：源区域 |
|SourceIp|String|否|1.2.3.5|访问者源IP地址。 |
|Lang|String|否|zh|请求和接收消息的语言类型。取值：

 -   **zh**：中文
-   **en**：英文 |
|DestPort|String|否|80|访问控制策略中流量访问的目的端口。取值：

 -   当协议类型为ICMP时，DestPort取值为空。

**说明：** 协议类型为ICMP时，不支持对目的端口进行访问控制。

-   当协议类型为TCP、UDP或ANY时，并且目的端口类型（DestPortType）为group时，DestPort取值为空。

 **说明：** 访问控制策略目的端口类型选择group（目的端口地址簿）时，您无需设置具体的目的端口号。需要该访问控制策略管控的所有端口会包含在目的端口地址簿中。

 -   当协议类型为TCP、UDP或ANY时，并且目的端口类型（DestPortType）为port时，DestPort取值为目的端口号。 |
|DestPortType|String|否|port|访问控制策略中流量访问的目的端口类型。

 取值：

 -   **port**：端口
-   **group**：端口地址簿 |
|DestPortGroup|String|否|my\_port\_group|访问控制策略中访问流量的目的端口地址簿名称。

 **说明：** DestPortType设置为group时，您需要设置目的端口地址簿名称。 |
|Release|String|否|true|访问控制策略的启用状态。策略创建后默认启用该策略。取值：

 -   **true**：启用访问控制策略
-   **false**：不启用访问控制策略 |

地区编号如下：

-   中国：ZD
-   北京市：BJ11
-   天津市：TJ12
-   河北省：HB13
-   山西省：SX14
-   辽宁省：LN21
-   吉林省：JL22
-   上海市：SH31
-   江苏省：JS32
-   浙江省：ZJ33
-   安徽省：AH34
-   福建省：FJ35
-   江西省：JX36
-   山东省：SD37
-   河南省：HN41
-   湖北省：HB42
-   湖南省：HN43
-   广东省：GD44
-   海南省：HN46
-   重庆市：CQ50
-   四川省：SC51
-   贵州省：GZ52
-   云南省：YN53
-   陕西省：SX61
-   甘肃省：GS62
-   青海省：QH63
-   黑龙江省：HLJ23
-   西藏自治区：XZ54
-   广西壮族自治区：GX45
-   内蒙古自治区：NMG15
-   宁夏回族自治区：NX64
-   新疆维吾尔自治区：XJ65
-   台湾省：TW
-   香港特别行政区：HK
-   澳门特别行政区：MO
-   海外：ZB
-   亚洲（中国内地除外）：ZC
-   欧洲：EU
-   非洲：AF
-   北美洲：NA
-   南美洲：LA
-   大洋洲：OA
-   南极洲：AQ

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|AclUuid|String|00281255-d220-4db1-8f4f-c4df221ad84c|互联网边界防火墙访问控制策略的唯一标识ID。 |
|RequestId|String|CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D|返回结果的请求ID。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=AddControlPolicy
&AclAction=accept
&ApplicationName=ANY
&Description=demo_rule_1
&Destination=1.2.3.4/24
&DestinationType=net
&Direction=in
&NewOrder=-1
&Proto=TCP
&Source=1.2.3.0/24
&SourceType=net
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<AddControlPolicyResponse>
	  <RequestId>CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D</RequestId>
	  <AclUuid>00281255-d220-4db1-8f4f-c4df221ad84c</AclUuid>
</AddControlPolicyResponse>
```

`JSON` 格式

```
{
    "RequestId": "CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D",
    "AclUuid": "00281255-d220-4db1-8f4f-c4df221ad84c"
}
```

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Cloudfw)查看更多错误码。


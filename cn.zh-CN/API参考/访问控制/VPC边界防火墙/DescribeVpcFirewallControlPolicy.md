# DescribeVpcFirewallControlPolicy

调用DescribeVpcFirewallControlPolicy接口查询指定的VPC边界防火墙所有的访问控制策略信息。

**说明：** 防护每个云企业网的VPC防火墙实例和防护每个高速通道的VPC防火墙实例使用不同的访问控制策略。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cloudfw&api=DescribeVpcFirewallControlPolicy&type=RPC&version=2017-12-07)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeVpcFirewallControlPolicy|系统规定参数。

 取值：**DescribeVpcFirewallControlPolicy**。 |
|CurrentPage|String|是|1|分页查询时，显示的当前页的页码。

 默认值为1。 |
|PageSize|String|是|10|分页查询时，显示的每页数据的最大条数。

 可设置值最大为50。 |
|VpcFirewallId|String|是|vfw-a42bbb7b887148c9\*\*\*\*|VPC边界防火墙的访问控制策略组ID。您可调用DescribeVpcFirewallAclGroupList接口获取该ID。

 取值：

 -   VPC边界防火墙防护云企业网时，策略组ID使用云企业网实例ID。

例如：cen-ervw0g12b5jbw\*\*\*\*

-   VPC边界防火墙防护高速通道时，策略组ID使用VPC边界防火墙实例ID。

例如：vfw-a42bbb7b887148c9\*\*\*\* |
|Lang|String|否|zh|请求和接收消息的语言类型。

 取值：

 -   **zh**：中文
-   **en**：英文 |
|Source|String|否|10.0.1.0/24|VPC边界防火墙访问控制策略中的访问源地址。支持使用模糊查询。

 取值：

 -   当**SourceType**为`net`时，Source为访问源CIDR地址。

例如：10.0.1.0/24

-   当**SourceType**为`group`时，Source为源地址簿名称。

例如：db\_group

-   为空：表示查询所有访问控制源。

 **说明：** SourceType（即源类型）不同，访问源地址的取值也不同。 |
|Destination|String|否|10.0.3.0|VPC边界防火墙访问控制策略中的目的地址。支持模糊查询。

 取值：

 -   当**DestinationType**为`net`时，Destination为目的CIDR地址。

例如：10.0.3.0/24

-   当**DestinationType**为`domain`时，Destination为目的域名。

例如：aliyun.com

-   当**DestinationType**为`group`时，Destination为目的地址簿名称。

例如：db\_group

-   为空：查询所有访问控制策略的目的地址。

 **说明：** DestinationType（即目的类型）不同，目的地址的取值也不同。 |
|Description|String|否|test|VPC边界防火墙访问控制策略的描述信息。支持模糊查询。

 **说明：** 为空表示查询所有访问控制策略的描述信息。 |
|Proto|String|否|TCP|VPC边界防火墙访问控制策略中访问流量的协议类型。

 取值：

 -   **TCP**
-   **UDP**
-   **ICMP**
-   为空（查询所有协议类型）
-   **ANY**（查询所有协议类型） |
|AclAction|String|否|accept|VPC边界防火墙访问控制策略中设置的访问流量通过云防火墙的方式（动作）。

 取值：

 -   **accept**：放行
-   **drop**：拒绝
-   **log**：观察
-   **为空**：查询所有动作类型的访问控制策略 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Policys|Array| |VPC边界防火墙访问控制策略的信息。 |
|AclAction|String|accept|VPC边界防火墙访问控制策略中设置的访问流量通过云防火墙的方式（动作）。

 取值：

 -   **accept**：放行
-   **drop**：拒绝
-   **log**：观察 |
|AclUuid|String|00281255-d220-4db1-8f4f-c4df221a\*\*\*\*|VPC边界防火墙访问控制策略的唯一标识ID。 |
|ApplicationId|String|10\*\*|VPC边界防火墙访问控制策略中设置访问流量的应用的ID。 |
|ApplicationName|String|HTTP|VPC边界防火墙访问控制策略支持的应用类型。

 取值：

 -   **HTTP**
-   **HTTPS**
-   **MySQL**
-   **SMTP**
-   **SMTPS**
-   **RDP**
-   **VNC**
-   **SSH**
-   **Redis**
-   **MQTT**
-   **MongoDB**
-   **Memcache**
-   **SSL**
-   **ANY**（表示查询访问控制策略所有的应用类型） |
|Description|String|test|VPC边界防火墙访问控制策略的描述信息。 |
|DestPort|String|80|VPC边界防火墙访问控制策略中访问流量的目的端口。 |
|DestPortGroup|String|my\_port\_group|VPC边界防火墙访问控制策略中访问流量的目的端口地址簿名称。 |
|DestPortGroupPorts|List|\[80,443\]|目的端口地址簿中包含的端口列表。 |
|DestPortType|String|port|VPC边界防火墙访问控制策略中访问流量的目的端口类型。

 取值：

 -   **port**：端口
-   **group**：端口地址簿 |
|Destination|String|10.0.3.0/24|VPC边界防火墙访问控制策略中的目的地址。

 取值：

 -   当**DestinationType**为`net`时，Destination为目的CIDR地址。

例如：10.0.3.0/24

-   当**DestinationType**为`domain`时，Destination为目的域名。

例如：aliyuncs.com

-   当**DestinationType**为`group`时，Destination为目的地址簿名称。

例如：db\_group


 **说明：** DestinationType（即目的类型）不同，目的地址的取值也不同。 |
|DestinationGroupCidrs|List|\["10.0.4.0/24", "10.0.0.1/32"\]|VPC边界防火墙访问控制策略中目的地址簿中的网段列表。 |
|DestinationType|String|net|VPC边界防火墙访问控制策略中目的地址的类型。

 取值：

 -   **net**：目的网段
-   **group**：目的地址簿
-   **domain**：目的域名 |
|Direction|String|in|VPC边界防火墙访问控制策略的流量方向。

 取值：

 -   **in**：外对内访问流量
-   **out**：内对外访问流量 |
|HitTimes|Integer|100|VPC边界防火墙访问控制策略的命中次数。 |
|Order|Integer|1|VPC边界防火墙访问控制策略生效的优先级。

 优先级数字从1开始顺序递增，优先级数字越小，表示优先级越高。**－1**表示优先级最低。 |
|Proto|String|TCP|VPC边界防火墙访问控制策略中访问流量的协议类型。

 取值：

 -   **TCP**
-   **UDP**
-   **ICMP**
-   **ANY**（表示查询所有协议类型） |
|Source|String|10.0.6.0/24|VPC边界防火墙访问控制策略中的访问源地址。

 取值：

 -   当**SourceType**为`net`时，Source为访问源CIDR地址。

例如：10.0.6.0/24

-   当**SourceType**为`group`时，Source为源地址簿名称。

例如：db\_group


 **说明：** SourceType（即源类型）不同，访问源地址的取值也不同。 |
|SourceGroupCidrs|List|\["10.0.6.0/24", "10.0.0.2/32"\]|VPC边界防火墙访问控制策略中，源地址簿中的网段列表。 |
|SourceType|String|net|VPC边界防火墙访问控制策略中源地址类型。

 取值：

 -   **net**：源网段地址（CIDR）
-   **group**：源地址簿 |
|RequestId|String|CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D|结果的请求ID。 |
|TotalCount|String|20|VPC边界防火墙访问控制策略的总数量。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeVpcFirewallControlPolicy
&CurrentPage=1
&PageSize=10
&VpcFirewallId=vfw-a42bbb7b887148c9****
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<DescribeVpcFirewallControlPolicyResponse>
  <TotalCount>1</TotalCount>
  <PageNo>1</PageNo>
  <PageSize>10</PageSize>
  <RequestId>A08BC58F-A83D-43EB-BC31-2F0D723929CC</RequestId>
  <Policys>
        <ApplicationName>HTTP</ApplicationName>
        <Description>11</Description>
        <HitTimes>0</HitTimes>
        <DestinationType>net</DestinationType>
        <SourceType>net</SourceType>
        <Proto>TCP</Proto>
        <Order>5</Order>
        <ApplicationId>27</ApplicationId>
        <DestPortType>port</DestPortType>
        <Source>10.1.1.1/32</Source>
        <DestPort>80/80</DestPort>
        <AclAction>accept</AclAction>
        <AclUuid>53d82f0e-9bf1-4761-ab3b-a070b4811234</AclUuid>
        <Destination>10.2.1.1/32</Destination>
  </Policys>
</DescribeVpcFirewallControlPolicyResponse>
```

`JSON` 格式

```
{
    "TotalCount":1,
    "PageNo":1,
    "PageSize":10,
    "RequestId":"A08BC58F-A83D-43EB-BC31-2F0D723929CC",
    "Policys":[
        {
            "DestinationGroupCidrs":[

            ],
            "SourceGroupCidrs":[

            ],
            "ApplicationName":"HTTP",
            "Description":"11",
            "HitTimes":0,
            "DestinationType":"net",
            "SourceType":"net",
            "Proto":"TCP",
            "Order":5,
            "ApplicationId":"27",
            "DestPortType":"port",
            "Source":"10.1.1.1/32",
            "DestPort":"80/80",
            "AclAction":"accept",
            "DestPortGroupPorts":[

            ],
            "AclUuid":"53d82f0e-9bf1-4761-ab3b-a070b4811234",
            "Destination":"10.2.1.1/32"
        }
    ]
}
```


# DescribeControlPolicy

调用DescribeControlPolicy接口获取所有访问控制策略的信息。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cloudfw&api=DescribeControlPolicy&type=RPC&version=2017-12-07)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeControlPolicy|需要执行的操作。

 取值：**DescribeControlPolicy**。 |
|CurrentPage|String|是|1|分页查询时，显示的当前页的页码。

 默认值为1。 |
|Direction|String|是|in|访问控制策略控制的流量方向。取值：

 -   **in**：外对内方向的流量访问控制。
-   **out**：内对外方向的流量访问控制。 |
|PageSize|String|是|10|分页查询时，显示的每页数据的最大条数。

 可设置值最大为50。 |
|SourceIp|String|否|1.2.3.4|访问源的IP地址。 |
|Lang|String|否|zh|请求和接收消息的语言类型。取值：

 -   **zh**：中文
-   **en**：英文 |
|Source|String|否|1.2.3.5|访问控制策略中的访问源地址。支持使用模糊查询的方式进行查询。SourceType（源类型）不同，访问源地址的取值也不同。

 -   当SourceType为`net`时，访问源为IP/CIDR地址。例如：10.0.1.0/24。
-   当SourceType为`group`时，访问源为源地址簿名称。例如：db\_group为空（表示查询所有访问控制源）。
-   当SourceType为`location`时，访问源为源区域。例如：北京或beijing（支持使用中文或英文进行查询）。
-   当SourceType为`空`时，表示查询所有类型的访问源。 |
|Destination|String|否|1.2.3.0|访问控制策略中的目的地址。支持模糊查询。DestinationType（目的类型）不同，目的地址的取值也不同。

 -   当DestinationType为`net`时，目的地址为IP/CIDR地址。例如：10.0.3.0/24。
-   当DestinationType为`domain`时，目的地址为域名。例如：aliyun。
-   当DestinationType为`group`时，目的地址为地址簿的名称。例如：db\_group。
-   当DestinationType为`location`时，目的地址为目的区域。例如：北京或beijing（支持使用中文或英文进行查询）。
-   当DestinationType为`空`时，表示查询所有类型的目的地址。 |
|Description|String|否|test|访问控制策略的描述信息。支持模糊查询。

 **说明：** 为空表示查询所有策略的描述信息。 |
|Proto|String|否|TCP|访问控制策略中访问流量的协议类型。取值：

 -   **TCP**
-   **UDP**
-   **ICMP**
-   **ANY**（表示所有类型的协议）
-   **为空**（表示所有类型的协议） |
|AclAction|String|否|accept|访问控制策略中设置的流量通过云防火墙的方式（动作）。取值：

 -   **accept**：放行
-   **drop**：拒绝
-   **log**：观察
-   **为空**：所有的动作类型 |
|Release|String|否|true|访问控制策略的启用状态。策略创建后默认启用该策略。取值：

 -   **true**：启用访问控制策略
-   **false**：不启用访问控制策略 |
|AclUuid|String|否|00281255-d220-4db1-8f4f-c4df221ad84c|访问控制策略的唯一标识ID。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|PageNo|String|1|分页查询时，显示的当前页的页码。 |
|PageSize|String|10|分页查询时，显示的每页数据的最大条数。 |
|Policys|Array| |访问控制策略的信息。 |
|AclAction|String|accept|访问控制策略中设置的流量通过云防火墙的方式（动作）。取值：

 -   **accept**：放行
-   **drop**：拒绝
-   **log**：观察 |
|AclUuid|String|00281255-d220-4db1-8f4f-c4df221ad84c|访问控制策略的唯一标识ID。 |
|ApplicationId|String|10\*\*\*|访问控制策略中设置访问流量的应用ID。 |
|ApplicationName|String|HTTP|访问控制策略支持的应用类型。取值：

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
-   **ANY**（表示所有类型的应用） |
|Description|String|test|访问控制策略的描述信息。 |
|DestPort|String|80|访问控制策略中访问流量的目的端口。 |
|DestPortGroup|String|my\_port\_group|访问控制策略中流量访问的目的端口地址簿名称。 |
|DestPortGroupPorts|List|\[80,443\]|目的端口地址簿中包含的端口列表。 |
|DestPortType|String|port|访问控制策略中流量访问的目的端口类型。取值：

 -   **port**：端口
-   **group**：端口地址簿 |
|Destination|String|1.2.3.4/24|访问控制策略中的目的地址。DestinationType（目的类型）不同，目的地址的取值也不同。取值：

 -   当**DestinationType**为**net**时，目的地址为IP/CIDR地址。例如：10.0.3.0/24。
-   当**DestinationType**为**domain**时，目的地址为域名。例如：aliyuncs.com。
-   当**DestinationType**为**group**时，目的地址为地址簿的名称。例如：db\_group。
-   当**DestinationType**为**location**时，目的地址为区域名称（具体区域位置编码请参见[AddControlPolicy](~~138867~~)）。例如： \["BJ11", "ZB"\]。 |
|DestinationGroupCidrs|List|\["1.2.3.0/24", "1.2.3.1/32"\]|访问控制策略中的目的地址簿中的网段列表。 |
|DestinationGroupType|String|ip|访问控制策略中的目的地址簿类型。取值：

 -   **ip**：IP地址簿，包含一个或多个IP地址段。
-   **tag**：ECS标签地址簿，包含一个或多个ECS标签下的IP地址。
-   **domain**：域名地址簿，包含一个或多个域名地址。
-   **threat**：威胁地址簿，包含一个或多个恶意IP或域名地址。
-   **backsrc**：回源地址簿，包含一个或多个DDoS防护实例或WAF实例的回源地址。 |
|DestinationType|String|net|访问控制策略中的目的地址类型。取值：

 -   **net**：目的网段（CIDR）
-   **group**：目的地址簿
-   **domain**：目的域名
-   **location**：目的区域 |
|Direction|String|in|访问控制策略的流量方向。取值：

 -   **in**：外对内流量访问控制
-   **out**：内对外流量访问控制 |
|DnsResult|String|1.1.1.1,2.2.2.2|DNS解析结果。 |
|DnsResultTime|Long|1579261141|DNS解析的时间戳。 |
|HitTimes|Integer|100|访问控制策略的命中次数。 |
|Order|Integer|1|访问控制策略生效的优先级。

 优先级数字从1开始顺序递增，优先级数字越小，优先级越高。

 **说明：** **－1**表示优先级最低。 |
|Proto|String|TCP|访问控制策略中流量访问的安全协议类型。取值：

 -   **ANY**
-   **TCP**
-   **UDP**
-   **ICMP** |
|Release|String|true|访问控制策略的启用状态。策略创建后默认启用该策略。取值：

 -   **true**：启用访问控制策略
-   **false**：不启用访问控制策略 |
|Source|String|1.2.3.0/24|访问控制策略中的访问源地址。取值：

 -   当**SourceType**为`net`时，访问源地址为CIDR地址。例如：10.0.1.0/24。
-   当**SourceType**为`group`时，访问源地址为源地址簿名称。例如：db\_group。
-   当**SourceType**为`location`时，访问源地址为区域（具体区域位置编码请参见[AddControlPolicy](~~138867~~)）。例如： \["BJ11", "ZB"\]。 |
|SourceGroupCidrs|List|\["10.0.0.0/24", "10.0.0.1/32"\]|访问控制策略中的源地址簿中的网段列表。 |
|SourceGroupType|String|ip|访问控制策略中的源地址簿类型。取值：

 -   **ip**：IP地址簿，包含一个或多个IP地址段。
-   **tag**：ECS标签地址簿，包含一个或多个ECS标签下的IP地址。
-   **domain**：域名地址簿，包含一个或多个域名地址。
-   **threat**：威胁地址簿，包含一个或多个恶意IP或域名地址。
-   **backsrc**：回源地址簿，包含一个或多个DDoS防护实例或WAF实例的回源地址。 |
|SourceType|String|net|访问控制策略中的源地址类型。取值：

 -   **net**：源网段（CIDR地址）
-   **group**：源地址簿
-   **location**：源区域 |
|RequestId|String|CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D|结果的请求ID。 |
|TotalCount|String|100|访问控制策略的总数量。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeControlPolicy
&CurrentPage=1
&Direction=in
&PageSize=10
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<DescribeControlPolicyResponse>
  <TotalCount>58</TotalCount>
  <PageNo>1</PageNo>
  <PageSize>10</PageSize>
  <RequestId>A08BC58F-A83D-43EB-BC31-2F0D723929CC</RequestId>
  <Policys>
        <ApplicationName>RDP</ApplicationName>
        <Description>11</Description>
        <HitTimes>0</HitTimes>
        <DestinationType>net</DestinationType>
        <SourceType>net</SourceType>
        <Proto>TCP</Proto>
        <Order>5</Order>
        <ApplicationId>27</ApplicationId>
        <Direction>in</Direction>
        <DestPortType>port</DestPortType>
        <Source>1.1.1.1/32</Source>
        <DestPort>1/1</DestPort>
        <AclAction>accept</AclAction>
        <AclUuid>53d82f0e-9bf1-4761-ab3b-a070b4811234</AclUuid>
        <Destination>1.1.1.1/32</Destination>
        <DnsResult>1.1.1.1,2.2.2.2</DnsResult>
        <DnsResultTime>1579261141</DnsResultTime>
  </Policys>
</DescribeControlPolicyResponse>
```

`JSON` 格式

```
{
    "TotalCount":58,
    "PageNo":1,
    "PageSize":10,
    "RequestId":"A08BC58F-A83D-43EB-BC31-2F0D723929CC",
    "Policys":[
        {
            "DestinationGroupCidrs":[

            ],
            "SourceGroupCidrs":[

            ],
            "ApplicationName":"RDP",
            "Description":"11",
            "HitTimes":0,
            "DestinationType":"net",
            "SourceType":"net",
            "Proto":"TCP",
            "Order":5,
            "ApplicationId":"27",
            "Direction":"in",
            "DestPortType":"port",
            "Source":"1.1.1.1/32",
            "DestPort":"1/1",
            "AclAction":"accept",
            "DestPortGroupPorts":[

            ],
            "AclUuid":"53d82f0e-9bf1-4761-ab3b-a070b4811234",
            "Destination":"1.1.1.1/32",
            "DnsResult": "1.1.1.1,2.2.2.2",
            "DnsResultTime": 1579261141
        }
    ]
}
```


# DescribeControlPolicy {#doc_api_Cloudfw_DescribeControlPolicy .reference}

调用DescribeControlPolicy接口获取访问控制策略列表。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cloudfw&api=DescribeControlPolicy&type=RPC&version=2017-12-07)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeControlPolicy|系统规定参数。取值：DescribeControlPolicy。

 |
|CurrentPage|String|是|1|指定返回结果的当前页码。默认值为1。

 |
|Direction|String|是|in|访问控制策略的流量方向。

 -   **in**：外对内流量访问控制
-   **out**：内对外流量访问控制

 |
|PageSize|String|是|10|指定列表每页显示数据条数。可设置值最大为50。

 |
|AclAction|String|否|accept|安全策略的流量通过云防火墙的方式。不填表示查询所有流量访问方式的策略。

 -   **accept**：放行
-   **drop**：拒绝
-   **log**：观察

 |
|Description|String|否|test|待查询策略的描述信息。

 **说明：** 支持模糊查询，不填表示查询所有策略的描述信息。

 |
|Destination|String|否|1.2.3.0|访问控制目的地址。

 对于不同DestinationType的策略，支持以下几种模糊查询的方式：

 -   当DestinationType为net时，Destination为目的CIDR。例如：1.2.3.0/24
-   当DestinationType为domain时，Destination为目的CIDR。例如：aliyun
-   当DestinationType为group时，Destination为目的地址簿名称。例如：db\_group
-   当DestinationType为location时，Destination为目的区域，支持中文或英文的模糊查询。例如北京或beijing

 **说明：** 访问控制目的支持模糊查询，不填表示查询所有访问控制目的。

 |
|Lang|String|否|zh|指定请求和接收消息的语言类型。

 -   **zh**：中文
-   **en**：英文

 |
|Proto|String|否|TCP|策略的安全协议，不填表示查询所有协议。

 -   ANY
-   TCP
-   UDP
-   ICMP

 |
|Source|String|否|1.2.3.5|访问控制源地址。

 对于不同SourceType的策略，支持以下几种模糊查询的方式：

 -   当SourceType为net时，Source为源CIDR。例如：1.2.3.4/24
-   当SourceType为group时，Source为源地址簿名称。例如：db\_group
-   当SourceType为location时，Source为源区域，支持中文或英文的查询。例如：北京或beijing

 **说明：** 访问控制源支持模糊查询，不填表示查询所有访问控制源。

 |
|SourceIp|String|否|1.2.3.4|访问者源IP地址。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|PageNo|String|1|返回结果中显示的当前页码。

 |
|PageSize|String|10|返回结果中每页显示数据条数。

 |
|Policys| | |访问控制策略列表。

 |
|AclAction|String|accept|安全策略的流量通过云防火墙的方式。

 -   **accept**：放行
-   **drop**：拒绝
-   **log**：观察

 |
|AclUuid|String|00281255-d220-4db1-8f4f-c4df221ad84c|访问控制策略的唯一ID。

 |
|ApplicationId|String|10\*\*\*|策略中设置访问的应用ID。

 |
|ApplicationName|String|HTTP|安全策略支持的应用类型。

 支持的应用类型有以下几种:：

 -   **ANY**
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

 **说明：** **ANY**表示策略应用在所有类型的应用中。

 |
|Description|String|test|安全策略的描述信息。

 |
|DestPort|String|80|控制访问策略中流量访问的目的端口。

 |
|DestPortGroup|String|my\_port\_group|流量访问的目的端口地址簿名称。

 |
|DestPortGroupPorts| |\[80,443\]|目的端口地址簿中包含的端口列表。

 |
|DestPortType|String|port|目的端口类型。

 -   **port**：端口
-   **group**：端口地址簿

 |
|Destination|String|1.2.3.4/24|访问控制目的地址。

 -   当DestinationType为net时，Destination为目的CIDR。例如：1.2.3.4/24
-   当DestinationType为group时，Destination为目的地址簿名称。例如：db\_group
-   当DestinationType为domain时，Destination为目的域名。例如：\*.aliyuncs.com
-   当DestinationType为location时，Destination为目的区域（具体区域位置编码见后文）。例如： \["BJ11", "ZB"\]

 |
|DestinationGroupCidrs| |\["1.2.3.0/24", "1.2.3.1/32"\]|目的地址簿中的网段列表。

 |
|DestinationGroupType|String|ip|目的地址簿类型。

 -   ip：IP地址簿
-   tag：ECS标签地址簿
-   domain：域名地址簿
-   threat：威胁地址簿
-   backsrc：回源地址簿

 |
|DestinationType|String|net|目的地址类型。

 -   net：目的网段\(CIDR\)
-   group：目的地址簿
-   domain：目的域名
-   location：目的区域

 |
|Direction|String|in|访问控制策略的流量方向。

 -   **in**：外对内流量访问控制
-   **out**：内对外流量访问控制

 |
|HitTimes|Integer|100|策略命中次数统计。

 |
|Order|Integer|1|策略优先级。优先级数字从1开始顺序递增，优先级数字越小，优先级越高。

 **说明：** **－1**表示优先级最低。

 |
|Proto|String|TCP|策略的安全协议。

 -   ANY
-   TCP
-   UDP
-   ICMP

 |
|Source|String|1.2.3.0/24|访问控制源地址。

 -   当SourceType为net时，Source为源CIDR。例如：1.2.3.0/24
-   当SourceType为group时，Source为源地址簿名称。例如：db\_group
-   当SourceType为location时，Source为源区域（具体区域位置编码见后文）。例如\["BJ11", "ZB"\]

 |
|SourceGroupCidrs| |\["10.0.0.0/24", "10.0.0.1/32"\]|源地址簿中的网段列表。

 |
|SourceGroupType|String|ip|源地址簿类型:

 -   ip：IP地址簿
-   tag：ECS标签地址簿
-   domain：域名地址簿
-   threat：威胁地址簿
-   backsrc：回源地址簿

 |
|SourceType|String|net|源地址类型。

 -   net：源网段\(CIDR\)
-   group：源地址簿
-   location：源区域

 |
|RequestId|String|CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D|返回结果的请求ID。

 |
|TotalCount|String|100|返回的访问控制策略总数量。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DescribeControlPolicy
&CurrentPage=1
&Direction=in
&PageSize=10
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DescribeControlPolicy>
	  <TotalCount>58</TotalCount>
	  <RequestId>A08BC58F-A83D-43EB-BC31-2F0D723929CC</RequestId>
	  <Policys>
		    <ApplicationName>RDP</ApplicationName>
		    <Description>11</Description>
		    <HitTimes>0</HitTimes>
		    <DestinationType>net</DestinationType>
		    <SourceType>net</SourceType>
		    <Proto>TCP</Proto>
		    <Order>5</Order>
		    <DestinationGroupType></DestinationGroupType>
		    <SourceGroupType></SourceGroupType>
		    <ApplicationId>27</ApplicationId>
		    <Direction>in</Direction>
		    <DestPortType>port</DestPortType>
		    <Source>1.1.1.1/32</Source>
		    <DestPortGroup></DestPortGroup>
		    <DestPort>1/1</DestPort>
		    <AclAction>accept</AclAction>
		    <AclUuid>53d82f0e-9bf1-4761-ab3b-a070b481686a</AclUuid>
		    <Destination>1.1.1.1/32</Destination>
	  </Policys>
</DescribeControlPolicy>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"TotalCount":58,
	"RequestId":"A08BC58F-A83D-43EB-BC31-2F0D723929CC",
	"Policys":[
		{
			"DestinationGroupCidrs":[],
			"SourceGroupCidrs":[],
			"ApplicationName":"RDP",
			"Description":"11",
			"HitTimes":0,
			"DestinationType":"net",
			"SourceType":"net",
			"Proto":"TCP",
			"Order":5,
			"DestinationGroupType":"",
			"SourceGroupType":"",
			"ApplicationId":"27",
			"Direction":"in",
			"Source":"1.1.1.1/32",
			"DestPortType":"port",
			"DestPort":"1/1",
			"DestPortGroup":"",
			"AclAction":"accept",
			"DestPortGroupPorts":[],
			"AclUuid":"53d82f0e-9bf1-4761-ab3b-a070b481686a",
			"Destination":"1.1.1.1/32"
		}
	]
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.aliyun.com/status/product/Cloudfw)查看更多错误码。


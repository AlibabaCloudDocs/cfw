# ModifyControlPolicy {#doc_api_Cloudfw_ModifyControlPolicy .reference}

调用ModifyControlPolicy接口修改访问控制策略。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cloudfw&api=ModifyControlPolicy&type=RPC&version=2017-12-07)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|AclAction|String|是|accept|安全策略的流量通过云防火墙的方式。

 -   **accept**：放行
-   **drop**：拒绝
-   **log**：观察

 |
|AclUuid|String|是|00281255-d220-4db1-8f4f-c4df221ad84c|访问控制策略唯一ID。

 |
|Action|String|是|ModifyControlPolicy|系统规定参数。取值：ModifyControlPolicy。

 |
|ApplicationId|String|是|10\*\*\*|策略中设置访问的应用ID。

 |
|ApplicationName|String|是|HTTP|安全策略支持的应用类型。

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
|Description|String|是|test|安全访问控制策略的描述信息。

 |
|Destination|String|是|1.2.3.4/24|访问控制目的地址。

 -   当DestinationType为net时，Destination为目的CIDR。例如：1.2.3.4/24
-   当DestinationType为group时，Destination为目的地址簿名称。例如：db\_group
-   当DestinationType为domain时，Destination为目的域名。例如：\*.aliyuncs.com
-   当DestinationType为location时，Destination为目的区域（具体区域位置编码见后文）。例如： \["BJ11", "ZB"\]

 |
|DestinationType|String|是|net|目的地址类型。

 -   net：目的网段\(CIDR\)
-   group：目的地址簿
-   domain：目的域名
-   location：目的区域

 |
|Direction|String|是|in|访问控制策略的流量方向。

 -   **in**：外对内流量访问控制
-   **out**：内对外流量访问控制

 |
|Proto|String|是|TCP|策略的安全协议。

 -   ANY
-   TCP
-   UDP
-   ICMP

 |
|Source|String|是|1.2.3.0/24|访问控制源地址。

 -   当SourceType为net时，Source为源CIDR。例如：1.2.3.0/24
-   当SourceType为group时，Source为源地址簿名称。例如：db\_group
-   当SourceType为location时，Source为源区域（具体区域位置编码见后文）。例如\["BJ11", "ZB"\]

 |
|SourceType|String|是|net|源地址类型。

 -   net：源网段\(CIDR\)
-   group：源地址簿
-   location：源区域

 |
|DestPort|String|否|80|控制访问策略中流量访问的目的端口。

 |
|DestPortGroup|String|否|my\_port\_group|流量访问的目的端口地址簿名称。

 |
|DestPortType|String|否|port|目的端口类型。

 -   **port**：端口
-   **group**：端口地址簿

 |
|Lang|String|否|zh|指定请求和接收消息的语言类型。

 -   **zh**：中文
-   **en**：英文

 |
|SourceIp|String|否|1.2.3.5|访问者源IP地址。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D|返回结果的请求ID。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=ModifyControlPolicy
&AclAction=accept
&AclUuid=00281255-d220-4db1-8f4f-c4df221ad84c
&ApplicationName=ANY
&Description=demo_rule_1
&Destination=1.2.3.4/24
&DestinationType=net
&Direction=in
&Proto=TCP
&Source=1.2.3.0/24
&SourceType=net
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<ModifyControlPolicy>
	  <RequestId>CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D</RequestId>
</ModifyControlPolicy>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"RequestId":"CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D"
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.aliyun.com/status/product/Cloudfw)查看更多错误码。


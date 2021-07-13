# ModifyVpcFirewallControlPolicy

调用ModifyControlPolicy接口修改指定VPC防火墙策略组的访问控制策略的配置信息。

**说明：** 防护每个云企业网的VPC防火墙实例和防护每个高速通道的VPC防火墙实例使用不同的访问控制策略。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cloudfw&api=ModifyVpcFirewallControlPolicy&type=RPC&version=2017-12-07)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|ModifyVpcFirewallControlPolicy|需要执行的操作。

 取值：**ModifyVpcFirewallControlPolicy**。 |
|AclAction|String|是|accept|安全访问控制策略中访问流量通过云防火墙的方式（动作）。

 取值：

 -   **accept**：放行
-   **drop**：拒绝
-   **log**：观察 |
|AclUuid|String|是|00281255-d220-4db1-8f4f-c4df221ad84c|访问控制策略的唯一标识ID。

 修改访问控制策略时，需要提供该策略的唯一标识ID。您可调用DescribeVpcFirewallControlPolicy接口获取该ID。 |
|ApplicationName|String|是|HTTP|访问控制策略支持的应用类型。

 取值：

 -   ANY
-   FTP
-   HTTP
-   HTTPS
-   MySQL
-   SMTP
-   SMTPS
-   RDP
-   VNC
-   SSH
-   Redis
-   MQTT
-   MongoDB
-   Memcache
-   SSL
-   ANY（表示查询所有类型的应用） |
|Description|String|是|test|访问控制策略的描述信息。 |
|Destination|String|是|10.2.3.0/24|访问控制策略中的目的地址。

 -   当**DestinationType**为`net`时，Destination为目的CIDR地址。

例如：10.2.3.0/24

-   当**DestinationType**为`group`时，Destination为目的地址簿名称。

例如：db\_group

-   当**DestinationType**为`domain`时，Destination为目的域名。

例如：\*.aliyuncs.com |
|DestinationType|String|是|net|访问控制策略中的目的地址类型。

 取值：

 -   **net**：目的网段（CIDR地址）
-   **group**：目的地址簿
-   **domain**：目的域名 |
|Proto|String|是|TCP|访问控制策略中流量访问的安全协议类型。

 取值：

 -   ANY（表示查询所有协议类型）
-   TCP
-   UDP
-   ICMP |
|Source|String|是|10.2.4.0/24|访问控制策略中的源地址。

 取值：

 -   当**SourceType**为`net`时，Source为源CIDR地址。

例如：10.2.4.0/24

-   当**SourceType**为`group`时，Source为源地址簿名称。

例如：db\_group |
|SourceType|String|是|net|访问控制策略中的源地址类型。

 取值：

 -   **net**：源网段（CIDR地址）
-   **group**：源地址簿 |
|VpcFirewallId|String|是|vfw-a42bbb7b887148c9\*\*\*\*|VPC边界防火墙的ACL策略组ID。您可调用DescribeVpcFirewallAclGroupList接口获取该ID。

 -   VPC边界防火墙防护云企业网时，策略组ID使用云企业网实例ID。

例如cen-ervw0g12b5jbw\*\*\*\*

-   VPC边界防火墙防护高速通道时，策略组ID使用VPC边界防火墙实例ID。

例如vfw-a42bbb7b887148c9\*\*\*\* |
|Lang|String|否|zh|请求和接收消息的语言类型。

 取值：

 -   **zh**：中文
-   **en**：英文 |
|DestPort|String|否|80|访问控制策略中访问流量的目的端口。 |
|DestPortType|String|否|port|安全访问控制策略中访问流量的目的端口类型。

 -   **port**：端口
-   **group**：端口地址簿 |
|DestPortGroup|String|否|my\_port\_group|访问控制策略中访问流量的目的端口地址簿名称。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D|结果的请求ID。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=ModifyVpcFirewallControlPolicy
&VpcFirewallId=vfw-a42bbb7b887148c9****
&AclAction=accept
&AclUuid=00281255-d220-4db1-8f4f-c4df221ad84c
&ApplicationName=ANY
&Description=demo_rule_1
&Destination=10.2.3.0/24
&DestinationType=net
&Proto=TCP
&Source=10.2.4.0/24
&SourceType=net
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<ModifyVpcFirewallControlPolicyResponse>
  <RequestId>CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D</RequestId>
</ModifyVpcFirewallControlPolicyResponse>
```

`JSON` 格式

```
{
    "RequestId": "CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D"
}
```


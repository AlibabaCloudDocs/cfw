# CreateVpcFirewallControlPolicy

调用CreateVpcFirewallControlPolicy接口为指定VPC防火墙策略组添加访问控制策略。

**说明：** 防护云企业网的VPC防火墙实例和防护高速通道的VPC防火墙实例使用不同的访问控制策略。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cloudfw&api=CreateVpcFirewallControlPolicy&type=RPC&version=2017-12-07)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|CreateVpcFirewallControlPolicy|需要执行的操作。

 取值：**CreateVpcFirewallControlPolicy**。 |
|AclAction|String|是|accept|VPC边界防火墙访问控制策略中设置的流量通过云防火墙的方式（动作）。取值：

 -   **accept**：放行
-   **drop**：拒绝
-   **log**：观察 |
|ApplicationName|String|是|HTTP|VPC边界防火墙访问控制策略支持的应用类型。取值：

 -   **FTP**
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
-   **ANY**（表示支持所有的应用类型） |
|Description|String|是|test|VPC边界防火墙访问控制策略的描述信息。 |
|Destination|String|是|10.2.3.0/24|VPC边界防火墙访问控制策略中流量访问的目的地址。

 取值：

 -   当**DestinationType**为`net`时，**Destination**为目的CIDR地址。

例如：10.2.3.0/24

-   当**DestinationType**为`group`时，**Destination**为目的地址簿名称。

例如：db\_group

-   当**DestinationType**为`domain`时，**Destination**为目的域名。

例如：\*.aliyuncs.com |
|DestinationType|String|是|net|VPC边界防火墙访问控制策略中的目的地址类型。取值：

 -   **net**：目的网段（CIDR）
-   **group**：目的地址簿
-   **domain**：目的域名 |
|NewOrder|String|是|-1|VPC边界防火墙访问控制策略生效的优先级。

 优先级数字从1开始顺序递增，优先级数字越小，优先级越高。

 **说明：** －1表示优先级最低。 |
|Proto|String|是|TCP|VPC边界防火墙访问控制策略中流量访问的安全协议类型。取值：

 -   **ANY**（不确定具体协议类型时可设置为ANY）
-   **TCP**
-   **UDP**
-   **ICMP** |
|Source|String|是|10.2.3.0/24|VPC边界防火墙访问控制策略中的源地址。

 -   当SourceType为`net`时，Source为源CIDR。例如：10.2.3.0/24。
-   当SourceType为`group`时，Source为源地址簿名称。例如：db\_group。 |
|SourceType|String|是|net|VPC边界防火墙访问控制策略中的源地址类型。取值：

 -   **net**：源网段（CIDR）
-   **group**：源地址簿 |
|VpcFirewallId|String|是|vfw-a42bbb7b887148c9\*\*\*\*|VPC边界防火墙访问控制策略组ID。

 -   当VPC边界防火墙防护云企业网时，策略组ID使用云企业网实例ID。例如：cen-ervw5jbw1234\*\*\*\*\*。
-   当VPC边界防火墙防护高速通道时，策略组ID使用VPC边界防火墙实例ID。例如：vfw-a42bbb748c91234\*\*\*\*\*。

 **说明：** 您可以调用[DescribeVpcFirewallAclGroupList](~~159760~~)接口获取该ID。 |
|Lang|String|否|zh|请求和接收消息的语言类型。取值：

 -   **zh**：中文
-   **en**：英文 |
|DestPort|String|否|80|VPC边界防火墙访问控制策略中流量访问的目的端口。

 **说明：** 当**DestPortType**为`port`时，设置该参数。 |
|DestPortType|String|否|net|VPC边界防火墙访问控制策略中流量访问的目的端口类型。取值：

 -   **port**：端口
-   **group**：端口地址簿 |
|DestPortGroup|String|否|my\_port\_group|VPC边界防火墙访问控制策略中流量访问的目的端口地址簿名称。

 **说明：** 当**DestPortType**为`group`时，设置该参数。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|AclUuid|String|00281255-d220-4db1-8f4f-c4df221ad84c|安全访问控制策略的唯一标识ID。 |
|RequestId|String|CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D|返回结果的请求ID。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=CreateVpcFirewallControlPolicy
&VpcFirewallId=vfw-a42bbb7b887148c9****
&AclAction=accept
&ApplicationName=ANY
&Description=demo_rule_1
&Destination=10.2.3.0/24
&DestinationType=net
&NewOrder=-1
&Proto=TCP
&Source=10.2.3.0/24
&SourceType=net
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<CreateVpcFirewallControlPolicyResponse>
    <RequestId>CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D</RequestId>
    <AclUuid>00281255-d220-4db1-8f4f-c4d*********</AclUuid>
</CreateVpcFirewallControlPolicyResponse>
```

`JSON` 格式

```
{
    "RequestId": "CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D",
    "AclUuid": "00281255-d220-4db1-8f4f-c4d*********"
}
```


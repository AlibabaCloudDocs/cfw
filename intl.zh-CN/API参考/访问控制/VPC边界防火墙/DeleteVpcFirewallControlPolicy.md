# DeleteVpcFirewallControlPolicy

调用DeleteVpcFirewallControlPolicy接口删除指定VPC防火墙策略组的访问控制策略。

**说明：** 防护每个云企业网的VPC防火墙实例和防护每个高速通道的VPC防火墙实例使用不同的访问控制策略。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cloudfw&api=DeleteVpcFirewallControlPolicy&type=RPC&version=2017-12-07)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DeleteVpcFirewallControlPolicy|需要执行的操作。

 取值：**DeleteVpcFirewallControlPolicy**。 |
|AclUuid|String|是|00281255-d220-4db1-8f4f-c4df2214\*\*\*\*|VPC边界防火墙访问控制策略的唯一标识ID。

 删除安全访问控制策略时，需要提供该策略的唯一标识ID。您可调用**DescribeVpcFirewallControlPolicy**接口获取该ID。 |
|VpcFirewallId|String|是|vfw-a42bbb7b887148c91\*\*\*\*|VPC边界防火墙的访问控制策略组ID。您可调用**DescribeVpcFirewallAclGroupList**接口获取该ID。

 取值：

 -   VPC边界防火墙防护云企业网时，策略组ID使用云企业网实例ID。

例如：cen-ervw0g12b5jbw\*\*\*\*

-   VPC边界防火墙防护高速通道时，策略组ID使用VPC边界防火墙实例ID。

例如：vfw-a42bbb7b887148c9\*\*\*\* |
|Lang|String|否|zh|请求和接收消息的语言类型。

 -   **zh**：中文
-   **en**：英文 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D|结果的请求ID。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DeleteVpcFirewallControlPolicy
&VpcFirewallId=vfw-a42bbb7b887148c9****
&AclUuid=00281255-d220-4db1-8f4f-c4df221ad84c
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<DeleteVpcFirewallControlPolicyResponse>
  <RequestId>CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D</RequestId>
</DeleteVpcFirewallControlPolicyResponse>
```

`JSON` 格式

```
{
    "RequestId": "CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D"
}
```


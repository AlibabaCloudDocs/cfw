# DescribeVpcFirewallPolicyPriorUsed

调用DescribeVpcFirewallPolicyPriorUsed接口查询指定VPC防火墙策略组访问控制策略优先级生效范围。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cloudfw&api=DescribeVpcFirewallPolicyPriorUsed&type=RPC&version=2017-12-07)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeVpcFirewallPolicyPriorUsed|系统规定参数。

 取值：**DescribeVpcFirewallPolicyPriorUsed**。 |
|VpcFirewallId|String|是|vfw-a42bbb7b887148c9\*\*\*\*|VPC边界防火墙的访问控制策略组ID。您可调用DescribeVpcFirewallAclGroupList接口获取该ID。

 取值：

 -   VPC边界防火墙防护云企业网时，策略组ID使用云企业网实例ID。

例如cen-ervw0g12b5jbw\*\*\*\*

-   VPC边界防火墙防护高速通道时，策略组ID使用VPC边界防火墙实例ID。

例如vfw-a42bbb7b887148c9\*\*\*\* |
|Lang|String|否|zh|请求和接收消息的语言类型。

 取值：

 -   **zh**：中文
-   **en**：英文 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|End|Integer|150|访问控制策略生效的优先级最低值。 |
|RequestId|String|CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D|结果的请求ID。 |
|Start|Integer|1|访问控制策略生效的优先级最高值。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeVpcFirewallPolicyPriorUsed
&VpcFirewallId=vfw-a42bbb7b887148c9****
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<DescribeVpcFirewallPolicyPriorUsedResponse>
  <RequestId>CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D</RequestId>
  <Start>1</Start>
  <End>150</End>
</DescribeVpcFirewallPolicyPriorUsedResponse>
```

`JSON` 格式

```
{
    "RequestId": "CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D",
    "Start": 1,
    "End": 150
}
```


# ResetVpcFirewallRuleHitCount

调用ResetVpcFirewallRuleHitCount接口，将指定的VPC防火墙策略组访问控制策略的命中计数清零。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cloudfw&api=ResetVpcFirewallRuleHitCount&type=RPC&version=2017-12-07)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|ResetVpcFirewallRuleHitCount|系统规定的参数。

 取值：**ResetVpcFirewallRuleHitCount**。 |
|AclUuid|String|是|00281255-d220-4db1-8f4f-c4df221ad84c|访问控制策略的唯一标识ID。

 删除访问控制策略时，需要提供该策略的唯一标识ID。您可调用DescribeVpcFirewallControlPolicy接口获取该ID。 |
|Lang|String|否|zh|请求和接收消息的语言类型。

 取值：

 -   **zh**：中文
-   **en**：英文 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D|结果的请求ID。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=ResetVpcFirewallRuleHitCount
&AclUuid=00281255-d220-4db1-8f4f-c4df221a1234
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<ResetVpcFirewallRuleHitCountResponse>
  <RequestId>CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D</RequestId>
</ResetVpcFirewallRuleHitCountResponse>
```

`JSON` 格式

```
{
    "RequestId": "CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D"
}
```


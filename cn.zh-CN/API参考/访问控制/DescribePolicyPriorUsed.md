# DescribePolicyPriorUsed

调用DescribePolicyPriorUsed接口查询访问控制策略优先级生效范围。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cloudfw&api=DescribePolicyPriorUsed&type=RPC&version=2017-12-07)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribePolicyPriorUsed|系统规定参数。取值：**DescribePolicyPriorUsed**。 |
|Direction|String|是|in|访问控制策略的流量方向。

 取值：

 -   **in**：外对内流量。
-   **out**：内对外流量。 |
|SourceIp|String|否|1.2.3.4|访问者源IP地址。 |
|Lang|String|否|zh|请求和接收消息的语言类型。

 取值：

 -   **zh**：中文
-   **en**：英文 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|End|Integer|150|访问控制策略生效的最低优先级。 |
|RequestId|String|CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D|结果的请求ID。 |
|Start|Integer|1|访问控制策略生效的最高优先级。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribePolicyPriorUsed
&Direction=in
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<DescribePolicyPriorUsedResponse>
	  <RequestId>CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D</RequestId>
	  <Start>1</Start>
	  <End>150</End>
</DescribePolicyPriorUsedResponse>
```

`JSON` 格式

```
{
    "RequestId": "CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D",
    "Start": 1,
    "End": 150
}
```


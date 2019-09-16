# DescribePolicyPriorUsed {#doc_api_Cloudfw_DescribePolicyPriorUsed .reference}

调用DescribePolicyPriorUsed接口查询访问控制策略优先级使用范围。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cloudfw&api=DescribePolicyPriorUsed&type=RPC&version=2017-12-07)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribePolicyPriorUsed|系统规定参数。取值：DescribePolicyPriorUsed。

 |
|Direction|String|是|in|访问控制策略的流量方向。

 -   **in**：外对内流量访问控制
-   **out**：内对外流量访问控制

 |
|Lang|String|否|zh|指定请求和接收消息的语言类型。

 -   **zh**：中文
-   **en**：英文

 |
|SourceIp|String|否|1.2.3.4|访问者源IP地址。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|End|Integer|150|访问控制策略优先级最低值。

 |
|RequestId|String|CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D|返回结果的请求ID。

 |
|Start|Integer|1|访问控制策略优先级最高值。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DescribePolicyPriorUsed
&Direction=in
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DescribePolicyPriorUsed>
	  <RequestId>CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D</RequestId>
	  <Start>1</Start>
	  <End>150</End>
</DescribePolicyPriorUsed>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"End":150,
	"Start":1,
	"RequestId":"CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D"
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.aliyun.com/status/product/Cloudfw)查看更多错误码。


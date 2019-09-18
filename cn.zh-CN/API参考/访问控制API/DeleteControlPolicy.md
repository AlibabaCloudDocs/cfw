# DeleteControlPolicy {#doc_api_Cloudfw_DeleteControlPolicy .reference}

调用DeleteControlPolicy接口删除访问控制策略。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cloudfw&api=DeleteControlPolicy&type=RPC&version=2017-12-07)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|AclUuid|String|是|00281255-d220-4db1-8f4f-c4df221ad84c|指定待删除的安全访问控制策略唯一ID。可通过DescribeControlPolicy接口获取安全策略的ID。

 |
|Action|String|是|DeleteControlPolicy|系统规定参数。取值：DeleteControlPolicy。

 |
|Direction|String|是|in|指定待删除安全访问控制策略的流量方向。

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
|RequestId|String|CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D|返回结果的请求ID。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DeleteControlPolicy
&AclUuid=00281255-d220-4db1-8f4f-c4df221ad84c
&Direction=in
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<RequestId>CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D</RequestId>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"RequestId":"CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D"
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.aliyun.com/status/product/Cloudfw)查看更多错误码。


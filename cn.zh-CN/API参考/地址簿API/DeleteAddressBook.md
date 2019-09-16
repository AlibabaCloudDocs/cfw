# DeleteAddressBook {#doc_api_Cloudfw_DeleteAddressBook .reference}

调用DeleteAddressBook接口删除访问控制地址簿。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cloudfw&api=DeleteAddressBook&type=RPC&version=2017-12-07)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DeleteAddressBook|系统规定参数。取值：DeleteAddressBook。

 |
|GroupUuid|String|是|0657ab9d-fe8b-4174-b2a6-6baf358ea4ad|地址簿唯一ID。指定待删除地址簿的ID。

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

http(s)://[Endpoint]/?Action=DeleteAddressBook
&GroupUuid=0657ab9d-fe8b-4174-b2a6-6baf358ea4ad
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DeleteAddressBook>
	  <RequestId>850A84D6-0DE4-4797-A1E8-00090125EEB1</RequestId>
</DeleteAddressBook>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"RequestId":"850A84D6-0DE4-4797-A1E8-00090125EEB1"
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.aliyun.com/status/product/Cloudfw)查看更多错误码。


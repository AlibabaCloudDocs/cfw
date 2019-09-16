# ModifyAddressBook {#doc_api_Cloudfw_ModifyAddressBook .reference}

调用ModifyAddressBook接口修改访问控制的地址簿。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cloudfw&api=ModifyAddressBook&type=RPC&version=2017-12-07)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|ModifyAddressBook|系统规定参数。取值：ModifyAddressBook。

 |
|Description|String|是|DEMO地址簿|地址簿的描述信息。

 |
|GroupName|String|是|demo\_address\_book|地址簿名称。

 |
|GroupUuid|String|是|0657ab9d-fe8b-4174-b2a6-6baf358ea4ad|地址簿唯一ID。

 |
|AddressList|String|否|1.1.1.1/32, 2.2.2.0/24|地址列表，多个地址间用英文逗号分隔。

 **说明：** 当GroupType为ip、port或domain时必须设置。

 -   当GroupType为ip时，地址列表中填写IP地址。例如：1.2.3.4/32, 1.2.3.0/24
-   当GroupType为port时，地址列表中填写端口或端口范围。例如：100/200, 80
-   当GroupType为domain时，地址列表中填写域名。例如：demo1.aliyun.com, demo2.aliyun.com

 |
|AutoAddTagEcs|String|否|1|是否自动添加新匹配标签的ECS公网IP到地址簿。

 -   **1**：表示自动添加
-   **0**：表示不自动添加

 |
|Lang|String|否|zh|指定请求和接收消息的语言类型。

 -   **zh**：中文
-   **en**：英文

 |
|SourceIp|String|否|1.2.3.4|访问者源IP地址。

 |
|TagList.N.TagKey|String|否|key1|待匹配的ECS标签Key。

 |
|TagList.N.TagValue|String|否|value1|待匹配的ECS标签值。

 |
|TagRelation|String|否|and|多个标签间的关系。

 -   **and**：多个标签间为“与”关系，即同时匹配多个标签的ECS公网IP才会被加入地址簿。
-   **or**：多个标签间为“或”关系，即只要匹配一个标签的ECS公网IP就会被加入地址簿。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D|返回结果的请求ID。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=ModifyAddressBook
&GroupUuid=0657ab9d-fe8b-4174-b2a6-6baf358ea4ad
&Description=DEMO地址簿
&GroupName=demo_address_book
&GroupType=ip
&AddressList=1.1.1.1/32,2.2.2.0/24
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<ModifyAddressBook>
	  <RequestId>CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D</RequestId>
</ModifyAddressBook>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"RequestId":"CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D"
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.aliyun.com/status/product/Cloudfw)查看更多错误码。


# AddAddressBook

调用AddAddressBook接口添加安全访问控制地址簿，包括IP地址簿、ECS标签地址簿、端口地址簿和域名地址簿。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cloudfw&api=AddAddressBook&type=RPC&version=2017-12-07)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|AddAddressBook|系统规定参数。取值：AddAddressBook。 |
|Description|String|是|DEMO地址簿|地址簿的描述信息。 |
|GroupName|String|是|demo\_address\_book|地址簿的名称。 |
|GroupType|String|是|ip|地址簿的类型，可选值包括：

 -   **ip**：IP地址簿
-   **domain**：域名地址簿
-   **port**：端口地址簿
-   **tag**：ECS标签地址簿 |
|AddressList|String|否|1.2.3.4/32, 1.2.3.0/24|地址簿的地址列表，多个地址间用英文逗号分隔。

 **说明：** 当GroupType为ip、port或domain时必须设置。

 -   当GroupType为ip时，地址列表中填写IP地址。例如：1.2.3.4/32, 1.2.3.0/24
-   当GroupType为port时，地址列表中填写端口或端口范围。例如：80, 100/200
-   当GroupType为domain时，地址列表中填写域名。例如：demo1.aliyun.com, demo2.aliyun.com |
|AutoAddTagEcs|String|否|1|是否自动添加新匹配标签的ECS公网IP到地址簿。

 -   **1**：表示自动添加
-   **0**：表示不自动添加 |
|Lang|String|否|zh|请求和接收消息的语言类型。

 -   **zh**：中文
-   **en**：英文 |
|SourceIp|String|否|1.2.3.4|访问者源IP地址。 |
|TagList.N.TagKey|String|否|key1|待匹配的ECS标签Key。 |
|TagList.N.TagValue|String|否|value1|待匹配的ECS标签值。 |
|TagRelation|String|否|and|待匹配的多个ECS标签间的关系。

 -   **and**：多个标签间为“与”关系，即同时匹配多个标签的ECS公网IP才会被加入地址簿。
-   **or**：多个标签间为“或”关系，即只要匹配一个标签的ECS公网IP就会被加入地址簿。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|GroupUuid|String|f04ac7ce-628b-4cb7-be61-310222b718e8|添加成功后返回的地址簿唯一标识ID。 |
|RequestId|String|CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D|结果的请求ID。 |

## 示例

请求示例

```

http(s)://[Endpoint]/?Action=AddAddressBook
&Description=DEMO地址簿
&GroupName=demo_address_book
&GroupType=ip
&AddressList=1.2.3.4/32,1.2.3.0/24
&<公共请求参数>

```

正常返回示例

`XML` 格式

```
<AddAddressBook>
	  <RequestId>B2841452-CB8D-4F7D-B247-38E1CF7334F8</RequestId>
	  <GroupUuid>0580bbd0-24cd-47ae-9e5a-f5a099251e32</GroupUuid>
    </AddAddressBook>
```

`JSON` 格式

```
{
	"RequestId":"B2841452-CB8D-4F7D-B247-38E1CF7334F8",
	"GroupUuid":"0580bbd0-24cd-47ae-9e5a-f5a099251e32"
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Cloudfw)查看更多错误码。


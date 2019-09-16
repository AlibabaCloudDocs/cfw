# DescribeAddressBook {#doc_api_Cloudfw_DescribeAddressBook .reference}

调用DescribeAddressBook接口查询访问控制地址簿的详细信息。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cloudfw&api=DescribeAddressBook&type=RPC&version=2017-12-07)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeAddressBook|系统规定参数。取值：DescribeAddressBook。

 |
|ContainPort|String|否|80|查询包含指定端口的地址簿, 仅当**GroupType**为**port**时有效。

 |
|CurrentPage|String|否|1|指定返回结果的当前页码。默认值为1。

 |
|GroupType|String|否|ip|待查询地址簿类型, 可选值包括：

 -   **ip**：IP地址簿
-   **domain**：域名地址簿
-   **port**：端口地址簿
-   **tag**：ECS标签地址簿

 |
|Lang|String|否|zh|指定请求和接收消息的语言类型。

 -   **zh**：中文
-   **en**：英文

 |
|PageSize|String|否|50|指定列表每页显示数据条数。可设置值最大为50。

 |
|Query|String|否|1.2.3.0|搜索条件，指定待搜索地址簿信息。

 |
|SourceIp|String|否|1.2.3.4|访问者源IP地址。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|Acls| | |地址簿列表。

 |
|AddressList| |\[ "1.2.3.4/32", "1.2.3.5/0", "1.2.3.6/32" \]|返回地址簿列表。

 |
|AddressListCount|Integer|3|返回的地址簿列表中地址的个数。

 |
|AutoAddTagEcs|Integer|1|是否自动添加新匹配标签的ECS公网IP到地址簿。

 -   **1**：表示自动添加
-   **0**：表示不自动添加

 |
|Description|String|DEMO地址簿|地址簿的描述信息。

 |
|Global|Integer|0|是否是全局地址簿。

 -   **1**：是全局地址簿
-   **0**：非全局地址簿

 |
|GroupName|String|demo\_address\_book|地址簿名称。

 |
|GroupType|String|ip|地址簿类型, 可选值包括：

 -   **ip**：IP地址簿
-   **domain**：域名地址簿
-   **port**：端口地址簿
-   **tag**：ECS标签地址簿

 |
|GroupUuid|String|f04ac7ce-628b-4cb7-be61-310222b718e8|地址簿唯一ID。

 |
|ReferenceCount|Integer|3|地址簿被引用次数。

 |
|TagList| | |地址簿标签列表。

 |
|TagKey|String|key1|待匹配的ECS标签Key。

 |
|TagValue|String|value1|待匹配的ECS标签值。

 |
|TagRelation|String|and|多个标签间的关系。

 -   **and**：多个标签间为“与”关系，即同时匹配多个标签的ECS公网IP才会被加入地址簿。
-   **or**：多个标签间为“或”关系，即只要匹配一个标签的ECS公网IP就会被加入地址簿。

 |
|PageNo|String|1|返回结果中显示的当前页码。

 |
|PageSize|String|10|返回结果中每页显示数据条数。

 |
|RequestId|String|B36F150A-1E27-43AA-B72C-D2AC712F09DA|返回结果的请求ID。

 |
|TotalCount|String|100|返回数据的总条数。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DescribeAddressBook
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DescribeAddressBook>
	  <TotalCount>123</TotalCount>
	  <PageSiNo>1</PageSiNo>
	  <PageSize>1</PageSize>
	  <RequestId>B36F150A-1E27-43AA-B72C-D2AC712F09DA</RequestId>
	  <Acls>
		    <Description>9-3IP地址簿</Description>
		    <GroupType>ip</GroupType>
		    <AddressList>1.1.1.1/32</AddressList>
		    <AddressList>0.0.0.0/0</AddressList>
		    <AddressList>10.0.0.217/32</AddressList>
		    <GroupName>9-3IP地址簿</GroupName>
		    <AutoAddTagEcs>0</AutoAddTagEcs>
		    <TagValue></TagValue>
		    <TagRelation></TagRelation>
		    <ReferenceCount>0</ReferenceCount>
		    <TagKey></TagKey>
		    <AddressListCount>3</AddressListCount>
		    <GroupUuid>a3c5e-018e-4c08-bea8-eafc95d1a54e</GroupUuid>
		    <Global>0</Global>
	  </Acls>
</DescribeAddressBook>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"TotalCount":123,
	"PageSize":1,
	"RequestId":"B36F150A-1E27-43AA-B72C-D2AC712F09DA",
	"Acls":[
		{
			"Description":"9-3IP地址簿",
			"GroupType":"ip",
			"AddressList":[
				"1.1.1.1/32",
				"0.0.0.0/0",
				"10.0.0.217/32"
			],
			"GroupName":"9-3IP地址簿",
			"AutoAddTagEcs":0,
			"TagValue":"",
			"TagRelation":"",
			"TagList":[],
			"ReferenceCount":0,
			"TagKey":"",
			"AddressListCount":3,
			"GroupUuid":"a3c5e-018e-4c08-bea8-eafc95d1a54e",
			"Global":0
		}
	],
	"PageSiNo":1
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.aliyun.com/status/product/Cloudfw)查看更多错误码。


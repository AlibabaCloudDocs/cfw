# DescribeAddressBook

调用DescribeAddressBook接口查询云防火墙访问控制策略地址簿的详细信息。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cloudfw&api=DescribeAddressBook&type=RPC&version=2017-12-07)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeAddressBook|要执行的操作。取值：**DescribeAddressBook**。 |
|SourceIp|String|否|1.2.3.4|访问者源IP地址。 |
|Lang|String|否|zh|请求和接收消息的语言类型。取值：

 -   **zh**：中文
-   **en**：英文 |
|CurrentPage|String|否|1|分页查询时的当前页的页码。默认值为1。 |
|PageSize|String|否|50|分页查询时每页显示数据条数。可设置的最大值为50。 |
|Query|String|否|1.2.3.0|搜索条件，输入待查询地址簿信息。 |
|GroupType|String|否|ip|地址簿的类型。取值：

 -   **ip**：IP地址簿
-   **domain**：域名地址簿
-   **port**：端口地址簿
-   **tag**：ECS标签地址簿 |
|ContainPort|String|否|80|查询包含指定端口的地址簿，仅当**GroupType**为**port**时有效。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Acls|Array| |地址簿信息。 |
|AddressList|List|\[ "1.2.3.4/32", "0.0.0.0/0" \]|地址簿的地址列表信息。 |
|AddressListCount|Integer|2|地址簿中包含地址的个数。 |
|AutoAddTagEcs|Integer|1|是否自动添加新匹配标签的ECS公网IP到地址簿。取值：

 -   **1**：表示自动添加
-   **0**：表示不自动添加 |
|Description|String|DEMO地址簿|地址簿的描述信息。 |
|Global|Integer|0|地址薄是否是全局地址簿。取值：

 -   **1**：是全局地址簿
-   **0**：非全局地址簿 |
|GroupName|String|demo\_address\_book|地址簿的名称。 |
|GroupType|String|ip|地址簿的类型。取值：

 -   **ip**：IP地址簿
-   **domain**：域名地址簿
-   **port**：端口地址簿
-   **tag**：ECS标签地址簿 |
|GroupUuid|String|f04ac7ce-628b-4cb7-be61-310222b718e8|地址簿的唯一标识ID。 |
|ReferenceCount|Integer|3|地址簿被引用次数。 |
|TagList|Array| |地址簿支持自动添加的待匹配ECS标签信息。 |
|TagKey|String|key1|待匹配的ECS标签Key。 |
|TagValue|String|value1|待匹配的ECS标签值。 |
|TagRelation|String|and|多个ECS标签间的关系。取值：

 -   **and**：多个标签间为“与”关系，即同时匹配多个标签的ECS公网IP才会被加入地址簿。
-   **or**：多个标签间为“或”关系，即只要匹配一个标签的ECS公网IP就会被加入地址簿。 |
|PageNo|String|1|当前页的页码。 |
|PageSize|String|10|每页显示数据条数。 |
|RequestId|String|B36F150A-1E27-43AA-B72C-D2AC712F09DA|结果的请求ID。 |
|TotalCount|String|100|地址簿的总数量。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeAddressBook
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<DescribeAddressBookResponse>
	  <TotalCount>123</TotalCount>
	  <PageSiNo>1</PageSiNo>
	  <PageSize>1</PageSize>
	  <RequestId>B36F150A-1E27-43AA-B72C-D2AC712F09DA</RequestId>
	  <Acls>
		    <Description>9-3IP地址簿</Description>
		    <GroupType>ip</GroupType>
		    <AddressList>1.2.3.4/32</AddressList>
		    <AddressList>0.0.0.0/0</AddressList>
		    <GroupName>9-3IP地址簿</GroupName>
		    <AutoAddTagEcs>0</AutoAddTagEcs>
		    <TagValue></TagValue>
		    <TagRelation></TagRelation>
		    <ReferenceCount>0</ReferenceCount>
		    <TagKey></TagKey>
		    <AddressListCount>2</AddressListCount>
		    <GroupUuid>a3c5e-018e-4c08-bea8-eafc95d1a54e</GroupUuid>
		    <Global>0</Global>
	  </Acls>
</DescribeAddressBookResponse>
```

`JSON` 格式

```
{
    "TotalCount":123,
    "PageSiNo": 1,
    "PageSize": 1,
    "RequestId":"B36F150A-1E27-43AA-B72C-D2AC712F09DA",
    "Acls":[
        {
            "Description":"9-3IP地址簿",
            "GroupType":"ip",
            "AddressList":[
                "1.2.3.4/32",
                "0.0.0.0/0"
            ],
            "GroupName":"9-3IP地址簿",
            "AutoAddTagEcs":0,
            "TagValue":"",
            "TagRelation":"",
            "TagList":[

            ],
            "ReferenceCount":0,
            "TagKey":"",
            "AddressListCount":2,
            "GroupUuid":"a3c5e-018e-4c08-bea8-eafc95d1a54e",
            "Global":0
        }
    ]
}
```


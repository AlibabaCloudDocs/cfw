# DeleteInstanceMembers

调用DeleteInstanceMembers接口，删除云防火墙成员账号。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cloudfw&api=DeleteInstanceMembers&type=RPC&version=2017-12-07)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DeleteInstanceMembers|系统规定参数。取值：**DeleteInstanceMembers**。 |
|MemberUids.N|RepeatList|是|1234123412341234|云防火墙成员账号的UID列表。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|03E8AA70-0CC9-42EA-97AA-EA68377930B4|本次请求的ID。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DeleteInstanceMembers
&MemberUids.1=1234123412341234
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<AddInstanceMembersResponse>
  <RequestId>03E8AA70-0CC9-42EA-97AA-EA68377930B4</RequestId>
</AddInstanceMembersResponse>
```

`JSON`格式

```
{
  "RequestId": "03E8AA70-0CC9-42EA-97AA-EA68377930B4"
}
```


# DeleteControlPolicy

调用DeleteControlPolicy接口删除访问控制策略。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cloudfw&api=DeleteControlPolicy&type=RPC&version=2017-12-07)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DeleteControlPolicy|系统规定参数。取值：**DeleteControlPolicy**。 |
|AclUuid|String|是|00281255-d220-4db1-8f4f-c4df221ad84c|访问控制策略的唯一标识ID。

 删除安全访问控制策略，需要提供该策略的唯一标识ID。您可调用[DescribeControlPolicy](~~138866~~)接口获取该ID。 |
|Direction|String|是|in|安全访问控制策略管控的流量方向。

 取值：

 -   **in**：流量从外到内。
-   **out**：流量从内到外。 |
|SourceIp|String|否|1.2.3.4|流量的源IP地址。 |
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
http(s)://[Endpoint]/?Action=DeleteControlPolicy
&AclUuid=00281255-d220-4db1-8f4f-c4df221ad84c
&Direction=in
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<DeleteControlPolicyResponse>
  <RequestId>CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D</RequestId>
</DeleteControlPolicyResponse>
```

`JSON` 格式

```
{
    "RequestId": "CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D"
}
```


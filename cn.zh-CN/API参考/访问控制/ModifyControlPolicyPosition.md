# ModifyControlPolicyPosition

调用ModifyControlPolicyPosition接口，修改访问控制策略的优先级。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cloudfw&api=ModifyControlPolicyPosition&type=RPC&version=2017-12-07)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|ModifyControlPolicyPosition|系统规定参数。取值：**ModifyControlPolicyPosition**。 |
|Direction|String|是|in|安全访问控制策略的流量方向。

 -   **in**：外对内流量访问控制
-   **out**：内对外流量访问控制 |
|NewOrder|String|是|1|修改后，访问控制策略生效的新优先级。 |
|OldOrder|String|是|5|修改前，访问控制策略生效的旧优先级。 |
|SourceIp|String|否|1.2.XX.XX|访问者源IP地址。 |
|Lang|String|否|zh|请求和接收消息的语言类型。

 -   **zh**：中文
-   **en**：英文 |

调用API时，除了本文中该API的请求参数，还需加入阿里云API公共请求参数。公共请求参数的详细介绍，请参见[公共参数](https://help.aliyun.com/document_detail/94763.html)。

调用API的请求格式，请参见本文**示例**中的请求示例。

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|850A84D6-0DE4-4797-A1E8-00090125EEB1|本次请求的ID。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=ModifyControlPolicyPosition
&Direction=in
&NewOrder=1
&OldOrder=5
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<ModifyControlPolicyPositionResponse>
  <RequestId>850A84D6-0DE4-4797-A1E8-00090125EEB1</RequestId>
</ModifyControlPolicyPositionResponse>
```

`JSON`格式

```
{
    "RequestId": "850A84D6-0DE4-4797-A1E8-00090125EEB1"
}
```


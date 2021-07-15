# PutDisableAllFwSwitch

调用PutDisableAllFwSwitch接口，关闭所有防火墙开关。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cloudfw&api=PutDisableAllFwSwitch&type=RPC&version=2017-12-07)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|PutDisableAllFwSwitch|需要执行的操作。

 取值：**PutDisableAllFwSwitch** |
|SourceIp|String|否|1.2.XX.XX|访问者源IP地址。 |
|Lang|String|否|zh|请求和接收消息的语言类型。

 -   **zh**：中文
-   **en**：英文 |
|InstanceId|String|否|i-2ze8v2x5kd9qyvp2\*\*\*\*|云防火墙实例的ID。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|B2841452-CB8D-4F7D-B247-38E1CF7334F8|本次请求的ID。 |

调用API时，除了本文中该API的请求参数，还需加入阿里云API公共请求参数。公共请求参数的详细介绍，请参见[公共参数](https://help.aliyun.com/document_detail/94763.html)。

调用API的请求格式，请参见本文**示例**中的请求示例。

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=PutDisableAllFwSwitch
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<PutDisableAllFwSwitchResponse>
  <RequestId>B2841452-CB8D-4F7D-B247-38E1CF7334F8</RequestId>
</PutDisableAllFwSwitchResponse>
```

`JSON`格式

```
{
    "RequestId":"B2841452-CB8D-4F7D-B247-38E1CF7334F8"
}
```


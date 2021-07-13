# ModifyPolicyAdvancedConfig

调用ModifyPolicyAdvancedConfig开启或关闭访问控制策略严格模式。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cloudfw&api=ModifyPolicyAdvancedConfig&type=RPC&version=2017-12-07)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|ModifyPolicyAdvancedConfig|要执行的操作。

 取值：**ModifyPolicyAdvancedConfig**。 |
|InternetSwitch|String|是|off|修改访问控制策略严格模式的开关状态。取值：

 -   **on**：开启严格模式。
-   **off**：关闭严格模式。 |
|SourceIp|String|否|1.2.3.4|访问者源IP地址。 |
|Lang|String|否|zh|请求和接收消息的语言类型。取值：

 -   **zh**：中文
-   **en**：英文 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|B2841452-CB8D-4F7D-B247-38E1CF7334F8|返回结果的请求ID。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=ModifyPolicyAdvancedConfig
&InternetSwitch=off
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<ModifyPolicyAdvancedConfigResponse>
   <RequestId>B2841452-CB8D-4F7D-B247-38E1CF7334F8</RequestId>
</ModifyPolicyAdvancedConfigResponse>
```

`JSON` 格式

```
{
    "RequestId":"B2841452-CB8D-4F7D-B247-38E1CF7334F8"
}
```


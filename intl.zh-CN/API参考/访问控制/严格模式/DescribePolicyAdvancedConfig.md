# DescribePolicyAdvancedConfig

调用DescribePolicyAdvancedConfig查询访问控制策略严格模式的开启状态。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cloudfw&api=DescribePolicyAdvancedConfig&type=RPC&version=2017-12-07)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribePolicyAdvancedConfig|要执行的操作。

 取值：**DescribePolicyAdvancedConfig**。 |
|SourceIp|String|否|1.2.3.4|访问者源IP地址。 |
|Lang|String|否|zh|请求和接收消息的语言类型。取值：

 -   **zh**：中文
-   **en**：英文 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|InternetSwitch|String|off|访问控制策略严格模式的开启状态。取值：

 -   **on**：严格模式已开启。
-   **off**：严格模式已关闭。 |
|RequestId|String|850A84D6-0DE4-4797-A1E8-00090125EEB1|返回结果的请求ID。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribePolicyAdvancedConfig
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<DescribePolicyAdvancedConfigResponse>
    <RequestId>850A84D6-0DE4-4797-A1E8-00090125EEB1</RequestId>
    <InternetSwitch>off</InternetSwitch>
</DescribePolicyAdvancedConfigResponse>
```

`JSON` 格式

```
{
    "RequestId":"850A84D6-0DE4-4797-A1E8-00090125EEB1",
    "InternetSwitch":"off"
}
```


# PutDisableFwSwitch

调用PutDisableFwSwitch接口，关闭防火墙开关。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cloudfw&api=PutDisableFwSwitch&type=RPC&version=2017-12-07)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|PutDisableFwSwitch|需要执行的操作。

 取值：**PutDisableFwSwitch** |
|SourceIp|String|否|1.2.XX.XX|访问者源IP地址。 |
|Lang|String|否|zh|请求和接收消息的语言类型。

 -   **zh**：中文
-   **en**：英文 |
|IpaddrList.N|RepeatList|否|\["1.2.XX.XX","5.6.XX.XX"\]|IP地址列表。 |
|RegionList.N|RepeatList|否|\["cn-hangzhou","cn-shanghai"\]|区域列表。 |
|ResourceTypeList.N|RepeatList|否|\["EcsPublicIp","NatEip"\]|资产类型列表。

 取值：

 -   BastionHostIP（堡垒机）
-   EcsEIP（ECS EIP）
-   EcsPublicIP （ECS公网IP）
-   EIP
-   EniEIP （弹性网卡EIP）
-   NatEIP（NAT EIP）
-   SlbEIP（SLB EIP）
-   SlbPublicIP（SLB公网IP）
-   NatPublicIP（NAT公网IP）
-   HAVIP（HA VIP） |

调用API时，除了本文中该API的请求参数，还需加入阿里云API公共请求参数。公共请求参数的详细介绍，请参见[公共参数](https://help.aliyun.com/document_detail/94763.html)。

调用API的请求格式，请参见本文**示例**中的请求示例。

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|B2841452-CB8D-4F7D-B247-38E1CF7334F8|本次请求的ID。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=PutDisableFwSwitch
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<PutDisableFwSwitchResponse>
  <RequestId>B2841452-CB8D-4F7D-B247-38E1CF7334F8</RequestId>
</PutDisableFwSwitchResponse>
```

`JSON`格式

```
{
    "RequestId":"B2841452-CB8D-4F7D-B247-38E1CF7334F8"
}
```


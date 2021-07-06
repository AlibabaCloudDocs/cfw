# PutEnableFwSwitch

开启防火墙开关。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cloudfw&api=PutEnableFwSwitch&type=RPC&version=2017-12-07)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|PutEnableFwSwitch|需要执行的操作。

 取值：PutEnableFwSwitch |
|SourceIp|String|否|1.2.X.X|访问者源IP地址。 |
|Lang|String|否|zh|请求和接收消息的语言类型。

 -   **zh**：中文
-   **en**：英文 |
|IpaddrList.N|RepeatList|否|\["1.2.X.X","5.6.X.X"\]|IP地址列表。

 **说明：** IpaddrList、RegionList、ResourceTypeList三个参数不允许同时为空，必须为其中一个参数设置取值。 |
|RegionList.N|RepeatList|否|\["cn-hangzhou","cn-shanghai"\]|区域列表。

 **说明：** IpaddrList、RegionList、ResourceTypeList三个参数不允许同时为空，必须为其中一个参数设置取值。 |
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
-   HAVIP（HA VIP）

 **说明：** IpaddrList、RegionList、ResourceTypeList三个参数不允许同时为空，必须为其中一个参数设置取值。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|B2841452-CB8D-4F7D-B247-38E1CF7334F8|请求ID。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=PutEnableFwSwitch&IpaddrList=["1.2.X.X","5.6.X.X."]
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<PutEnableFwSwitchResponse>
  <RequestId>B2841452-CB8D-4F7D-B247-38E1CF7334F8</RequestId>
</PutEnableFwSwitchResponse>
```

`JSON`格式

```
{
    "RequestId":"B2841452-CB8D-4F7D-B247-38E1CF7334F8"
}
```


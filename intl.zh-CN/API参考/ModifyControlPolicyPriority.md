# ModifyControlPolicyPriority

调用ModifyControlPolicyPriority接口，修改访问控制策略的优先级。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cloudfw&api=ModifyControlPolicyPriority&type=RPC&version=2017-12-07)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|ModifyControlPolicyPriority|系统规定参数。取值：ModifyControlPolicyPriority。 |
|AclUuid|String|是|3770d603-3534-4878-b845-f00095ee5048|访问控制策略唯一标识。 |
|Order|String|是|3|访问控制策略生效的优先级。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|586F34E8-3F16-4C08-9FFC-8FFDC64B9D0D|返回结果的请求ID。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=ModifyControlPolicyPriority
&AclUuid=3770d603-3534-4878-b845-f00095ee5048
&Order=3
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<ModifyControlPolicyPriorityResponse>
  <RequestId>586F34E8-3F16-4C08-9FFC-8FFDC64B9D0D</RequestId>
</ModifyControlPolicyPriorityResponse>
```

`JSON`格式

```
{
    "RequestId": "586F34E8-3F16-4C08-9FFC-8FFDC64B9D0D"
}
```

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Cloudfw)查看更多错误码。

## 相关文档

[DescribeControlPolicy](~~138866~~)：查询访问控制策略的信息（包括优先级）。


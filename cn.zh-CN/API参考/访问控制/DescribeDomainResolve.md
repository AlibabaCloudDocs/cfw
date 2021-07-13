# DescribeDomainResolve

调用DescribeDomainResolve接口获取域名DNS的解析结果。

**说明：** 当前仅支持从阿里云云解析DNS获取解析结果。要查询的域名必须使用云解析DNS，才能查询到其解析结果。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cloudfw&api=DescribeDomainResolve&type=RPC&version=2017-12-07)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeDomainResolve|要执行的操作。

 取值：**DescribeDomainResolve**。 |
|Domain|String|是|www.aliyun.com|待解析的域名地址。 |
|SourceIp|String|否|1.2.3.4|访问者源IP地址。 |
|Lang|String|否|zh|请求和接收消息的语言类型。

 取值包括：

 -   **zh**：中文
-   **en**：英文 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D|结果的请求ID。 |
|ResolveResult|Struct| |域名解析结果。 |
|IpAddrs|String|11.1.1.1,12.1.1.1|域名解析结果，多个IP地址用半角逗号（,）分隔。 |
|UpdateTime|Long|1579091739|解析时间戳。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeDomainResolve
&Domain=www.aliyun.com
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<DescribeDomainResolveResponse>
  <RequestId>412AF3C5-B225-4606-8323-A8924F796F16</RequestId>
  <ResolveResult>
        <IpAddrs>12.3.4,1.2.3.5,1.2.3.6</IpAddrs>
        <UpdateTime>1586765803</UpdateTime>
  </ResolveResult>
</DescribeDomainResolveResponse>
```

`JSON` 格式

```
{
	"RequestId": "412AF3C5-B225-4606-8323-A8924F796F16",
	"ResolveResult": {
		"IpAddrs": "12.3.4,1.2.3.5,1.2.3.6",
		"UpdateTime": 1586765803
	}
}
```


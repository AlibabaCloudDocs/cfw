# DescribeAssetList

调用DescribeAssetList查询云防火墙资产列表。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cloudfw&api=DescribeAssetList&type=RPC&version=2017-12-07)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeAssetList|系统规定参数。

 取值：**DescribeAssetList**。 |
|CurrentPage|String|是|1|分页查询时，显示的当前页的页码。 默认值为1。 |
|PageSize|String|是|10|分页查询时，显示的每页数据的最大条数。 可设置值最大为50。 |
|SourceIp|String|否|1.2.3.5|访问者源IP地址。 |
|Lang|String|否|zh|请求和接收消息的语言类型。取值：

 -   **zh**：中文
-   **en**：英文 |
|RegionNo|String|否|cn-hangzhou|云防火墙支持的地域的ID。 |
|Status|String|否|open|防火墙状态列表。取值：

 -   **open**：保护中
-   **opening**：保护开启中
-   **closed**：保护未开启
-   **closing**：保护关闭中 |
|SearchItem|String|否|1.1.1.1|搜索项目的IP或者实例ID。 |
|Type|String|否|eip|本参数已废弃。 |
|ResourceType|String|否|EcsEIP|资产类型列表。取值：

 -   **BastionHostEgressIP**：堡垒机出口IP
-   **BastionHostIngressIP**：堡垒机入口IP
-   **EcsEIP**：ECS EIP
-   **EcsPublicIP**：ECS公网IP
-   **EIP**：弹性公网IP
-   **EniEIP**：弹性网卡EIP
-   **NatEIP**：NAT EIP
-   **SlbEIP**：SLB EIP
-   **SlbPublicIP**：SLB公网IP
-   **NatPublicIP**：NAT公网IP
-   **HAVIP**：高可用虚拟IP |
|SgStatus|String|否|open|安全组策略状态。取值：

 -   **pass**：已下发
-   **block**：未下发
-   **unsupport**：不支持 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Assets|Array of Resource| |云防火墙资产信息。 |
|AliUid|Long|1234123412341234|阿里云UID。 |
|BindInstanceId|String|i-8vbdrjrxzt78\*\*\*\*|绑定资产实例ID。 |
|BindInstanceName|String|instance01|绑定资产实例名称。 |
|InternetAddress|String|1.1.1.1|服务器公网IP。 |
|IntranetAddress|String|192.168.XX.XX|服务器内网IP。 |
|Name|String|instance01|云防火墙防护的云资产的实例名称。 |
|Note|String|REGION\_NOT\_SUPPORT|备注信息列表。取值：

 -   **REGION\_NOT\_SUPPORT**：地域不支持
-   **NETWORK\_NOT\_SUPPORT**：网络不支持
-   取值为空 |
|ProtectStatus|String|open|防火墙状态列表。取值：

 -   **open**：保护中
-   **opening**：保护开启中
-   **closed**：未受保护
-   **closing**：保护关闭中 |
|RegionID|String|cn-hangzhou|云防火墙支持的地域的ID。 |
|RegionStatus|String|enable|地区防火墙支持状态列表。取值：

 -   **enable**：支持
-   **disable**：不支持 |
|ResourceInstanceId|String|i-8vbdrjrxzt78\*\*\*\*|资源实例ID。 |
|ResourceType|String|EcsPublicIP|资产类型列表。取值：

 -   **BastionHostEgressIP**：堡垒机出口IP
-   **BastionHostIngressIP**：堡垒机入口IP
-   **EcsEIP**：ECS EIP
-   **EcsPublicIP**：ECS公网IP
-   **EIP**：弹性公网IP
-   **EniEIP**：弹性网卡EIP
-   **NatEIP**：NAT EIP
-   **SlbEIP**：SLB EIP
-   **SlbPublicIP**：SLB公网IP
-   **NatPublicIP**：NAT公网IP
-   **HAVIP**：高可用虚拟IP |
|SgStatus|String|block|安全组策略。取值：

 -   **pass**：已下发
-   **block**：未下发 |
|SgStatusTime|Long|1615082937|最近一次安全组状态检测时间。单位：秒。 |
|SyncStatus|String|enable|资产引流支持状态列表。取值：

 -   **enable**：支持引流
-   **disable**：不支持引流 |
|Type|String|eip|该参数已废弃。 |
|RequestId|String|CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D|结果的请求ID。 |
|TotalCount|Integer|12|云防火墙防护的资产的总数量。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeAssetList
&CurrentPage=1
&PageSize=10
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<DescribeAssetListResponse>
  <TotalCount>12</TotalCount>
  <RequestId>CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D</RequestId>
  <Assets>
        <BindInstanceId>i-8vbdrjrxzt78****</BindInstanceId>
        <InternetAddress>1.1.1.1</InternetAddress>
        <RegionStatus>enable</RegionStatus>
        <SgStatusTime>1615082937</SgStatusTime>
        <SyncStatus>enable</SyncStatus>
        <ResourceType>EcsPublicIP</ResourceType>
        <Name>instance01</Name>
        <SgStatus>block</SgStatus>
        <IntranetAddress>192.168.XX.XX</IntranetAddress>
        <Type>eip</Type>
        <Note>REGION_NOT_SUPPORT</Note>
        <BindInstanceName>instance01</BindInstanceName>
        <ProtectStatus>open</ProtectStatus>
        <RegionID>cn-hangzhou</RegionID>
        <ResourceInstanceId>i-8vbdrjrxzt78****</ResourceInstanceId>
        <AliUid>1234123412341234</AliUid>
  </Assets>
</DescribeAssetListResponse>
```

`JSON`格式

```
{
	"TotalCount": "12",
	"RequestId": "CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D",
	"Assets": [
		{
			"BindInstanceId": "i-8vbdrjrxzt78****",
			"InternetAddress": "1.1.1.1",
			"RegionStatus": "enable",
			"SgStatusTime": "1615082937",
			"SyncStatus": "enable",
			"ResourceType": "EcsPublicIP",
			"Name": "instance01",
			"SgStatus": "block",
			"IntranetAddress": "192.168.XX.XX",
			"Type": "eip",
			"Note": "REGION_NOT_SUPPORT",
			"BindInstanceName": "instance01",
			"ProtectStatus": "open",
			"RegionID": "cn-hangzhou",
			"ResourceInstanceId": "i-8vbdrjrxzt78****",
			"AliUid": "1234123412341234"
		}
	]
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Cloudfw)查看更多错误码。


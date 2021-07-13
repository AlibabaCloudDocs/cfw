# DescribeVpcFirewallAclGroupList

调用DescribeVpcFirewallAclGroupList接口获取VPC防火墙所有访问控制策略组信息。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cloudfw&api=DescribeVpcFirewallAclGroupList&type=RPC&version=2017-12-07)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeVpcFirewallAclGroupList|需要执行的操作。

 取值：**DescribeVpcFirewallAclGroupList**。 |
|Lang|String|否|zh|请求和接收消息的语言类型。

 -   **zh**：中文
-   **en**：英文 |
|FirewallConfigureStatus|String|否|configured|VPC防火墙的配置状态。

 -   **notconfigured**：VPC边界防火墙未配置（即未创建防火墙） 。
-   **configured**：VPC边界防火墙已配置（即已创建了防火墙）。
-   不填表示查询所有VPC防火墙配置状态对应的策略组。 |
|CurrentPage|String|否|1|分页查询时，显示的当前页的页码。

 默认值为1。 |
|PageSize|String|否|10|分页查询时，显示的每页数据的最大条数。

 可设置值最大为50。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|AclGroupList|Array| |VPC防火墙访问控制策略组的信息。 |
|AclGroupId|String|vfw-a42bbb7b887148c9\*\*\*\*|VPC边界防火墙的访问控制策略组ID。您可调用**DescribeVpcFirewallAclGroupList**接口获取该ID。

 取值：

 -   VPC边界防火墙防护云企业网时，策略组ID使用云企业网实例ID。

例如：cen-ervw0g12b5jbw\*\*\*\*

-   VPC边界防火墙防护高速通道时，策略组ID使用VPC边界防火墙实例ID。

例如：vfw-a42bbb7b887148c9\*\*\*\* |
|AclGroupName|String|group\_test|VPC边界防火墙的访问控制策略组名称。

 -   VPC边界防火墙防护云企业网时，策略组名称使用云企业网名称。
-   VPC边界防火墙防护高速通道时，策略组名称使用VPC边界防火墙名称。 |
|RequestId|String|CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D|结果的请求ID。 |
|TotalCount|Integer|1|VPC防火墙访问控制策略组的总数量。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeVpcFirewallAclGroupList
&FirewallConfigureStatus=configured
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<DescribeVpcFirewallAclGroupListResponse>
  <TotalCount>1</TotalCount>
  <AclGroupList>
        <AclGroupId>vfw-a42bbb7b887148c9****</AclGroupId>
        <AclGroupName>group_test</AclGroupName>
  </AclGroupList>
</DescribeVpcFirewallAclGroupListResponse>
```

`JSON` 格式

```
{"TotalCount":1,"AclGroupList":[{"AclGroupId":"vfw-a42bbb7b887148c9****","AclGroupName":"group_test"}]}
```


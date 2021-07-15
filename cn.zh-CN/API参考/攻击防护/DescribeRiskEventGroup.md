# DescribeRiskEventGroup

调用DescribeRiskEventGroup接口，获取入侵防御事件的详细数据。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cloudfw&api=DescribeRiskEventGroup&type=RPC&version=2017-12-07)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeRiskEventGroup|系统规定参数。取值：**DescribeRiskEventGroup**。 |
|DataType|String|是|session|风险事件类型。

 默认值**session**：阻断活动事件。 |
|EndTime|String|是|1534408189|本次查询的结束时间。

 **说明：** 使用秒级时间戳格式。 |
|SourceCode|String|是|yundun|调用接口的应用名称。 |
|StartTime|String|是|1534408189|本次查询的开始时间。

 **说明：** 使用秒级时间戳格式。 |
|Lang|String|否|zh|请求和接收消息的语言类型。取值：

 -   **zh**：中文
-   **en**：英文 |
|Direction|String|否|in|流量的方向。取值：

 -   **in**：进方向
-   **out**：出方向

**说明：** 不填写该参数表示查询所有流量方向。

**说明：** 不填写该参数表示查询所有流量方向。 |
|PageSize|String|否|6|分页查询时，每页包含多少条结果。

 默认值为**6**，表示每页包含6条结果。 |
|CurrentPage|String|否|1|分页查询时，返回第几页数据。

 默认值为**1**，表示返回第1页数据。 |
|RuleSource|String|否|1|规则来源。取值：

 -   **1**：基础防御
-   **2**：虚拟补丁
-   **4**：威胁情报

**说明：** 不填写该参数表示查询所有规则来源。 |
|RuleResult|String|否|1|防御状态，如果不填，默认为全部防御状态。取值：

 -   **1**：告警
-   **2**：拦截

 **说明：** 不填写该参数表示查询所有防御状态。 |
|SrcIP|String|否|1.2.XX.XX|源IP。 |
|DstIP|String|否|2.3.XX.XX|目的IP。 |
|VulLevel|String|否|1|安全等级。取值：

 -   **1**：低危
-   **2**：中危
-   **3**：高危

**说明：** 不填写该参数表示查询所有安全等级。 |
|FirewallType|String|否|InternetFirewall|防火墙类型。取值：

 -   **VpcFirewall**：VPC边界防火墙。
-   **InternetFirewall**（默认）：互联网边界防火墙。 |
|SrcNetworkInstanceId|String|否|vpc-uf6e9a9zyokj2ywuo\*\*\*\*|源网络实例ID。

 **说明：** FirewallType为VpcFirewall时有效。 |
|DstNetworkInstanceId|String|否|vpc-uf6e9a9zyokj2ywuo\*\*\*\*|目的网络实例ID。

 **说明：** FirewallType为VpcFirewall时有效。 |
|AttackType|String|否|1|攻击类型。取值：

 -   **1**：异常连接
-   **2**：命令执行
-   **3**：暴力破解
-   **4**：扫描
-   **5**：其它
-   **6**：信息泄露
-   **7**：Dos攻击
-   **8**：溢出攻击
-   **9**：Web攻击
-   **10**：木马后门
-   **11**：病毒蠕虫
-   **12**：挖矿行为
-   **13**：反弹Shell

**说明：** 不填写该参数表示查询全部攻击类型。 |
|AttackApp|String|否|MySql|被攻击应用的名称。 |
|NoLocation|String|否|false|是否查询IP地址位置信息。

 -   **true**： 不查询IP地理位置信息。
-   **false**：查询IP地理位置信息。

**说明：** 查询入侵防御事件时默认为false，下载入侵防御事件时默认为true。 |

调用API时，除了本文中该API的请求参数，还需加入阿里云API公共请求参数。公共请求参数的详细介绍，请参见[公共参数](https://help.aliyun.com/document_detail/94763.html)。

调用API的请求格式，请参见本文**示例**中的请求示例。

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|DataList|Array of Data| |返回数据列表。 |
|AttackApp|String|MySql|被攻击应用的名称。 |
|AttackType|Integer|1|攻击类型。 |
|Description|String|检测到HTTP请求的WEB访问中使用了目录穿越攻击。|事件描述。 |
|Direction|String|in|流量的方向。取值：

 -   **in**：进方向。
-   **out**：出方向。 |
|DstIP|String|1.2.XX.XX|目的公网IP。 |
|EventCount|Integer|100|入侵防御事件数。 |
|EventId|String|2b58efae-4c4b-4d96-9544-a586fb1f\*\*\*\*|入侵防御事件ID。 |
|EventName|String|WEB目录穿越攻击|入侵防御事件名称。 |
|FirstEventTime|Integer|1534408189|入侵事件首次发生时间。

 **说明：** 使用秒级时间戳格式。 |
|IPLocationInfo|Struct| |IP地理位置信息。 |
|CityId|String|510100|城市ID。 |
|CityName|String|四川省成都|城市名。 |
|CountryId|String|CN|国家ID。 |
|CountryName|String|中国|国家名。 |
|LastEventTime|Integer|1534408189|入侵事件上次发生时间。

 **说明：** 使用秒级时间戳格式。 |
|ResourcePrivateIPList|Array of ResourcePrivateIPListItem| |内网IP列表。 |
|RegionNo|String|cn-hangzhou|地域 |
|ResourceInstanceId|String|i-wz92jf4scg2zb74p\*\*\*\*|实例ID |
|ResourceInstanceName|String|LD-shenzhen-zy\*\*\*\*|实例名 |
|ResourcePrivateIP|String|10.255.XX.XX|私网IP |
|ResourceType|String|EcsPublicIP|公网IP类型。取值：

 -   **EcsPublicIP**
    -   **EcsEIP**
    -   **NatPublicIP**
    -   **NatEIP**
-   **EIP** |
|RuleId|String|1000\*\*\*\*|规则ID。 |
|RuleResult|Integer|2|防御状态。取值：

 -   **1**：告警。
-   **2**：拦截。 |
|RuleSource|Integer|1|规则来源。取值：

 -   **1**：基础防御
-   **2**：虚拟补丁
-   **4**：威胁情报 |
|SrcIP|String|1.1.XX.XX|源公网IP。 |
|SrcPrivateIPList|List|\["192.168.XX.XX","192.168.XX.XX"\]|源内网IP列表。

 **说明：** 只有出方向会携带。 |
|Tag|String|重保情报|重保情报标签。 |
|VpcDstInfo|Struct| |目的VPC信息。 |
|EcsInstanceId|String|i-wz92jf4scg2zb74p\*\*\*\*|ECS实例ID。 |
|EcsInstanceName|String|LD-shenzhen-zy\*\*\*\*|ECS实例名。 |
|NetworkInstanceId|String|vpc-uf6e9a9zyokj2ywuo\*\*\*\*|网络实例ID。 |
|NetworkInstanceName|String|VPC-SH-TX\*\*\*\*|网络实例名。 |
|RegionNo|String|cn-hangzhou|地域。 |
|VpcSrcInfo|Struct| |源VPC信息。 |
|EcsInstanceId|String|i-wz92jf4scg2zb74p\*\*\*\*|ECS实例ID。 |
|EcsInstanceName|String|LD-shenzhen-zy\*\*\*\*|ECS实例名。 |
|NetworkInstanceId|String|vpc-uf6e9a9zyokj2ywuo\*\*\*\*|网络实例ID。 |
|NetworkInstanceName|String|VPC-SH-TX\*\*\*\*|网络实例名。 |
|RegionNo|String|cn-hangzhou|地域。 |
|VulLevel|Integer|1|安全等级。取值：

 -   **1**：低危
-   **2**：中危
-   **3**：高危 |
|RequestId|String|B14757D0-4640-4B44-AC67-7F558FE7E6EF|本次请求的ID。 |
|TotalCount|Integer|20|风险事件的总数量。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeRiskEventGroup
&DataType=session
&EndTime=1534408189
&SourceCode=yundun
&StartTime=1534408189
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<DescribeRiskEventGroupResponse>
  <DataList>
        <RuleSource>1</RuleSource>
        <Description>检测到HTTP请求的WEB访问中使用了目录穿越攻击。</Description>
        <FirstEventTime>1534408189</FirstEventTime>
        <EventCount>100</EventCount>
        <RuleId>1000****</RuleId>
        <AttackType>1</AttackType>
        <ResourceType>EcsPublicIP</ResourceType>
        <RuleResult>2</RuleResult>
        <EventName>WEB目录穿越攻击</EventName>
        <Direction>in</Direction>
        <SrcIP>1.1.XX.XX</SrcIP>
        <DstIP>1.2.XX.XX</DstIP>
        <EventId>2b58efae-4c4b-4d96-9544-a586fb1f****</EventId>
        <Tag>重保情报</Tag>
        <LastEventTime>1534408189</LastEventTime>
        <AttackApp>MySql</AttackApp>
        <VulLevel>1</VulLevel>
        <ResourcePrivateIPList>
              <RegionNo>cn-hangzhou</RegionNo>
              <ResourcePrivateIP>10.255.XX.XX</ResourcePrivateIP>
              <ResourceInstanceName>LD-shenzhen-zy****</ResourceInstanceName>
              <ResourceInstanceId>i-wz92jf4scg2zb74p****</ResourceInstanceId>
        </ResourcePrivateIPList>
        <SrcPrivateIPList>["192.168.XX.XX","192.168.XX.XX"]</SrcPrivateIPList>
        <VpcSrcInfo>
              <EcsInstanceName>LD-shenzhen-zy****</EcsInstanceName>
              <EcsInstanceId>i-wz92jf4scg2zb74p****</EcsInstanceId>
              <RegionNo>cn-hangzhou</RegionNo>
              <NetworkInstanceId>vpc-uf6e9a9zyokj2ywuo****</NetworkInstanceId>
              <NetworkInstanceName>VPC-SH-TX****</NetworkInstanceName>
        </VpcSrcInfo>
        <VpcDstInfo>
              <EcsInstanceName>LD-shenzhen-zy****</EcsInstanceName>
              <EcsInstanceId>i-wz92jf4scg2zb74p****</EcsInstanceId>
              <RegionNo>cn-hangzhou</RegionNo>
              <NetworkInstanceId>vpc-uf6e9a9zyokj2ywuo****</NetworkInstanceId>
              <NetworkInstanceName>VPC-SH-TX****</NetworkInstanceName>
        </VpcDstInfo>
        <IPLocationInfo>
              <CountryId>CN</CountryId>
              <CityId>510100</CityId>
              <CountryName>中国</CountryName>
              <CityName>四川省成都</CityName>
        </IPLocationInfo>
  </DataList>
  <TotalCount>20</TotalCount>
  <RequestId>B14757D0-4640-4B44-AC67-7F558FE7E6EF</RequestId>
</DescribeRiskEventGroupResponse>
```

`JSON`格式

```
{
    "DataList": {
        "RuleSource": 1,
        "Description": "检测到HTTP请求的WEB访问中使用了目录穿越攻击。",
        "FirstEventTime": 1534408189,
        "EventCount": 100,
        "RuleId": "1000****",
        "AttackType": 1,
        "ResourceType": "EcsPublicIP",
        "RuleResult": 2,
        "EventName": "WEB目录穿越攻击",
        "Direction": "in",
        "SrcIP": "1.1.XX.XX",
        "DstIP": "1.2.XX.XX",
        "EventId": "2b58efae-4c4b-4d96-9544-a586fb1f****",
        "Tag": "重保情报",
        "LastEventTime": 1534408189,
        "AttackApp": "MySql",
        "VulLevel": 1,
        "ResourcePrivateIPList": {
            "RegionNo": "cn-hangzhou",
            "ResourcePrivateIP": "10.255.XX.XX",
            "ResourceInstanceName": "LD-shenzhen-zy****",
            "ResourceInstanceId": "i-wz92jf4scg2zb74p****"
        },
        "SrcPrivateIPList": "[\"192.168.XX.XX\",\"192.168.XX.XX\"]",
        "VpcSrcInfo": {
            "EcsInstanceName": "LD-shenzhen-zy****",
            "EcsInstanceId": "i-wz92jf4scg2zb74p****",
            "RegionNo": "cn-hangzhou",
            "NetworkInstanceId": "vpc-uf6e9a9zyokj2ywuo****",
            "NetworkInstanceName": "VPC-SH-TX****"
        },
        "VpcDstInfo": {
            "EcsInstanceName": "LD-shenzhen-zy****",
            "EcsInstanceId": "i-wz92jf4scg2zb74p****",
            "RegionNo": "cn-hangzhou",
            "NetworkInstanceId": "vpc-uf6e9a9zyokj2ywuo****",
            "NetworkInstanceName": "VPC-SH-TX****"
        },
        "IPLocationInfo": {
            "CountryId": "CN",
            "CityId": 510100,
            "CountryName": "中国",
            "CityName": "四川省成都"
        }
    },
    "TotalCount": 20,
    "RequestId": "B14757D0-4640-4B44-AC67-7F558FE7E6EF"
}
```


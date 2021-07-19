# DescribeRiskEventGroup

调用DescribeRiskEventGroup接口，获取入侵防御事件的详细数据。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cloudfw&api=DescribeRiskEventGroup&type=RPC&version=2017-12-07)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeRiskEventGroup|系统规定参数。取值：**DescribeRiskEventGroup**。 |
|DataType|String|是|session|风险事件类型。

 默认值为**session**，表示阻断活动事件。 |
|EndTime|String|是|1534408267|设置查询结束时间。使用秒级时间戳格式表示。 |
|StartTime|String|是|1534408189|设置查询开始时间。使用秒级时间戳格式表示。 |
|Lang|String|否|zh|请求和接收消息的语言类型。取值：

 -   **zh**（默认）：表示中文。
-   **en**：表示英文。 |
|Direction|String|否|in|入侵防御事件的流量的方向。取值：

 -   **in**：表示进方向。
-   **out**：表示出方向。

**说明：** 不设置该参数表示查询所有流量方向。 |
|PageSize|String|否|6|设置分页查询每页包含多少条结果。

 默认值为**6**，表示每页包含6条结果。 |
|CurrentPage|String|否|1|设置分页查询返回第几页数据。

 默认值为**1**，表示返回第1页数据。 |
|RuleSource|String|否|1|检测到入侵防御事件的规则来源。取值：

 -   **1**：表示基础防御。
-   **2**：表示虚拟补丁。
-   **4**：表示威胁情报。

**说明：** 不设置该参数表示查询所有规则来源。 |
|RuleResult|String|否|1|云防火墙的防御状态。取值：

 -   **1**：表示告警。
-   **2**：表示拦截。

 **说明：** 不设置该参数表示查询所有防御状态。 |
|SrcIP|String|否|1.2.XX.XX|要查询的源IP。设置该参数表示查询具有指定源IP的入侵防御事件。 |
|DstIP|String|否|2.3.XX.XX|要查询的目的IP。设置该参数表示查询具有指定目的IP的入侵防御事件。 |
|VulLevel|String|否|1|入侵防御事件的安全等级。取值：

 -   **1**：表示低危。
-   **2**：表示中危。
-   **3**：表示高危。

**说明：** 不设置该参数表示查询所有安全等级。 |
|FirewallType|String|否|InternetFirewall|云防火墙类型。取值：

 -   **VpcFirewall**：表示VPC边界防火墙。
-   **InternetFirewall**（默认）：表示互联网边界防火墙。 |
|SrcNetworkInstanceId|String|否|vpc-uf6e9a9zyokj2ywuo\*\*\*\*|源VPC实例ID。

 **说明：** FirewallType为VpcFirewall时有效。 |
|DstNetworkInstanceId|String|否|vpc-uf6e9a9zyokj2ywuo\*\*\*\*|目的VPC实例ID。

 **说明：** FirewallType为VpcFirewall时有效。 |
|AttackType|String|否|1|入侵防御事件的攻击类型。取值：

 -   **1**：表示异常连接。
-   **2**：表示命令执行。
-   **3**：表示暴力破解。
-   **4**：表示扫描。
-   **5**：表示其它。
-   **6**：表示信息泄露。
-   **7**：表示Dos攻击。
-   **8**：表示溢出攻击。
-   **9**：表示Web攻击。
-   **10**：表示木马后门。
-   **11**：表示病毒蠕虫。
-   **12**：表示挖矿行为。
-   **13**：表示反弹Shell。

**说明：** 不设置该参数表示查询全部攻击类型。 |
|AttackApp|String|否|MySql|被攻击应用的名称。 |
|NoLocation|String|否|false|是否查询IP地址位置信息。

 -   **true**： 表示不查询IP地理位置信息。
-   **false**（默认）：表示查询IP地理位置信息。 |

调用API时，除了本文中该API的请求参数，还需加入阿里云API公共请求参数。公共请求参数的详细介绍，请参见[公共参数](https://help.aliyun.com/document_detail/94763.html)。

调用API的请求格式，请参见本文**示例**中的请求示例。

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|DataList|Array of Data| |返回数据列表。 |
|AttackApp|String|MySql|被攻击应用的名称。 |
|AttackType|Integer|1|该入侵防御事件的攻击类型。取值：

 -   **1**：表示异常连接。
-   **2**：表示命令执行。
-   **3**：表示暴力破解。
-   **4**：表示扫描。
-   **5**：表示其它。
-   **6**：表示信息泄露。
-   **7**：表示Dos攻击。
-   **8**：表示溢出攻击。
-   **9**：表示Web攻击。
-   **10**：表示木马后门。
-   **11**：表示病毒蠕虫。
-   **12**：表示挖矿行为。
-   **13**：表示反弹Shell。 |
|Description|String|检测到HTTP请求的WEB访问中使用了目录穿越攻击。|该入侵防御事件的描述。 |
|Direction|String|in|该入侵防御事件的流量方向。取值：

 -   **in**：表示进方向。
-   **out**：表示出方向。 |
|DstIP|String|1.2.XX.XX|查询到的目的IP。表示查询具有此处指定目的IP的入侵防御事件。 |
|EventCount|Integer|100|入侵防御事件数。 |
|EventId|String|2b58efae-4c4b-4d96-9544-a586fb1f\*\*\*\*|入侵防御事件ID。 |
|EventName|String|WEB目录穿越攻击|入侵防御事件名称。 |
|FirstEventTime|Integer|1534408189|入侵事件首次发生时间。使用秒级时间戳格式表示。 |
|IPLocationInfo|Struct| |IP地理位置信息。 |
|CityId|String|510100|城市ID。 |
|CityName|String|四川省成都|城市名。 |
|CountryId|String|CN|国家ID。 |
|CountryName|String|中国|国家名。 |
|LastEventTime|Integer|1534408267|入侵防御事件上次发生的时间。使用秒级时间戳格式表示。 |
|ResourcePrivateIPList|Array of ResourcePrivateIPListItem| |该入侵防御事件的私网IP列表。 |
|RegionNo|String|cn-hangzhou|地域ID。表示私网IP所属的地域ID。 |
|ResourceInstanceId|String|i-wz92jf4scg2zb74p\*\*\*\*|实例ID。 |
|ResourceInstanceName|String|LD-shenzhen-zy\*\*\*\*|实例名。 |
|ResourcePrivateIP|String|10.255.XX.XX|私网IP。 |
|ResourceType|String|EcsPublicIP|该入侵防御事件的公网IP类型。取值：

 -   **EIP**：表示弹性公网IP。
-   **EcsPublicIP**：表示ECS公网IP。
-   **EcsEIP**：表示ECS EIP。
-   **NatPublicIP**：表示NAT公网IP。
-   **NatEIP**：表示NAT EIP。 |
|RuleId|String|1000\*\*\*\*|检测到本次入侵防御事件的防护规则ID。 |
|RuleResult|Integer|2|防御状态。取值：

 -   **1**：表示告警。
-   **2**：表示拦截。 |
|RuleSource|Integer|1|检测到本次入侵防御事件的规则来源。取值：

 -   **1**：表示基础防御。
-   **2**：表示虚拟补丁。
-   **4**：表示威胁情报。 |
|SrcIP|String|1.1.XX.XX|查询到的源IP。表示查询具有此处指定的目的公网IP的入侵防御事件。 |
|SrcPrivateIPList|List|\["192.168.XX.XX","192.168.XX.XX"\]|入侵防御事件的源私网IP列表。

 **说明：** 只有出方向会返回该参数的值。 |
|Tag|String|重保情报|重保情报标签。 |
|VpcDstInfo|Struct| |该入侵防御事件的目的VPC信息。 |
|EcsInstanceId|String|i-wz92jf4scg2zb74p\*\*\*\*|ECS实例ID。 |
|EcsInstanceName|String|LD-shenzhen-zy\*\*\*\*|ECS实例名。 |
|NetworkInstanceId|String|vpc-uf6e9a9zyokj2ywuo\*\*\*\*|VPC实例ID。 |
|NetworkInstanceName|String|VPC-SH-TX\*\*\*\*|VPC实例名。 |
|RegionNo|String|cn-hangzhou|地域ID。表示目的VPC实例所属的地域ID。 |
|VpcSrcInfo|Struct| |该入侵防御事件的源VPC信息。 |
|EcsInstanceId|String|i-wz92jf4scg2zb74p\*\*\*\*|ECS实例ID。 |
|EcsInstanceName|String|LD-shenzhen-zy\*\*\*\*|ECS实例名。 |
|NetworkInstanceId|String|vpc-uf6e9a9zyokj2ywuo\*\*\*\*|VPC实例ID。 |
|NetworkInstanceName|String|VPC-SH-TX\*\*\*\*|VPC实例名。 |
|RegionNo|String|cn-hangzhou|地域ID。表示源VPC实例所属的地域ID。 |
|VulLevel|Integer|1|该入侵防御事件的安全等级。取值：

 -   **1**：表示低危。
-   **2**：表示中危。
-   **3**：表示高危。 |
|RequestId|String|B14757D0-4640-4B44-AC67-7F558FE7E6EF|本次请求的ID。 |
|TotalCount|Integer|20|风险事件的总数量。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeRiskEventGroup
&DataType=session
&EndTime=1534408267
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
        <LastEventTime>1534408267</LastEventTime>
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
        "LastEventTime": 1534408267,
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


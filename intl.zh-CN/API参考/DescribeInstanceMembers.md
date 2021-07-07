# DescribeInstanceMembers

调用DescribeInstanceMembers接口，获取云防火墙成员账号信息。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cloudfw&api=DescribeInstanceMembers&type=RPC&version=2017-12-07)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeInstanceMembers|系统规定参数。取值：**DescribeInstanceMembers**。 |
|CurrentPage|String|否|1|分页查询时，返回第几页数据。

 默认值为**1**，表示返回第1页数据。 |
|PageSize|String|否|20|分页查询时，每页包含多少条结果。

 默认值为**20**，表示每页包含20条结果。 |
|MemberUid|String|否|1234123412341234|云防火墙成员账号的UID。 |
|MemberDisplayName|String|否|cloudfirewall\_2|云防火墙成员账号的名称。 |
|MemberDesc|String|否|renewal|云防火墙成员账号的备注。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Members|Array of Data| |云防火墙成员账号的信息。 |
|CreateTime|Integer|1615189819|云防火墙成员账号的加入时间。

 **说明：** 使用秒级时间戳格式。 |
|MemberDesc|String|renewal|云防火墙成员账号的备注信息。 |
|MemberDisplayName|String|cloudfirewall\_2|云防火墙成员账号的名称。 |
|MemberStatus|String|normal|云防火墙成员账号的状态。取值：

 -   **normal**：正常
-   **deleting**：删除中 |
|MemberUid|Long|1234123412341234|云防火墙成员账号的UID。 |
|ModifyTime|Integer|1615189819|云防火墙成员账号的最近修改时间。

 **说明：** 使用秒级时间戳格式。 |
|PageInfo|Struct| |分页查询时的页面信息。 |
|CurrentPage|Integer|1|本次查询第几页数据。 |
|PageSize|Integer|20|本次查询每页包含多少条结果。 |
|TotalCount|Integer|20|云防火墙成员账号的总数量。 |
|RequestId|String|A531AE1A-FBA2-48B6-BAB8-84D02BD409EE|本次请求的ID。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeInstanceMembers
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<DescribeInstanceMembersResponse>
  <PageInfo>
        <TotalCount>20</TotalCount>
        <PageSize>20</PageSize>
        <CurrentPage>1</CurrentPage>
  </PageInfo>
  <RequestId>A531AE1A-FBA2-48B6-BAB8-84D02BD409EE</RequestId>
  <Members>
        <ModifyTime>1615189819</ModifyTime>
        <MemberDesc>test</MemberDesc>
        <MemberUid>1234123412341234</MemberUid>
        <CreateTime>1615189819</CreateTime>
        <MemberDisplayName>cloudfirewall_test2</MemberDisplayName>
        <MemberStatus>normal</MemberStatus>
  </Members>
</DescribeInstanceMembersResponse>
```

`JSON`格式

```
{
    "PageInfo": {
        "TotalCount": 20,
        "PageSize": 20,
        "CurrentPage": 1
    },
    "RequestId": "A531AE1A-FBA2-48B6-BAB8-84D02BD409EE",
    "Members": {
        "ModifyTime": 1615189819,
        "MemberDesc": "test",
        "MemberUid": 1234123412341234,
        "CreateTime": 1615189819,
        "MemberDisplayName": "cloudfirewall_test2",
        "MemberStatus": "normal"
    }
}
```


# DescribeAppGroupList {#concept_u1t_fx1_pfb .concept}

调用本API接口获取云防火墙应用组列表。

## 请求参数 {#section_lgd_3rt_vdb .section}

|参数|类型|是否必选|示例值|描述|
|RegionNo|String|否|cn-hangzhou|区域。|
|VpcId|String|否|vpc-318574052523|应用组所属VPC的VPC ID。|
|BizId|Number|否|1|应用组所属业务区ID。|
|CurrentPage|Number|否|1|起始页， 默认1。|
|PageSize|Number|否|20|每页大小，默认20。|
|AppGroupName|String|否|测试|应用组名称，支持模糊查询。|

## 返回参数 {#section_e1p_3nc_pfb .section}

|参数|类型|描述|
|code|Number|请求结果，code为200代表请求成功。|
|message|String|操作是否成功的消息提示。|
|data|Object|操作返回的结果。|
|PageInfo|Object|应用组列表页面信息，包含每页数量、当前页和总条数信息。|
|PageSize|Number|每页数量。|
|CurrentPage|Number|当前页。|
|TotalCount|Number|应用组列表的总条数。|
|AppGroupList|10|Array|应用组列表。|
|AppGroupId|Number|应用组ID。|
|RegionNo|String|应用组所属区域。|
|VpcId|String|应用组所属VPC的VPC ID。|
|AppGroupName|String|应用组名称。|
|Remark|String|应用组备注。|
|Level|String|应用组的重要程度。-   high：高等级
-   middle：中等级
-   low：低等级

|
|BizId|Number|应用组所属的业务区ID。|
|VpcName|String|应用组所属的VPC名称。|
|BizName|String|应用组所属的业务区名称。|
|EcsNum|Number|应用组下的ECS机器数量。|
|AppNum|Number|应用组下的应用数量。|
|Type|String|应用组创建的类型。-   auto：自动创建
-   manu：手动创建

|

## 示例 {#section_sz4_ctt_vdb .section}

**请求示例**

```

https://cloudfw.cn-hangzhou.aliyuncs.com/?Action=DescribeAppGroupList
&RegionNo=cn-hangzhou
&VpcId=vpc-ads123123412dsa
&BizId=1206
&CurrentPage=1
&PageSize=10
&公共请求参数
```

**返回示例**

```
{
   "code": 200, 
  "message": "successful",
   "data": {
     "PageInfo": {
     "PageSize": 6,
     "CurrentPage": 1, 
     "TotalCount": 12
   },
   "AppGroupList": [
     { 
       "AppGroupId": 1674, 
       "RegionNo": "cn-hangzhou",
       "VpcId": "vpc-as1231212a", 
       "AppGroupName": "group1",
       "Remark": "xxx",
       "Level": "middle",
       "BizId": 1,
       "VpcName": "测试VPC",
       "BizName": "测试业务区", 
       "EcsNum": 10,
       "AppNum": 10,
       "Type": "auto" 
   },
   {
       "AppGroupId": 1608,
       "RegionNo": "cn-hangzhou",
       "VpcId": "vpc-as1231212a", 
       "AppGroupName": "group1",
       "Remark": "xxx",
       "Level": "middle",
       "BizId": 1,
       "VpcName": "测试VPC",
       "BizName": "测试业务区",
       "EcsNum": 10,
       "AppNum": 10,
       "Type": "auto"
    },
    {
       "AppGroupId": 581,
       "RegionNo": "cn-hangzhou",
       "VpcId": "vpc-as1231212a",
       "AppGroupName": "group1",
       "Remark": "xxx", 
       "Level": "middle",
       "BizId": 1,
       "VpcName": "测试VPC",
       "BizName": "测试业务区",
       "EcsNum": 10,
       "AppNum": 10,
       "Type": "auto" 
    },
    { 
       "AppGroupId": 1283,
       "RegionNo": "cn-hangzhou",
       "VpcId": "vpc-as1231212a",
       "AppGroupName": "group1",
       "Remark": "xxx",
       "Level": "middle", 
       "BizId": 1,
       "VpcName": "测试VPC",
       "BizName": "测试业务区",
       "EcsNum": 10,
       "AppNum": 10,
       "Type": "auto"
    },
    {
       "AppGroupId": 816,
       "RegionNo": "cn-hangzhou",
       "VpcId": "vpc-as1231212a",
       "AppGroupName": "group1", 
       "Remark": "xxx",
       "Level": "middle",
       "BizId": 1, 
       "VpcName": "测试VPC",
       "BizName": "测试业务区",
       "EcsNum": 10, 
       "AppNum": 10,
       "Type": "auto"
     },
     { 
       "AppGroupId": 1251,
       "RegionNo": "cn-hangzhou",
       "VpcId": "vpc-as1231212a",
       "AppGroupName": "group1",
       "Remark": "xxx",
       "Level": "middle",
       "BizId": 1, 
       "VpcName": "测试VPC", 
       "BizName": "测试业务区",
        "EcsNum": 10,
        "AppNum": 10,
        "Type": "auto"
      },
      { 
       "AppGroupId": 1041,
        "RegionNo": "cn-hangzhou",
        "VpcId": "vpc-as1231212a",
        "AppGroupName": "group1",
        "Remark": "xxx", 
       "Level": "middle",
        "BizId": 1, 
       "VpcName": "测试VPC",
        "BizName": "测试业务区",
        "EcsNum": 10,
        "AppNum": 10,
        "Type": "auto"
      },
      {
        "AppGroupId": 1572,
        "RegionNo": "cn-hangzhou",
        "VpcId": "vpc-as1231212a",
        "AppGroupName": "group1",
        "Remark": "xxx",
        "Level": "middle",
        "BizId": 1, 
       "VpcName": "测试VPC",
        "BizName": "测试业务区", 
       "EcsNum": 10,
        "AppNum": 10,
        "Type": "auto" 
      },
      {
        "AppGroupId": 1687,
        "RegionNo": "cn-hangzhou",
        "VpcId": "vpc-as1231212a",
        "AppGroupName": "group1",
        "Remark": "xxx", 
       "Level": "middle",
        "BizId": 1,
        "VpcName": "测试VPC",
        "BizName": "测试业务区",
        "EcsNum": 10,
        "AppNum": 10, 
        "Type": "auto"
      },
      {
        "AppGroupId": 1282,
        "RegionNo": "cn-hangzhou", 
        "VpcId": "vpc-as1231212a",
        "AppGroupName": "group1",
        "Remark": "xxx", 
        "Level": "middle", 
        "BizId": 1,
        "VpcName": "测试VPC",
        "BizName": "测试业务区",
        "EcsNum": 10,
         "AppNum": 10, 
        "Type": "auto"
      }
    ]
  }
 }

```


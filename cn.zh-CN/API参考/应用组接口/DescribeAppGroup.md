# DescribeAppGroup {#concept_uds_yw1_pfb .concept}

调用本API接口查询云防火墙应用组。

## 请求参数 {#section_lgd_3rt_vdb .section}

|参数|类型|是否必选|示例值|描述|
|:-|:-|:---|:--|:-|
|AppGroupId|Number|是|1|应用组ID|

## 返回参数 {#section_e1p_3nc_pfb .section}

|参数|类型|描述|
|:-|:-|:-|
|code|Number|请求结果，code为200代表请求成功。|
|message|String|操作是否成功的消息提示。|
|data|Object|操作返回的结果。|
|AppGroupId|Number|应用组ID。|
|RegionNo|String|应用组所属区域。|
|VpcId|String|应用组所属VPC的VPC ID。|
|AppGroupName|String|应用组名称。|
|Remark|String|应用组备注。|
|Level|String|应用组的重要等级。-   high：高等级
-   middle：中等级
-   low：低等级

|
|BizId|Number|应用组所属业务区ID。|
|BizName|String|应用组所属业务区名称。|
|VpcName|String|应用组所属VPC名称。|
|Type|String|应用组创建的类型。-   auto：自动创建
-   manu：手动创建

|

## 示例 {#section_sz4_ctt_vdb .section}

**请求示例**

```

https://cloudfw.cn-hangzhou.aliyuncs.com/?Action=DescribeAppGroup
&AppGroupId=12
&公共请求参数
```

**返回示例**

```
{ 
  "code": 200,
  "message": "successful", 
  "data": {
    "AppGroupId": 1,
    "RegionNo": "cn-hangzhou",
    "VpcId": "vpc-as1231212a", 
    "AppGroupName": "group1", 
    "Remark": "xxx",
    "Level": "middle",
    "BizId": 1,
    "BizName": "测试业务区",
    "VpcName": "测试VPC",
    "Type": "auto" 
  } 
}

```


# DescribeBizList {#concept_ndf_pw1_pfb .concept}

调用本API接口可获取云防火墙业务区列表。

## 请求参数 {#section_lgd_3rt_vdb .section}

|参数|类型|是否必选|示例值|描述|
|:-|:-|:---|:--|:-|
|RegionNo|String|否|cn-hangzhou|业务区所属区域。|
|VpcId|String|否|vpc-ads123123412dsa|业务区所属VPC ID。|
|CurrentPage|Number|否|1|起始页，默认1。|
|PageSize|Number|否|20|每页显示数。量，默认20。|
|BizName|String|否|测试|业务区名称, 支持模糊查询。|

## 返回参数 {#section_trk_zx1_pfb .section}

|参数|类型|描述|
|:-|:-|:-|
|code|Number|请求结果，code为200代表请求成功。|
|message|String|操作是否成功的消息提示。|
|data|Object|操作返回的结果。|
|PageInfo|Object|业务区列表页面信息，包含当前页、每页显示量等。|
|PageSize|Number|每页数量。|
|CurrentPage|Number|当前页。|
|TotalCount|Number|应用组列表总条数。|
|BizList|Array|业务区列表。|
|RegionNo|String|业务区所属区域。|
|VpcId|String|业务区所属VPC的VPC ID。|
|BizName|String|业务区名称。|
|Remark|String|业务区备注。|
|Level|String|业务区重要等级。-   high：高等级
-   middle：中等级
-   low：低等级

|
|BizId|Number|业务区ID。|
|VpcName|String|业务区所属VPC名称。|
|AppGroupNum|Number|业务区下应用组数量。|
|AppNum|Number|业务区下应用数量。|
|EcsNum|Number|业务区下ECS机器数量。|
|Type|String|业务区创建的类型。-   auto：自动创建
-   manu：手动创建

|

## 示例 {#section_sz4_ctt_vdb .section}

**请求示例**

```

https://cloudfw.cn-hangzhou.aliyuncs.com/?Action=DescribeBizList
&RegionNo=cn-hangzhou
&VpcId=vpc-ads123123412dsa
&CurrentPage=1
&PageSize=10
&公共请求参数
```

**返回示例**

JSON格式

```
{ 
  "code": 200, 
  "message": "successful",  
  "data": {
    "PageInfo": { 
      "PageSize": 6, 
      "CurrentPage": 1,
      "TotalCount": 120
    },
    "BizList": [ 
      {
         "RegionNo": "cn-hangzhou", 
         "VpcId": "vpc-wz9rxkduq0k77srpxocxt",
         "BizName": "支付业务",
         "Remark": "x x x",
         "Level": "high",
         "BizId": 1,
         "VpcName": "测试VPC",
         "AppGroupNum": 0,
         "AppNum": 0,
         "EcsNum": 0, 
         "Type": "auto"
      }
    ] 
  } 
}
```


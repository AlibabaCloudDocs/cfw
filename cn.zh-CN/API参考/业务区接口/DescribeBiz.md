# DescribeBiz {#concept_yd4_kw1_pfb .concept}

调用本API接口可查询云防火墙业务区。

## 请求参数 {#section_lgd_3rt_vdb .section}

|参数|类型|是否必选|示例值|描述|
|:-|:-|:---|:--|:-|
|BizId|Number|是|1|业务区ID|

## 返回参数 {#section_trk_zx1_pfb .section}

|参数|类型|描述|
|:-|:-|:-|
|code|Number|请求结果，code为200代表请求成功。|
|message|String|操作是否成功的消息提示。|
|data|Object|操作返回的结果。|
|BizId|Number|业务区ID。|
|RegionNo|String|业务区所属区域。|
|VpcId|String|业务区所属VPC的VPC ID。|
|BizName|String|业务区名称。|
|Remark|String|业务区备注。|
|Level|String|业务区重要程度等级，默认值high。-   high：高等级
-   middle：中等级
-   low：低等级

 |
|VpcName|String|业务区所属VPC名称。|
|Type|String|业务区创建的类型。 -   auto：自动类型
-   manu：手动类型

 |

## 示例 {#section_sz4_ctt_vdb .section}

**请求示例**

```

https://cloudfw.cn-hangzhou.aliyuncs.com/?Action=DescribeBiz
&BizId=1068
&公共请求参数
```

**返回示例**

JSON格式

```
{ 
  "code": 200, 
  "message": "successful",
   "data": {
     "RegionNo": "cn-hangzhou",
     "VpcId": "vpc-wz9rxkduq0k77srpxocxt",
     "BizName": "支付业务",
     "Remark": "x x x", 
     "Level": "high",
     "BizId": 1, 
     "VpcName": "测试VPC", 
     "Type": "auto" 
}
 }
```


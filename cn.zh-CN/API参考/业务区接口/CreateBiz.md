# CreateBiz {#concept_isx_fw1_pfb .concept}

调用本接口新增云防火墙业务区。

## 请求参数 {#section_lgd_3rt_vdb .section}

|参数|类型|是否必选|示例值|描述|
|:-|:-|:---|:--|:-|
|VpcId|String|是|vpc-wz9rxkduq0k77srpxocxt|业务区所属VPC的ID。|
|BizName|String|是|支付业务|业务区名称。|
|Remark|String|否|提供登录服务|备注信息。|
|Level|String|否|middle|业务区重要等级，默认值为middle。-   high：高等级
-   middle：中等级
-   low：低等级

 |

## 返回参数 {#section_trk_zx1_pfb .section}

|参数|类型|描述|
|:-|:-|:-|
|code|Number|请求结果，code为200代表请求成功。|
|message|String|操作是否成功的消息提示。|
|data|Object|操作返回的结果。|
|BizId|Number|业务区ID。|

## 示例 {#section_sz4_ctt_vdb .section}

**请求示例**

```

https://cloudfw.cn-hangzhou.aliyuncs.com/?Action=CreateBiz
&VpcId=vpc-wz9rxkduq0k77srpxocxt
&BizName=登录业务
&Remark=提供了登录服务
&Level=middle
&公共请求参数
```

**返回示例**

JSON格式

```
{
  "code": 200, 
  "message": "successful", 
  "data": { 
  "BizId": 1 
  } 
}
```


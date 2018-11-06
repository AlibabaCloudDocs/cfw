# ModifyBiz {#concept_ycn_mw1_pfb .concept}

调用本接口可修改云防火墙业务区。

## 请求参数 {#section_lgd_3rt_vdb .section}

|参数|类型|是否必选|示例值|描述|
|BizId|String|是|1068|业务区ID。|
|BizName|String|否|登录业务|业务区名称。|
|Remark|String|否|提供登录服务|业务区备注。|
|Level|String|否|middle|业务区重要程度，默认值middle。-   high：高等级
-   middle：中等级
-   low：低等级

 |

## 返回参数 {#section_trk_zx1_pfb .section}

|参数|类型|描述|
|code|Number|请求结果，code为200代表请求成功。|
|message|String|操作是否成功的消息提示。|

## 示例 {#section_sz4_ctt_vdb .section}

**请求示例**

```

https://cloudfw.cn-hangzhou.aliyuncs.com/?Action=ModifyBiz
&BizId=1068
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
 }
```


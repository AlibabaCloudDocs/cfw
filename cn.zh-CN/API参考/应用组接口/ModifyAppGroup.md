# ModifyAppGroup {#concept_own_xw1_pfb .concept}

调用本API接口修改云防火墙应用组接口。

## 请求参数 {#section_lgd_3rt_vdb .section}

|参数|类型|是否必选|示例值|描述|
|:-|:-|:---|:--|:-|
|AppGroupId|Number|是|1|应用组ID。|
|AppGroupName|String|否|group1|应用组名称。|
|Remark|String|否|提供MYSQL服务|应用组备注。|
|Level|String|否|middle|应用组重要等级，默认值middle。-   high：高等级
-   middle：中等级
-   low：低等级

|
|BizId|Number|否|1|所属的业务区ID。|

## 返回参数 {#section_e1p_3nc_pfb .section}

|参数|类型|描述|
|:-|:-|:-|
|code|Number|请求结果，code为200代表请求成功。|
|message|String|操作是否成功的消息提示。|

## 示例 {#section_sz4_ctt_vdb .section}

**请求示例**

```

https://cloudfw.cn-hangzhou.aliyuncs.com/?Action=ModifyAppGroup
&AppGroupId=12
&AppGroupName=mysql
&Remark=提供了mysql服务
&Level=middle
&BizId=1068
&公共请求参数
```

**返回示例**

```
{
   "code": 200,
   "message": "successful",
}

```


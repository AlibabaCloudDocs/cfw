# DeleteAppGroup {#concept_kfy_vw1_pfb .concept}

调用本API接口删除云防火墙应用组。

## 请求参数 {#section_lgd_3rt_vdb .section}

|参数|类型|是否必选|示例值|描述|
|:-|:-|:---|:--|:-|
|AppGroupIdList|Array|是|\[1,2,3\]|应用组ID列表。|

## 返回参数 {#section_e1p_3nc_pfb .section}

|参数|类型|描述|
|:-|:-|:-|
|code|Number|请求结果，code为200代表请求成功。|
|message|String|操作是否成功的消息提示。|

## 示例 {#section_sz4_ctt_vdb .section}

**请求示例**

```

https://cloudfw.cn-hangzhou.aliyuncs.com/?Action=DeleteAppGroup
&AppGroupIdList=[12,368]
&公共请求参数
```

**返回示例**

```
{
   "code": 200,
   "message": "successful",
}

```


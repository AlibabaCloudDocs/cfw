# DeleteBiz {#concept_nly_3w1_pfb .concept}

调用本接口可删除云防火墙业务区。

## 请求参数 {#section_lgd_3rt_vdb .section}

|参数|类型|是否必选|示例值|描述|
|:-|:-|:---|:--|:-|
|BizIdList|Array|是|\[1,2,3\]|业务区ID列表|

## 返回参数 {#section_trk_zx1_pfb .section}

|参数|类型|描述|
|:-|:-|:-|
|code|Number|请求结果，code为200代表请求成功。|
|message|String|操作是否成功的消息提示。|

## 示例 {#section_sz4_ctt_vdb .section}

**请求示例**

```
https://cloudfw.cn-hangzhou.aliyuncs.com/?Action=DeleteBiz
&BizIdList=[1068,1792]
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


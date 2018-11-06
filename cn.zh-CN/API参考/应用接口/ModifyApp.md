# ModifyApp {#concept_gxf_kx1_pfb .concept}

调用本API修改云防火墙应用。

## 请求参数 {#section_lgd_3rt_vdb .section}

|参数|类型|是否必选|示例值|描述|
|AppId|Number|是|1|应用ID。|
|AppGroupId|Number|否|1|应用所属的应用组ID。|
|ProcPortList|Array|否|列表名称|进程端口监听列表，至少包含一个成员。|
|ListenPort|Number|是|80|监听端口, 范围1-65535。|
|ProcName|String|是|java|进程名称。|

## 返回参数 {#section_e1p_3nc_pfb .section}

|参数|类型|描述|
|code|Number|请求结果，code为200代表请求成功。|
|message|String|操作是否成功的消息提示。|

## 示例 {#section_sz4_ctt_vdb .section}

**请求示例**

```

https://cloudfw.cn-hangzhou.aliyuncs.com/?Action=ModifyApp
&AppId=12
&AppGroupId=1206
&ProcPortList=[{"ListenPort":3306,"ProcName":"mysql"},{"ListenPort":80,"ProcName":"tomcat"}]
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


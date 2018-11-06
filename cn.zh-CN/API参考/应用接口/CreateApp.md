# CreateApp {#concept_lfx_cx1_pfb .concept}

调用本API接口新增云防火墙应用。

## 请求参数 {#section_lgd_3rt_vdb .section}

|参数|类型|是否必选|示例值|描述|
|VpcId|String|是|vpc-wg123w38fgd9|应用所属的VPC ID。|
|AppGroupId|Number|是|1|应用所属的应用组ID。|
|AppParamList|Array|是|应用参数列表名称|应用参数列表。|
|EcsInstanceId|String|是|ecs-w89s9e8892w|应用所属的ECS实例ID。|
|ProcPortList|Array|是|进程端口监听列表名称|进程端口监听列表，至少包含一个成员。|
|ListenPort|Number|是|80|监听端口，范围1-65535。|
|ProcName|String|是|java|进程名。|

## 返回参数 {#section_e1p_3nc_pfb .section}

|参数|类型|描述|
|code|Number|请求结果，code为200代表请求成功。|
|message|String|操作是否成功的消息提示。|

## 示例 {#section_sz4_ctt_vdb .section}

**请求示例**

```

https://cloudfw.cn-hangzhou.aliyuncs.com/?Action=CreateApp
&VpcId=vpc-wz9rxkduq0k77srpxocxt
&AppGroupId=1206
&AppParamList=[{"EcsInstanceId":"ecs-w89s9e8892w","ProcPortList":[{"ListenPort":80,"ProcName":"java"}]}]
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


# DescribeAppListByEcs {#concept_qmb_qx1_pfb .concept}

调用本API接口可按ECS维度获取云防火墙应用列表。

## 请求参数 {#section_lgd_3rt_vdb .section}

|参数|类型|是否必选|示例值|描述|
|:-|:-|:---|:--|:-|
|RegionNo|String|否|cn-hangzhou|应用所属区域。|
|SortList|Array|否|排序参数|排序列表。|
|SortKey|String|是|ecsName|支持排序的关键字：EcsInstanecId、 EcsName、PublicIp、PrivateIp、RegionNo、VpcId|
|Dir|String|是|desc|应用列表字段排序的种类。-   desc：降序排序
-   asc：升序排序

|
|EcsInstanceId|String|否|ecs-28jwf8sa8230sd|应用对应的ECS实例ID，支持模糊查询。|
|EcsName|String|否|测试机器|应用对应的ECS实例名称，支持模糊查询。|
|EcsTag|String|否|tag1|应用对应的ECS标签，支持模糊查询。|
|PublicIp|String|否|1.1.1.1|公网IP，支持模糊查询。|
|PrivateIp|String|否|1.1.1.1|私网IP，支持模糊查询。|
|VpcId|String|否|vpc-as021n4k23023kjs|VPC ID。|
|ProcName|String|否|java|进程名，支持模糊查询。|
|BizName|String|否|testBiz|业务区名称，支持模糊查询。|
|AppGroupName|String|否|testAppGroup|应用组名称，支持模糊查询。|
|CurrentPage|Number|否|1|列表起始页，默认1。|
|PageSize|Number|否|60|列表每页数量，默认20。|
|ListenPort|Number|否|80|监听端口。|
|BizId|Number|否|1|业务区ID。|
|AppGroupId|Number|否|1|应用组ID。|

## 返回参数 {#section_e1p_3nc_pfb .section}

|参数|类型|描述|
|:-|:-|:-|
|code|Number|请求结果，code为200代表请求成功。|
|message|String|操作是否成功的消息提示。|
|data|Object|操作返回的结果。|
|PageInfo|Object|应用接口列表页面信息，包含每页数量、当前页和总条数信息。|
|PageSize|Number|每页数量。|
|CurrentPage|Number|当前页。|
|TotalCount|Number|总数量。|
|List|Array|ECS示例列表。|
|RegionNo|String|应用所属区域。|
|VpcId|String|应用所属VPC的VPC ID。|
|EcsInstanceId|String|应用对应ECS机器的实例ID。|
|EcsName|String|应用对应ECS机器的名称。|
|EcsTags|Array|应用对应ECS机器的标签。|
|PublicIp|String|公网IP。|
|PrivateIp|String|私网IP。|
|AppList|Array|应用列表。|
|AppGroupId|Number|应用组ID。|
|AppId|Number|应用ID。|
|AppGroupName|String|应用组名称。|
|BizId|Number|业务区ID。|
|BizName|String|业务区名称。|
|ProcPortList|Array|应用参数列表。|
|ListenPort|Number|监听端口。|
|ProcName|String|进程名。|
|Type|String|应用创建的类型。-   auto：自动创建
-   manu：手动创建

|
|Tags|String|应用的标签。|

## 示例 {#section_sz4_ctt_vdb .section}

**请求示例**

```

https://cloudfw.cn-hangzhou.aliyuncs.com/?Action=DescribeAppListByEcs
&RegionNo=cn-hangzhou
&VpcId=vpc-ads123123412dsa
&PrivateIp=172.0.46.1
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
       "TotalCount": 12 
     },
     "List": [
     {
        "RegionNo": "cn-hangzhou", 
        "VpcId": "vpc-wg123w38fgd9",
         "EcsInstanceId": "ecs-w89s9e8892w",
         "EcsName": "测试机器",
         "EcsTags": [
           "tag1", 
           "tag2" 
         ],
         "PublicIp": "1.1.1.1", 
         "PrivateIp": "1.1.1.1",
         "AppList": [
           {
           "AppGroupId": 1,
           "AppId": 817,
           "AppGroupName": "db组",
            "BizId": 1,
            "BizName": "支付业务",
            "ProcPortList": [
              { 
                "ListenPort": 53055,
                "ProcName": "java" 
              },
              {
                "ListenPort": 52248,
                "ProcName": "java"
               }
             ],
             "Type": "auto",
             "Tags": "web" },
           { 
             "AppGroupId": 1,
             "AppId": 168,
             "AppGroupName": "db组",
             "BizId": 1,
             "BizName": "支付业务",
             "ProcPortList": [
               {
                 "ListenPort": 48679,
                 "ProcName": "java" 
               },
               {
                 "ListenPort": 8098,
                 "ProcName": "java"
                }
              ],
              "Type": "auto",
              "Tags": "web"
            },
            {
              "AppGroupId": 1,
              "AppId": 424,
              "AppGroupName": "db组",
              "BizId": 1,
              "BizName": "支付业务",
              "ProcPortList": [
                { 
                  "ListenPort": 61623,
                  "ProcName": "java" 
                },
                {
                  "ListenPort": 59466,
                  "ProcName": "java"
                }
              ],
              "Type": "auto", 
              "Tags": "web"
            } 
          ] 
       },
       { 
          "RegionNo": "cn-hangzhou",
          "VpcId": "vpc-wg123w38fgd9",
          "EcsInstanceId": "ecs-w89s9e8892w",
          "EcsName": "测试机器",
          "EcsTags": [
            "tag1",
            "tag2"
          ],
          "PublicIp": "1.1.1.1",
          "PrivateIp": "1.1.1.1",
          "AppList": [
            { 
              "AppGroupId": 1,
              "AppId": 364,
              "AppGroupName": "db组",
              "BizId": 1, 
              "BizName": "支付业务",
              "ProcPortList": [
                { 
                  "ListenPort": 28180,
                  "ProcName": "java"
                },
                {
                  "ListenPort": 35036,
                  "ProcName": "java"
                }
              ],
              "Type": "auto",
              "Tags": "web"
            },
            { 
              "AppGroupId": 1,
              "AppId": 535,
              "AppGroupName": "db组",
              "BizId": 1,
              "BizName": "支付业务",
              "ProcPortList": [ 
                { 
                  "ListenPort": 52477,
                  "ProcName": "java"
                },
                {
                  "ListenPort": 55260,
                  "ProcName": "java"
                }
              ],
              "Type": "auto",
              "Tags": "web"
             },
             { 
              "AppGroupId": 1,
              "AppId": 322,
              "AppGroupName": "db组",
              "BizId": 1,
              "BizName": "支付业务",
              "ProcPortList": [
                { 
                  "ListenPort": 1508,
                  "ProcName": "java"
                },
                {
                  "ListenPort": 28814,
                  "ProcName": "java" 
                }
              ],
              "Type": "auto",
              "Tags": "web"
            } 
          ] 
        } 
      ] 
    }
 } 

```


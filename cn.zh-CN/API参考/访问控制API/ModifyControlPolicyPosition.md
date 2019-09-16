# ModifyControlPolicyPosition {#doc_api_Cloudfw_ModifyControlPolicyPosition .reference}

调用ModifyControlPolicyPosition接口修改访问控制策略的优先级。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cloudfw&api=ModifyControlPolicyPosition&type=RPC&version=2017-12-07)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|ModifyControlPolicyPosition|系统规定参数。取值：ModifyControlPolicyPosition。

 |
|Direction|String|是|in|访问控制策略的流量方向。

 -   **in**：外对内流量访问控制
-   **out**：内对外流量访问控制

 |
|NewOrder|String|是|1|新优先级。修改访问控制策略优先级为新设置的优先级。

 |
|OldOrder|String|是|5|老优先级。待修改访问控制策略的优先级。

 |
|Lang|String|否|zh|指定请求和接收消息的语言类型。

 -   **zh**：中文
-   **en**：英文

 |
|SourceIp|String|否|1.2.3.4|访问者源IP地址。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|850A84D6-0DE4-4797-A1E8-00090125EEB1|返回结果的请求ID。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=ModifyControlPolicyPosition
&Direction=in
&NewOrder=1
&OldOrder=5
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<ModifyControlPolicyPosition>
	  <RequestId>850A84D6-0DE4-4797-A1E8-00090125EEB1</RequestId>
</ModifyControlPolicyPosition>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"RequestId":"850A84D6-0DE4-4797-A1E8-00090125EEB1"
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.aliyun.com/status/product/Cloudfw)查看更多错误码。


# ModifyPolicyAdvancedConfig

Controls whether to enable the strict mode for an access control policy.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cloudfw&api=ModifyPolicyAdvancedConfig&type=RPC&version=2017-12-07)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|ModifyPolicyAdvancedConfig|The operation that you want to perform.

 Set the value to **ModifyPolicyAdvancedConfig**. |
|InternetSwitch|String|Yes|off|Specifies whether to enable the strict mode for the access control policy. Valid values:

 -   **on**: Enable the strict mode.
-   **off**: Disable the strict mode. |
|SourceIp|String|No|1.2.3.4|The source IP address of the request. |
|Lang|String|No|zh|The language of the request and response. Valid values:

 -   **zh**: Chinese
-   **en**: English |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|B2841452-CB8D-4F7D-B247-38E1CF7334F8|The ID of the request. |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=ModifyPolicyAdvancedConfig
&InternetSwitch=off
&<Common request parameters>
```

Sample success responses

`XML` format

```
<ModifyPolicyAdvancedConfigResponse>
   <RequestId>B2841452-CB8D-4F7D-B247-38E1CF7334F8</RequestId>
</ModifyPolicyAdvancedConfigResponse>
```

`JSON` format

```
{
    "RequestId":"B2841452-CB8D-4F7D-B247-38E1CF7334F8"
}
```


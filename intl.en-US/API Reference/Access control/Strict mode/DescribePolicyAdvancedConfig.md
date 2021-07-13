# DescribePolicyAdvancedConfig

Queries whether the strict mode is enabled for an access control policy.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cloudfw&api=DescribePolicyAdvancedConfig&type=RPC&version=2017-12-07)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribePolicyAdvancedConfig|The operation that you want to perform.

 Set the value to **DescribePolicyAdvancedConfig**. |
|SourceIp|String|No|1.2.3.4|The source IP address of the request. |
|Lang|String|No|zh|The language of the request and response. Valid values:

 -   **zh**: Chinese
-   **en**: English |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|InternetSwitch|String|off|Indicates whether the strict mode is enabled for the access control policy. Valid values:

 -   **on**: The strict mode is enabled.
-   **off**: The strict mode is disabled. |
|RequestId|String|850A84D6-0DE4-4797-A1E8-00090125EEB1|The ID of the request. |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=DescribePolicyAdvancedConfig
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DescribePolicyAdvancedConfigResponse>
    <RequestId>850A84D6-0DE4-4797-A1E8-00090125EEB1</RequestId>
    <InternetSwitch>off</InternetSwitch>
</DescribePolicyAdvancedConfigResponse>
```

`JSON` format

```
{
    "RequestId":"850A84D6-0DE4-4797-A1E8-00090125EEB1",
    "InternetSwitch":"off"
}
```


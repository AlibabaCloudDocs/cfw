# ResetVpcFirewallRuleHitCount

Resets the count on hits of an access control policy in a specific policy group for a VPC firewall.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cloudfw&api=ResetVpcFirewallRuleHitCount&type=RPC&version=2017-12-07)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|ResetVpcFirewallRuleHitCount|The operation that you want to perform.

 Set the value to **ResetVpcFirewallRuleHitCount**. |
|AclUuid|String|Yes|00281255-d220-4db1-8f4f-c4df221ad84c|The unique ID of the access control policy.

 If you want to delete an access control policy, you must provide the ID of the policy. You can call the DescribeVpcFirewallControlPolicy operation to obtain the ID. |
|Lang|String|No|zh|The natural language of the request and response. Valid values:

 Valid values:

 -   **zh**: Chinese
-   **en**: English |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D|The ID of the request. |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=ResetVpcFirewallRuleHitCount
&AclUuid=00281255-d220-4db1-8f4f-c4df221a1234
&<Common request parameters>
```

Sample success responses

`XML` format

```
<ResetVpcFirewallRuleHitCountResponse>
  <RequestId>CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D</RequestId>
</ResetVpcFirewallRuleHitCountResponse>
```

`JSON` format

```
{
    "RequestId": "CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D"
}
```


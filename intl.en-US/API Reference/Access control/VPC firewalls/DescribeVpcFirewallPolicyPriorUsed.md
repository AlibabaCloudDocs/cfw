# DescribeVpcFirewallPolicyPriorUsed

Queries the priority range of access control policies in a specific policy group for a VPC firewall.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cloudfw&api=DescribeVpcFirewallPolicyPriorUsed&type=RPC&version=2017-12-07)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeVpcFirewallPolicyPriorUsed|The operation that you want to perform.

 Set the value to **DescribeVpcFirewallPolicyPriorUsed**. |
|VpcFirewallId|String|Yes|vfw-a42bbb7b887148c9\*\*\*\*|The ID of the access control policy group. You can call the DescribeVpcFirewallAclGroupList operation to obtain the ID.

 Valid values:

 -   If the VPC firewall is used to protect a Cloud Enterprise Network \(CEN\), the ID of the CEN instance is used.

Example: cen-ervw0g12b5jbw\*\*\*\*

-   If the VPC firewall is used to protect an Express Connect, the ID of the VPC firewall instance is used.

Example: vfw-a42bbb7b887148c9\*\*\*\* |
|Lang|String|No|zh|The natural language of the request and response. Valid values:

 Valid values:

 -   **zh**: Chinese
-   **en**: English |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|End|Integer|150|The lowest priority for the access control policies in the policy group. |
|RequestId|String|CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D|The ID of the request. |
|Start|Integer|1|The highest priority for the access control policies in the policy group. |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=DescribeVpcFirewallPolicyPriorUsed
&VpcFirewallId=vfw-a42bbb7b887148c9****
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DescribeVpcFirewallPolicyPriorUsedResponse>
  <RequestId>CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D</RequestId>
  <Start>1</Start>
  <End>150</End>
</DescribeVpcFirewallPolicyPriorUsedResponse>
```

`JSON` format

```
{
    "RequestId": "CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D",
    "Start": 1,
    "End": 150
}
```


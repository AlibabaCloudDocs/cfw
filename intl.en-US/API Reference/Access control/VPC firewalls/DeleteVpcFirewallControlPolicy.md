# DeleteVpcFirewallControlPolicy

Deletes an access control policy from a specific policy group for a VPC firewall.

**Note:** The VPC firewall instance used to protect each Cloud Enterprise Network \(CEN\) and the VPC firewall instance used to protect each Express Connect use different access control policies.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cloudfw&api=DeleteVpcFirewallControlPolicy&type=RPC&version=2017-12-07)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DeleteVpcFirewallControlPolicy|The operation that you want to perform.

 Set the value to **DeleteVpcFirewallControlPolicy**. |
|AclUuid|String|Yes|00281255-d220-4db1-8f4f-c4df2214\*\*\*\*|The unique ID of the access control policy.

 If you want to delete an access control policy, you must provide the ID of the policy. You can call the **DescribeVpcFirewallControlPolicy** operation to obtain the ID. |
|VpcFirewallId|String|Yes|vfw-a42bbb7b887148c91\*\*\*\*|The ID of the access control policy group. You can call the **DescribeVpcFirewallAclGroupList** operation to obtain the ID.

 Valid values:

 -   If the VPC firewall is used to protect a CEN, the ID of the CEN instance is used.

Example: cen-ervw0g12b5jbw\*\*\*\*

-   If the VPC firewall is used to protect an Express Connect, the ID of the VPC firewall instance is used.

Example: vfw-a42bbb7b887148c9\*\*\*\* |
|Lang|String|No|zh|The natural language of the request and response. Valid values:

 -   **zh**: Chinese
-   **en**: English |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D|The ID of the request. |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=DeleteVpcFirewallControlPolicy
&VpcFirewallId=vfw-a42bbb7b887148c9****
&AclUuid=00281255-d220-4db1-8f4f-c4df221ad84c
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DeleteVpcFirewallControlPolicyResponse>
  <RequestId>CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D</RequestId>
</DeleteVpcFirewallControlPolicyResponse>
```

`JSON` format

```
{
    "RequestId": "CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D"
}
```


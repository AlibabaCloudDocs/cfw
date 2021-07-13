# ModifyVpcFirewallControlPolicyPosition

Modifies the priority of an access control policy in a specific policy group for a VPC firewall.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cloudfw&api=ModifyVpcFirewallControlPolicyPosition&type=RPC&version=2017-12-07)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|ModifyVpcFirewallControlPolicyPosition|The operation that you want to perform.

Set the value to **ModifyVpcFirewallControlPolicyPosition**. |
|NewOrder|String|Yes|1|The new priority of the access control policy. |
|OldOrder|String|Yes|5|The original priority of the access control policy. |
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
|RequestId|String|850A84D6-0DE4-4797-A1E8-00090125EEB1|The ID of the request. |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=ModifyVpcFirewallControlPolicyPosition
&VpcFirewallId=vfw-a42bbb7b887148c9****
&NewOrder=1
&OldOrder=5
&<Common request parameters>
```

Sample success responses

`XML` format

```
<ModifyVpcFirewallControlPolicyPositionResponse>
  <RequestId>850A84D6-0DE4-4797-A1E8-00090125EEB1</RequestId>
</ModifyVpcFirewallControlPolicyPositionResponse>
```

`JSON` format

```
{
    "RequestId": "850A84D6-0DE4-4797-A1E8-00090125EEB1"
}
```


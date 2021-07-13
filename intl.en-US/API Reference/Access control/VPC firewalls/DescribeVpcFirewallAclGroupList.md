# DescribeVpcFirewallAclGroupList

Queries information about access control policy groups for VPC firewalls.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cloudfw&api=DescribeVpcFirewallAclGroupList&type=RPC&version=2017-12-07)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeVpcFirewallAclGroupList|The operation that you want to perform.

Set the value to **DescribeVpcFirewallAclGroupList**. |
|Lang|String|No|zh|The natural language of the request and response. Valid values:

-   **zh**: Chinese
-   **en**: English |
|FirewallConfigureStatus|String|No|configured|Specifies whether VPC firewalls are configured.

-   **notconfigured**: VPC firewalls are not configured.
-   **configured**: VPC firewalls are configured.
-   If you do not specify this parameter, all access control policy groups are queried, regardless of whether VPC firewalls are configured. |
|CurrentPage|String|No|1|The number of the page to return.

Default value: 1. |
|PageSize|String|No|10|The number of entries to return on each page.

Maximum value: 50. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|AclGroupList|Array| |The information about access control policy groups for VPC firewalls. |
|AclGroupId|String|vfw-a42bbb7b887148c9\*\*\*\*|The ID of the access control policy group. You can call the **DescribeVpcFirewallAclGroupList** operation to obtain the ID.

Valid values:

-   If the VPC firewall is used to protect a CEN, the ID of the CEN instance is returned.

Example: cen-ervw0g12b5jbw\*\*\*\*

-   If the VPC firewall is used to protect an Express Connect, the ID of the VPC firewall instance is returned.

Example: vfw-a42bbb7b887148c9\*\*\*\* |
|AclGroupName|String|group\_test|The name of the access control policy group.

-   If the VPC firewall is used to protect a CEN, the name of the CEN instance is returned.
-   If the VPC firewall is used to protect an Express Connect, the name of the VPC firewall is returned. |
|RequestId|String|CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D|The ID of the request. |
|TotalCount|Integer|1|The total number of the access control policy groups for the VPC firewalls. |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=DescribeVpcFirewallAclGroupList
&FirewallConfigureStatus=configured
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DescribeVpcFirewallAclGroupListResponse>
  <TotalCount>1</TotalCount>
  <AclGroupList>
        <AclGroupId>vfw-a42bbb7b887148c9****</AclGroupId>
        <AclGroupName>group_test</AclGroupName>
  </AclGroupList>
</DescribeVpcFirewallAclGroupListResponse>
```

`JSON` format

```
{"TotalCount":1,"AclGroupList":[{"AclGroupId":"vfw-a42bbb7b887148c9****","AclGroupName":"group_test"}]}
```


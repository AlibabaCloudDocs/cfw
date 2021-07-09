# DescribeAssetList

Queries the assets that are protected by Cloud Firewall.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cloudfw&api=DescribeAssetList&type=RPC&version=2017-12-07)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeAssetList|The operation that you want to perform.

 Set the value to **DescribeAssetList**. |
|CurrentPage|String|Yes|1|The page number of the current page. Default value: 1. |
|PageSize|String|Yes|10|The number of entries to return on each page. Maximum value: 50. |
|SourceIp|String|No|1.2.3.5|The source IP address of the request. |
|Lang|String|No|zh|The natural language of the request and response. Valid values:

 -   **zh**: Chinese
-   **en**: English |
|RegionNo|String|No|cn-hangzhou|The ID of the region that Cloud Firewall supports. |
|Status|String|No|open|The status of the firewall. Valid values:

 -   **open**: The firewall is enabled.
-   **opening**: The firewall is being enabled.
-   **closed**: The firewall is disabled.
-   **closing**: The firewall is being disabled. |
|SearchItem|String|No|1.1.XX.XX|The ID or the IP address of the asset that you want to query. |
|Type|String|No|eip|This parameter is deprecated. |
|ResourceType|String|No|EcsEIP|The type of the asset. Valid values:

 -   **BastionHostEgressIP**: the egress IP address of a bastion host
-   **BastionHostIngressIP**: the ingress IP address of a bastion host
-   **EcsEIP**: the elastic IP address \(EIP\) of an Elastic Compute Service \(ECS\) instance
-   **EcsPublicIP**: the public IP address of an ECS instance
-   **EIP**: the EIP
-   **EniEIP**: the EIP of an elastic network interface \(ENI\)
-   **NatEIP**: the EIP of a Network Address Translation \(NAT\) gateway
-   **SlbEIP**: the EIP of a Server Load Balancer \(SLB\) instance
-   **SlbPublicIP**: the public IP address of an SLB instance
-   **NatPublicIP**: the public IP address of a NAT gateway
-   **HAVIP**: the high-availability virtual IP address \(HAVIP\) |
|SgStatus|String|No|pass|The status of the security group policy. Valid values:

 -   **pass**: delivered
-   **block**: undelivered
-   **unsupport**: unsupported |
|IpVersion|String|No|6|The IP version of the asset that is protected by Cloud Firewall.

 Valid values:

 -   4: IPv4
-   6: IPv6 |
|MemberUid|Long|No|1111222233334444|The user ID \(UID\) of the member account that is added to Cloud Firewall. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Assets|Array of Resource| |The details about the assets that are protected by Cloud Firewall. |
|AliUid|Long|1234123412341234|The UID of the Alibaba Cloud account. |
|BindInstanceId|String|i-8vbdrjrxzt78\*\*\*\*|The ID of the asset that is bound to Cloud Firewall. |
|BindInstanceName|String|instance01|The name of the asset that is bound to Cloud Firewall. |
|InternetAddress|String|1.1.XX.XX|The public IP address of the server. |
|IntranetAddress|String|192.168.XX.XX|The internal IP address of the server. |
|IpVersion|Integer|6|The IP version of the asset that is protected by Cloud Firewall.

 Valid values:

 -   4: IPv4
-   6: IPv6 |
|MemberUid|Long|1111222233334444|The UID of the member account that is added to Cloud Firewall. |
|Name|String|instance01|The name of the asset that is protected by Cloud Firewall. |
|Note|String|REGION\_NOT\_SUPPORT|The remarks. Valid values:

 -   **REGION\_NOT\_SUPPORT**: The region is not supported.
-   **NETWORK\_NOT\_SUPPORT**: The network is not supported.
-   This parameter is left empty. |
|ProtectStatus|String|open|The status of the firewall. Valid values:

 -   **open**: The firewall is enabled.
-   **opening**: The firewall is being enabled.
-   **closed**: The firewall is disabled.
-   **closing**: The firewall is being disabled. |
|RegionID|String|cn-hangzhou|The ID of the region that Cloud Firewall supports. |
|RegionStatus|String|enable|Indicates whether the firewall is supported in the region. Valid values:

 -   **enable**: supported
-   **disable**: unsupported |
|ResourceInstanceId|String|i-8vbdrjrxzt78\*\*\*\*|The ID of the asset. |
|ResourceType|String|EcsPublicIP|The type of the asset. Valid values:

 -   **BastionHostEgressIP**: the egress IP address of a bastion host
-   **BastionHostIngressIP**: the ingress IP address of a bastion host
-   **EcsEIP**: the EIP of an ECS instance
-   **EcsPublicIP**: the public IP address of an ECS instance
-   **EIP**: the EIP
-   **EniEIP**: the EIP of an ENI
-   **NatEIP**: the EIP of a NAT gateway
-   **SlbEIP**: the EIP of an SLB instance
-   **SlbPublicIP**: the public IP address of an SLB instance
-   **NatPublicIP**: the public IP address of a NAT gateway
-   **HAVIP**: the HAVIP |
|SgStatus|String|block|The status of the security group policy. Valid values:

 -   **pass**: delivered
-   **block**: undelivered |
|SgStatusTime|Long|1615082937|The time when the status of the security group was last checked. Unit: seconds. |
|SyncStatus|String|enable|The status of traffic redirection for an asset. Valid values:

 -   **enable**: Traffic redirection is supported.
-   **disable**: Traffic redirection is not supported. |
|Type|String|eip|This parameter is deprecated. |
|RequestId|String|CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D|The ID of the request. |
|TotalCount|Integer|12|The total number of the assets that are protected by Cloud Firewall. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=DescribeAssetList
&CurrentPage=1
&PageSize=10
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DescribeAssetListResponse>
  <TotalCount>12</TotalCount>
  <RequestId>CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D</RequestId>
  <Assets>
        <BindInstanceId>i-8vbdrjrxzt78****</BindInstanceId>
        <InternetAddress>1.1.XX.XX</InternetAddress>
        <MemberUid>1111222233334444</MemberUid>
        <RegionStatus>enable</RegionStatus>
        <IpVersion>6</IpVersion>
        <SgStatusTime>1615082937</SgStatusTime>
        <SyncStatus>enable</SyncStatus>
        <ResourceType>EcsPublicIP</ResourceType>
        <Name>instance01</Name>
        <SgStatus>block</SgStatus>
        <IntranetAddress>192.168.XX.XX</IntranetAddress>
        <Type>eip</Type>
        <Note>REGION_NOT_SUPPORT</Note>
        <BindInstanceName>instance01</BindInstanceName>
        <ProtectStatus>open</ProtectStatus>
        <RegionID>cn-hangzhou</RegionID>
        <ResourceInstanceId>i-8vbdrjrxzt78****</ResourceInstanceId>
        <AliUid>1234123412341234</AliUid>
  </Assets>
</DescribeAssetListResponse>
```

`JSON` format

```
{
    "TotalCount": 12,
    "RequestId": "CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D",
    "Assets": {
        "BindInstanceId": "i-8vbdrjrxzt78****",
        "InternetAddress": "1.1.XX.XX",
        "MemberUid": 1111222233334444,
        "RegionStatus": "enable",
        "IpVersion": 6,
        "SgStatusTime": 1615082937,
        "SyncStatus": "enable",
        "ResourceType": "EcsPublicIP",
        "Name": "instance01",
        "SgStatus": "block",
        "IntranetAddress": "192.168.XX.XX",
        "Type": "eip",
        "Note": "REGION_NOT_SUPPORT",
        "BindInstanceName": "instance01",
        "ProtectStatus": "open",
        "RegionID": "cn-hangzhou",
        "ResourceInstanceId": "i-8vbdrjrxzt78****",
        "AliUid": 1234123412341234
    }
}
```


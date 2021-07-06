# PutEnableFwSwitch

You can call this operation to turn on a firewall switch.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cloudfw&api=PutEnableFwSwitch&type=RPC&version=2017-12-07)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|PutEnableFwSwitch|The operation that you want to perform.

Set the value to PutEnableFwSwitch. |
|SourceIp|String|No|1.2.X.X|The source IP address of the request. |
|Lang|String|No|zh|The natural language of the request and response. Valid values:

-   **zh**: Chinese
-   **en**: English |
|IpaddrList.N|RepeatList|No|\["1.2.X.X","5.6.X.X"\]|The list of IP addresses.

**Note:** You must configure at least one of the IpaddrList, RegionList, ResourceTypeList parameters. |
|RegionList.N|RepeatList|No|\["cn-hangzhou","cn-shanghai"\]|The list of regions.

**Note:** You must configure at least one of the IpaddrList, RegionList, ResourceTypeList parameters. |
|ResourceTypeList.N|RepeatList|No|\["EcsPublicIp","NatEip"\]|The list of asset types.

Valid values:

-   BastionHostIP: the IP address of a bastion host
-   EcsEIP: the EIP of an ECS instance
-   EcsPublicIP: the public IP address of an ECS instance
-   EIP
-   EniEIP: the EIP of an ENI
-   NatEIP: the EIP of a NAT gateway
-   SlbEIP: the EIP of an SLB instance
-   SlbPublicIP: the public IP address of an SLB instance
-   NatPublicIP: the public IP address of a NAT gateway
-   HAVIP: the HA VIP

**Note:** You must configure at least one of the IpaddrList, RegionList, ResourceTypeList parameters. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|B2841452-CB8D-4F7D-B247-38E1CF7334F8|The ID of the request. |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=PutEnableFwSwitch&IpaddrList=["1.2.X.X","5.6.X.X"]
&<Common request parameters>
```

Sample success responses

`XML` format

```
<RequestId>B2841452-CB8D-4F7D-B247-38E1CF7334F8</RequestId>
```

`JSON` format

```
{
    "RequestId":"B2841452-CB8D-4F7D-B247-38E1CF7334F8"
}
```


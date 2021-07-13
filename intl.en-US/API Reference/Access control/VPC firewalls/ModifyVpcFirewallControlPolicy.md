# ModifyVpcFirewallControlPolicy

Modifies the configuration of an access control policy in a specific policy group for a VPC firewall.

**Note:** The VPC firewall instance used to protect each Cloud Enterprise Network \(CEN\) and the VPC firewall instance used to protect each Express Connect use different access control policies.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cloudfw&api=ModifyVpcFirewallControlPolicy&type=RPC&version=2017-12-07)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|ModifyVpcFirewallControlPolicy|The operation that you want to perform.

Set the value to **ModifyVpcFirewallControlPolicy**. |
|AclAction|String|Yes|accept|The action that Cloud Firewall performs on the traffic.

Valid values:

-   **accept:**allows the traffic.
-   **drop:**denies the traffic.
-   **log:**monitors the traffic. |
|AclUuid|String|Yes|00281255-d220-4db1-8f4f-c4df221ad84c|The unique ID of the access control policy.

If you want to modify an access control policy, you must provide the ID of the policy. You can call the DescribeVpcFirewallControlPolicy operation to obtain the ID. |
|ApplicationName|String|Yes|HTTP|The application type that the access control policy supports.

Valid values:

-   **ANY** \(indicates that all application types are supported\)
-   **FTP**
-   **HTTP**
-   **HTTPS**
-   **MySQL**
-   **SMTP**
-   **SMTPS**
-   **RDP**
-   **VNC**
-   **SSH**
-   **Redis**
-   **MQTT**
-   **MongoDB**
-   **Memcache**
-   **SSL** |
|Description|String|Yes|test|The description of the access control policy. |
|Destination|String|Yes|10.2.3.0/24|The destination address in the access control policy.

-   If **DestinationType** is set to `net`, the value of this parameter is a CIDR block.

Example: 10.2.3.0/24

-   If **DestinationType** is set to `group`, the value of this parameter is an address book.

Example: db\_group

-   If **DestinationType** is set to `domain`, the value of this parameter is a domain name.

Example: \*.aliyuncs.com |
|DestinationType|String|Yes|net|The type of the destination address in the access control policy.

Valid values:

-   **net**: CIDR block
-   **group**: address book
-   **domain:**domain name |
|Proto|String|Yes|TCP|The type of the security protocol in the access control policy.

Valid values:

-   **ANY** \(indicates all protocol types\)
-   **TCP**
-   **UDP**
-   **ICMP** |
|Source|String|Yes|10.2.4.0/24|The source address in the access control policy.

Valid values:

-   If **SourceType** is set to `net`, the value of this parameter is a CIDR block.

Example: 10.2.4.0/24

-   If **SourceType** is set to `group`, the value of this parameter is an address book.

Example: db\_group |
|SourceType|String|Yes|net|The type of the source address in the access control policy.

Valid values:

-   **net**: CIDR block
-   **group:**address book |
|VpcFirewallId|String|Yes|vfw-a42bbb7b887148c9\*\*\*\*|The ID of the access control policy group. You can call the DescribeVpcFirewallAclGroupList operation to obtain the ID.

-   If the VPC firewall is used to protect a CEN, the ID of the CEN instance is used.

Example: cen-ervw0g12b5jbw\*\*\*\*

-   If the VPC firewall is used to protect an Express Connect, the ID of the VPC firewall instance is used.

Example: vfw-a42bbb7b887148c9\*\*\*\* |
|Lang|String|No|zh|The natural language of the request and response. Valid values:

Valid values:

-   **zh**: Chinese
-   **en**: English |
|DestPort|String|No|80|The destination port in the access control policy. |
|DestPortType|String|No|port|The type of the destination port in the access control policy.

-   **port:**port
-   **group** :port address book |
|DestPortGroup|String|No|my\_port\_group|The destination port address book in the access control policy. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D|The ID of the request. |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=ModifyVpcFirewallControlPolicy
&VpcFirewallId=vfw-a42bbb7b887148c9****
&AclAction=accept
&AclUuid=00281255-d220-4db1-8f4f-c4df221ad84c
&ApplicationName=ANY
&Description=demo_rule_1
&Destination=10.2.3.0/24
&DestinationType=net
&Proto=TCP
&Source=10.2.4.0/24
&SourceType=net
&<Common request parameters>
```

Sample success responses

`XML` format

```
<ModifyVpcFirewallControlPolicyResponse>
  <RequestId>CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D</RequestId>
</ModifyVpcFirewallControlPolicyResponse>
```

`JSON` format

```
{
    "RequestId": "CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D"
}
```


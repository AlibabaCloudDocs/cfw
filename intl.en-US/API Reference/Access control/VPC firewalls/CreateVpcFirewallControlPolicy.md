# CreateVpcFirewallControlPolicy

Adds an access control policy to a specific policy group for a Virtual Private Cloud \(VPC\) firewall.

**Note:** You must create different access control policies for a VPC firewall used to protect Cloud Enterprise Network \(CEN\) and a VPC firewall used to protect Express Connect.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cloudfw&api=CreateVpcFirewallControlPolicy&type=RPC&version=2017-12-07)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|CreateVpcFirewallControlPolicy|The operation that you want to perform.

Set the value to **CreateVpcFirewallControlPolicy**. |
|AclAction|String|Yes|accept|The action that Cloud Firewall performs on the traffic. Valid values:

-   **accept**: allows the traffic.
-   **drop**: denies the traffic.
-   **log**: monitors the traffic. |
|ApplicationName|String|Yes|HTTP|The application type that the access control policy supports. Valid values:

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
-   **SSL**
-   **ANY**: indicates that all application types are supported. |
|Description|String|Yes|test|The description of the access control policy. |
|Destination|String|Yes|10.2.3.0/24|The destination address in the access control policy.

Set this parameter in the following way:

-   If the **DestinationType** parameter is set to `net`, set the value to a Classless Inter-Domain Routing \(CIDR\) block.****

Example: 10.2.3.0/24.

-   If the **DestinationType** parameter is set to `group`, set the value to the name of an address book.****

Example: db\_group.

-   If the **DestinationType** parameter is set to `domain`, set the value to a domain name.****

Example: \*.aliyuncs.com. |
|DestinationType|String|Yes|net|The type of the destination address in the access control policy. Valid values:

-   **net**: CIDR block
-   **group**: address book
-   **domain**: domain name |
|NewOrder|String|Yes|-1|The priority of the access control policy.

The priority value starts from 1. A smaller priority value indicates a higher priority.

**Note:** The value of -1 indicates the lowest priority. |
|Proto|String|Yes|TCP|The security protocol in the access control policy. Valid values:

-   **ANY**: indicates that all protocols are supported.
-   **TCP**
-   **UDP**
-   **ICMP** |
|Source|String|Yes|10.2.3.0/24|The source address in the access control policy.

-   If the SourceType parameter is set to `net`, set the value to a CIDR block. Example: 10.2.3.0/24.
-   If the SourceType parameter is set to `group`, set the value to the name of an address book. Example: db\_group. |
|SourceType|String|Yes|net|The type of the source address in the access control policy. Valid values:

-   **net**: CIDR block
-   **group**: address book |
|VpcFirewallId|String|Yes|vfw-a42bbb7b887148c9\*\*\*\*|The ID of the policy group to which you want to add the access control policy.

-   If the VPC firewall is used to protect CEN, set the value to the ID of the CEN instance that the VPC firewall protects. Example: cen-ervw5jbw1234\*\*\*\*\*.
-   If the VPC firewall is used to protect Express Connect, set the value to the ID of the VPC firewall instance. Example: vfw-a42bbb748c91234\*\*\*\*\*.

**Note:** You can call the [DescribeVpcFirewallAclGroupList](~~159760~~) operation to query the ID of the policy group. |
|Lang|String|No|zh|The natural language of the request and response. Valid values:

-   **zh**: Chinese
-   **en**: English |
|DestPort|String|No|80|The destination port in the access control policy.

**Note:** This parameter must be specified if the **DestPortType** parameter is set to `port`. |
|DestPortType|String|No|net|The type of the destination port in the access control policy. Valid values:

-   **port**: port
-   **group**: address book |
|DestPortGroup|String|No|my\_port\_group|The address book of destination ports in the access control policy.

**Note:** This parameter must be specified if the **DestPortType** parameter is set to `group`. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|AclUuid|String|00281255-d220-4db1-8f4f-c4df221ad84c|The unique ID of the access control policy. |
|RequestId|String|CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D|The ID of the request. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=CreateVpcFirewallControlPolicy
&VpcFirewallId=vfw-a42bbb7b887148c9****
&AclAction=accept
&ApplicationName=ANY
&Description=demo_rule_1
&Destination=10.2.3.0/24
&DestinationType=net
&NewOrder=-1
&Proto=TCP
&Source=10.2.3.0/24
&SourceType=net
&<Common request parameters>
```

Sample success responses

`XML` format

```
<CreateVpcFirewallControlPolicyResponse>
    <RequestId>CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D</RequestId>
    <AclUuid>00281255-d220-4db1-8f4f-c4d*********</AclUuid>
</CreateVpcFirewallControlPolicyResponse>
```

`JSON` format

```
{
    "RequestId": "CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D",
    "AclUuid": "00281255-d220-4db1-8f4f-c4d*********"
}
```


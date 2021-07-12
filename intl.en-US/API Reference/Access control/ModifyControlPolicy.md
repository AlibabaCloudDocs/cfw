# ModifyControlPolicy

You can call this operation to modify the configurations of an access control policy.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cloudfw&api=ModifyControlPolicy&type=RPC&version=2017-12-07)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|AclAction|String|Yes|accept|The action that Cloud Firewall performs on the traffic. Valid values:

 -   **accept**: Allow
-   **drop**: Deny
-   **log**: Monitor |
|AclUuid|String|Yes|00281255-d220-4db1-8f4f-c4df221ad84c|The unique ID of the access control policy.

 You can call the DescribeControlPolicy operation to query the ID. |
|Action|String|Yes|ModifyControlPolicy|The operation that you want to perform. Set the value to ModifyControlPolicy. |
|ApplicationName|String|Yes|HTTP|The application type defined in the access control policy.

 Valid values:

 -   **ANY**
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

 **Note:** The value of **ANY** indicates that the policy is applied to all types of applications. |
|Description|String|Yes|test|The description of the access control policy. |
|Destination|String|Yes|1.2.3.4/24|The destination address defined in the access control policy.

 -   If the DestinationType parameter is set to net, this parameter specifies the destination CIDR block. Example: 1.2.3.4/24
-   If the DestinationType parameter is set to group, this parameter specifies the name of the destination address book. Example: db\_group
-   If the DestinationType parameter is set to domain, this parameter specifies the destination domain name. Example: \*.aliyuncs.com
-   If the DestinationType parameter is set to location, this parameter specifies the destination region. For more information about region codes, see the following section. Example: \["BJ11", "ZB"\] |
|DestinationType|String|Yes|net|The type of the destination address defined in the access control policy. Valid values:

 -   net: destination CIDR block
-   group: destination address book
-   domain: destination domain name
-   location: destination region |
|Direction|String|Yes|in|The traffic direction defined in the access control policy. Valid values:

 -   **in**: inbound traffic
-   **out**: outbound traffic |
|Proto|String|Yes|TCP|The security protocol type defined in the access control policy. If you cannot determine the protocol type, you can set this parameter to **ANY**. Valid values:

 -   ANY
-   TCP
-   UDP
-   ICMP |
|Source|String|Yes|1.2.3.0/24|The source address defined in the access control policy.

 -   If the SourceType parameter is set to net, this parameter specifies the source CIDR block. Example: 1.2.3.0/24
-   If the SourceType parameter is set to group, this parameter specifies the name of the source address book. Example: db\_group
-   If the SourceType parameter is set to location, this parameter specifies the source region. For more information about region codes, see the following section. Example: \["BJ11", "ZB"\] |
|SourceType|String|Yes|net|The source address type defined in the access control policy. Valid values:

 -   net: source CIDR block
-   group: source address book
-   location: source region |
|DestPort|String|No|80|The destination port defined in the access control policy. |
|DestPortGroup|String|No|my\_port\_group|The name of the destination port address book defined in the access control policy. |
|DestPortType|String|No|port|The type of the destination port defined in the access control policy. Valid values:

 -   **port**: port
-   **group**: port address book |
|Lang|String|No|zh|The language of the request and response. Valid values:

 -   **en**: English
-   **zh**: Chinese |
|SourceIp|String|No|1.2.3.5|The source IP address of the request. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D|The ID of the request. |

## Examples

Sample requests

```

http(s)://[Endpoint]/? Action=ModifyControlPolicy
&AclAction=accept
&AclUuid=00281255-d220-4db1-8f4f-c4df221ad84c
&ApplicationName=ANY
&Description=demo_rule_1
&Destination=1.2.3.4/24
&DestinationType=net
&Direction=in
&Proto=TCP
&Source=1.2.3.0/24
&SourceType=net
&<Common request parameters>

```

Sample success responses

`XML` format

```
<ModifyControlPolicy>
	  <RequestId>CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D</RequestId>
</ModifyControlPolicy>
```

`JSON` format

```
{
	"RequestId":"CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cloudfw).


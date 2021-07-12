# ModifyControlPolicy

Modifies the configurations of an access control policy.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cloudfw&api=ModifyControlPolicy&type=RPC&version=2017-12-07)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|ModifyControlPolicy|The operation that you want to perform. Set the value to **ModifyControlPolicy**. |
|AclAction|String|Yes|accept|The action that Cloud Firewall performs on the traffic. Valid values: Valid values:

 -   **accept**: allows the traffic.
-   **drop**: denies the traffic.
-   **log**: monitors the traffic. |
|AclUuid|String|Yes|00281255-d220-4db1-8f4f-c4df221ad84c|The ID of the access control policy.

 **Note:** To modify the access control policy, you must provide the ID of the policy. You can call the [DescribeControlPolicy](~~138866~~) operation to obtain the IDs of access control policies. |
|ApplicationName|String|Yes|HTTP|The type of the application that the access control policy supports. Valid values:

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

 **Note:** The value **ANY** indicates all types of applications. |
|Description|String|Yes|test|The description of the access control policy. |
|Destination|String|Yes|1.2.3.4/24|The destination address in the access control policy.

 -   If **DestinationType** is set to net, the value of this parameter is the **destination CIDR block**. Example: 1.2.3.4/24.
-   If **DestinationType** is set to group, the value of this parameter is the **destination address book**. Example: db\_group.
-   If **DestinationType** is set to domain, the value of this parameter is the **destination domain name**. Example: \*.aliyuncs.com.
-   If **DestinationType** is set to location, the value of this parameter is the **destination location**. For more information about the location codes, see the "AddControlPolicy" topic. Example: \["BJ11", "ZB"\]. |
|DestinationType|String|Yes|net|The type of the destination address in the access control policy. Valid values:

 -   **net**: destination CIDR block
-   **group**: destination address book
-   **domain**: destination domain name
-   **location**: destination location |
|Direction|String|Yes|in|The direction of the traffic to which the access control policy applies. Valid values:

 -   **in**: inbound traffic
-   **out**: outbound traffic |
|Proto|String|Yes|TCP|The security protocol type defined in the access control policy. Valid values: Valid values:

 -   **ANY**
-   **TCP**
-   **UDP**
-   **ICMP**

 **Note:** The value **ANY** indicates all types of applications. |
|Source|String|Yes|1.2.3.0/24|The source address in the access control policy.

 -   If **SourceType** is set to net, the value of this parameter is the **source CIDR block**. Example: 1.2.3.0/24.
-   If **SourceType** is set to group, the value of this parameter is the name of the **source address book**. Example: db\_group.
-   If **SourceType** is set to location, the value of this parameter is the **source location**. For more information about the location codes, see the "AddControlPolicy" topic. Example: \["BJ11", "ZB"\]. |
|SourceType|String|Yes|net|The type of the source address in the access control policy. Valid values:

 -   **net**: source CIDR block
-   **group**: source address book
-   **location**: source location |
|SourceIp|String|No|1.2.3.5|The source IP address of the request. |
|Lang|String|No|zh|The natural language of the request and response. Valid values:

 -   **zh**: Chinese
-   **en**: English |
|DestPort|String|No|80|The destination port in the access control policy. |
|DestPortType|String|No|port|The type of the destination port in the access control policy. Valid values:

 -   **port**: port
-   **group**: port address book |
|DestPortGroup|String|No|my\_port\_group|The name of the destination port address book in the access control policy. |
|Release|String|No|true|The status of the access control policy. Valid values:

 -   true: enables the policy.
-   false: disables the policy. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D|The ID of the request. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=ModifyControlPolicy
&AclAction=accept
&AclUuid=00281255-d220-4db1-8f4f-c4df221ad84c
&ApplicationName=HTTP
&Description=test
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
<ModifyControlPolicyResponse>
  <RequestId>CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D</RequestId>
</ModifyControlPolicyResponse>
```

`JSON` format

```
{
    "RequestId": "CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D"
}
```


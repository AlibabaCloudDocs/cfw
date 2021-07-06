# AddControlPolicy

Creates an access control policy.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cloudfw&api=AddControlPolicy&type=RPC&version=2017-12-07)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|AddControlPolicy|The operation that you want to perform.

Set the value to **AddControlPolicy**. |
|AclAction|String|Yes|accept|The action that Cloud Firewall performs on the traffic. Valid values:

-   **accept**: allows the traffic.
-   **drop**: denies the traffic.
-   **log**: monitors the traffic. |
|ApplicationName|String|Yes|HTTP|The application type that the access control policy supports. Valid values:

-   **FTP**
-   **HTTP**
-   **HTTPS**
-   **Memcache**
-   **MongoDB**
-   **MQTT**
-   **MySQL**
-   **RDP**
-   **Redis**
-   **SMTP**
-   **SMTPS**
-   **SSH**
-   **SSL**
-   **VNC**
-   **ANY**: all types of applications

**Note:** The value of this parameter depends on the value of Proto. If Proto is set to TCP, ApplicationName can be set to any valid value. If Proto is set to UDP, ICMP, or ANY, you must set ApplicationName to ANY. |
|Description|String|Yes|Allow all TCP traffic|The description of the access control policy. |
|Destination|String|Yes|1.2.3.4/24|The destination address defined in the access control policy. Valid values:

-   If DestinationType is set to net, the value of this parameter is a CIDR block.

Example: 1.2.3.4/24.

-   If DestinationType is set to group, the value of this parameter is an address book.

Example: db\_group.

-   If DestinationType is set to domain, the value of this parameter is a domain name.

Example: \*.aliyuncs.com.

-   If DestinationType is set to location, the value of this parameter is a region.

Example: \["BJ11", "ZB"\]. |
|DestinationType|String|Yes|net|The destination address type defined in the access control policy. Valid values:

-   **net**: CIDR block
-   **group**: address book
-   **domain**: domain name
-   **location**: region |
|Direction|String|Yes|in|The direction of traffic to which the access control policy applies. Valid values:

-   **in**: inbound traffic
-   **out**: outbound traffic |
|NewOrder|String|Yes|-1|The priority of the access control policy. The priority value starts from 1. A small priority value indicates a high priority.

**Note:** The value of **-1** indicates the lowest priority. |
|Proto|String|Yes|TCP|The protocol type of traffic to which the access control policy applies. Valid values:

-   **ANY**\(any protocol type\)
-   **TCP**
-   **UDP**
-   **ICMP** |
|Source|String|Yes|1.2.3.0/24|The source address defined in the access control policy. Valid values:

-   If SourceType is set to net, the value of this parameter is a CIDR block.

Example: 1.2.3.0/24.

-   If SourceType is set to group, the value of this parameter is an address book.

Example: db\_group.

-   If SourceType is set to location, the value of this parameter is a region.

Example: \["BJ11", "ZB"\]. |
|SourceType|String|Yes|net|The type of the source address book defined in the access control policy. Valid values:

-   **net**: CIDR block
-   **group**: address book
-   **location**: source region |
|SourceIp|String|No|1.2.3.5|The source IP address of the request. |
|Lang|String|No|zh|The natural language of the request and response. Valid values:

-   **zh**: Chinese
-   **en**: English |
|DestPort|String|No|80|The destination port defined in the access control policy. Valid values:

-   If Proto is set to ICMP, the value of DestPort is empty.

**Note:** If Proto is set to ICMP, access control does not take effect on the destination port.

-   If Proto is set to TCP, UDP, or ANY and DestPortType is set to group, the value of DestPort is empty.

**Note:** If DestPortType is set to group, you do not need to specify the destination port number. All ports that are to be controlled by the access control policy are included in the destination port address book.

-   If Proto is set to TCP, UDP, or ANY and DestPortType is set to port, the value of DestPort is the destination port number. |
|DestPortType|String|No|port|The destination port type defined in the access control policy.

Valid values:

-   **port**: port
-   **group**: port address book |
|DestPortGroup|String|No|my\_port\_group|The destination port address book defined in the access control policy.

**Note:** If DestPortType is set to group, you must specify the destination port address book. |
|Release|String|No|true|Specifies whether the access control policy is enabled. By default, an access control policy is enabled after it is created. Valid values:

-   **true**: The access control policy is enabled.
-   **false**: The access control policy is not enabled. |

Location codes:

-   China: ZD
-   Beijing: BJ11
-   Tianjin: TJ12
-   Hebei: HB13
-   Shanxi: SX14
-   Liaoning: LN21
-   Jilin: JL22
-   Shanghai: SH31
-   Jiangsu: JS32
-   Zhejiang: ZJ33
-   Anhui: AH34
-   Fujian: FJ35
-   Jiangxi: JX36
-   Shandong: SD37
-   Henan: HN41
-   Hubei: HB42
-   Hunan: HN43
-   Guangdong: GD44
-   Hainan: HN46
-   Chongqing: CQ50
-   Sichuan: SC51
-   Guizhou: GZ52
-   Yunnan: YN53
-   Shaanxi: SX61
-   Gansu: GS62
-   Qinghai: QH63
-   Heilongjiang: HLJ23
-   Xizang: XZ54
-   Guangxi: GX45
-   Nei Mongol: NMG15
-   Ningxia: NX64
-   Xinjiang: XJ65
-   Taiwan: TW
-   Hong Kong S.A.R: HK
-   Macao S.A.R: MO
-   Areas outside China: ZB
-   Asia \(except mainland China\):ZC
-   Europe: EU
-   Africa: AF
-   North America: NA
-   South America: LA
-   Oceania: OA
-   Antarctica: AQ

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|AclUuid|String|00281255-d220-4db1-8f4f-c4df221ad84c|The unique ID of the access control policy. |
|RequestId|String|CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D|The ID of the request. |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=AddControlPolicy
&AclAction=accept
&ApplicationName=ANY
&Description=demo_rule_1
&Destination=1.2.3.4/24
&DestinationType=net
&Direction=in
&NewOrder=-1
&Proto=TCP
&Source=1.2.3.0/24
&SourceType=net
&<Common request parameters>
```

Sample success responses

`XML` format

```
<AddControlPolicyResponse>
      <RequestId>CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D</RequestId>
      <AclUuid>00281255-d220-4db1-8f4f-c4df221ad84c</AclUuid>
</AddControlPolicyResponse>
```

`JSON` format

```
{
    "RequestId": "CBF1E9B7-D6A0-4E9E-AD3E-2B47E6C2837D",
    "AclUuid": "00281255-d220-4db1-8f4f-c4df221ad84c"
}
```


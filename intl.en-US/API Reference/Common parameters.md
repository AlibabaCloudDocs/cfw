# Common parameters

This topic describes the common parameters for API operations provided by Cloud Firewall.

## Common request parameters

|Parameter|Type|Required|Description|
|---------|----|--------|-----------|
|Region|String|Yes|The region ID of the Cloud Firewall instance. Set the value to `cn-hangzhou` \(indicating mainland China\).|
|Format|String|No|The format in which to return the response. Default value: JSON. Valid values: -   `JSON`
-   `XML` |
|Version|String|Yes|The version number of the API, in the format of YYYY-MM-DD. Set the value to `2017-12-07`.|
|AccessKeyId|String|Yes|The AccessKey ID provided to you by Alibaba Cloud.|
|Signature|String|Yes|The signature string of the current request.|
|SignatureMethod|String|Yes|The encryption method of the signature string. Set the value to `HMAC-SHA1`.|
|Timestamp|String|Yes|The timestamp of the request. Specify the time in the ISO 8601 standard in the `YYYY-MM-DDThh:mm:ssZ` format. The time must be in UTC. For example, `2013-01-10T12:00:00Z` indicates January 10, 2013, 20:00:00 \(UTC+8\).|
|SignatureVersion|String|Yes|The version of the signature encryption algorithm. Set the value to 1.0.|
|SignatureNonce|String|Yes|A unique, random number used to prevent replay attacks. You must use different numbers for different requests.|
|ResourceOwnerAccount|String|No|The account that owns the resource to be accessed through this API request.|

**Examples**

```
https://cloudfw.cn-hangzhou.aliyuncs.com/?Action=AddControlPolicy
&​BizId=13688
​&Region=cn
&Format=xml
&Version=2017-12-07
&Signature=xxxx%xxxx%3D
&SignatureMethod=HMAC-SHA1
&SignatureNonce=15215528852396
&SignatureVersion=1.0
&AccessKeyId=key-test
&TimeStamp=2012-06-01T12:00:00Z
```

## Common response parameters

API responses use the HTTP response format where a 2xx status code indicates a successful call and a 4xx or 5xx status code indicates a failed call.

Responses can be returned in either the JSON or XML format. You can specify the response format in the request. The default response format is JSON.

Every response returns a unique RequestID regardless of whether the call is successful.

-   XML format

    ```
    <? xml version="1.0" encoding="utf-8"? > 
        <!--Result Root Node-->
        <Interface Name+Response>
            <!--Return Request Tag-->
            <RequestId>4C467B38-3910-447D-87BC-AC049166F216</RequestId>
            <!--Return Result Data-->
        </Interface Name+Response>
                        
    ```

-   JSON format

    ```
    {
        "RequestId":"4C467B38-3910-447D-87BC-AC049166F216",
        /*Response data*/
        }
    ```



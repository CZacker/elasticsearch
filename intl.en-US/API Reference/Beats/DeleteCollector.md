# DeleteCollector

Call DeleteCollector to delete the collector.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=elasticsearch&api=DeleteCollector&type=ROA&version=2017-06-13)

## Request header

This operation uses only common request headers. For more information, see the Common request parameters topic.

## Request structure

```
DELETE /openapi/collectors/[ResId] HTTPS|HTTP
```

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|ResId|String|Yes|ct-cn-92z1h38882dal\*\*\*\*|The collector ID. |
|ClientToken|String|No|5A2CFF0E-5718-45B5-9D4D-70B3FF\*\*\*\*|A unique token generated by the client to guarantee the idempotency of the request. You can use the client to generate the value, but you must ensure that it is unique among different requests. The token can only contain ASCII characters and cannot exceed 64 characters in length. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|5FFD9ED4-C2EC-4E89-B22B-1ACB6FE1\*\*\*\*|The ID of the request. |
|Result|Boolean|true|Return results:

-   true: deleted
-   false: failed to delete the instance |

## Examples

Sample requests

```
DELETE /openapi/collectors/ct-cn-77uqof2s7rg5c**** HTTP/1.1
Common request header
```

Sample success responses

`XML` format

```
<Result>true</Result>
<RequestId>1A8571CF-8591-485B-AE44-131C49DC****</RequestId>
```

`JSON` format

```
{
    "Result": true,
    "RequestId": "1A8571CF-8591-485B-AE44-131C49DC****"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/elasticsearch).

# DeleteSnapshotRepo

Call DeleteSnapshotRepo to delete a cross-cluster OSS repository.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=elasticsearch&api=DeleteSnapshotRepo&type=ROA&version=2017-06-13)

## Request header

This operation uses common request parameters only. For more information, see Common parameters.

## Request syntax

```
DELETE /openapi/instances/[InstanceId]/snapshot-repos HTTPS|HTTP
```

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|InstanceId|String|Yes|es-cn-n6w1o1x0w001c\*\*\*\*|The ID of the instance. |
|repoPath|String|Yes|es-cn-n6w1rux8i000w\*\*\*\*|Reference instance ID. |
|clientToken|String|No|5A2CFF0E-5718-45B5-9D4D-70B3FF\*\*\*\*|A unique token generated by the client to guarantee the idempotency of the request. You can use the client to generate the value, but you must ensure that it is unique among different requests. The token can only contain ASCII characters and cannot exceed 64 characters in length. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|5FFD9ED4-C2EC-4E89-B22B-1ACB6FE1\*\*\*\*|The ID of the request. |
|Result|Boolean|true|Return results:

-   true: reference warehouse deleted successfully
-   false: reference warehouse deleted successfully failed |

## Examples

Sample requests

```
DELETE /openapi/instances/es-cn-n6w1o1x0w001c****/snapshot-repos? repoPath=es-cn-n6w1rux8i000w**** HTTP/1.1
Common request header
```

Sample success responses

`XML` format

```
<Result>true</Result>
<RequestId>93005691-1899-4515-A5CE-FD28D347****</RequestId>
```

`JSON` format

```
{
    "Result": true,
    "RequestId": "93005691-1899-4515-A5CE-FD28D347****"
}
```

## Error codes

|HttpCode|Error code|Error message|Description|
|--------|----------|-------------|-----------|
|400|InstanceNotFound|The instanceId provided does not exist.|The error message returned because the specified instance cannot be found. Check the instance status.|

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/elasticsearch).

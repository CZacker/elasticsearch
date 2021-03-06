# DeleteDataTask

调用DeleteDataTask，删除索引迁移任务。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=elasticsearch&api=DeleteDataTask&type=ROA&version=2017-06-13)

## 请求头

该接口使用公共请求头，无特殊请求头。请参见公共请求参数文档。

## 请求语法

```
DELETE /openapi/instances/[InstanceId]/data-task HTTPS|HTTP
```

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|ClientToken|String|是|5A2CFF0E-5718-45B5-9D4D-70B3FF\*\*\*\*|用于保证请求的幂等性。由客户端生成该参数值，要保证在不同请求间唯一，最大不超过64个ASCII字符。 |
|InstanceId|String|是|es-cn-oew1oxiro000f\*\*\*\*|实例ID。 |
|taskId|String|是|et\_cn\_0oyg09o96ib40\*\*\*\*|索引迁移任务ID。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|5FFD9ED4-C2EC-4E89-B22B-1ACB6FE1D\*\*\*|请求ID。 |
|Result|Boolean|true|返回结果。 |

## 示例

请求示例

```
DELETE /openapi/instances/es-cn-oew1oxiro000f****/data-task?taskId=et_cn_0oyg09o96ib40****&ClientToken=5A2CFF0E-5718-45B5-9D4D-70B3FF**** HTTP/1.1
公共请求头
```

正常返回示例

`XML` 格式

```
<Result>true</Result>
<RequestId>3F71A6D2-7BD0-4A53-9119-386A2F0B****</RequestId>
```

`JSON` 格式

```
{
	"Result": true,
	"RequestId": "3F71A6D2-7BD0-4A53-9119-386A2F0B****"
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/elasticsearch)查看更多错误码。


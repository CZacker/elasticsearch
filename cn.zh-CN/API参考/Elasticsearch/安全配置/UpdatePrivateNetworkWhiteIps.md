# UpdatePrivateNetworkWhiteIps

调用UpdatePrivateNetworkWhiteIps，更新指定实例的VPC私网访问白名单。

调用该接口时，请注意：

当实例状态为生效中（activating）、失效（invalid）和冻结（inactive）时，无法更新实例的VPC私网访问白名单。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=elasticsearch&api=UpdatePrivateNetworkWhiteIps&type=ROA&version=2017-06-13)

## 请求头

该接口使用公共请求头，无特殊请求头。请参见公共请求参数文档。

## 请求语法

```
POST /openapi/instances/[InstanceId]/private-network-white-ips HTTPS|HTTP
```

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|InstanceId|String|是|es-cn-n6w1o1x0w001c\*\*\*\*|实例ID。 |
|clientToken|String|否|5A2CFF0E-5718-45B5-9D4D-70B3FF\*\*\*\*|用于保证请求的幂等性。由客户端生成该参数值，要保证在不同请求间唯一，最大不超过64个ASCII字符。 |

## RequestBody

RequestBody中还需填入**privateNetworkIpWhiteList**参数，用来指定在白名单中添加的IP地址，示例如下。

```

{
  "privateNetworkIpWhiteList": ["192.168.**.**/24"]
}

```

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|C82758DD-282F-4D48-934F-92170A33\*\*\*\*|请求ID。 |
|Result|Struct| |返回结果。 |
|privateNetworkIpWhiteList|List|\["192.168.\*\*.\*\*/24"\]|VPC私网访问白名单列表。 |

**说明：** 下文返回示例中，本文只保证包含返回数据列表中的参数，而未提到的参数仅供参考，参数说明可参见[ListInstance](~~142230~~)。程序中不能强制依赖获取这些参数。

## 示例

请求示例

```
POST /openapi/instances/es-cn-n6w1o1x0w001c****/private-network-white-ips HTTP/1.1
公共请求头
{
  "privateNetworkIpWhiteList": ["192.168.**.**/24"]
}
```

正常返回示例

`XML` 格式

```
<Result>
    <instanceId>es-cn-n6w1o1x0w001c****</instanceId>
    <version>6.7.0_with_X-Pack</version>
    <description>test</description>
    <nodeAmount>4</nodeAmount>
    <paymentType>postpaid</paymentType>
    <status>active</status>
    <privateNetworkIpWhiteList>192.168.**.**/24</privateNetworkIpWhiteList>
    <enablePublic>true</enablePublic>
    <nodeSpec>
        <spec>elasticsearch.sn2ne.large</spec>
        <disk>2048</disk>
        <diskType>cloud_ssd</diskType>
        <diskEncryption>false</diskEncryption>
    </nodeSpec>
    <networkConfig>
        <vpcId>vpc-bp16k1dvzxtmagcva****</vpcId>
        <vswitchId>vsw-bp1k4ec6s7sjdbudw****</vswitchId>
        <vsArea>cn-hangzhou-i</vsArea>
        <type>vpc</type>
    </networkConfig>
    <createdAt>2020-05-25T02:26:59.021Z</createdAt>
    <updatedAt>2020-07-03T06:00:55.944Z</updatedAt>
    <commodityCode>elasticsearch</commodityCode>
    <extendConfigs>
        <configType>maintainTime</configType>
        <maintainStartTime>02:00Z</maintainStartTime>
        <maintainEndTime>06:00Z</maintainEndTime>
    </extendConfigs>
    <extendConfigs>
        <configType>usageScenario</configType>
        <value>analysisVisualization</value>
    </extendConfigs>
    <extendConfigs>
        <configType>aliVersion</configType>
        <aliVersion>ali1.2.0</aliVersion>
    </extendConfigs>
    <endTime>4748169600000</endTime>
    <vpcInstanceId>es-cn-n6w1o1x0w001c****-worker</vpcInstanceId>
    <resourceGroupId>rg-acfm2h5vbzd****</resourceGroupId>
    <zoneCount>1</zoneCount>
    <protocol>HTTP</protocol>
    <zoneInfos>
        <zoneId>cn-hangzhou-i</zoneId>
        <status>NORMAL</status>
    </zoneInfos>
    <instanceType>elasticsearch</instanceType>
    <inited>true</inited>
    <domain>es-cn-n6w1o1x0w001c****.elasticsearch.aliyuncs.com</domain>
    <port>9200</port>
    <esVersion>6.7.0_with_X-Pack</esVersion>
    <esConfig>
        <action.destructive_requires_name>true</action.destructive_requires_name>
        <xpack.security.audit.outputs>index</xpack.security.audit.outputs>
        <xpack.watcher.enabled>false</xpack.watcher.enabled>
        <xpack.security.audit.enabled>false</xpack.security.audit.enabled>
        <action.auto_create_index>true</action.auto_create_index>
    </esConfig>
    <esIPWhitelist>192.168.**.**/24</esIPWhitelist>
    <kibanaIPWhitelist>0.0.0.0/0</kibanaIPWhitelist>
    <kibanaIPWhitelist>::/0</kibanaIPWhitelist>
    <publicIpWhitelist>::1</publicIpWhitelist>
    <publicIpWhitelist>0.0.0.0/0</publicIpWhitelist>
    <kibanaDomain>es-cn-n6w1o1x0w001c****.kibana.elasticsearch.aliyuncs.com</kibanaDomain>
    <kibanaPort>5601</kibanaPort>
    <publicPort>9200</publicPort>
    <publicDomain>es-cn-n6w1o1x0w001c****.public.elasticsearch.aliyuncs.com</publicDomain>
    <haveKibana>true</haveKibana>
    <instanceCategory>x-pack</instanceCategory>
    <dedicateMaster>false</dedicateMaster>
    <advancedDedicateMaster>false</advancedDedicateMaster>
    <masterConfiguration/>
    <haveClientNode>false</haveClientNode>
    <warmNode>false</warmNode>
    <warmNodeConfiguration/>
    <clientNodeConfiguration/>
    <kibanaConfiguration>
        <spec>elasticsearch.n4.small</spec>
        <amount>1</amount>
        <disk>0</disk>
    </kibanaConfiguration>
    <dictList>
        <name>SYSTEM_MAIN.dic</name>
        <fileSize>2782602</fileSize>
        <sourceType>ORIGIN</sourceType>
        <type>MAIN</type>
    </dictList>
    <dictList>
        <name>SYSTEM_STOPWORD.dic</name>
        <fileSize>132</fileSize>
        <sourceType>ORIGIN</sourceType>
        <type>STOP</type>
    </dictList>
    <haveGrafana>false</haveGrafana>
    <haveCerebro>false</haveCerebro>
    <enableKibanaPublicNetwork>true</enableKibanaPublicNetwork>
    <enableKibanaPrivateNetwork>false</enableKibanaPrivateNetwork>
    <advancedSetting>
        <gcName>CMS</gcName>
    </advancedSetting>
</Result>
<RequestId>36E85891-0719-4B31-B62A-1418684D****</RequestId>
```

`JSON` 格式

```
{
	"Result": {
		"instanceId": "es-cn-n6w1o1x0w001c****",
		"version": "6.7.0_with_X-Pack",
		"description": "test",
		"nodeAmount": 4,
		"paymentType": "postpaid",
		"status": "active",
		"privateNetworkIpWhiteList": [
			"192.168.**.**/24"
		],
		"enablePublic": true,
		"nodeSpec": {
			"spec": "elasticsearch.sn2ne.large",
			"disk": 2048,
			"diskType": "cloud_ssd",
			"diskEncryption": false
		},
		"networkConfig": {
			"vpcId": "vpc-bp16k1dvzxtmagcva****",
			"vswitchId": "vsw-bp1k4ec6s7sjdbudw****",
			"vsArea": "cn-hangzhou-i",
			"type": "vpc"
		},
		"createdAt": "2020-05-25T02:26:59.021Z",
		"updatedAt": "2020-07-03T06:00:55.944Z",
		"commodityCode": "elasticsearch",
		"extendConfigs": [
			{
				"configType": "maintainTime",
				"maintainStartTime": "02:00Z",
				"maintainEndTime": "06:00Z"
			},
			{
				"configType": "usageScenario",
				"value": "analysisVisualization"
			},
			{
				"configType": "aliVersion",
				"aliVersion": "ali1.2.0"
			}
		],
		"endTime": 4748169600000,
		"clusterTasks": [],
		"vpcInstanceId": "es-cn-n6w1o1x0w001c****-worker",
		"resourceGroupId": "rg-acfm2h5vbzd****",
		"zoneCount": 1,
		"protocol": "HTTP",
		"zoneInfos": [
			{
				"zoneId": "cn-hangzhou-i",
				"status": "NORMAL"
			}
		],
		"instanceType": "elasticsearch",
		"inited": true,
		"tags": [],
		"domain": "es-cn-n6w1o1x0w001c****.elasticsearch.aliyuncs.com",
		"port": 9200,
		"esVersion": "6.7.0_with_X-Pack",
		"esConfig": {
			"action.destructive_requires_name": "true",
			"xpack.security.audit.outputs": "index",
			"xpack.watcher.enabled": "false",
			"xpack.security.audit.enabled": "false",
			"action.auto_create_index": "true"
		},
		"esIPWhitelist": [
			"192.168.**.**/24"
		],
		"esIPBlacklist": [],
		"kibanaIPWhitelist": [
			"0.0.0.0/0",
			"::/0"
		],
		"kibanaPrivateIPWhitelist": [],
		"publicIpWhitelist": [
			"::1",
			"0.0.0.0/0"
		],
		"kibanaDomain": "es-cn-n6w1o1x0w001c****.kibana.elasticsearch.aliyuncs.com",
		"kibanaPort": 5601,
		"publicPort": 9200,
		"publicDomain": "es-cn-n6w1o1x0w001c****.public.elasticsearch.aliyuncs.com",
		"haveKibana": true,
		"instanceCategory": "x-pack",
		"dedicateMaster": false,
		"advancedDedicateMaster": false,
		"masterConfiguration": {},
		"haveClientNode": false,
		"warmNode": false,
		"warmNodeConfiguration": {},
		"clientNodeConfiguration": {},
		"kibanaConfiguration": {
			"spec": "elasticsearch.n4.small",
			"amount": 1,
			"disk": 0
		},
		"dictList": [
			{
				"name": "SYSTEM_MAIN.dic",
				"fileSize": 2782602,
				"sourceType": "ORIGIN",
				"type": "MAIN"
			},
			{
				"name": "SYSTEM_STOPWORD.dic",
				"fileSize": 132,
				"sourceType": "ORIGIN",
				"type": "STOP"
			}
		],
		"synonymsDicts": [],
		"ikHotDicts": [],
		"aliwsDicts": [],
		"haveGrafana": false,
		"haveCerebro": false,
		"enableKibanaPublicNetwork": true,
		"enableKibanaPrivateNetwork": false,
		"advancedSetting": {
			"gcName": "CMS"
		}
	},
	"RequestId": "36E85891-0719-4B31-B62A-1418684D****"
}
```

## 错误码

|HttpCode|错误码|错误信息|描述|
|--------|---|----|--|
|400|InstanceNotFound|The instanceId provided does not exist.|实例找不到，请核对实例状态。|

访问[错误中心](https://error-center.aliyun.com/status/product/elasticsearch)查看更多错误码。


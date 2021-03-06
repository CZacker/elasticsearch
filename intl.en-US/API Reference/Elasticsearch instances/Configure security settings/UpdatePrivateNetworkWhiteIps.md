# UpdatePrivateNetworkWhiteIps

Call UpdatePrivateNetworkWhiteIps, updates the instance of the VPC intranet access whitelist.

When you call this operation, take note of the following items:

When an instance is in the activating, invalid, or inactive state, you cannot update its VPC whitelist.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=elasticsearch&api=UpdatePrivateNetworkWhiteIps&type=ROA&version=2017-06-13)

## Request header

This operation uses common request parameters only. For more information, see Common parameters.

## Request syntax

```
POST /openapi/instances/[InstanceId]/private-network-white-ips HTTPS|HTTP
```

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|InstanceId|String|Yes|es-cn-n6w1o1x0w001c\*\*\*\*|The ID of the instance. |
|clientToken|String|No|5A2CFF0E-5718-45B5-9D4D-70B3FF\*\*\*\*|A unique token generated by the client to guarantee the idempotency of the request. You can use the client to generate the value, but you must ensure that it is unique among different requests. The token can only contain ASCII characters and cannot exceed 64 characters in length. |

## RequestBody

The **privateNetworkIpWhiteList** parameter needs to be filled in the RequestBody to specify the IP address to be added to the whitelist. Example:

```

{
  "privateNetworkIpWhiteList": ["192.168.**.**/24"]
}

```

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|C82758DD-282F-4D48-934F-92170A33\*\*\*\*|The ID of the request. |
|Result|Struct| |The returned results. |
|privateNetworkIpWhiteList|List|\["192.168. \*\*. \*\*/24"\]|The IP addresses in the VPC whitelist. |

**Note:** In the following response examples, only the parameters in the returned data list are guaranteed to be included. The parameters that are not described in this topic are only for reference. For more information about Parameter descriptions, see[ListInstance](~~142230~~). The program must not rely on obtaining these parameters.

## Examples

Sample requests

```
POST /openapi/instances/es-cn-n6w1o1x0w001c****/private-network-white-ips HTTP/1.1
Common request parameters
{
  "privateNetworkIpWhiteList": ["192.168. **. **/24"]
}
```

Sample success responses

`XML` format

```
<Result>
    <instanceId>es-cn-n6w1o1x0w001c****</instanceId>
    <version>6.7.0_with_X-Pack</version>
    <description>test</description>
    <nodeAmount>4</nodeAmount>
    <paymentType>postpaid</paymentType>
    <status>active</status>
    <privateNetworkIpWhiteList>192.168. **.**/24</privateNetworkIpWhiteList>
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
    <esIPWhitelist>192.168. **.**/24</esIPWhitelist>
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
        <gcName>CMS
    </advancedSetting>
</Result>
<RequestId>36E85891-0719-4B31-B62A-1418684D****</RequestId>
```

`JSON` format

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
            "192.168. **.**/24"
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
            "192.168. **.**/24"
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

## Error codes

|HttpCode|Error code|Error message|Description|
|--------|----------|-------------|-----------|
|400|InstanceNotFound|The instanceId provided does not exist.|The error message returned because the specified instance cannot be found. Check the instance status.|

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/elasticsearch).


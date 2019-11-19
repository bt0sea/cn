# describeVpcs


## 描述
查询私有网络列表

## 请求方式
GET

## 请求地址
https://edcps.jdcloud-api.com/v1/regions/{regionId}/vpcs

|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**regionId**|String|True| |地域ID，可调用接口（describeEdCPSRegions）获取分布式云物理服务器支持的地域|

## 请求参数
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**pageNumber**|Integer|False|1|页码；默认为1|
|**pageSize**|Integer|False|20|分页大小；默认为20；取值范围[20, 100]|
|**name**|String|False| |私有网络名称|
|**filters**|<a href="#Filter">Filter[]</a>|False| |vpcId - 私有网络ID，精确匹配，支持多个<br>|

### <a name="Filter">Filter</a>
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**name**|String|True| |过滤条件的名称|
|**operator**|String|False| |过滤条件的操作符，默认eq|
|**values**|String[]|True| |过滤条件的值|

## 返回参数
|名称|类型|描述|
|---|---|---|
|**result**|<a href="#Result">Result</a>| |
|**requestId**|String| |

### <a name="Result">Result</a>
|名称|类型|描述|
|---|---|---|
|**vpcs**|<a href="#Vpc">Vpc[]</a>| |
|**pageNumber**|Integer|页码；默认为1|
|**pageSize**|Integer|分页大小；默认为20；取值范围[20, 100]|
|**totalCount**|Integer|查询结果总数|
### <a name="Vpc">Vpc</a>
|名称|类型|描述|
|---|---|---|
|**region**|String|地域代码, 如cn-east-tz1|
|**vpcId**|String|私有网络ID|
|**name**|String|私有网络名称|
|**cidr**|String|私有网络CIDR|
|**description**|String|描述|
|**createTime**|String|创建时间|

## 返回码
|返回码|描述|
|---|---|
|**200**|OK|
|**400**|Bad request|
|**404**|Not found|
|**500**|Internal server error|
|**503**|Service unavailable|
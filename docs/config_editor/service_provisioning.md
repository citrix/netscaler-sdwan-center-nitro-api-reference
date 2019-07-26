# service\_provisioning


<a name="overview"></a>
## Overview
API to get the services enabled on the wan links by the current configuration and modify the corresponding bandwidth allocation settings.


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* service\_provisioning : Operations related to service\_provisioning 




<a name="paths"></a>
## Paths

<a name="service\_provisioning-get"></a>
### Get operation for service\_provisioning
```
GET /service_provisioning
```


#### Description
Use this operation to get the service provisioning details for each of the services enabled on the wan links.


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[service\_provisioning\_response\_schema](#service\_provisioning\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* service\_provisioning


<a name="service\_provisioning-put"></a>
### PUT operation for service\_provisioning
```
PUT /service_provisioning
```


#### Description
Use this operation to modify the service provisioning settings for each of the services enabled on the wan links.


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[service\_provisioning\_request\_schema](#service\_provisioning\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[service\_provisioning\_put\_success\_schema](#service\_provisioning\_put\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* service\_provisioning




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="id"></a>
### id
Auto-generated ID to uniquely identify the service provisioning.

*Type* : integer


<a name="lan\_to\_wan\_fair\_bitrate"></a>
### lan\_to\_wan\_fair\_bitrate
The fair bit rate of the Service, based on its shares out of all Services in the Group (LAN to WAN direction). Includes the Min rate, and will not exceed the Max rate.

*Type* : integer


<a name="lan\_to\_wan\_maximum\_allowed\_bitrate"></a>
### lan\_to\_wan\_maximum\_allowed\_bitrate
The maximum bandwidth the Service is allowed to utilize in LAN to WAN direction. (A value of 0 implies no limit.)

*Type* : integer


<a name="lan\_to\_wan\_minimum\_reserved\_bitrate"></a>
### lan\_to\_wan\_minimum\_reserved\_bitrate
The minimum bandwidth reserved exclusively for the Service in LAN to WAN direction.

*Type* : integer


<a name="lan\_to\_wan\_rate\_fair\_share"></a>
### lan\_to\_wan\_rate\_fair\_share
The number of fair shares the Service should take out of its Group's eligible bandwidth in LAN to WAN direction.

*Type* : integer


<a name="package\_name"></a>
### package\_name
Config package name using which the site API operation should be performed.

*Type* : string


<a name="provisioning\_group\_name"></a>
### provisioning\_group\_name
The provisioning group assigned to the service.

*Type* : string


<a name="service\_name"></a>
### service\_name
The name of the Service.

*Type* : string


<a name="service\_provisioning"></a>
### service\_provisioning

|Name|Schema|
|---|---|
|**id**  <br>*optional*|[id](#id)|
|**lan\_to\_wan\_maximum\_allowed\_bitrate**  <br>*optional*|[lan\_to\_wan\_maximum\_allowed\_bitrate](#lan\_to\_wan\_maximum\_allowed\_bitrate)|
|**lan\_to\_wan\_minimum\_reserved\_bitrate**  <br>*optional*|[lan\_to\_wan\_minimum\_reserved\_bitrate](#lan\_to\_wan\_minimum\_reserved\_bitrate)|
|**lan\_to\_wan\_rate\_fair\_share**  <br>*optional*|[lan\_to\_wan\_rate\_fair\_share](#lan\_to\_wan\_rate\_fair\_share)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**provisioning\_group\_name**  <br>*optional*|[provisioning\_group\_name](#provisioning\_group\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**wan\_to\_lan\_maximum\_allowed\_bitrate**  <br>*optional*|[wan\_to\_lan\_maximum\_allowed\_bitrate](#wan\_to\_lan\_maximum\_allowed\_bitrate)|
|**wan\_to\_lan\_minimum\_reserved\_bitrate**  <br>*optional*|[wan\_to\_lan\_minimum\_reserved\_bitrate](#wan\_to\_lan\_minimum\_reserved\_bitrate)|
|**wan\_to\_lan\_rate\_fair\_share**  <br>*optional*|[wan\_to\_lan\_rate\_fair\_share](#wan\_to\_lan\_rate\_fair\_share)|


<a name="service\_provisioning\_delete\_success\_schema"></a>
### service\_provisioning\_delete\_success\_schema

|Name|Schema|
|---|---|
|**service\_provisioning**  <br>*optional*|[service\_provisioning](#service\_provisioning\_delete\_success\_schema-service\_provisioning)|

<a name="service\_provisioning\_delete\_success\_schema-service\_provisioning"></a>
**service\_provisioning**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="service\_provisioning\_post\_success\_schema"></a>
### service\_provisioning\_post\_success\_schema

|Name|Schema|
|---|---|
|**service\_provisioning**  <br>*optional*|[service\_provisioning](#service\_provisioning\_post\_success\_schema-service\_provisioning)|

<a name="service\_provisioning\_post\_success\_schema-service\_provisioning"></a>
**service\_provisioning**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="service\_provisioning\_put\_success\_schema"></a>
### service\_provisioning\_put\_success\_schema

|Name|Schema|
|---|---|
|**service\_provisioning**  <br>*optional*|[service\_provisioning](#service\_provisioning\_put\_success\_schema-service\_provisioning)|

<a name="service\_provisioning\_put\_success\_schema-service\_provisioning"></a>
**service\_provisioning**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="service\_provisioning\_request\_schema"></a>
### service\_provisioning\_request\_schema

|Name|Schema|
|---|---|
|**service\_provisioning**  <br>*optional*|[service\_provisioning](#service\_provisioning)|


<a name="service\_provisioning\_response\_schema"></a>
### service\_provisioning\_response\_schema
*Type* : < [service\_provisioning\_response\_schema](#service\_provisioning\_response\_schema-inline) > array

<a name="service\_provisioning\_response\_schema-inline"></a>
**service\_provisioning\_response\_schema**

|Name|Schema|
|---|---|
|**id**  <br>*optional*|[id](#id)|
|**lan\_to\_wan\_fair\_bitrate**  <br>*optional*|[lan\_to\_wan\_fair\_bitrate](#lan\_to\_wan\_fair\_bitrate)|
|**lan\_to\_wan\_maximum\_allowed\_bitrate**  <br>*optional*|[lan\_to\_wan\_maximum\_allowed\_bitrate](#lan\_to\_wan\_maximum\_allowed\_bitrate)|
|**lan\_to\_wan\_minimum\_reserved\_bitrate**  <br>*optional*|[lan\_to\_wan\_minimum\_reserved\_bitrate](#lan\_to\_wan\_minimum\_reserved\_bitrate)|
|**lan\_to\_wan\_rate\_fair\_share**  <br>*optional*|[lan\_to\_wan\_rate\_fair\_share](#lan\_to\_wan\_rate\_fair\_share)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**provisioning\_group\_name**  <br>*optional*|[provisioning\_group\_name](#provisioning\_group\_name)|
|**service\_name**  <br>*optional*|[service\_name](#service\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**wan\_link\_name**  <br>*optional*|[wan\_link\_name](#wan\_link\_name)|
|**wan\_to\_lan\_fair\_bitrate**  <br>*optional*|[wan\_to\_lan\_fair\_bitrate](#wan\_to\_lan\_fair\_bitrate)|
|**wan\_to\_lan\_maximum\_allowed\_bitrate**  <br>*optional*|[wan\_to\_lan\_maximum\_allowed\_bitrate](#wan\_to\_lan\_maximum\_allowed\_bitrate)|
|**wan\_to\_lan\_minimum\_reserved\_bitrate**  <br>*optional*|[wan\_to\_lan\_minimum\_reserved\_bitrate](#wan\_to\_lan\_minimum\_reserved\_bitrate)|
|**wan\_to\_lan\_rate\_fair\_share**  <br>*optional*|[wan\_to\_lan\_rate\_fair\_share](#wan\_to\_lan\_rate\_fair\_share)|


<a name="site\_name"></a>
### site\_name
Site Name

*Type* : string


<a name="wan\_link\_name"></a>
### wan\_link\_name
The WAN Link name

*Type* : string


<a name="wan\_to\_lan\_fair\_bitrate"></a>
### wan\_to\_lan\_fair\_bitrate
The fair bit rate of the Service, based on its shares out of all Services in the Group (WAN to LAN direction). Includes the Min rate, and will not exceed the Max rate.

*Type* : integer


<a name="wan\_to\_lan\_maximum\_allowed\_bitrate"></a>
### wan\_to\_lan\_maximum\_allowed\_bitrate
The maximum bandwidth the Service is allowed to utilize in WAN to LAN direction. (A value of 0 implies no limit.)

*Type* : integer


<a name="wan\_to\_lan\_minimum\_reserved\_bitrate"></a>
### wan\_to\_lan\_minimum\_reserved\_bitrate
The minimum bandwidth reserved exclusively for the Service in WAN to LAN direction.

*Type* : integer


<a name="wan\_to\_lan\_rate\_fair\_share"></a>
### wan\_to\_lan\_rate\_fair\_share
The number of fair shares the Service should take out of its Group's eligible bandwidth in WAN to LAN direction.

*Type* : integer






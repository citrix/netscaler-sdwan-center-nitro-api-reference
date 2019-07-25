# ha\_service


<a name="overview"></a>
## Overview
API to add, delete, get, modify HA Service.


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* ha\_service : Operations related to ha\_service 




<a name="paths"></a>
## Paths

<a name="ha\_service-post"></a>
### POST operation for ha\_service
```
POST /ha_service
```


#### Description
Use this operation to add HA Service


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[ha\_service\_request\_schema](#ha\_service\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[ha\_service\_post\_success\_schema](#ha\_service\_post\_success\_schema)|
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

* ha\_service


<a name="ha\_service-get"></a>
### Get operation for ha\_service
```
GET /ha_service
```


#### Description
Use this operation to get HA Service


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[ha\_service\_response\_schema](#ha\_service\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* ha\_service


<a name="ha\_service-put"></a>
### PUT operation for ha\_service
```
PUT /ha_service
```


#### Description
Use this operation to modify HA Service


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[ha\_service\_put\_success\_schema](#ha\_service\_put\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* ha\_service


<a name="ha\_service-deletepathparam-delete"></a>
### DELETE operation for ha\_service
```
DELETE /ha_service/{deletePathParam}
```


#### Description
Use this operation to delete HA Service


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[ha\_service\_delete\_success\_schema](#ha\_service\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* ha\_service




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="ha\_interface\_group"></a>
### ha\_interface\_group
HA Interface group

*Type* : < [ha\_interface\_group](#ha\_interface\_group-inline) > array

<a name="ha\_interface\_group-inline"></a>
**ha\_interface\_group**

|Name|Description|Schema|
|---|---|---|
|**external\_tracker**  <br>*optional*|External Tracker IP Address|< [external\_tracker](#ha\_interface\_group-external\_tracker) > array|
|**id**  <br>*optional*|Auto-generated ID to uniquely identify HA Interface Group|integer|
|**interface\_properties**  <br>*optional*|HA Interface properties|< [interface\_properties](#ha\_interface\_group-interface\_properties) > array|

<a name="ha\_interface\_group-external\_tracker"></a>
**external\_tracker**

|Name|Description|Schema|
|---|---|---|
|**id**  <br>*optional*|Auto-generated ID to uniquely identify HA External Tracker|integer|
|**ip\_addr**  <br>*optional*|The IP Address of an external device that will respond to ARP requests to determine the state of the Primary Appliance|string|

<a name="ha\_interface\_group-interface\_properties"></a>
**interface\_properties**

|Name|Description|Schema|
|---|---|---|
|**id**  <br>*optional*|Auto-generated ID to uniquely identify HA Interface Properties|integer|
|**primary\_ip\_addr**  <br>*optional*|A unique Virtual IP Address on the Primary Appliance used for communication with its peer|string|
|**secondary\_ip\_addr**  <br>*optional*|A unique Virtual IP Address on the Secondary Appliance used for communication with its peer|string|
|**virtual\_interface\_name**  <br>*optional*|A Virtual Interface used for communication between the appliances in the HA pair|string|


<a name="ha\_service"></a>
### ha\_service

|Name|Schema|
|---|---|
|**ha\_interface\_group**  <br>*optional*|[ha\_interface\_group](#ha\_interface\_group)|
|**ha\_service\_properties**  <br>*optional*|[ha\_service\_properties](#ha\_service\_properties)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|


<a name="ha\_service\_delete\_success\_schema"></a>
### ha\_service\_delete\_success\_schema

|Name|Schema|
|---|---|
|**ha\_service**  <br>*optional*|[ha\_service](#ha\_service\_delete\_success\_schema-ha\_service)|

<a name="ha\_service\_delete\_success\_schema-ha\_service"></a>
**ha\_service**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="ha\_service\_post\_success\_schema"></a>
### ha\_service\_post\_success\_schema

|Name|Schema|
|---|---|
|**ha\_service**  <br>*optional*|[ha\_service](#ha\_service\_post\_success\_schema-ha\_service)|

<a name="ha\_service\_post\_success\_schema-ha\_service"></a>
**ha\_service**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="ha\_service\_properties"></a>
### ha\_service\_properties
HA Service properties

*Type* : < [ha\_service\_properties](#ha\_service\_properties-inline) > array

<a name="ha\_service\_properties-inline"></a>
**ha\_service\_properties**

|Name|Description|Schema|
|---|---|---|
|**disable\_shared\_mac**  <br>*optional*|Disable Shared MAC Address of the two Appliances|boolean|
|**failover\_ms**  <br>*optional*|The amount of time, upon losing contact with the active Appliance, that the standby Appliance should wait before going active (in milliseconds)|integer|
|**primary\_appliance\_name**  <br>*optional*  <br>*read-only*|The primary appliance name|string|
|**primary\_reclaim**  <br>*optional*|If enabled, the designated Primary Appliance will reclaim control from the active Appliance upon restarting after failover|boolean|
|**secondary\_appliance\_name**  <br>*optional*  <br>*read-only*|The secondary appliance name|string|
|**shared\_mac**  <br>*optional*|Shared MAC Address of the two Appliances|string|
|**swap\_primary\_secondary**  <br>*optional*|If enabled, the secondary Appliance will become the Primary Appliance and take precendence if both appliances come up simultaneously|boolean|
|**use\_serial\_ha**  <br>*optional*|Designates whether the two appliances are connected serially inline as a Fail-to-Wire pair|boolean|


<a name="ha\_service\_put\_success\_schema"></a>
### ha\_service\_put\_success\_schema

|Name|Schema|
|---|---|
|**ha\_service**  <br>*optional*|[ha\_service](#ha\_service\_put\_success\_schema-ha\_service)|

<a name="ha\_service\_put\_success\_schema-ha\_service"></a>
**ha\_service**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="ha\_service\_request\_schema"></a>
### ha\_service\_request\_schema

|Name|Schema|
|---|---|
|**ha\_service**  <br>*optional*|[ha\_service](#ha\_service)|


<a name="ha\_service\_response\_schema"></a>
### ha\_service\_response\_schema
*Type* : < [ha\_service\_response\_schema](#ha\_service\_response\_schema-inline) > array

<a name="ha\_service\_response\_schema-inline"></a>
**ha\_service\_response\_schema**

|Name|Schema|
|---|---|
|**ha\_interface\_group**  <br>*optional*|[ha\_interface\_group](#ha\_interface\_group)|
|**ha\_service\_properties**  <br>*optional*|[ha\_service\_properties](#ha\_service\_properties)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|


<a name="package\_name"></a>
### package\_name
Config package name using which the site API operation should be performed.

*Type* : string


<a name="site\_name"></a>
### site\_name
Site Name

*Type* : string






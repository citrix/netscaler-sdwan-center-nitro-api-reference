# intranet\_service


<a name="overview"></a>
## Overview
API to add, delete, get, modify Intranet Services


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* intranet\_service : Operations related to intranet\_service 




<a name="paths"></a>
## Paths

<a name="intranet\_service-post"></a>
### POST operation for intranet\_service
```
POST /intranet_service
```


#### Description
Use this operation to add Intranet services


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[intranet\_service\_request\_schema](#intranet\_service\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[intranet\_service\_post\_success\_schema](#intranet\_service\_post\_success\_schema)|
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

* intranet\_service


<a name="intranet\_service-get"></a>
### Get operation for intranet\_service
```
GET /intranet_service
```


#### Description
Use this operation to get the list of Intranet Services with basic settings


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[intranet\_service\_response\_schema](#intranet\_service\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* intranet\_service


<a name="intranet\_service-put"></a>
### PUT operation for intranet\_service
```
PUT /intranet_service
```


#### Description
Use this operation to modify Intranet services


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[intranet\_service\_put\_success\_schema](#intranet\_service\_put\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* intranet\_service


<a name="intranet\_service-deletepathparam-delete"></a>
### DELETE operation for intranet\_service
```
DELETE /intranet_service/{deletePathParam}
```


#### Description
Use this operation to delete Intranet services


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[intranet\_service\_delete\_success\_schema](#intranet\_service\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* intranet\_service




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
Auto-generated ID to uniquely identify intranet service

*Type* : integer


<a name="intranet\_service"></a>
### intranet\_service

|Name|Schema|
|---|---|
|**id**  <br>*optional*|[id](#id)|
|**intranet\_service\_name**  <br>*optional*|[intranet\_service\_name](#intranet\_service\_name)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**properties**  <br>*optional*|[properties](#properties)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|


<a name="intranet\_service\_delete\_success\_schema"></a>
### intranet\_service\_delete\_success\_schema

|Name|Schema|
|---|---|
|**intranet\_service**  <br>*optional*|[intranet\_service](#intranet\_service\_delete\_success\_schema-intranet\_service)|

<a name="intranet\_service\_delete\_success\_schema-intranet\_service"></a>
**intranet\_service**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="intranet\_service\_name"></a>
### intranet\_service\_name
The name for this intranet service

*Type* : string


<a name="intranet\_service\_post\_success\_schema"></a>
### intranet\_service\_post\_success\_schema

|Name|Schema|
|---|---|
|**intranet\_service**  <br>*optional*|[intranet\_service](#intranet\_service\_post\_success\_schema-intranet\_service)|

<a name="intranet\_service\_post\_success\_schema-intranet\_service"></a>
**intranet\_service**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="intranet\_service\_put\_success\_schema"></a>
### intranet\_service\_put\_success\_schema

|Name|Schema|
|---|---|
|**intranet\_service**  <br>*optional*|[intranet\_service](#intranet\_service\_put\_success\_schema-intranet\_service)|

<a name="intranet\_service\_put\_success\_schema-intranet\_service"></a>
**intranet\_service**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="intranet\_service\_request\_schema"></a>
### intranet\_service\_request\_schema

|Name|Schema|
|---|---|
|**intranet\_service**  <br>*optional*|[intranet\_service](#intranet\_service)|


<a name="intranet\_service\_response\_schema"></a>
### intranet\_service\_response\_schema
*Type* : < [intranet\_service\_response\_schema](#intranet\_service\_response\_schema-inline) > array

<a name="intranet\_service\_response\_schema-inline"></a>
**intranet\_service\_response\_schema**

|Name|Schema|
|---|---|
|**id**  <br>*optional*|[id](#id)|
|**intranet\_service\_name**  <br>*optional*|[intranet\_service\_name](#intranet\_service\_name)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**properties**  <br>*optional*|[properties](#properties)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|


<a name="package\_name"></a>
### package\_name
Config package name using which the site API operation should be performed.

*Type* : string


<a name="properties"></a>
### properties
Intranet Service Properties


|Name|Description|Schema|
|---|---|---|
|**default\_set**  <br>*optional*|The name of the Default Set that will be used to populate rules for the Service on the Site|string|
|**enable\_primary\_reclaim**  <br>*optional*|If enabled, the (use=primary) Usage associated with this service on a WAN Link will forcefully reclaim status as the active service on that WAN Link|boolean|
|**firewall\_zone**  <br>*optional*|The firewall zone|string|
|**ignore\_wanlink\_status**  <br>*optional*|If enabled, packets destined for this service will still choose this service even if all WAN Links for this service are unavailable|boolean|
|**intranet\_service\_in\_use**  <br>*optional*|The type of SaaS service associated with this intranet service|enum (none, saas\_gateway\_service, azure\_virtual\_wan)|


<a name="site\_name"></a>
### site\_name
Site Name

*Type* : string






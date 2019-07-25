# dynamic\_virtual\_path\_default\_set


<a name="overview"></a>
## Overview
API to add, modify, get, delete Dynamic Virtual Path Default Set


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* dynamic\_virtual\_path\_default\_set : Operations related to dynamic\_virtual\_path\_default\_set 




<a name="paths"></a>
## Paths

<a name="dynamic\_virtual\_path\_default\_set-post"></a>
### POST operation for dynamic\_virtual\_path\_default\_set
```
POST /dynamic_virtual_path_default_set
```


#### Description
Use this operation to add Dynamic Virtual Path Default Set


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[dynamic\_virtual\_path\_default\_set\_post\_success\_schema](#dynamic\_virtual\_path\_default\_set\_post\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* dynamic\_virtual\_path\_default\_set


<a name="dynamic\_virtual\_path\_default\_set-get"></a>
### Get operation for dynamic\_virtual\_path\_default\_set
```
GET /dynamic_virtual_path_default_set
```


#### Description
Use this operation to get the list of Dynamic Virtual Path Default Sets


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[dynamic\_virtual\_path\_default\_set\_response\_schema](#dynamic\_virtual\_path\_default\_set\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* dynamic\_virtual\_path\_default\_set


<a name="dynamic\_virtual\_path\_default\_set-put"></a>
### PUT operation for dynamic\_virtual\_path\_default\_set
```
PUT /dynamic_virtual_path_default_set
```


#### Description
Use this operation to modify Dynamic Virtual Path Default Set


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[dynamic\_virtual\_path\_default\_set\_request\_schema](#dynamic\_virtual\_path\_default\_set\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[dynamic\_virtual\_path\_default\_set\_put\_success\_schema](#dynamic\_virtual\_path\_default\_set\_put\_success\_schema)|
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

* dynamic\_virtual\_path\_default\_set


<a name="dynamic\_virtual\_path\_default\_set-deletepathparam-delete"></a>
### DELETE operation for dynamic\_virtual\_path\_default\_set
```
DELETE /dynamic_virtual_path_default_set/{deletePathParam}
```


#### Description
Use this operation to delete Dynamic Virtual Path Default Set


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[dynamic\_virtual\_path\_default\_set\_delete\_success\_schema](#dynamic\_virtual\_path\_default\_set\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* dynamic\_virtual\_path\_default\_set




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="dynamic\_virtual\_path\_default\_set"></a>
### dynamic\_virtual\_path\_default\_set

|Name|Schema|
|---|---|
|**dynamic\_virtual\_path\_default\_set\_properties**  <br>*optional*|[dynamic\_virtual\_path\_default\_set\_properties](#dynamic\_virtual\_path\_default\_set\_properties)|
|**id**  <br>*optional*|[id](#id)|
|**name**  <br>*optional*|[name](#name)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|


<a name="dynamic\_virtual\_path\_default\_set\_delete\_success\_schema"></a>
### dynamic\_virtual\_path\_default\_set\_delete\_success\_schema

|Name|Schema|
|---|---|
|**dynamic\_virtual\_path\_default\_set**  <br>*optional*|[dynamic\_virtual\_path\_default\_set](#dynamic\_virtual\_path\_default\_set\_delete\_success\_schema-dynamic\_virtual\_path\_default\_set)|

<a name="dynamic\_virtual\_path\_default\_set\_delete\_success\_schema-dynamic\_virtual\_path\_default\_set"></a>
**dynamic\_virtual\_path\_default\_set**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="dynamic\_virtual\_path\_default\_set\_post\_success\_schema"></a>
### dynamic\_virtual\_path\_default\_set\_post\_success\_schema

|Name|Schema|
|---|---|
|**dynamic\_virtual\_path\_default\_set**  <br>*optional*|[dynamic\_virtual\_path\_default\_set](#dynamic\_virtual\_path\_default\_set\_post\_success\_schema-dynamic\_virtual\_path\_default\_set)|

<a name="dynamic\_virtual\_path\_default\_set\_post\_success\_schema-dynamic\_virtual\_path\_default\_set"></a>
**dynamic\_virtual\_path\_default\_set**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="dynamic\_virtual\_path\_default\_set\_properties"></a>
### dynamic\_virtual\_path\_default\_set\_properties
Dynamic Virtual Path Default Set properties


|Name|Description|Schema|
|---|---|---|
|**creation\_sample\_time**  <br>*optional*|The amount of time, in seconds, over which packet counts and bandwidth will be measured to determine if a Dynamic Virtual Path needs to be created between two sites|integer|
|**creation\_throughput\_kbps**  <br>*optional*|The threshold, in kbps, of total throughput between two sites, measured over the Sample Time, at which Dynamic Virtual Path will be triggered|integer|
|**creation\_throughput\_pps**  <br>*optional*|The threshold, in pps, of total throughput between two sites, measured over the Sample Time, at which Dynamic Virtual Path will be triggered|integer|
|**recreate\_virtual\_path\_hold\_time**  <br>*optional*|The time, in minutes, after which a Dynamic Virtual Path removed for being DEAD can be recreated|string|
|**removal\_sample\_time**  <br>*optional*|The amount of time, in minutes, over which packet counts and bandwidth will be measured to determine if a Dynamic Virtual Path needs to be removed between two sites|integer|
|**removal\_throughput\_kbps**  <br>*optional*|The threshold, in kbps, of total throughput between two sites, measured over the Sample Time, at which Dynamic Virtual Path will be removed|integer|
|**removal\_throughput\_pps**  <br>*optional*|The threshold, in pps, of total throughput between two sites, measured over the Sample Time, at which Dynamic Virtual Path will be removed|integer|
|**remove\_virtual\_path\_down\_wait\_time**  <br>*optional*|The time, in minutes, after which a DEAD Dynamic Virtual Path will be removed|integer|
|**route\_cost**  <br>*optional*|This Cost will be added to Routes learned via the Dynamic Virtual Path and can be any value from 0 to 65535|integer|


<a name="dynamic\_virtual\_path\_default\_set\_put\_success\_schema"></a>
### dynamic\_virtual\_path\_default\_set\_put\_success\_schema

|Name|Schema|
|---|---|
|**dynamic\_virtual\_path\_default\_set**  <br>*optional*|[dynamic\_virtual\_path\_default\_set](#dynamic\_virtual\_path\_default\_set\_put\_success\_schema-dynamic\_virtual\_path\_default\_set)|

<a name="dynamic\_virtual\_path\_default\_set\_put\_success\_schema-dynamic\_virtual\_path\_default\_set"></a>
**dynamic\_virtual\_path\_default\_set**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="dynamic\_virtual\_path\_default\_set\_request\_schema"></a>
### dynamic\_virtual\_path\_default\_set\_request\_schema

|Name|Schema|
|---|---|
|**dynamic\_virtual\_path\_default\_set**  <br>*optional*|[dynamic\_virtual\_path\_default\_set](#dynamic\_virtual\_path\_default\_set)|


<a name="dynamic\_virtual\_path\_default\_set\_response\_schema"></a>
### dynamic\_virtual\_path\_default\_set\_response\_schema
*Type* : < [dynamic\_virtual\_path\_default\_set\_response\_schema](#dynamic\_virtual\_path\_default\_set\_response\_schema-inline) > array

<a name="dynamic\_virtual\_path\_default\_set\_response\_schema-inline"></a>
**dynamic\_virtual\_path\_default\_set\_response\_schema**

|Name|Schema|
|---|---|
|**dynamic\_virtual\_path\_default\_set\_properties**  <br>*optional*|[dynamic\_virtual\_path\_default\_set\_properties](#dynamic\_virtual\_path\_default\_set\_properties)|
|**id**  <br>*optional*|[id](#id)|
|**name**  <br>*optional*|[name](#name)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|


<a name="id"></a>
### id
Auto-generated ID to uniquely identify Dynamic Virtual Path Default Set

*Type* : integer


<a name="name"></a>
### name
The name for this Dynamic Virtual Path Default Set

*Type* : string


<a name="package\_name"></a>
### package\_name
Config package name using which the API operation should be performed.

*Type* : string






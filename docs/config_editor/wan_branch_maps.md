# wan\_branch\_maps


<a name="overview"></a>
## Overview
API to add, modify, delete, and get configuration for wan-branch maps


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* wan\_branch\_maps : Operations related to wan\_branch\_maps 




<a name="paths"></a>
## Paths

<a name="wan\_branch\_maps-post"></a>
### POST operation for wan\_branch\_maps
```
POST /wan_branch_maps
```


#### Description
Use this operation to add wan branch map entry


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[wan\_branch\_maps\_post\_success\_schema](#wan\_branch\_maps\_post\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* wan\_branch\_maps


<a name="wan\_branch\_maps-get"></a>
### Get operation for wan\_branch\_maps
```
GET /wan_branch_maps
```


#### Description
Use this operation to get the list of wan branch map entry


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[wan\_branch\_maps\_response\_schema](#wan\_branch\_maps\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* wan\_branch\_maps


<a name="wan\_branch\_maps-put"></a>
### PUT operation for wan\_branch\_maps
```
PUT /wan_branch_maps
```


#### Description
Use this operation to modify a wan branch map entry


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[wan\_branch\_maps\_request\_schema](#wan\_branch\_maps\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[wan\_branch\_maps\_put\_success\_schema](#wan\_branch\_maps\_put\_success\_schema)|
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

* wan\_branch\_maps


<a name="wan\_branch\_maps-deletepathparam-delete"></a>
### DELETE operation for wan\_branch\_maps
```
DELETE /wan_branch_maps/{deletePathParam}
```


#### Description
Use this operation to delete a wan branch map entry


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[wan\_branch\_maps\_delete\_success\_schema](#wan\_branch\_maps\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* wan\_branch\_maps




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
Auto-generated ID. Use this ID to modify or delete a wan\_branch\_map

*Type* : integer


<a name="name"></a>
### name
Wan resource name

*Type* : string


<a name="package\_name"></a>
### package\_name
Config package name using which the ipsec\_tunnel API operation should be performed.

*Type* : string


<a name="service\_name1"></a>
### service\_name1
Intranet Service name

*Type* : string


<a name="service\_name2"></a>
### service\_name2
Intranet Service name

*Type* : string


<a name="sitename"></a>
### sitename
Sitename

*Type* : string


<a name="tunnel\_id"></a>
### tunnel\_id
parent key, tunnel-id

*Type* : integer


<a name="wan\_branch\_maps"></a>
### wan\_branch\_maps

|Name|Schema|
|---|---|
|**id**  <br>*optional*|[id](#id)|
|**name**  <br>*optional*|[name](#name)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**service\_name1**  <br>*optional*|[service\_name1](#service\_name1)|
|**service\_name2**  <br>*optional*|[service\_name2](#service\_name2)|
|**sitename**  <br>*optional*|[sitename](#sitename)|
|**tunnel\_id**  <br>*optional*|[tunnel\_id](#tunnel\_id)|
|**wanname**  <br>*optional*|[wanname](#wanname)|


<a name="wan\_branch\_maps\_delete\_success\_schema"></a>
### wan\_branch\_maps\_delete\_success\_schema

|Name|Schema|
|---|---|
|**wan\_branch\_maps**  <br>*optional*|[wan\_branch\_maps](#wan\_branch\_maps\_delete\_success\_schema-wan\_branch\_maps)|

<a name="wan\_branch\_maps\_delete\_success\_schema-wan\_branch\_maps"></a>
**wan\_branch\_maps**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="wan\_branch\_maps\_post\_success\_schema"></a>
### wan\_branch\_maps\_post\_success\_schema

|Name|Schema|
|---|---|
|**wan\_branch\_maps**  <br>*optional*|[wan\_branch\_maps](#wan\_branch\_maps\_post\_success\_schema-wan\_branch\_maps)|

<a name="wan\_branch\_maps\_post\_success\_schema-wan\_branch\_maps"></a>
**wan\_branch\_maps**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="wan\_branch\_maps\_put\_success\_schema"></a>
### wan\_branch\_maps\_put\_success\_schema

|Name|Schema|
|---|---|
|**wan\_branch\_maps**  <br>*optional*|[wan\_branch\_maps](#wan\_branch\_maps\_put\_success\_schema-wan\_branch\_maps)|

<a name="wan\_branch\_maps\_put\_success\_schema-wan\_branch\_maps"></a>
**wan\_branch\_maps**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="wan\_branch\_maps\_request\_schema"></a>
### wan\_branch\_maps\_request\_schema

|Name|Schema|
|---|---|
|**wan\_branch\_maps**  <br>*optional*|[wan\_branch\_maps](#wan\_branch\_maps)|


<a name="wan\_branch\_maps\_response\_schema"></a>
### wan\_branch\_maps\_response\_schema
*Type* : < [wan\_branch\_maps\_response\_schema](#wan\_branch\_maps\_response\_schema-inline) > array

<a name="wan\_branch\_maps\_response\_schema-inline"></a>
**wan\_branch\_maps\_response\_schema**

|Name|Schema|
|---|---|
|**id**  <br>*optional*|[id](#id)|
|**name**  <br>*optional*|[name](#name)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**service\_name1**  <br>*optional*|[service\_name1](#service\_name1)|
|**service\_name2**  <br>*optional*|[service\_name2](#service\_name2)|
|**sitename**  <br>*optional*|[sitename](#sitename)|
|**tunnel\_id**  <br>*optional*|[tunnel\_id](#tunnel\_id)|
|**wanname**  <br>*optional*|[wanname](#wanname)|


<a name="wanname"></a>
### wanname
Wan resource name

*Type* : string






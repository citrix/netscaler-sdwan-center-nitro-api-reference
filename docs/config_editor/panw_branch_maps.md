# panw\_branch\_maps


<a name="overview"></a>
## Overview
API to add, modify, delete, and get configuration for panw-branch maps


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* panw\_branch\_maps : Operations related to panw\_branch\_maps 




<a name="paths"></a>
## Paths

<a name="panw\_branch\_maps-post"></a>
### POST operation for panw\_branch\_maps
```
POST /panw_branch_maps
```


#### Description
Use this operation to add panw branch map entry


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[panw\_branch\_maps\_post\_success\_schema](#panw\_branch\_maps\_post\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* panw\_branch\_maps


<a name="panw\_branch\_maps-get"></a>
### Get operation for panw\_branch\_maps
```
GET /panw_branch_maps
```


#### Description
Use this operation to get the list of panw branch map entry


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[panw\_branch\_maps\_response\_schema](#panw\_branch\_maps\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* panw\_branch\_maps


<a name="panw\_branch\_maps-put"></a>
### PUT operation for panw\_branch\_maps
```
PUT /panw_branch_maps
```


#### Description
Use this operation to modify a panw branch map entry


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[panw\_branch\_maps\_request\_schema](#panw\_branch\_maps\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[panw\_branch\_maps\_put\_success\_schema](#panw\_branch\_maps\_put\_success\_schema)|
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

* panw\_branch\_maps


<a name="panw\_branch\_maps-deletepathparam-delete"></a>
### DELETE operation for panw\_branch\_maps
```
DELETE /panw_branch_maps/{deletePathParam}
```


#### Description
Use this operation to delete a panw branch map entry


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[panw\_branch\_maps\_delete\_success\_schema](#panw\_branch\_maps\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* panw\_branch\_maps




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="appobj"></a>
### appobj
Application object to specify the match criteria

*Type* : string


<a name="bandwidth"></a>
### bandwidth
bandwidth

*Type* : string


<a name="id"></a>
### id
Auto-generated ID. Use this ID to modify or delete a panw\_branch\_map

*Type* : integer


<a name="package\_name"></a>
### package\_name
Config package name using which the panw branch map API operation should be performed.

*Type* : string


<a name="panw\_branch\_maps"></a>
### panw\_branch\_maps

|Name|Schema|
|---|---|
|**appobj**  <br>*optional*|[appobj](#appobj)|
|**bandwidth**  <br>*optional*|[bandwidth](#bandwidth)|
|**id**  <br>*optional*|[id](#id)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**primarywanlink**  <br>*optional*|[primarywanlink](#primarywanlink)|
|**psk**  <br>*optional*|[psk](#psk)|
|**region**  <br>*optional*|[region](#region)|
|**secondarywanlink**  <br>*optional*|[secondarywanlink](#secondarywanlink)|
|**sitename**  <br>*optional*|[sitename](#sitename)|
|**tunnel\_id**  <br>*optional*|[tunnel\_id](#tunnel\_id)|


<a name="panw\_branch\_maps\_delete\_success\_schema"></a>
### panw\_branch\_maps\_delete\_success\_schema

|Name|Schema|
|---|---|
|**panw\_branch\_maps**  <br>*optional*|[panw\_branch\_maps](#panw\_branch\_maps\_delete\_success\_schema-panw\_branch\_maps)|

<a name="panw\_branch\_maps\_delete\_success\_schema-panw\_branch\_maps"></a>
**panw\_branch\_maps**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="panw\_branch\_maps\_post\_success\_schema"></a>
### panw\_branch\_maps\_post\_success\_schema

|Name|Schema|
|---|---|
|**panw\_branch\_maps**  <br>*optional*|[panw\_branch\_maps](#panw\_branch\_maps\_post\_success\_schema-panw\_branch\_maps)|

<a name="panw\_branch\_maps\_post\_success\_schema-panw\_branch\_maps"></a>
**panw\_branch\_maps**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="panw\_branch\_maps\_put\_success\_schema"></a>
### panw\_branch\_maps\_put\_success\_schema

|Name|Schema|
|---|---|
|**panw\_branch\_maps**  <br>*optional*|[panw\_branch\_maps](#panw\_branch\_maps\_put\_success\_schema-panw\_branch\_maps)|

<a name="panw\_branch\_maps\_put\_success\_schema-panw\_branch\_maps"></a>
**panw\_branch\_maps**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="panw\_branch\_maps\_request\_schema"></a>
### panw\_branch\_maps\_request\_schema

|Name|Schema|
|---|---|
|**panw\_branch\_maps**  <br>*optional*|[panw\_branch\_maps](#panw\_branch\_maps)|


<a name="panw\_branch\_maps\_response\_schema"></a>
### panw\_branch\_maps\_response\_schema
*Type* : < [panw\_branch\_maps\_response\_schema](#panw\_branch\_maps\_response\_schema-inline) > array

<a name="panw\_branch\_maps\_response\_schema-inline"></a>
**panw\_branch\_maps\_response\_schema**

|Name|Schema|
|---|---|
|**appobj**  <br>*optional*|[appobj](#appobj)|
|**bandwidth**  <br>*optional*|[bandwidth](#bandwidth)|
|**id**  <br>*optional*|[id](#id)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**primarywanlink**  <br>*optional*|[primarywanlink](#primarywanlink)|
|**psk**  <br>*optional*|[psk](#psk)|
|**region**  <br>*optional*|[region](#region)|
|**secondarywanlink**  <br>*optional*|[secondarywanlink](#secondarywanlink)|
|**sitename**  <br>*optional*|[sitename](#sitename)|
|**tunnel\_id**  <br>*optional*|[tunnel\_id](#tunnel\_id)|


<a name="primarywanlink"></a>
### primarywanlink
primary wanlink name

*Type* : string


<a name="psk"></a>
### psk
pre shared key for network objects

*Type* : string


<a name="region"></a>
### region
VPN endpoint location

*Type* : string


<a name="secondarywanlink"></a>
### secondarywanlink
secondary wanlink name

*Type* : string


<a name="sitename"></a>
### sitename
Sitename

*Type* : string


<a name="tunnel\_id"></a>
### tunnel\_id
parent key, tunnel-id

*Type* : integer






# rule\_groups


<a name="overview"></a>
## Overview
API to add, delete, get, modify rule groups


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* rule\_groups : Operations related to rule\_groups 




<a name="paths"></a>
## Paths

<a name="rule\_groups-post"></a>
### POST operation for rule\_groups
```
POST /rule_groups
```


#### Description
Use this operation to add rule groups


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[rule\_groups\_post\_success\_schema](#rule\_groups\_post\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* rule\_groups


<a name="rule\_groups-get"></a>
### Get operation for rule\_groups
```
GET /rule_groups
```


#### Description
Use this operation to get the rule groups


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[rule\_groups\_response\_schema](#rule\_groups\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* rule\_groups


<a name="rule\_groups-put"></a>
### PUT operation for rule\_groups
```
PUT /rule_groups
```


#### Description
Use this operation to modify rule groups


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[rule\_groups\_request\_schema](#rule\_groups\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[rule\_groups\_put\_success\_schema](#rule\_groups\_put\_success\_schema)|
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

* rule\_groups


<a name="rule\_groups-deletepathparam-delete"></a>
### DELETE operation for rule\_groups
```
DELETE /rule_groups/{deletePathParam}
```


#### Description
Use this operation to delete rule groups


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[rule\_groups\_delete\_success\_schema](#rule\_groups\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* rule\_groups




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
Auto-generated ID to uniquely identify the rule group

*Type* : integer


<a name="name"></a>
### name
The name for the rule group

*Type* : string


<a name="package\_name"></a>
### package\_name
Config package name using which the API operation should be performed.

*Type* : string


<a name="properties"></a>
### properties
Properties for the autopath group


|Name|Description|Schema|
|---|---|---|
|**enable\_mos**  <br>*optional*|Enabling this field gathers statistics for the application at the WAN to LAN side of the Virtual Path, and derives a quality score for that application as if that application were a VOIP call|boolean|


<a name="rule\_groups"></a>
### rule\_groups

|Name|Schema|
|---|---|
|**id**  <br>*optional*|[id](#id)|
|**name**  <br>*optional*|[name](#name)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**properties**  <br>*optional*|[properties](#properties)|


<a name="rule\_groups\_delete\_success\_schema"></a>
### rule\_groups\_delete\_success\_schema

|Name|Schema|
|---|---|
|**rule\_groups**  <br>*optional*|[rule\_groups](#rule\_groups\_delete\_success\_schema-rule\_groups)|

<a name="rule\_groups\_delete\_success\_schema-rule\_groups"></a>
**rule\_groups**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="rule\_groups\_post\_success\_schema"></a>
### rule\_groups\_post\_success\_schema

|Name|Schema|
|---|---|
|**rule\_groups**  <br>*optional*|[rule\_groups](#rule\_groups\_post\_success\_schema-rule\_groups)|

<a name="rule\_groups\_post\_success\_schema-rule\_groups"></a>
**rule\_groups**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="rule\_groups\_put\_success\_schema"></a>
### rule\_groups\_put\_success\_schema

|Name|Schema|
|---|---|
|**rule\_groups**  <br>*optional*|[rule\_groups](#rule\_groups\_put\_success\_schema-rule\_groups)|

<a name="rule\_groups\_put\_success\_schema-rule\_groups"></a>
**rule\_groups**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="rule\_groups\_request\_schema"></a>
### rule\_groups\_request\_schema

|Name|Schema|
|---|---|
|**rule\_groups**  <br>*optional*|[rule\_groups](#rule\_groups)|


<a name="rule\_groups\_response\_schema"></a>
### rule\_groups\_response\_schema
*Type* : < [rule\_groups\_response\_schema](#rule\_groups\_response\_schema-inline) > array

<a name="rule\_groups\_response\_schema-inline"></a>
**rule\_groups\_response\_schema**

|Name|Schema|
|---|---|
|**id**  <br>*optional*|[id](#id)|
|**name**  <br>*optional*|[name](#name)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**properties**  <br>*optional*|[properties](#properties)|






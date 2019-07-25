# virtual\_path\_default\_set


<a name="overview"></a>
## Overview
API to add, modify, get, delete Virtual Path Default Set


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* virtual\_path\_default\_set : Operations related to virtual\_path\_default\_set 




<a name="paths"></a>
## Paths

<a name="virtual\_path\_default\_set-post"></a>
### POST operation for virtual\_path\_default\_set
```
POST /virtual_path_default_set
```


#### Description
Use this operation to add Virtual Path Default Set


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[virtual\_path\_default\_set\_post\_success\_schema](#virtual\_path\_default\_set\_post\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* virtual\_path\_default\_set


<a name="virtual\_path\_default\_set-get"></a>
### Get operation for virtual\_path\_default\_set
```
GET /virtual_path_default_set
```


#### Description
Use this operation to get the list of Virtual Path Default Sets


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[virtual\_path\_default\_set\_response\_schema](#virtual\_path\_default\_set\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* virtual\_path\_default\_set


<a name="virtual\_path\_default\_set-put"></a>
### PUT operation for virtual\_path\_default\_set
```
PUT /virtual_path_default_set
```


#### Description
Use this operation to modify Virtual Path Default Set


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[virtual\_path\_default\_set\_request\_schema](#virtual\_path\_default\_set\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[virtual\_path\_default\_set\_put\_success\_schema](#virtual\_path\_default\_set\_put\_success\_schema)|
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

* virtual\_path\_default\_set


<a name="virtual\_path\_default\_set-deletepathparam-delete"></a>
### DELETE operation for virtual\_path\_default\_set
```
DELETE /virtual_path_default_set/{deletePathParam}
```


#### Description
Use this operation to delete Virtual Path Default Set


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[virtual\_path\_default\_set\_delete\_success\_schema](#virtual\_path\_default\_set\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* virtual\_path\_default\_set




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
Auto-generated ID to uniquely identify Virtual Path Default Set

*Type* : integer


<a name="name"></a>
### name
The name for this Virtual Path Default Set

*Type* : string


<a name="package\_name"></a>
### package\_name
Config package name using which the API operation should be performed.

*Type* : string


<a name="virtual\_path\_default\_set"></a>
### virtual\_path\_default\_set

|Name|Schema|
|---|---|
|**id**  <br>*optional*|[id](#id)|
|**name**  <br>*optional*|[name](#name)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|


<a name="virtual\_path\_default\_set\_delete\_success\_schema"></a>
### virtual\_path\_default\_set\_delete\_success\_schema

|Name|Schema|
|---|---|
|**virtual\_path\_default\_set**  <br>*optional*|[virtual\_path\_default\_set](#virtual\_path\_default\_set\_delete\_success\_schema-virtual\_path\_default\_set)|

<a name="virtual\_path\_default\_set\_delete\_success\_schema-virtual\_path\_default\_set"></a>
**virtual\_path\_default\_set**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="virtual\_path\_default\_set\_post\_success\_schema"></a>
### virtual\_path\_default\_set\_post\_success\_schema

|Name|Schema|
|---|---|
|**virtual\_path\_default\_set**  <br>*optional*|[virtual\_path\_default\_set](#virtual\_path\_default\_set\_post\_success\_schema-virtual\_path\_default\_set)|

<a name="virtual\_path\_default\_set\_post\_success\_schema-virtual\_path\_default\_set"></a>
**virtual\_path\_default\_set**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="virtual\_path\_default\_set\_put\_success\_schema"></a>
### virtual\_path\_default\_set\_put\_success\_schema

|Name|Schema|
|---|---|
|**virtual\_path\_default\_set**  <br>*optional*|[virtual\_path\_default\_set](#virtual\_path\_default\_set\_put\_success\_schema-virtual\_path\_default\_set)|

<a name="virtual\_path\_default\_set\_put\_success\_schema-virtual\_path\_default\_set"></a>
**virtual\_path\_default\_set**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="virtual\_path\_default\_set\_request\_schema"></a>
### virtual\_path\_default\_set\_request\_schema

|Name|Schema|
|---|---|
|**virtual\_path\_default\_set**  <br>*optional*|[virtual\_path\_default\_set](#virtual\_path\_default\_set)|


<a name="virtual\_path\_default\_set\_response\_schema"></a>
### virtual\_path\_default\_set\_response\_schema
*Type* : < [virtual\_path\_default\_set\_response\_schema](#virtual\_path\_default\_set\_response\_schema-inline) > array

<a name="virtual\_path\_default\_set\_response\_schema-inline"></a>
**virtual\_path\_default\_set\_response\_schema**

|Name|Schema|
|---|---|
|**id**  <br>*optional*|[id](#id)|
|**name**  <br>*optional*|[name](#name)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|






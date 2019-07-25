# routing\_domain


<a name="overview"></a>
## Overview
API to add, delete, get and modify global routing domains


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* routing\_domain : Operations related to routing\_domain 




<a name="paths"></a>
## Paths

<a name="routing\_domain-post"></a>
### POST operation for routing\_domain
```
POST /routing_domain
```


#### Description
Use this operation to add global routing domains


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[routing\_domain\_request\_schema](#routing\_domain\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[routing\_domain\_post\_success\_schema](#routing\_domain\_post\_success\_schema)|
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

* routing\_domain


<a name="routing\_domain-get"></a>
### Get operation for routing\_domain
```
GET /routing_domain
```


#### Description
Use this operation to get the global routing domains


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[routing\_domain\_response\_schema](#routing\_domain\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* routing\_domain


<a name="routing\_domain-put"></a>
### PUT operation for routing\_domain
```
PUT /routing_domain
```


#### Description
Use this operation to modify global routing domains


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[routing\_domain\_put\_success\_schema](#routing\_domain\_put\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* routing\_domain


<a name="routing\_domain-deletepathparam-delete"></a>
### DELETE operation for routing\_domain
```
DELETE /routing_domain/{deletePathParam}
```


#### Description
Use this operation to delete global routing domains


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[routing\_domain\_delete\_success\_schema](#routing\_domain\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* routing\_domain




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
Auto-generated ID to uniquely identify Routing Domain

*Type* : integer


<a name="name"></a>
### name
The name for the Routing Domain

*Type* : string


<a name="package\_name"></a>
### package\_name
Config package name using which the API operation should be performed.

*Type* : string


<a name="properties"></a>
### properties
Properties for the routing domain


|Name|Description|Schema|
|---|---|---|
|**is\_default**  <br>*optional*|Set to true to use as the default domain for the network|boolean|
|**redirect\_to\_wanop**  <br>*optional*|Set to true to optimize traffic from this domain|boolean|


<a name="routing\_domain"></a>
### routing\_domain

|Name|Schema|
|---|---|
|**id**  <br>*optional*|[id](#id)|
|**name**  <br>*optional*|[name](#name)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**properties**  <br>*optional*|[properties](#properties)|


<a name="routing\_domain\_delete\_success\_schema"></a>
### routing\_domain\_delete\_success\_schema

|Name|Schema|
|---|---|
|**routing\_domain**  <br>*optional*|[routing\_domain](#routing\_domain\_delete\_success\_schema-routing\_domain)|

<a name="routing\_domain\_delete\_success\_schema-routing\_domain"></a>
**routing\_domain**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="routing\_domain\_post\_success\_schema"></a>
### routing\_domain\_post\_success\_schema

|Name|Schema|
|---|---|
|**routing\_domain**  <br>*optional*|[routing\_domain](#routing\_domain\_post\_success\_schema-routing\_domain)|

<a name="routing\_domain\_post\_success\_schema-routing\_domain"></a>
**routing\_domain**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="routing\_domain\_put\_success\_schema"></a>
### routing\_domain\_put\_success\_schema

|Name|Schema|
|---|---|
|**routing\_domain**  <br>*optional*|[routing\_domain](#routing\_domain\_put\_success\_schema-routing\_domain)|

<a name="routing\_domain\_put\_success\_schema-routing\_domain"></a>
**routing\_domain**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="routing\_domain\_request\_schema"></a>
### routing\_domain\_request\_schema

|Name|Schema|
|---|---|
|**routing\_domain**  <br>*optional*|[routing\_domain](#routing\_domain)|


<a name="routing\_domain\_response\_schema"></a>
### routing\_domain\_response\_schema
*Type* : < [routing\_domain\_response\_schema](#routing\_domain\_response\_schema-inline) > array

<a name="routing\_domain\_response\_schema-inline"></a>
**routing\_domain\_response\_schema**

|Name|Schema|
|---|---|
|**id**  <br>*optional*|[id](#id)|
|**name**  <br>*optional*|[name](#name)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**properties**  <br>*optional*|[properties](#properties)|






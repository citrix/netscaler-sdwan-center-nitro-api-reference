# app\_qoe


<a name="overview"></a>
## Overview
API to add, delete, get, modify global application qoe


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* app\_qoe : Operations related to app\_qoe 




<a name="paths"></a>
## Paths

<a name="app\_qoe-post"></a>
### POST operation for app\_qoe
```
POST /app_qoe
```


#### Description
This operation is to add application QoE objects


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[app\_qoe\_post\_success\_schema](#app\_qoe\_post\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* app\_qoe


<a name="app\_qoe-get"></a>
### Get operation for app\_qoe
```
GET /app_qoe
```


#### Description
This operation is to get the application QoE objects


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[app\_qoe\_response\_schema](#app\_qoe\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* app\_qoe


<a name="app\_qoe-put"></a>
### PUT operation for app\_qoe
```
PUT /app_qoe
```


#### Description
This operation is to modify existing application QoE object


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[app\_qoe\_request\_schema](#app\_qoe\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[app\_qoe\_put\_success\_schema](#app\_qoe\_put\_success\_schema)|
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

* app\_qoe


<a name="app\_qoe-deletepathparam-delete"></a>
### DELETE operation for app\_qoe
```
DELETE /app_qoe/{deletePathParam}
```


#### Description
This operation is to delete the application QoE object


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[app\_qoe\_delete\_success\_schema](#app\_qoe\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* app\_qoe




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="app\_qoe"></a>
### app\_qoe

|Name|Schema|
|---|---|
|**application\_name**  <br>*optional*|[application\_name](#application\_name)|
|**application\_object\_name**  <br>*optional*|[application\_object\_name](#application\_object\_name)|
|**id**  <br>*optional*|[id](#id)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**qoe\_profile**  <br>*optional*|[qoe\_profile](#qoe\_profile)|
|**type**  <br>*optional*|[type](#type)|


<a name="app\_qoe\_delete\_success\_schema"></a>
### app\_qoe\_delete\_success\_schema

|Name|Schema|
|---|---|
|**app\_qoe**  <br>*optional*|[app\_qoe](#app\_qoe\_delete\_success\_schema-app\_qoe)|

<a name="app\_qoe\_delete\_success\_schema-app\_qoe"></a>
**app\_qoe**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="app\_qoe\_post\_success\_schema"></a>
### app\_qoe\_post\_success\_schema

|Name|Schema|
|---|---|
|**app\_qoe**  <br>*optional*|[app\_qoe](#app\_qoe\_post\_success\_schema-app\_qoe)|

<a name="app\_qoe\_post\_success\_schema-app\_qoe"></a>
**app\_qoe**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="app\_qoe\_put\_success\_schema"></a>
### app\_qoe\_put\_success\_schema

|Name|Schema|
|---|---|
|**app\_qoe**  <br>*optional*|[app\_qoe](#app\_qoe\_put\_success\_schema-app\_qoe)|

<a name="app\_qoe\_put\_success\_schema-app\_qoe"></a>
**app\_qoe**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="app\_qoe\_request\_schema"></a>
### app\_qoe\_request\_schema

|Name|Schema|
|---|---|
|**app\_qoe**  <br>*optional*|[app\_qoe](#app\_qoe)|


<a name="app\_qoe\_response\_schema"></a>
### app\_qoe\_response\_schema
*Type* : < [app\_qoe\_response\_schema](#app\_qoe\_response\_schema-inline) > array

<a name="app\_qoe\_response\_schema-inline"></a>
**app\_qoe\_response\_schema**

|Name|Schema|
|---|---|
|**application\_name**  <br>*optional*|[application\_name](#application\_name)|
|**application\_object\_name**  <br>*optional*|[application\_object\_name](#application\_object\_name)|
|**id**  <br>*optional*|[id](#id)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**qoe\_profile**  <br>*optional*|[qoe\_profile](#qoe\_profile)|
|**type**  <br>*optional*|[type](#type)|


<a name="application\_name"></a>
### application\_name
Application name

*Type* : string


<a name="application\_object\_name"></a>
### application\_object\_name
Application object name

*Type* : string


<a name="id"></a>
### id
Auto-generated ID to uniquely identify application qoe

*Type* : integer


<a name="package\_name"></a>
### package\_name
Config package name using which the API operation should be performed.

*Type* : string


<a name="qoe\_profile"></a>
### qoe\_profile
QoE profile to be applied to the application QoE

*Type* : string


<a name="type"></a>
### type
Specifies whether the QoE entry is for an application or an application object

*Type* : enum (application, application\_objects)






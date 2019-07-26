# application\_objects


<a name="overview"></a>
## Overview
API to add, delete, get, modify global application objects


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* application\_objects : Operations related to application\_objects 




<a name="paths"></a>
## Paths

<a name="application\_objects-post"></a>
### POST operation for application\_objects
```
POST /application_objects
```


#### Description
Use this operation to add global application objects


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[application\_objects\_request\_schema](#application\_objects\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[application\_objects\_post\_success\_schema](#application\_objects\_post\_success\_schema)|
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

* application\_objects


<a name="application\_objects-get"></a>
### Get operation for application\_objects
```
GET /application_objects
```


#### Description
Use this operation to get the global application objects


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[application\_objects\_response\_schema](#application\_objects\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* application\_objects


<a name="application\_objects-put"></a>
### PUT operation for application\_objects
```
PUT /application_objects
```


#### Description
Use this operation to modify global application objects


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[application\_objects\_put\_success\_schema](#application\_objects\_put\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* application\_objects


<a name="application\_objects-deletepathparam-delete"></a>
### DELETE operation for application\_objects
```
DELETE /application_objects/{deletePathParam}
```


#### Description
Use this operation to delete global application objects


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[application\_objects\_delete\_success\_schema](#application\_objects\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* application\_objects




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="application\_match\_criteria"></a>
### application\_match\_criteria
The Application Match Criteria

*Type* : < [application\_match\_criteria](#application\_match\_criteria-inline) > array

<a name="application\_match\_criteria-inline"></a>
**application\_match\_criteria**

|Name|Description|Schema|
|---|---|---|
|**application**  <br>*optional*|Match Type for the application groups|string|
|**application\_family**  <br>*optional*|Match Type for the application groups. The inputs are case sensitive|enum (Antivirus, Application Service Service, Audio/Video/Video, Authentication, Behavioral, Citrix Protocol Protocol, Compression, Database, ERP, Encrypted, File Server Server, File Transfer Transfer, Forum, Game, Instant Messaging Messaging, Mail, Microsoft Office Office, Middleware, Network Management Management, Network Service Service, Peer to Peer to Peer, Printer, Routing, Security Service Service, Standard, Telephony, Terminal, Thin Client Client, Tunneling, Wap, Web, Webmail)|
|**dscp**  <br>*optional*|Match IP DSCP tag|enum (any, af11, af12, af13, af21, af22, af23, af31, af32, af33, af41, af42, af43, cs1, cs2, cs3, cs4, cs5, cs6, cs7, default, ef)|
|**id**  <br>*optional*|Auto-generated ID to uniquely identify the application match criteria|integer|
|**match\_type**  <br>*optional*|Match Type for the application groups|enum (application\_family, application, ip\_protocol)|
|**network\_ip\_address1**  <br>*optional*|Match source or destination IP address|string|
|**port1**  <br>*optional*|Match on either source or destination port number. Or specify a port range|string|
|**protocol**  <br>*optional*|Match on IP Protocol. Should be a numeric protocol number from 0 to 254 or ANY in case of all protocols|string|


<a name="application\_objects"></a>
### application\_objects

|Name|Schema|
|---|---|
|**application\_match\_criteria**  <br>*optional*|[application\_match\_criteria](#application\_match\_criteria)|
|**id**  <br>*optional*|[id](#id)|
|**name**  <br>*optional*|[name](#name)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**priority**  <br>*optional*|[priority](#priority)|
|**properties**  <br>*optional*|[properties](#properties)|


<a name="application\_objects\_delete\_success\_schema"></a>
### application\_objects\_delete\_success\_schema

|Name|Schema|
|---|---|
|**application\_objects**  <br>*optional*|[application\_objects](#application\_objects\_delete\_success\_schema-application\_objects)|

<a name="application\_objects\_delete\_success\_schema-application\_objects"></a>
**application\_objects**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="application\_objects\_post\_success\_schema"></a>
### application\_objects\_post\_success\_schema

|Name|Schema|
|---|---|
|**application\_objects**  <br>*optional*|[application\_objects](#application\_objects\_post\_success\_schema-application\_objects)|

<a name="application\_objects\_post\_success\_schema-application\_objects"></a>
**application\_objects**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="application\_objects\_put\_success\_schema"></a>
### application\_objects\_put\_success\_schema

|Name|Schema|
|---|---|
|**application\_objects**  <br>*optional*|[application\_objects](#application\_objects\_put\_success\_schema-application\_objects)|

<a name="application\_objects\_put\_success\_schema-application\_objects"></a>
**application\_objects**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="application\_objects\_request\_schema"></a>
### application\_objects\_request\_schema

|Name|Schema|
|---|---|
|**application\_objects**  <br>*optional*|[application\_objects](#application\_objects)|


<a name="application\_objects\_response\_schema"></a>
### application\_objects\_response\_schema
*Type* : < [application\_objects\_response\_schema](#application\_objects\_response\_schema-inline) > array

<a name="application\_objects\_response\_schema-inline"></a>
**application\_objects\_response\_schema**

|Name|Schema|
|---|---|
|**application\_match\_criteria**  <br>*optional*|[application\_match\_criteria](#application\_match\_criteria)|
|**id**  <br>*optional*|[id](#id)|
|**name**  <br>*optional*|[name](#name)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**priority**  <br>*optional*|[priority](#priority)|
|**properties**  <br>*optional*|[properties](#properties)|


<a name="id"></a>
### id
Auto-generated ID to uniquely identify application object

*Type* : integer


<a name="name"></a>
### name
The name for the application object

*Type* : string


<a name="package\_name"></a>
### package\_name
Config package name using which the API operation should be performed.

*Type* : string


<a name="priority"></a>
### priority
The order/precedence in which Applications are chosen for reporting (automatically redistributed)

*Type* : integer


<a name="properties"></a>
### properties
Properties for the autopath group


|Name|Description|Schema|
|---|---|---|
|**enable\_reporting**  <br>*optional*|If this application is set to false, then the statistics will not be recorded|boolean|






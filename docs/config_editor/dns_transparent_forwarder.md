# dns\_transparent\_forwarder


<a name="overview"></a>
## Overview
API to add, delete, get, modify transparent DNS forwarders


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* dns\_transparent\_forwarder : Operations related to dns\_transparent\_forwarder 




<a name="paths"></a>
## Paths

<a name="dns\_transparent\_forwarder-post"></a>
### POST operation for dns\_transparent\_forwarder
```
POST /dns_transparent_forwarder
```


#### Description
Use this operation to add the transparent DNS forwarder


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[dns\_transparent\_forwarder\_post\_success\_schema](#dns\_transparent\_forwarder\_post\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* dns\_transparent\_forwarder


<a name="dns\_transparent\_forwarder-get"></a>
### Get operation for dns\_transparent\_forwarder
```
GET /dns_transparent_forwarder
```


#### Description
Use this operation to get the transparent DNS forwarders configured


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[dns\_transparent\_forwarder\_response\_schema](#dns\_transparent\_forwarder\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* dns\_transparent\_forwarder


<a name="dns\_transparent\_forwarder-put"></a>
### PUT operation for dns\_transparent\_forwarder
```
PUT /dns_transparent_forwarder
```


#### Description
Use this operation to modify transparent DNS forwarder rule


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[dns\_transparent\_forwarder\_request\_schema](#dns\_transparent\_forwarder\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[dns\_transparent\_forwarder\_put\_success\_schema](#dns\_transparent\_forwarder\_put\_success\_schema)|
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

* dns\_transparent\_forwarder


<a name="dns\_transparent\_forwarder-deletepathparam-delete"></a>
### DELETE operation for dns\_transparent\_forwarder
```
DELETE /dns_transparent_forwarder/{deletePathParam}
```


#### Description
Use this operation to delete transparent transparent DNS forwarder configured


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[dns\_transparent\_forwarder\_delete\_success\_schema](#dns\_transparent\_forwarder\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* dns\_transparent\_forwarder




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="application\_name"></a>
### application\_name
The name of the application used in the transparent forwarder

*Type* : string


<a name="dns\_service\_name"></a>
### dns\_service\_name
The name for the DNS service used in the transparent forwarder

*Type* : string


<a name="dns\_transparent\_forwarder"></a>
### dns\_transparent\_forwarder

|Name|Schema|
|---|---|
|**application\_name**  <br>*optional*|[application\_name](#application\_name)|
|**dns\_service\_name**  <br>*optional*|[dns\_service\_name](#dns\_service\_name)|
|**id**  <br>*optional*|[id](#id)|
|**order**  <br>*optional*|[order](#order)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|


<a name="dns\_transparent\_forwarder\_delete\_success\_schema"></a>
### dns\_transparent\_forwarder\_delete\_success\_schema

|Name|Schema|
|---|---|
|**dns\_transparent\_forwarder**  <br>*optional*|[dns\_transparent\_forwarder](#dns\_transparent\_forwarder\_delete\_success\_schema-dns\_transparent\_forwarder)|

<a name="dns\_transparent\_forwarder\_delete\_success\_schema-dns\_transparent\_forwarder"></a>
**dns\_transparent\_forwarder**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="dns\_transparent\_forwarder\_post\_success\_schema"></a>
### dns\_transparent\_forwarder\_post\_success\_schema

|Name|Schema|
|---|---|
|**dns\_transparent\_forwarder**  <br>*optional*|[dns\_transparent\_forwarder](#dns\_transparent\_forwarder\_post\_success\_schema-dns\_transparent\_forwarder)|

<a name="dns\_transparent\_forwarder\_post\_success\_schema-dns\_transparent\_forwarder"></a>
**dns\_transparent\_forwarder**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="dns\_transparent\_forwarder\_put\_success\_schema"></a>
### dns\_transparent\_forwarder\_put\_success\_schema

|Name|Schema|
|---|---|
|**dns\_transparent\_forwarder**  <br>*optional*|[dns\_transparent\_forwarder](#dns\_transparent\_forwarder\_put\_success\_schema-dns\_transparent\_forwarder)|

<a name="dns\_transparent\_forwarder\_put\_success\_schema-dns\_transparent\_forwarder"></a>
**dns\_transparent\_forwarder**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="dns\_transparent\_forwarder\_request\_schema"></a>
### dns\_transparent\_forwarder\_request\_schema

|Name|Schema|
|---|---|
|**dns\_transparent\_forwarder**  <br>*optional*|[dns\_transparent\_forwarder](#dns\_transparent\_forwarder)|


<a name="dns\_transparent\_forwarder\_response\_schema"></a>
### dns\_transparent\_forwarder\_response\_schema
*Type* : < [dns\_transparent\_forwarder\_response\_schema](#dns\_transparent\_forwarder\_response\_schema-inline) > array

<a name="dns\_transparent\_forwarder\_response\_schema-inline"></a>
**dns\_transparent\_forwarder\_response\_schema**

|Name|Schema|
|---|---|
|**application\_name**  <br>*optional*|[application\_name](#application\_name)|
|**dns\_service\_name**  <br>*optional*|[dns\_service\_name](#dns\_service\_name)|
|**id**  <br>*optional*|[id](#id)|
|**is\_auto**  <br>*optional*|[is\_auto](#is\_auto)|
|**order**  <br>*optional*|[order](#order)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|


<a name="id"></a>
### id
Auto-generated ID to uniquely identify the DNS forwarder

*Type* : integer


<a name="is\_auto"></a>
### is\_auto
To indicate that this is auto-generated

*Type* : boolean


<a name="order"></a>
### order
The tranparent DNS forwarder rule order

*Type* : integer


<a name="package\_name"></a>
### package\_name
Config package name using which the API operation should be performed.

*Type* : string


<a name="site\_name"></a>
### site\_name
Site Name

*Type* : string






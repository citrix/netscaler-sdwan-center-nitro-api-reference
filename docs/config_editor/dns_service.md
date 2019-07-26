# dns\_service


<a name="overview"></a>
## Overview
API to add, delete, get, modify DNS services


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* dns\_service : Operations related to dns\_service 




<a name="paths"></a>
## Paths

<a name="dns\_service-post"></a>
### POST operation for dns\_service
```
POST /dns_service
```


#### Description
Use this operation to add DNS service


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[dns\_service\_post\_success\_schema](#dns\_service\_post\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* dns\_service


<a name="dns\_service-get"></a>
### Get operation for dns\_service
```
GET /dns_service
```


#### Description
Use this operation to get the DNS services configured


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[dns\_service\_response\_schema](#dns\_service\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* dns\_service


<a name="dns\_service-put"></a>
### PUT operation for dns\_service
```
PUT /dns_service
```


#### Description
Use this operation to modify DNS services


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[dns\_service\_request\_schema](#dns\_service\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[dns\_service\_put\_success\_schema](#dns\_service\_put\_success\_schema)|
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

* dns\_service


<a name="dns\_service-deletepathparam-delete"></a>
### DELETE operation for dns\_service
```
DELETE /dns_service/{deletePathParam}
```


#### Description
Use this operation to delete DNS service


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[dns\_service\_delete\_success\_schema](#dns\_service\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* dns\_service




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="dns\_service"></a>
### dns\_service

|Name|Schema|
|---|---|
|**dns\_service\_name**  <br>*optional*|[dns\_service\_name](#dns\_service\_name)|
|**id**  <br>*optional*|[id](#id)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**primary\_dns\_server\_ip**  <br>*optional*|[primary\_dns\_server\_ip](#primary\_dns\_server\_ip)|
|**secondary\_dns\_server\_ip**  <br>*optional*|[secondary\_dns\_server\_ip](#secondary\_dns\_server\_ip)|


<a name="dns\_service\_delete\_success\_schema"></a>
### dns\_service\_delete\_success\_schema

|Name|Schema|
|---|---|
|**dns\_service**  <br>*optional*|[dns\_service](#dns\_service\_delete\_success\_schema-dns\_service)|

<a name="dns\_service\_delete\_success\_schema-dns\_service"></a>
**dns\_service**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="dns\_service\_name"></a>
### dns\_service\_name
The name for the DNS service

*Type* : string


<a name="dns\_service\_post\_success\_schema"></a>
### dns\_service\_post\_success\_schema

|Name|Schema|
|---|---|
|**dns\_service**  <br>*optional*|[dns\_service](#dns\_service\_post\_success\_schema-dns\_service)|

<a name="dns\_service\_post\_success\_schema-dns\_service"></a>
**dns\_service**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="dns\_service\_put\_success\_schema"></a>
### dns\_service\_put\_success\_schema

|Name|Schema|
|---|---|
|**dns\_service**  <br>*optional*|[dns\_service](#dns\_service\_put\_success\_schema-dns\_service)|

<a name="dns\_service\_put\_success\_schema-dns\_service"></a>
**dns\_service**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="dns\_service\_request\_schema"></a>
### dns\_service\_request\_schema

|Name|Schema|
|---|---|
|**dns\_service**  <br>*optional*|[dns\_service](#dns\_service)|


<a name="dns\_service\_response\_schema"></a>
### dns\_service\_response\_schema
*Type* : < [dns\_service\_response\_schema](#dns\_service\_response\_schema-inline) > array

<a name="dns\_service\_response\_schema-inline"></a>
**dns\_service\_response\_schema**

|Name|Schema|
|---|---|
|**dns\_service\_name**  <br>*optional*|[dns\_service\_name](#dns\_service\_name)|
|**id**  <br>*optional*|[id](#id)|
|**is\_auto**  <br>*optional*|[is\_auto](#is\_auto)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**primary\_dns\_server\_ip**  <br>*optional*|[primary\_dns\_server\_ip](#primary\_dns\_server\_ip)|
|**secondary\_dns\_server\_ip**  <br>*optional*|[secondary\_dns\_server\_ip](#secondary\_dns\_server\_ip)|


<a name="id"></a>
### id
Auto-generated ID to uniquely identify the DNS service

*Type* : integer


<a name="is\_auto"></a>
### is\_auto
to indicate that this is auto-generated

*Type* : boolean


<a name="package\_name"></a>
### package\_name
Config package name using which the API operation should be performed.

*Type* : string


<a name="primary\_dns\_server\_ip"></a>
### primary\_dns\_server\_ip
The IP Address of the Primary DNS server

*Type* : string


<a name="secondary\_dns\_server\_ip"></a>
### secondary\_dns\_server\_ip
The IP Address of the secondary DNS server

*Type* : string






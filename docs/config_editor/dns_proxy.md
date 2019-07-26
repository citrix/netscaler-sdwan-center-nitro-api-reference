# dns\_proxy


<a name="overview"></a>
## Overview
API to add, modify, delete, and get configuration for dns proxy


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* dns\_proxy : Operations related to dns\_proxy 




<a name="paths"></a>
## Paths

<a name="dns\_proxy-post"></a>
### POST operation for dns\_proxy
```
POST /dns_proxy
```


#### Description
Use this operation to add the DNS proxy


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[dns\_proxy\_post\_success\_schema](#dns\_proxy\_post\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* dns\_proxy


<a name="dns\_proxy-get"></a>
### Get operation for dns\_proxy
```
GET /dns_proxy
```


#### Description
Use this operation to get the DNS proxy configuration


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[dns\_proxy\_response\_schema](#dns\_proxy\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* dns\_proxy


<a name="dns\_proxy-put"></a>
### PUT operation for dns\_proxy
```
PUT /dns_proxy
```


#### Description
Use this operation to modify the DNS proxy


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[dns\_proxy\_request\_schema](#dns\_proxy\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[dns\_proxy\_put\_success\_schema](#dns\_proxy\_put\_success\_schema)|
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

* dns\_proxy


<a name="dns\_proxy-deletepathparam-delete"></a>
### DELETE operation for dns\_proxy
```
DELETE /dns_proxy/{deletePathParam}
```


#### Description
Use this operation to delete the DNS proxy


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[dns\_proxy\_delete\_success\_schema](#dns\_proxy\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* dns\_proxy




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="default\_dns\_service"></a>
### default\_dns\_service
*Type* : string


<a name="dns\_forwarder"></a>
### dns\_forwarder
The DNS service name

*Type* : < [dns\_forwarder](#dns\_forwarder-inline) > array

<a name="dns\_forwarder-inline"></a>
**dns\_forwarder**

|Name|Description|Schema|
|---|---|---|
|**application\_name**  <br>*optional*|Application Name or Custom domain created|string|
|**dns\_service\_name**  <br>*optional*|The DNS service name|string|
|**id**  <br>*optional*|Auto-generated ID to uniquely identify application object|integer|
|**is\_auto**  <br>*optional*  <br>*read-only*|to indicate that this is auto-generated|boolean|
|**order**  <br>*optional*|The DNS forwarder rule order|integer|


<a name="dns\_proxy"></a>
### dns\_proxy

|Name|Schema|
|---|---|
|**default\_dns\_service**  <br>*optional*|[default\_dns\_service](#default\_dns\_service)|
|**dns\_forwarder**  <br>*optional*|[dns\_forwarder](#dns\_forwarder)|
|**dns\_proxy\_interface**  <br>*optional*|[dns\_proxy\_interface](#dns\_proxy\_interface)|
|**dns\_proxy\_name**  <br>*optional*|[dns\_proxy\_name](#dns\_proxy\_name)|
|**id**  <br>*optional*|[id](#id)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|


<a name="dns\_proxy\_delete\_success\_schema"></a>
### dns\_proxy\_delete\_success\_schema

|Name|Schema|
|---|---|
|**dns\_proxy**  <br>*optional*|[dns\_proxy](#dns\_proxy\_delete\_success\_schema-dns\_proxy)|

<a name="dns\_proxy\_delete\_success\_schema-dns\_proxy"></a>
**dns\_proxy**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="dns\_proxy\_interface"></a>
### dns\_proxy\_interface
The Virtual Interface Name

*Type* : < [dns\_proxy\_interface](#dns\_proxy\_interface-inline) > array

<a name="dns\_proxy\_interface-inline"></a>
**dns\_proxy\_interface**

|Name|Description|Schema|
|---|---|---|
|**dns\_proxy\_interface\_name**  <br>*optional*|The name of the dns proxy virtual interface|string|
|**id**  <br>*optional*|Auto-generated ID to uniquely identify the Virtual interface name|integer|


<a name="dns\_proxy\_name"></a>
### dns\_proxy\_name
The name of the DNS proxy

*Type* : string


<a name="dns\_proxy\_post\_success\_schema"></a>
### dns\_proxy\_post\_success\_schema

|Name|Schema|
|---|---|
|**dns\_proxy**  <br>*optional*|[dns\_proxy](#dns\_proxy\_post\_success\_schema-dns\_proxy)|

<a name="dns\_proxy\_post\_success\_schema-dns\_proxy"></a>
**dns\_proxy**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="dns\_proxy\_put\_success\_schema"></a>
### dns\_proxy\_put\_success\_schema

|Name|Schema|
|---|---|
|**dns\_proxy**  <br>*optional*|[dns\_proxy](#dns\_proxy\_put\_success\_schema-dns\_proxy)|

<a name="dns\_proxy\_put\_success\_schema-dns\_proxy"></a>
**dns\_proxy**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="dns\_proxy\_request\_schema"></a>
### dns\_proxy\_request\_schema

|Name|Schema|
|---|---|
|**dns\_proxy**  <br>*optional*|[dns\_proxy](#dns\_proxy)|


<a name="dns\_proxy\_response\_schema"></a>
### dns\_proxy\_response\_schema
*Type* : < [dns\_proxy\_response\_schema](#dns\_proxy\_response\_schema-inline) > array

<a name="dns\_proxy\_response\_schema-inline"></a>
**dns\_proxy\_response\_schema**

|Name|Schema|
|---|---|
|**default\_dns\_service**  <br>*optional*|[default\_dns\_service](#default\_dns\_service)|
|**dns\_forwarder**  <br>*optional*|[dns\_forwarder](#dns\_forwarder)|
|**dns\_proxy\_interface**  <br>*optional*|[dns\_proxy\_interface](#dns\_proxy\_interface)|
|**dns\_proxy\_name**  <br>*optional*|[dns\_proxy\_name](#dns\_proxy\_name)|
|**id**  <br>*optional*|[id](#id)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|


<a name="id"></a>
### id
Object id for DNS proxy

*Type* : integer


<a name="package\_name"></a>
### package\_name
Package name to be used for the API operations

*Type* : string


<a name="site\_name"></a>
### site\_name
Site Name to add DNS proxy

*Type* : string






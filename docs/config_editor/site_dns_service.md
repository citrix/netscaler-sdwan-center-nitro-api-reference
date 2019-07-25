# site\_dns\_service


<a name="overview"></a>
## Overview
API to add, delete, get, modify DNS services at site level


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* site\_dns\_service : Operations related to site\_dns\_service 




<a name="paths"></a>
## Paths

<a name="site\_dns\_service-post"></a>
### POST operation for site\_dns\_service
```
POST /site_dns_service
```


#### Description
Use this operation to add DNS service


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[site\_dns\_service\_request\_schema](#site\_dns\_service\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[site\_dns\_service\_post\_success\_schema](#site\_dns\_service\_post\_success\_schema)|
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

* site\_dns\_service


<a name="site\_dns\_service-get"></a>
### Get operation for site\_dns\_service
```
GET /site_dns_service
```


#### Description
Use this operation to get the DNS services configured


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[site\_dns\_service\_response\_schema](#site\_dns\_service\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* site\_dns\_service


<a name="site\_dns\_service-put"></a>
### PUT operation for site\_dns\_service
```
PUT /site_dns_service
```


#### Description
Use this operation to modify DNS services


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[site\_dns\_service\_put\_success\_schema](#site\_dns\_service\_put\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* site\_dns\_service


<a name="site\_dns\_service-deletepathparam-delete"></a>
### DELETE operation for site\_dns\_service
```
DELETE /site_dns_service/{deletePathParam}
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
|**200**|Resource delete added|[site\_dns\_service\_delete\_success\_schema](#site\_dns\_service\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* site\_dns\_service




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="dns\_service\_name"></a>
### dns\_service\_name
The name for the DNS service

*Type* : string


<a name="id"></a>
### id
Auto-generated ID to uniquely identify the DNS service

*Type* : integer


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


<a name="site\_dns\_service"></a>
### site\_dns\_service

|Name|Schema|
|---|---|
|**dns\_service\_name**  <br>*optional*|[dns\_service\_name](#dns\_service\_name)|
|**id**  <br>*optional*|[id](#id)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**primary\_dns\_server\_ip**  <br>*optional*|[primary\_dns\_server\_ip](#primary\_dns\_server\_ip)|
|**secondary\_dns\_server\_ip**  <br>*optional*|[secondary\_dns\_server\_ip](#secondary\_dns\_server\_ip)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|


<a name="site\_dns\_service\_delete\_success\_schema"></a>
### site\_dns\_service\_delete\_success\_schema

|Name|Schema|
|---|---|
|**site\_dns\_service**  <br>*optional*|[site\_dns\_service](#site\_dns\_service\_delete\_success\_schema-site\_dns\_service)|

<a name="site\_dns\_service\_delete\_success\_schema-site\_dns\_service"></a>
**site\_dns\_service**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="site\_dns\_service\_post\_success\_schema"></a>
### site\_dns\_service\_post\_success\_schema

|Name|Schema|
|---|---|
|**site\_dns\_service**  <br>*optional*|[site\_dns\_service](#site\_dns\_service\_post\_success\_schema-site\_dns\_service)|

<a name="site\_dns\_service\_post\_success\_schema-site\_dns\_service"></a>
**site\_dns\_service**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="site\_dns\_service\_put\_success\_schema"></a>
### site\_dns\_service\_put\_success\_schema

|Name|Schema|
|---|---|
|**site\_dns\_service**  <br>*optional*|[site\_dns\_service](#site\_dns\_service\_put\_success\_schema-site\_dns\_service)|

<a name="site\_dns\_service\_put\_success\_schema-site\_dns\_service"></a>
**site\_dns\_service**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="site\_dns\_service\_request\_schema"></a>
### site\_dns\_service\_request\_schema

|Name|Schema|
|---|---|
|**site\_dns\_service**  <br>*optional*|[site\_dns\_service](#site\_dns\_service)|


<a name="site\_dns\_service\_response\_schema"></a>
### site\_dns\_service\_response\_schema
*Type* : < [site\_dns\_service\_response\_schema](#site\_dns\_service\_response\_schema-inline) > array

<a name="site\_dns\_service\_response\_schema-inline"></a>
**site\_dns\_service\_response\_schema**

|Name|Schema|
|---|---|
|**dns\_service\_name**  <br>*optional*|[dns\_service\_name](#dns\_service\_name)|
|**id**  <br>*optional*|[id](#id)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**primary\_dns\_server\_ip**  <br>*optional*|[primary\_dns\_server\_ip](#primary\_dns\_server\_ip)|
|**secondary\_dns\_server\_ip**  <br>*optional*|[secondary\_dns\_server\_ip](#secondary\_dns\_server\_ip)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|


<a name="site\_name"></a>
### site\_name
Site Name

*Type* : string






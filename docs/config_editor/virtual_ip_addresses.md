# virtual\_ip\_addresses


<a name="overview"></a>
## Overview
API to add, modify, delete, and get Virtual IP Address


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* virtual\_ip\_addresses : Operations related to virtual\_ip\_addresses 




<a name="paths"></a>
## Paths

<a name="virtual\_ip\_addresses-post"></a>
### POST operation for virtual\_ip\_addresses
```
POST /virtual_ip_addresses
```


#### Description
Use this operation to add a Virtual IP address


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[virtual\_ip\_addresses\_request\_schema](#virtual\_ip\_addresses\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[virtual\_ip\_addresses\_post\_success\_schema](#virtual\_ip\_addresses\_post\_success\_schema)|
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

* virtual\_ip\_addresses


<a name="virtual\_ip\_addresses-get"></a>
### Get operation for virtual\_ip\_addresses
```
GET /virtual_ip_addresses
```


#### Description
Use this operation to get the list of Virtual IP addresses


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[virtual\_ip\_addresses\_response\_schema](#virtual\_ip\_addresses\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* virtual\_ip\_addresses


<a name="virtual\_ip\_addresses-put"></a>
### PUT operation for virtual\_ip\_addresses
```
PUT /virtual_ip_addresses
```


#### Description
Use this operation to modify a Virtual IP address


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[virtual\_ip\_addresses\_put\_success\_schema](#virtual\_ip\_addresses\_put\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* virtual\_ip\_addresses


<a name="virtual\_ip\_addresses-deletepathparam-delete"></a>
### DELETE operation for virtual\_ip\_addresses
```
DELETE /virtual_ip_addresses/{deletePathParam}
```


#### Description
Use this operation to delete a Virtual IP address


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[virtual\_ip\_addresses\_delete\_success\_schema](#virtual\_ip\_addresses\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* virtual\_ip\_addresses




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
Auto-generated ID. Use this ID to modify or delete a Virtual IP address

*Type* : integer


<a name="ip\_address"></a>
### ip\_address
IP Address with prefix

*Type* : string


<a name="is\_auto"></a>
### is\_auto
Tells that this Virtual IP address is auto-generated

*Type* : boolean


<a name="is\_identity"></a>
### is\_identity
If enabled, the Virtual IP Address will be used for IP services

*Type* : boolean


<a name="is\_private"></a>
### is\_private
If enabled, the Virtual IP Address will only be routable on the local Appliance

*Type* : boolean


<a name="package\_name"></a>
### package\_name
Config package name using which the virtual\_ip\_addresses API operation should be performed.

*Type* : string


<a name="site\_name"></a>
### site\_name
Site Name

*Type* : string


<a name="virtual\_interface\_name"></a>
### virtual\_interface\_name
Enter one of the associated Virtual Interfaces

*Type* : string


<a name="virtual\_ip\_addresses"></a>
### virtual\_ip\_addresses

|Name|Schema|
|---|---|
|**id**  <br>*optional*|[id](#id)|
|**ip\_address**  <br>*optional*|[ip\_address](#ip\_address)|
|**is\_auto**  <br>*optional*|[is\_auto](#is\_auto)|
|**is\_identity**  <br>*optional*|[is\_identity](#is\_identity)|
|**is\_private**  <br>*optional*|[is\_private](#is\_private)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**virtual\_interface\_name**  <br>*optional*|[virtual\_interface\_name](#virtual\_interface\_name)|


<a name="virtual\_ip\_addresses\_delete\_success\_schema"></a>
### virtual\_ip\_addresses\_delete\_success\_schema

|Name|Schema|
|---|---|
|**virtual\_ip\_addresses**  <br>*optional*|[virtual\_ip\_addresses](#virtual\_ip\_addresses\_delete\_success\_schema-virtual\_ip\_addresses)|

<a name="virtual\_ip\_addresses\_delete\_success\_schema-virtual\_ip\_addresses"></a>
**virtual\_ip\_addresses**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="virtual\_ip\_addresses\_post\_success\_schema"></a>
### virtual\_ip\_addresses\_post\_success\_schema

|Name|Schema|
|---|---|
|**virtual\_ip\_addresses**  <br>*optional*|[virtual\_ip\_addresses](#virtual\_ip\_addresses\_post\_success\_schema-virtual\_ip\_addresses)|

<a name="virtual\_ip\_addresses\_post\_success\_schema-virtual\_ip\_addresses"></a>
**virtual\_ip\_addresses**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="virtual\_ip\_addresses\_put\_success\_schema"></a>
### virtual\_ip\_addresses\_put\_success\_schema

|Name|Schema|
|---|---|
|**virtual\_ip\_addresses**  <br>*optional*|[virtual\_ip\_addresses](#virtual\_ip\_addresses\_put\_success\_schema-virtual\_ip\_addresses)|

<a name="virtual\_ip\_addresses\_put\_success\_schema-virtual\_ip\_addresses"></a>
**virtual\_ip\_addresses**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="virtual\_ip\_addresses\_request\_schema"></a>
### virtual\_ip\_addresses\_request\_schema

|Name|Schema|
|---|---|
|**virtual\_ip\_addresses**  <br>*optional*|[virtual\_ip\_addresses](#virtual\_ip\_addresses)|


<a name="virtual\_ip\_addresses\_response\_schema"></a>
### virtual\_ip\_addresses\_response\_schema
*Type* : < [virtual\_ip\_addresses\_response\_schema](#virtual\_ip\_addresses\_response\_schema-inline) > array

<a name="virtual\_ip\_addresses\_response\_schema-inline"></a>
**virtual\_ip\_addresses\_response\_schema**

|Name|Schema|
|---|---|
|**id**  <br>*optional*|[id](#id)|
|**ip\_address**  <br>*optional*|[ip\_address](#ip\_address)|
|**is\_auto**  <br>*optional*|[is\_auto](#is\_auto)|
|**is\_identity**  <br>*optional*|[is\_identity](#is\_identity)|
|**is\_private**  <br>*optional*|[is\_private](#is\_private)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**virtual\_interface\_name**  <br>*optional*|[virtual\_interface\_name](#virtual\_interface\_name)|






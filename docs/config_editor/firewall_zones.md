# firewall\_zones


<a name="overview"></a>
## Overview
API to add, delete, get, modify firewall zones


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* firewall\_zones : Operations related to firewall\_zones 




<a name="paths"></a>
## Paths

<a name="firewall\_zones-post"></a>
### POST operation for firewall\_zones
```
POST /firewall_zones
```


#### Description
Use this operation to add firewall zones


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[firewall\_zones\_request\_schema](#firewall\_zones\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[firewall\_zones\_post\_success\_schema](#firewall\_zones\_post\_success\_schema)|
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

* firewall\_zones


<a name="firewall\_zones-get"></a>
### Get operation for firewall\_zones
```
GET /firewall_zones
```


#### Description
Use this operation to get the firewall zones


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[firewall\_zones\_response\_schema](#firewall\_zones\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* firewall\_zones


<a name="firewall\_zones-put"></a>
### PUT operation for firewall\_zones
```
PUT /firewall_zones
```


#### Description
Use this operation to modify firewall zones


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[firewall\_zones\_put\_success\_schema](#firewall\_zones\_put\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* firewall\_zones


<a name="firewall\_zones-deletepathparam-delete"></a>
### DELETE operation for firewall\_zones
```
DELETE /firewall_zones/{deletePathParam}
```


#### Description
Use this operation to delete firewall zones


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[firewall\_zones\_delete\_success\_schema](#firewall\_zones\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* firewall\_zones




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="firewall\_zones"></a>
### firewall\_zones

|Name|Schema|
|---|---|
|**id**  <br>*optional*|[id](#id)|
|**name**  <br>*optional*|[name](#name)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|


<a name="firewall\_zones\_delete\_success\_schema"></a>
### firewall\_zones\_delete\_success\_schema

|Name|Schema|
|---|---|
|**firewall\_zones**  <br>*optional*|[firewall\_zones](#firewall\_zones\_delete\_success\_schema-firewall\_zones)|

<a name="firewall\_zones\_delete\_success\_schema-firewall\_zones"></a>
**firewall\_zones**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="firewall\_zones\_post\_success\_schema"></a>
### firewall\_zones\_post\_success\_schema

|Name|Schema|
|---|---|
|**firewall\_zones**  <br>*optional*|[firewall\_zones](#firewall\_zones\_post\_success\_schema-firewall\_zones)|

<a name="firewall\_zones\_post\_success\_schema-firewall\_zones"></a>
**firewall\_zones**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="firewall\_zones\_put\_success\_schema"></a>
### firewall\_zones\_put\_success\_schema

|Name|Schema|
|---|---|
|**firewall\_zones**  <br>*optional*|[firewall\_zones](#firewall\_zones\_put\_success\_schema-firewall\_zones)|

<a name="firewall\_zones\_put\_success\_schema-firewall\_zones"></a>
**firewall\_zones**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="firewall\_zones\_request\_schema"></a>
### firewall\_zones\_request\_schema

|Name|Schema|
|---|---|
|**firewall\_zones**  <br>*optional*|[firewall\_zones](#firewall\_zones)|


<a name="firewall\_zones\_response\_schema"></a>
### firewall\_zones\_response\_schema
*Type* : < [firewall\_zones\_response\_schema](#firewall\_zones\_response\_schema-inline) > array

<a name="firewall\_zones\_response\_schema-inline"></a>
**firewall\_zones\_response\_schema**

|Name|Schema|
|---|---|
|**id**  <br>*optional*|[id](#id)|
|**name**  <br>*optional*|[name](#name)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|


<a name="id"></a>
### id
Auto-generated ID to uniquely identify the firewall zone

*Type* : integer


<a name="name"></a>
### name
The name for the firewall zone

*Type* : string


<a name="package\_name"></a>
### package\_name
Config package name using which the API operation should be performed.

*Type* : string






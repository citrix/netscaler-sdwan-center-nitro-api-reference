# service\_provider


<a name="overview"></a>
## Overview
API to add, delete, get, modify service providers


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* service\_provider : Operations related to service\_provider 




<a name="paths"></a>
## Paths

<a name="service\_provider-post"></a>
### POST operation for service\_provider
```
POST /service_provider
```


#### Description
Use this operation to add service providers


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[service\_provider\_post\_success\_schema](#service\_provider\_post\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* service\_provider


<a name="service\_provider-get"></a>
### Get operation for service\_provider
```
GET /service_provider
```


#### Description
Use this operation to get the service providers


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[service\_provider\_response\_schema](#service\_provider\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* service\_provider


<a name="service\_provider-put"></a>
### PUT operation for service\_provider
```
PUT /service_provider
```


#### Description
Use this operation to modify service providers


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[service\_provider\_request\_schema](#service\_provider\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[service\_provider\_put\_success\_schema](#service\_provider\_put\_success\_schema)|
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

* service\_provider


<a name="service\_provider-deletepathparam-delete"></a>
### DELETE operation for service\_provider
```
DELETE /service_provider/{deletePathParam}
```


#### Description
Use this operation to delete service providers


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[service\_provider\_delete\_success\_schema](#service\_provider\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* service\_provider




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
Auto-generated ID to uniquely identify service providers

*Type* : integer


<a name="name"></a>
### name
The name for the service provider

*Type* : string


<a name="package\_name"></a>
### package\_name
Config package name using which the API operation should be performed.

*Type* : string


<a name="service\_provider"></a>
### service\_provider

|Name|Schema|
|---|---|
|**id**  <br>*optional*|[id](#id)|
|**name**  <br>*optional*|[name](#name)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**templates**  <br>*optional*|[templates](#templates)|


<a name="service\_provider\_delete\_success\_schema"></a>
### service\_provider\_delete\_success\_schema

|Name|Schema|
|---|---|
|**service\_provider**  <br>*optional*|[service\_provider](#service\_provider\_delete\_success\_schema-service\_provider)|

<a name="service\_provider\_delete\_success\_schema-service\_provider"></a>
**service\_provider**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="service\_provider\_post\_success\_schema"></a>
### service\_provider\_post\_success\_schema

|Name|Schema|
|---|---|
|**service\_provider**  <br>*optional*|[service\_provider](#service\_provider\_post\_success\_schema-service\_provider)|

<a name="service\_provider\_post\_success\_schema-service\_provider"></a>
**service\_provider**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="service\_provider\_put\_success\_schema"></a>
### service\_provider\_put\_success\_schema

|Name|Schema|
|---|---|
|**service\_provider**  <br>*optional*|[service\_provider](#service\_provider\_put\_success\_schema-service\_provider)|

<a name="service\_provider\_put\_success\_schema-service\_provider"></a>
**service\_provider**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="service\_provider\_request\_schema"></a>
### service\_provider\_request\_schema

|Name|Schema|
|---|---|
|**service\_provider**  <br>*optional*|[service\_provider](#service\_provider)|


<a name="service\_provider\_response\_schema"></a>
### service\_provider\_response\_schema
*Type* : < [service\_provider\_response\_schema](#service\_provider\_response\_schema-inline) > array

<a name="service\_provider\_response\_schema-inline"></a>
**service\_provider\_response\_schema**

|Name|Schema|
|---|---|
|**id**  <br>*optional*|[id](#id)|
|**name**  <br>*optional*|[name](#name)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**templates**  <br>*optional*|[templates](#templates)|


<a name="templates"></a>
### templates
Templates for service providers

*Type* : < [templates](#templates-inline) > array

<a name="templates-inline"></a>
**templates**

|Name|Description|Schema|
|---|---|---|
|**id**  <br>*optional*|Auto-generated ID to uniquely identify the template|integer|
|**mpls\_queue\_template**  <br>*optional*|Templates for mpls queue|< [mpls\_queue\_template](#templates-mpls\_queue\_template) > array|
|**name**  <br>*optional*|Template Name|string|
|**properties**  <br>*optional*|Properties for the templates of mpls queue|[properties](#templates-properties)|

<a name="templates-mpls\_queue\_template"></a>
**mpls\_queue\_template**

|Name|Description|Schema|
|---|---|---|
|**dscp\_tag**  <br>*optional*|The DSCP Tag of the MPLS Queue|enum (any, af11, af12, af13, af21, af22, af23, af31, af32, af33, af41, af42, af43, cs1, cs2, cs3, cs4, cs5, cs6, cs7, default, ef)|
|**id**  <br>*optional*|Auto-generated ID to uniquely identify the MPLS template|integer|
|**lan\_2\_wan\_permitted\_rate**  <br>*optional*|The available or allowed rate, in kbps, for LAN to WAN traffic|integer|
|**wan\_2\_lan\_permitted\_rate**  <br>*optional*|The available or allowed rate, in kbps, for WAN to LAN traffic|integer|

<a name="templates-properties"></a>
**properties**

|Name|Description|Schema|
|---|---|---|
|**autopath\_group**  <br>*optional*|Autopath Group|string|
|**lan\_2\_wan\_auto\_learn**  <br>*optional*|LAN to WAN Auto Learn|boolean|
|**lan\_2\_wan\_physical\_rate**  <br>*optional*|LAN to WAN Physical Rate|integer|
|**link\_type**  <br>*optional*|Link Type|enum (internet, private\_link, mpls)|
|**wan\_2\_lan\_auto\_learn**  <br>*optional*|WAN to LAN Auto Learn|boolean|
|**wan\_2\_lan\_physical\_rate**  <br>*optional*|WAN to LAN Physical Rate|integer|






# ospf\_area


<a name="overview"></a>
## Overview
API to add, delete, get, modify OSPF areas.


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* ospf\_area : Operations related to ospf\_area 




<a name="paths"></a>
## Paths

<a name="ospf\_area-post"></a>
### POST operation for ospf\_area
```
POST /ospf_area
```


#### Description
Use this operation to add OSPF area


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[ospf\_area\_post\_success\_schema](#ospf\_area\_post\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* ospf\_area


<a name="ospf\_area-get"></a>
### Get operation for ospf\_area
```
GET /ospf_area
```


#### Description
Use this operation to get OSPF areas


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[ospf\_area\_response\_schema](#ospf\_area\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* ospf\_area


<a name="ospf\_area-put"></a>
### PUT operation for ospf\_area
```
PUT /ospf_area
```


#### Description
Use this operation to modify OSPF area


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[ospf\_area\_request\_schema](#ospf\_area\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[ospf\_area\_put\_success\_schema](#ospf\_area\_put\_success\_schema)|
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

* ospf\_area


<a name="ospf\_area-deletepathparam-delete"></a>
### DELETE operation for ospf\_area
```
DELETE /ospf_area/{deletePathParam}
```


#### Description
Use this operation to delete OSPF area


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[ospf\_area\_delete\_success\_schema](#ospf\_area\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* ospf\_area




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
Auto-generated ID to uniquely identify OSPF area

*Type* : integer


<a name="ospf\_area"></a>
### ospf\_area

|Name|Schema|
|---|---|
|**id**  <br>*optional*|[id](#id)|
|**ospf\_area\_properties**  <br>*optional*|[ospf\_area\_properties](#ospf\_area\_properties)|
|**ospf\_area\_virtual\_interface**  <br>*optional*|[ospf\_area\_virtual\_interface](#ospf\_area\_virtual\_interface)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|


<a name="ospf\_area\_delete\_success\_schema"></a>
### ospf\_area\_delete\_success\_schema

|Name|Schema|
|---|---|
|**ospf\_area**  <br>*optional*|[ospf\_area](#ospf\_area\_delete\_success\_schema-ospf\_area)|

<a name="ospf\_area\_delete\_success\_schema-ospf\_area"></a>
**ospf\_area**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="ospf\_area\_post\_success\_schema"></a>
### ospf\_area\_post\_success\_schema

|Name|Schema|
|---|---|
|**ospf\_area**  <br>*optional*|[ospf\_area](#ospf\_area\_post\_success\_schema-ospf\_area)|

<a name="ospf\_area\_post\_success\_schema-ospf\_area"></a>
**ospf\_area**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="ospf\_area\_properties"></a>
### ospf\_area\_properties
OSPF area properties

*Type* : < [ospf\_area\_properties](#ospf\_area\_properties-inline) > array

<a name="ospf\_area\_properties-inline"></a>
**ospf\_area\_properties**

|Name|Description|Schema|
|---|---|---|
|**area\_id**  <br>*optional*|The IP Address or Area ID(INT) to identify the area that OSPF will learn routes from and advertise routes to|string|
|**stub\_area**  <br>*optional*|If enabled, the Area will not receive route advertisements from outside of the designated Autonomous System|boolean|


<a name="ospf\_area\_put\_success\_schema"></a>
### ospf\_area\_put\_success\_schema

|Name|Schema|
|---|---|
|**ospf\_area**  <br>*optional*|[ospf\_area](#ospf\_area\_put\_success\_schema-ospf\_area)|

<a name="ospf\_area\_put\_success\_schema-ospf\_area"></a>
**ospf\_area**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="ospf\_area\_request\_schema"></a>
### ospf\_area\_request\_schema

|Name|Schema|
|---|---|
|**ospf\_area**  <br>*optional*|[ospf\_area](#ospf\_area)|


<a name="ospf\_area\_response\_schema"></a>
### ospf\_area\_response\_schema
*Type* : < [ospf\_area\_response\_schema](#ospf\_area\_response\_schema-inline) > array

<a name="ospf\_area\_response\_schema-inline"></a>
**ospf\_area\_response\_schema**

|Name|Schema|
|---|---|
|**id**  <br>*optional*|[id](#id)|
|**ospf\_area\_properties**  <br>*optional*|[ospf\_area\_properties](#ospf\_area\_properties)|
|**ospf\_area\_virtual\_interface**  <br>*optional*|[ospf\_area\_virtual\_interface](#ospf\_area\_virtual\_interface)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|


<a name="ospf\_area\_virtual\_interface"></a>
### ospf\_area\_virtual\_interface
OSPF area virtual interface

*Type* : < [ospf\_area\_virtual\_interface](#ospf\_area\_virtual\_interface-inline) > array

<a name="ospf\_area\_virtual\_interface-inline"></a>
**ospf\_area\_virtual\_interface**

|Name|Description|Schema|
|---|---|---|
|**authentication\_type**  <br>*optional*|The authentication type from 'none', 'plain\_text' or 'md5' can used for authentication|enum (none, plain\_text, md5)|
|**dead\_interval**  <br>*optional*|The amount of time to wait to recieve a Hello protocol packet before marking a router as dead|integer|
|**hello\_interval**  <br>*optional*|The amount of time to wait between sending Hello protocol packets to directly connected neighbors|integer|
|**id**  <br>*optional*|Auto-generated ID to uniquely identify the OSPF area virtual interface|integer|
|**interface\_cost**  <br>*optional*|The base cost for routes learned on the interface|integer|
|**network\_type**  <br>*optional*|The type of network from 'auto', 'pointtopoint', 'broadcast' can be used to determine connection of OSPF interface|enum (auto, pointtopoint, broadcast)|
|**password**  <br>*optional*|The password used to encrypt and decrypt OSPF packets when password\_type is chosen from plain\_text or md5|string|
|**routing\_domain**  <br>*optional*|Choose one of the configured Routing Domains, Leave blank or any for Any Routing Domain|string|
|**virtual\_interface\_name**  <br>*optional*|The Virtual Interface Name of which source IP address is used to send OSPF messages for this interface|string|


<a name="package\_name"></a>
### package\_name
Config package name using which the site API operation should be performed.

*Type* : string


<a name="site\_name"></a>
### site\_name
Site Name

*Type* : string






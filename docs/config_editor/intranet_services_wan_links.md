# intranet\_services\_wan\_links


<a name="overview"></a>
## Overview
API to get, modify wan links for Intranet Services


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* intranet\_services\_wan\_links : Operations related to intranet\_services\_wan\_links 




<a name="paths"></a>
## Paths

<a name="intranet\_services\_wan\_links-post"></a>
### POST operation for intranet\_services\_wan\_links
```
POST /intranet_services_wan_links
```


#### Description
Use this operation to enable the intranet service for a particular wan link


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[intranet\_services\_wan\_links\_post\_success\_schema](#intranet\_services\_wan\_links\_post\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* intranet\_services\_wan\_links


<a name="intranet\_services\_wan\_links-get"></a>
### Get operation for intranet\_services\_wan\_links
```
GET /intranet_services_wan_links
```


#### Description
Use this operation to get the wan links for Intranet Services. Only enabled wan links are listed


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[intranet\_services\_wan\_links\_response\_schema](#intranet\_services\_wan\_links\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* intranet\_services\_wan\_links


<a name="intranet\_services\_wan\_links-put"></a>
### PUT operation for intranet\_services\_wan\_links
```
PUT /intranet_services_wan_links
```


#### Description
Use this operation to modify wan links for Intranet Services. This operation can only be used when the wan link is enabled for intranet service


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[intranet\_services\_wan\_links\_request\_schema](#intranet\_services\_wan\_links\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[intranet\_services\_wan\_links\_put\_success\_schema](#intranet\_services\_wan\_links\_put\_success\_schema)|
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

* intranet\_services\_wan\_links


<a name="intranet\_services\_wan\_links-deletepathparam-delete"></a>
### DELETE operation for intranet\_services\_wan\_links
```
DELETE /intranet_services_wan_links/{deletePathParam}
```


#### Description
Use this operation to disable the intranet service for a particular wan link


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[intranet\_services\_wan\_links\_delete\_success\_schema](#intranet\_services\_wan\_links\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* intranet\_services\_wan\_links




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="access\_interface\_failover"></a>
### access\_interface\_failover
If enabled, internet/intranet packets with mismatched vlan can still use the service.

*Type* : boolean


<a name="id"></a>
### id
Auto-generated ID to uniquely identify the WAN Link

*Type* : integer


<a name="intranet\_service\_name"></a>
### intranet\_service\_name
Intranet Service Name

*Type* : string


<a name="intranet\_services\_wan\_links"></a>
### intranet\_services\_wan\_links

|Name|Schema|
|---|---|
|**access\_interface\_failover**  <br>*optional*|[access\_interface\_failover](#access\_interface\_failover)|
|**id**  <br>*optional*|[id](#id)|
|**intranet\_service\_name**  <br>*optional*|[intranet\_service\_name](#intranet\_service\_name)|
|**lan\_to\_wan\_max\_delay**  <br>*optional*|[lan\_to\_wan\_max\_delay](#lan\_to\_wan\_max\_delay)|
|**lan\_to\_wan\_tagging**  <br>*optional*|[lan\_to\_wan\_tagging](#lan\_to\_wan\_tagging)|
|**mode**  <br>*optional*|[mode](#mode)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**tunnel\_header\_size**  <br>*optional*|[tunnel\_header\_size](#tunnel\_header\_size)|
|**wan\_link\_name**  <br>*optional*|[wan\_link\_name](#wan\_link\_name)|
|**wan\_to\_lan\_grooming**  <br>*optional*|[wan\_to\_lan\_grooming](#wan\_to\_lan\_grooming)|
|**wan\_to\_lan\_matching**  <br>*optional*|[wan\_to\_lan\_matching](#wan\_to\_lan\_matching)|
|**wan\_to\_lan\_tagging**  <br>*optional*|[wan\_to\_lan\_tagging](#wan\_to\_lan\_tagging)|


<a name="intranet\_services\_wan\_links\_delete\_success\_schema"></a>
### intranet\_services\_wan\_links\_delete\_success\_schema

|Name|Schema|
|---|---|
|**intranet\_services\_wan\_links**  <br>*optional*|[intranet\_services\_wan\_links](#intranet\_services\_wan\_links\_delete\_success\_schema-intranet\_services\_wan\_links)|

<a name="intranet\_services\_wan\_links\_delete\_success\_schema-intranet\_services\_wan\_links"></a>
**intranet\_services\_wan\_links**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="intranet\_services\_wan\_links\_post\_success\_schema"></a>
### intranet\_services\_wan\_links\_post\_success\_schema

|Name|Schema|
|---|---|
|**intranet\_services\_wan\_links**  <br>*optional*|[intranet\_services\_wan\_links](#intranet\_services\_wan\_links\_post\_success\_schema-intranet\_services\_wan\_links)|

<a name="intranet\_services\_wan\_links\_post\_success\_schema-intranet\_services\_wan\_links"></a>
**intranet\_services\_wan\_links**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="intranet\_services\_wan\_links\_put\_success\_schema"></a>
### intranet\_services\_wan\_links\_put\_success\_schema

|Name|Schema|
|---|---|
|**intranet\_services\_wan\_links**  <br>*optional*|[intranet\_services\_wan\_links](#intranet\_services\_wan\_links\_put\_success\_schema-intranet\_services\_wan\_links)|

<a name="intranet\_services\_wan\_links\_put\_success\_schema-intranet\_services\_wan\_links"></a>
**intranet\_services\_wan\_links**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="intranet\_services\_wan\_links\_request\_schema"></a>
### intranet\_services\_wan\_links\_request\_schema

|Name|Schema|
|---|---|
|**intranet\_services\_wan\_links**  <br>*optional*|[intranet\_services\_wan\_links](#intranet\_services\_wan\_links)|


<a name="intranet\_services\_wan\_links\_response\_schema"></a>
### intranet\_services\_wan\_links\_response\_schema
*Type* : < [intranet\_services\_wan\_links\_response\_schema](#intranet\_services\_wan\_links\_response\_schema-inline) > array

<a name="intranet\_services\_wan\_links\_response\_schema-inline"></a>
**intranet\_services\_wan\_links\_response\_schema**

|Name|Schema|
|---|---|
|**access\_interface\_failover**  <br>*optional*|[access\_interface\_failover](#access\_interface\_failover)|
|**id**  <br>*optional*|[id](#id)|
|**intranet\_service\_name**  <br>*optional*|[intranet\_service\_name](#intranet\_service\_name)|
|**lan\_to\_wan\_max\_delay**  <br>*optional*|[lan\_to\_wan\_max\_delay](#lan\_to\_wan\_max\_delay)|
|**lan\_to\_wan\_tagging**  <br>*optional*|[lan\_to\_wan\_tagging](#lan\_to\_wan\_tagging)|
|**mode**  <br>*optional*|[mode](#mode)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**tunnel\_header\_size**  <br>*optional*|[tunnel\_header\_size](#tunnel\_header\_size)|
|**wan\_link\_name**  <br>*optional*|[wan\_link\_name](#wan\_link\_name)|
|**wan\_to\_lan\_grooming**  <br>*optional*|[wan\_to\_lan\_grooming](#wan\_to\_lan\_grooming)|
|**wan\_to\_lan\_matching**  <br>*optional*|[wan\_to\_lan\_matching](#wan\_to\_lan\_matching)|
|**wan\_to\_lan\_tagging**  <br>*optional*|[wan\_to\_lan\_tagging](#wan\_to\_lan\_tagging)|


<a name="lan\_to\_wan\_max\_delay"></a>
### lan\_to\_wan\_max\_delay
The maximum time, in milliseconds, to buffer packets when the WAN Link's bandwidth is exceeded

*Type* : integer


<a name="lan\_to\_wan\_tagging"></a>
### lan\_to\_wan\_tagging
The DSCP tag to apply to LAN to WAN packets on the Service

*Type* : enum (any, default, af11, af12, af13, af21, af22, af23, af31, af32, af33, af41, af42, af43, cs1, cs2, cs3, cs4, cs5, cs6, cs7, ef)


<a name="mode"></a>
### mode
The Service's mode for traffic redundancy or load balancing

*Type* : enum (primary, secondary, auto)


<a name="package\_name"></a>
### package\_name
Config package name using which the site API operation should be performed.

*Type* : string


<a name="site\_name"></a>
### site\_name
Site Name

*Type* : string


<a name="tunnel\_header\_size"></a>
### tunnel\_header\_size
The size, in bytes, of the tunnel header, if applicable

*Type* : integer


<a name="wan\_link\_name"></a>
### wan\_link\_name
The WAN Link name

*Type* : string


<a name="wan\_to\_lan\_grooming"></a>
### wan\_to\_lan\_grooming
If enabled, packets will be randomly discarded to prevent WAN to LAN traffic from exceeding the Service's provisioned bandwidth

*Type* : boolean


<a name="wan\_to\_lan\_matching"></a>
### wan\_to\_lan\_matching
WAN to LAN packets matching this tag will be assigned to the Service

*Type* : enum (any, default, af11, af12, af13, af21, af22, af23, af31, af32, af33, af41, af42, af43, cs1, cs2, cs3, cs4, cs5, cs6, cs7, ef)


<a name="wan\_to\_lan\_tagging"></a>
### wan\_to\_lan\_tagging
The DSCP tag to apply to WAN to LAN packets on the Service

*Type* : enum (any, default, af11, af12, af13, af21, af22, af23, af31, af32, af33, af41, af42, af43, cs1, cs2, cs3, cs4, cs5, cs6, cs7, ef)






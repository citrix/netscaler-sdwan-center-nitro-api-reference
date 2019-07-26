# bgp\_policy


<a name="overview"></a>
## Overview
API to add, delete, get, modify BGP policies- a collection of BGP attributes which can be used to set or modify route attributes for each BGP Peer.


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* bgp\_policy : Operations related to bgp\_policy 




<a name="paths"></a>
## Paths

<a name="bgp\_policy-post"></a>
### POST operation for bgp\_policy
```
POST /bgp_policy
```


#### Description
Use this operation to add BGP policies


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[bgp\_policy\_request\_schema](#bgp\_policy\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[bgp\_policy\_post\_success\_schema](#bgp\_policy\_post\_success\_schema)|
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

* bgp\_policy


<a name="bgp\_policy-get"></a>
### Get operation for bgp\_policy
```
GET /bgp_policy
```


#### Description
Use this operation to get the BGP policies


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[bgp\_policy\_response\_schema](#bgp\_policy\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* bgp\_policy


<a name="bgp\_policy-put"></a>
### PUT operation for bgp\_policy
```
PUT /bgp_policy
```


#### Description
Use this operation to modify BGP policies


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[bgp\_policy\_put\_success\_schema](#bgp\_policy\_put\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* bgp\_policy


<a name="bgp\_policy-deletepathparam-delete"></a>
### DELETE operation for bgp\_policy
```
DELETE /bgp_policy/{deletePathParam}
```


#### Description
Use this operation to delete BGP policies


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[bgp\_policy\_delete\_success\_schema](#bgp\_policy\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* bgp\_policy




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="bgp\_policy"></a>
### bgp\_policy

|Name|Schema|
|---|---|
|**bgp\_policy\_id**  <br>*optional*|[bgp\_policy\_id](#bgp\_policy\_id)|
|**name**  <br>*optional*|[name](#name)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**policy\_attribute**  <br>*optional*|[policy\_attribute](#policy\_attribute)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|


<a name="bgp\_policy\_delete\_success\_schema"></a>
### bgp\_policy\_delete\_success\_schema

|Name|Schema|
|---|---|
|**bgp\_policy**  <br>*optional*|[bgp\_policy](#bgp\_policy\_delete\_success\_schema-bgp\_policy)|

<a name="bgp\_policy\_delete\_success\_schema-bgp\_policy"></a>
**bgp\_policy**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="bgp\_policy\_id"></a>
### bgp\_policy\_id
Auto-generated ID to uniquely identify BGP Policy

*Type* : integer


<a name="bgp\_policy\_post\_success\_schema"></a>
### bgp\_policy\_post\_success\_schema

|Name|Schema|
|---|---|
|**bgp\_policy**  <br>*optional*|[bgp\_policy](#bgp\_policy\_post\_success\_schema-bgp\_policy)|

<a name="bgp\_policy\_post\_success\_schema-bgp\_policy"></a>
**bgp\_policy**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="bgp\_policy\_put\_success\_schema"></a>
### bgp\_policy\_put\_success\_schema

|Name|Schema|
|---|---|
|**bgp\_policy**  <br>*optional*|[bgp\_policy](#bgp\_policy\_put\_success\_schema-bgp\_policy)|

<a name="bgp\_policy\_put\_success\_schema-bgp\_policy"></a>
**bgp\_policy**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="bgp\_policy\_request\_schema"></a>
### bgp\_policy\_request\_schema

|Name|Schema|
|---|---|
|**bgp\_policy**  <br>*optional*|[bgp\_policy](#bgp\_policy)|


<a name="bgp\_policy\_response\_schema"></a>
### bgp\_policy\_response\_schema
*Type* : < [bgp\_policy\_response\_schema](#bgp\_policy\_response\_schema-inline) > array

<a name="bgp\_policy\_response\_schema-inline"></a>
**bgp\_policy\_response\_schema**

|Name|Schema|
|---|---|
|**bgp\_policy\_id**  <br>*optional*|[bgp\_policy\_id](#bgp\_policy\_id)|
|**name**  <br>*optional*|[name](#name)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**policy\_attribute**  <br>*optional*|[policy\_attribute](#policy\_attribute)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|


<a name="name"></a>
### name
The name of the BGP Policy.

*Type* : string


<a name="package\_name"></a>
### package\_name
Config package name using which the site API operation should be performed.

*Type* : string


<a name="policy\_attribute"></a>
### policy\_attribute
Route Policy Attributes for BGP

*Type* : < [policy\_attribute](#policy\_attribute-inline) > array

<a name="policy\_attribute-inline"></a>
**policy\_attribute**

|Name|Description|Schema|
|---|---|---|
|**as\_prepend\_length**  <br>*optional*|Number of times ASN will be prepended to AS\_PATH|integer|
|**asn**  <br>*optional*|Autonomous system number for which the BGP community is applicable.|integer|
|**asn\_to\_prepend**  <br>*optional*|AS number that will be prepended to AS\_PATH|integer|
|**attribute**  <br>*optional*|BGP attribute|enum (med, as\_prepend\_length, community\_string)|
|**community\_string\_action**  <br>*optional*|Insert or remove the matching community from a route|enum (insert, remove)|
|**community\_string\_list\_name**  <br>*optional*|Select pre-configured BGP community list.|string|
|**copy\_cost\_to\_med**  <br>*optional*|Copy the cost from matching routes to MED value.|boolean|
|**is\_new\_format**  <br>*optional*|Use new format(aa:nn) for bgp community.|boolean|
|**policy\_attribute\_id**  <br>*optional*|Auto-generated ID to uniquely identify route policy attributes|integer|
|**value**  <br>*optional*|Value for BGP MED attribute/BGP community|integer|
|**well\_known\_option**  <br>*optional*|Select pre-configured BGP community or enter it manually.|enum (manual, no\_export, no\_advertise, community\_string\_list)|


<a name="site\_name"></a>
### site\_name
Site Name

*Type* : string






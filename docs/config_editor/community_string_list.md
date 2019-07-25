# community\_string\_list


<a name="overview"></a>
## Overview
API to add, delete, get, modify community string list for BGP - Community string list for BGP - a collection of BGP communities that can be used for route filtering. The community list can also be used to set, or modify the communities of a matching route.


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* community\_string\_list : Operations related to community\_string\_list 




<a name="paths"></a>
## Paths

<a name="community\_string\_list-post"></a>
### POST operation for community\_string\_list
```
POST /community_string_list
```


#### Description
Use this operation to add Community String Lists


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[community\_string\_list\_post\_success\_schema](#community\_string\_list\_post\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* community\_string\_list


<a name="community\_string\_list-get"></a>
### Get operation for community\_string\_list
```
GET /community_string_list
```


#### Description
Use this operation to get the Community String Lists


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[community\_string\_list\_response\_schema](#community\_string\_list\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* community\_string\_list


<a name="community\_string\_list-put"></a>
### PUT operation for community\_string\_list
```
PUT /community_string_list
```


#### Description
Use this operation to modify Community String Lists


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[community\_string\_list\_request\_schema](#community\_string\_list\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[community\_string\_list\_put\_success\_schema](#community\_string\_list\_put\_success\_schema)|
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

* community\_string\_list


<a name="community\_string\_list-deletepathparam-delete"></a>
### DELETE operation for community\_string\_list
```
DELETE /community_string_list/{deletePathParam}
```


#### Description
Use this operation to delete Community String Lists


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[community\_string\_list\_delete\_success\_schema](#community\_string\_list\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* community\_string\_list




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="community\_string"></a>
### community\_string
Community Strings for BGP

*Type* : < [community\_string](#community\_string-inline) > array

<a name="community\_string-inline"></a>
**community\_string**

|Name|Description|Schema|
|---|---|---|
|**community\_string\_asn**  <br>*optional*|Autonomous system number for which the BGP community is applicable.|integer|
|**community\_string\_value**  <br>*optional*|Value for BGP community|integer|
|**id**  <br>*optional*|Auto-generated ID to uniquely identify community strings|integer|
|**is\_new\_format**  <br>*optional*|Use new format(aa:nn) for bgp community.|boolean|
|**well\_known\_selection**  <br>*optional*|Select a well known BGP community (no\_export, no\_advertise) or manually enter bgp community.|enum (manual, no\_export, no\_advertise)|


<a name="community\_string\_list"></a>
### community\_string\_list

|Name|Schema|
|---|---|
|**community\_string**  <br>*optional*|[community\_string](#community\_string)|
|**id**  <br>*optional*|[id](#id)|
|**name**  <br>*optional*|[name](#name)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|


<a name="community\_string\_list\_delete\_success\_schema"></a>
### community\_string\_list\_delete\_success\_schema

|Name|Schema|
|---|---|
|**community\_string\_list**  <br>*optional*|[community\_string\_list](#community\_string\_list\_delete\_success\_schema-community\_string\_list)|

<a name="community\_string\_list\_delete\_success\_schema-community\_string\_list"></a>
**community\_string\_list**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="community\_string\_list\_post\_success\_schema"></a>
### community\_string\_list\_post\_success\_schema

|Name|Schema|
|---|---|
|**community\_string\_list**  <br>*optional*|[community\_string\_list](#community\_string\_list\_post\_success\_schema-community\_string\_list)|

<a name="community\_string\_list\_post\_success\_schema-community\_string\_list"></a>
**community\_string\_list**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="community\_string\_list\_put\_success\_schema"></a>
### community\_string\_list\_put\_success\_schema

|Name|Schema|
|---|---|
|**community\_string\_list**  <br>*optional*|[community\_string\_list](#community\_string\_list\_put\_success\_schema-community\_string\_list)|

<a name="community\_string\_list\_put\_success\_schema-community\_string\_list"></a>
**community\_string\_list**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="community\_string\_list\_request\_schema"></a>
### community\_string\_list\_request\_schema

|Name|Schema|
|---|---|
|**community\_string\_list**  <br>*optional*|[community\_string\_list](#community\_string\_list)|


<a name="community\_string\_list\_response\_schema"></a>
### community\_string\_list\_response\_schema
*Type* : < [community\_string\_list\_response\_schema](#community\_string\_list\_response\_schema-inline) > array

<a name="community\_string\_list\_response\_schema-inline"></a>
**community\_string\_list\_response\_schema**

|Name|Schema|
|---|---|
|**community\_string**  <br>*optional*|[community\_string](#community\_string)|
|**id**  <br>*optional*|[id](#id)|
|**name**  <br>*optional*|[name](#name)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|


<a name="id"></a>
### id
Auto-generated ID to uniquely identify Community String List

*Type* : integer


<a name="name"></a>
### name
The name of the Community String List.

*Type* : string


<a name="package\_name"></a>
### package\_name
Config package name using which the site API operation should be performed.

*Type* : string


<a name="site\_name"></a>
### site\_name
Site Name

*Type* : string






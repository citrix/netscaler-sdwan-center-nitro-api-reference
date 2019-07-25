# dynamic\_virtual\_paths


<a name="overview"></a>
## Overview
Dynamic Virtual Path Configuration


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* dynamic\_virtual\_paths : Operations related to dynamic\_virtual\_paths 




<a name="paths"></a>
## Paths

<a name="dynamic\_virtual\_paths-get"></a>
### Get operation for dynamic\_virtual\_paths
```
GET /dynamic_virtual_paths
```


#### Description
Use this operation to get the dynamic virtual path configuration


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[dynamic\_virtual\_paths\_response\_schema](#dynamic\_virtual\_paths\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* dynamic\_virtual\_paths


<a name="dynamic\_virtual\_paths-put"></a>
### PUT operation for dynamic\_virtual\_paths
```
PUT /dynamic_virtual_paths
```


#### Description
Use this operation to modify the dynamic virtual path configuration


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[dynamic\_virtual\_paths\_request\_schema](#dynamic\_virtual\_paths\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[dynamic\_virtual\_paths\_put\_success\_schema](#dynamic\_virtual\_paths\_put\_success\_schema)|
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

* dynamic\_virtual\_paths




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="dynamic\_virtual\_paths"></a>
### dynamic\_virtual\_paths

|Name|Schema|
|---|---|
|**enable\_dynamic\_virtual\_path**  <br>*optional*|[enable\_dynamic\_virtual\_path](#enable\_dynamic\_virtual\_path)|
|**maximum\_dynamic\_virtual\_path**  <br>*optional*|[maximum\_dynamic\_virtual\_path](#maximum\_dynamic\_virtual\_path)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|


<a name="dynamic\_virtual\_paths\_delete\_success\_schema"></a>
### dynamic\_virtual\_paths\_delete\_success\_schema

|Name|Schema|
|---|---|
|**dynamic\_virtual\_paths**  <br>*optional*|[dynamic\_virtual\_paths](#dynamic\_virtual\_paths\_delete\_success\_schema-dynamic\_virtual\_paths)|

<a name="dynamic\_virtual\_paths\_delete\_success\_schema-dynamic\_virtual\_paths"></a>
**dynamic\_virtual\_paths**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="dynamic\_virtual\_paths\_post\_success\_schema"></a>
### dynamic\_virtual\_paths\_post\_success\_schema

|Name|Schema|
|---|---|
|**dynamic\_virtual\_paths**  <br>*optional*|[dynamic\_virtual\_paths](#dynamic\_virtual\_paths\_post\_success\_schema-dynamic\_virtual\_paths)|

<a name="dynamic\_virtual\_paths\_post\_success\_schema-dynamic\_virtual\_paths"></a>
**dynamic\_virtual\_paths**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="dynamic\_virtual\_paths\_put\_success\_schema"></a>
### dynamic\_virtual\_paths\_put\_success\_schema

|Name|Schema|
|---|---|
|**dynamic\_virtual\_paths**  <br>*optional*|[dynamic\_virtual\_paths](#dynamic\_virtual\_paths\_put\_success\_schema-dynamic\_virtual\_paths)|

<a name="dynamic\_virtual\_paths\_put\_success\_schema-dynamic\_virtual\_paths"></a>
**dynamic\_virtual\_paths**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="dynamic\_virtual\_paths\_request\_schema"></a>
### dynamic\_virtual\_paths\_request\_schema

|Name|Schema|
|---|---|
|**dynamic\_virtual\_paths**  <br>*optional*|[dynamic\_virtual\_paths](#dynamic\_virtual\_paths)|


<a name="dynamic\_virtual\_paths\_response\_schema"></a>
### dynamic\_virtual\_paths\_response\_schema
*Type* : < [dynamic\_virtual\_paths\_response\_schema](#dynamic\_virtual\_paths\_response\_schema-inline) > array

<a name="dynamic\_virtual\_paths\_response\_schema-inline"></a>
**dynamic\_virtual\_paths\_response\_schema**

|Name|Schema|
|---|---|
|**enable\_dynamic\_virtual\_path**  <br>*optional*|[enable\_dynamic\_virtual\_path](#enable\_dynamic\_virtual\_path)|
|**maximum\_dynamic\_virtual\_path**  <br>*optional*|[maximum\_dynamic\_virtual\_path](#maximum\_dynamic\_virtual\_path)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**possible\_endpoints**  <br>*optional*|[possible\_endpoints](#possible\_endpoints)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|


<a name="enable\_dynamic\_virtual\_path"></a>
### enable\_dynamic\_virtual\_path
If enabled, Dynamic Virtual Paths will be allowed between this Site and other Sites connected through an intermediate node.

*Type* : boolean


<a name="maximum\_dynamic\_virtual\_path"></a>
### maximum\_dynamic\_virtual\_path
The Maximum number of Dynamic Virtual Paths allowed between this Site and other Sites connected through an intermediate node. Use 'max' to choose maximum number of dynamic virtual paths.

*Type* : enum (max, 1, 2, 3, 4, 5, 6, 7, 8)


<a name="package\_name"></a>
### package\_name
Config package name using which the dynamic virtual path configuration should be performed.

*Type* : string


<a name="possible\_endpoints"></a>
### possible\_endpoints
The possible endpoint sites across the Dynamic Virtual Paths, Please invoke the compile option in order to get the possible end points

*Type* : < string > array


<a name="site\_name"></a>
### site\_name
The site name

*Type* : string






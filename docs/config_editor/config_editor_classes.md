# config\_editor\_classes


<a name="overview"></a>
## Overview
API to add, modify, delete, and get configuration for Classes


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* config\_editor\_classes : Operations related to config\_editor\_classes 




<a name="paths"></a>
## Paths

<a name="config\_editor\_classes-get"></a>
### Get operation for config\_editor\_classes
```
GET /config_editor_classes
```


#### Description
Use this operation to get the Classes settings


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[config\_editor\_classes\_response\_schema](#config\_editor\_classes\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* config\_editor\_classes


<a name="config\_editor\_classes-put"></a>
### PUT operation for config\_editor\_classes
```
PUT /config_editor_classes
```


#### Description
Use this operation to modify the Classes settings


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[config\_editor\_classes\_request\_schema](#config\_editor\_classes\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[config\_editor\_classes\_put\_success\_schema](#config\_editor\_classes\_put\_success\_schema)|
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

* config\_editor\_classes




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="config\_editor\_classes"></a>
### config\_editor\_classes

|Name|Schema|
|---|---|
|**id**  <br>*optional*|[id](#id)|
|**initial\_period**  <br>*optional*|[initial\_period](#initial\_period)|
|**initial\_rate**  <br>*optional*|[initial\_rate](#initial\_rate)|
|**initial\_share\_percent**  <br>*optional*|[initial\_share\_percent](#initial\_share\_percent)|
|**name**  <br>*optional*|[name](#name)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**sustained\_rate**  <br>*optional*|[sustained\_rate](#sustained\_rate)|
|**sustained\_share\_percent**  <br>*optional*|[sustained\_share\_percent](#sustained\_share\_percent)|
|**type**  <br>*optional*|[type](#type)|
|**virtual\_path\_name**  <br>*optional*|[virtual\_path\_name](#virtual\_path\_name)|


<a name="config\_editor\_classes\_delete\_success\_schema"></a>
### config\_editor\_classes\_delete\_success\_schema

|Name|Schema|
|---|---|
|**config\_editor\_classes**  <br>*optional*|[config\_editor\_classes](#config\_editor\_classes\_delete\_success\_schema-config\_editor\_classes)|

<a name="config\_editor\_classes\_delete\_success\_schema-config\_editor\_classes"></a>
**config\_editor\_classes**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="config\_editor\_classes\_post\_success\_schema"></a>
### config\_editor\_classes\_post\_success\_schema

|Name|Schema|
|---|---|
|**config\_editor\_classes**  <br>*optional*|[config\_editor\_classes](#config\_editor\_classes\_post\_success\_schema-config\_editor\_classes)|

<a name="config\_editor\_classes\_post\_success\_schema-config\_editor\_classes"></a>
**config\_editor\_classes**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="config\_editor\_classes\_put\_success\_schema"></a>
### config\_editor\_classes\_put\_success\_schema

|Name|Schema|
|---|---|
|**config\_editor\_classes**  <br>*optional*|[config\_editor\_classes](#config\_editor\_classes\_put\_success\_schema-config\_editor\_classes)|

<a name="config\_editor\_classes\_put\_success\_schema-config\_editor\_classes"></a>
**config\_editor\_classes**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="config\_editor\_classes\_request\_schema"></a>
### config\_editor\_classes\_request\_schema

|Name|Schema|
|---|---|
|**config\_editor\_classes**  <br>*optional*|[config\_editor\_classes](#config\_editor\_classes)|


<a name="config\_editor\_classes\_response\_schema"></a>
### config\_editor\_classes\_response\_schema
*Type* : < [config\_editor\_classes\_response\_schema](#config\_editor\_classes\_response\_schema-inline) > array

<a name="config\_editor\_classes\_response\_schema-inline"></a>
**config\_editor\_classes\_response\_schema**

|Name|Schema|
|---|---|
|**id**  <br>*optional*|[id](#id)|
|**initial\_period**  <br>*optional*|[initial\_period](#initial\_period)|
|**initial\_rate**  <br>*optional*|[initial\_rate](#initial\_rate)|
|**initial\_share\_percent**  <br>*optional*|[initial\_share\_percent](#initial\_share\_percent)|
|**name**  <br>*optional*|[name](#name)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**sustained\_rate**  <br>*optional*|[sustained\_rate](#sustained\_rate)|
|**sustained\_share\_percent**  <br>*optional*|[sustained\_share\_percent](#sustained\_share\_percent)|
|**type**  <br>*optional*|[type](#type)|
|**virtual\_path\_name**  <br>*optional*|[virtual\_path\_name](#virtual\_path\_name)|


<a name="id"></a>
### id
Class ID

*Type* : integer


<a name="initial\_period"></a>
### initial\_period
Duration to apply the Initial Rate before switching to the Sustained Rate, in milliseconds

*Type* : integer


<a name="initial\_rate"></a>
### initial\_rate
The maximum rate during the Initial Period, as a percentage or in kbps

*Type* : integer


<a name="initial\_share\_percent"></a>
### initial\_share\_percent
The maximum share of Virtual Path bandwidth during the Initial Period, as a percentage

*Type* : integer


<a name="name"></a>
### name
The class name

*Type* : string


<a name="package\_name"></a>
### package\_name
Package name

*Type* : string


<a name="site\_name"></a>
### site\_name
Site name for corresponding class

*Type* : string


<a name="sustained\_rate"></a>
### sustained\_rate
The maximum rate after the Initial Period, as a percent share of the Virtual Path or in kbps

*Type* : integer


<a name="sustained\_share\_percent"></a>
### sustained\_share\_percent
The maximum share of Virtual Path bandwidth after the Initial Period, as a percentage

*Type* : integer


<a name="type"></a>
### type
Class traffic type

*Type* : enum (realtime, interactive, bulk)


<a name="virtual\_path\_name"></a>
### virtual\_path\_name
Virtual Path for corresponding class

*Type* : string






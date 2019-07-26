# dynamic\_virtual\_path\_default\_set\_bulk\_classes


<a name="overview"></a>
## Overview
API to modify, get Dynamic Virtual Path Default Set Bulk Classes


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* dynamic\_virtual\_path\_default\_set\_bulk\_classes : Operations related to dynamic\_virtual\_path\_default\_set\_bulk\_classes 




<a name="paths"></a>
## Paths

<a name="dynamic\_virtual\_path\_default\_set\_bulk\_classes-get"></a>
### Get operation for dynamic\_virtual\_path\_default\_set\_bulk\_classes
```
GET /dynamic_virtual_path_default_set_bulk_classes
```


#### Description
Use this operation to get the Dynamic Virtual Path Default Set Bulk Classes


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[dynamic\_virtual\_path\_default\_set\_bulk\_classes\_response\_schema](#dynamic\_virtual\_path\_default\_set\_bulk\_classes\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* dynamic\_virtual\_path\_default\_set\_bulk\_classes


<a name="dynamic\_virtual\_path\_default\_set\_bulk\_classes-put"></a>
### PUT operation for dynamic\_virtual\_path\_default\_set\_bulk\_classes
```
PUT /dynamic_virtual_path_default_set_bulk_classes
```


#### Description
Use this operation to modify Dynamic Virtual Path Default Set Bulk Classes


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[dynamic\_virtual\_path\_default\_set\_bulk\_classes\_request\_schema](#dynamic\_virtual\_path\_default\_set\_bulk\_classes\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[dynamic\_virtual\_path\_default\_set\_bulk\_classes\_put\_success\_schema](#dynamic\_virtual\_path\_default\_set\_bulk\_classes\_put\_success\_schema)|
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

* dynamic\_virtual\_path\_default\_set\_bulk\_classes




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="class\_id"></a>
### class\_id
Class ID

*Type* : integer


<a name="dynamic\_virtual\_path\_default\_set\_bulk\_classes"></a>
### dynamic\_virtual\_path\_default\_set\_bulk\_classes

|Name|Schema|
|---|---|
|**class\_id**  <br>*optional*|[class\_id](#class\_id)|
|**dynamic\_virtual\_path\_default\_set\_name**  <br>*optional*|[dynamic\_virtual\_path\_default\_set\_name](#dynamic\_virtual\_path\_default\_set\_name)|
|**name**  <br>*optional*|[name](#name)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**sustained\_share\_percent**  <br>*optional*|[sustained\_share\_percent](#sustained\_share\_percent)|


<a name="dynamic\_virtual\_path\_default\_set\_bulk\_classes\_delete\_success\_schema"></a>
### dynamic\_virtual\_path\_default\_set\_bulk\_classes\_delete\_success\_schema

|Name|Schema|
|---|---|
|**dynamic\_virtual\_path\_default\_set\_bulk\_classes**  <br>*optional*|[dynamic\_virtual\_path\_default\_set\_bulk\_classes](#dynamic\_virtual\_path\_default\_set\_bulk\_classes\_delete\_success\_schema-dynamic\_virtual\_path\_default\_set\_bulk\_classes)|

<a name="dynamic\_virtual\_path\_default\_set\_bulk\_classes\_delete\_success\_schema-dynamic\_virtual\_path\_default\_set\_bulk\_classes"></a>
**dynamic\_virtual\_path\_default\_set\_bulk\_classes**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="dynamic\_virtual\_path\_default\_set\_bulk\_classes\_post\_success\_schema"></a>
### dynamic\_virtual\_path\_default\_set\_bulk\_classes\_post\_success\_schema

|Name|Schema|
|---|---|
|**dynamic\_virtual\_path\_default\_set\_bulk\_classes**  <br>*optional*|[dynamic\_virtual\_path\_default\_set\_bulk\_classes](#dynamic\_virtual\_path\_default\_set\_bulk\_classes\_post\_success\_schema-dynamic\_virtual\_path\_default\_set\_bulk\_classes)|

<a name="dynamic\_virtual\_path\_default\_set\_bulk\_classes\_post\_success\_schema-dynamic\_virtual\_path\_default\_set\_bulk\_classes"></a>
**dynamic\_virtual\_path\_default\_set\_bulk\_classes**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="dynamic\_virtual\_path\_default\_set\_bulk\_classes\_put\_success\_schema"></a>
### dynamic\_virtual\_path\_default\_set\_bulk\_classes\_put\_success\_schema

|Name|Schema|
|---|---|
|**dynamic\_virtual\_path\_default\_set\_bulk\_classes**  <br>*optional*|[dynamic\_virtual\_path\_default\_set\_bulk\_classes](#dynamic\_virtual\_path\_default\_set\_bulk\_classes\_put\_success\_schema-dynamic\_virtual\_path\_default\_set\_bulk\_classes)|

<a name="dynamic\_virtual\_path\_default\_set\_bulk\_classes\_put\_success\_schema-dynamic\_virtual\_path\_default\_set\_bulk\_classes"></a>
**dynamic\_virtual\_path\_default\_set\_bulk\_classes**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="dynamic\_virtual\_path\_default\_set\_bulk\_classes\_request\_schema"></a>
### dynamic\_virtual\_path\_default\_set\_bulk\_classes\_request\_schema

|Name|Schema|
|---|---|
|**dynamic\_virtual\_path\_default\_set\_bulk\_classes**  <br>*optional*|[dynamic\_virtual\_path\_default\_set\_bulk\_classes](#dynamic\_virtual\_path\_default\_set\_bulk\_classes)|


<a name="dynamic\_virtual\_path\_default\_set\_bulk\_classes\_response\_schema"></a>
### dynamic\_virtual\_path\_default\_set\_bulk\_classes\_response\_schema
*Type* : < [dynamic\_virtual\_path\_default\_set\_bulk\_classes\_response\_schema](#dynamic\_virtual\_path\_default\_set\_bulk\_classes\_response\_schema-inline) > array

<a name="dynamic\_virtual\_path\_default\_set\_bulk\_classes\_response\_schema-inline"></a>
**dynamic\_virtual\_path\_default\_set\_bulk\_classes\_response\_schema**

|Name|Schema|
|---|---|
|**class\_id**  <br>*optional*|[class\_id](#class\_id)|
|**dynamic\_virtual\_path\_default\_set\_name**  <br>*optional*|[dynamic\_virtual\_path\_default\_set\_name](#dynamic\_virtual\_path\_default\_set\_name)|
|**is\_auto**  <br>*optional*|[is\_auto](#is\_auto)|
|**name**  <br>*optional*|[name](#name)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**sustained\_share\_percent**  <br>*optional*|[sustained\_share\_percent](#sustained\_share\_percent)|
|**type**  <br>*optional*|[type](#type)|


<a name="dynamic\_virtual\_path\_default\_set\_name"></a>
### dynamic\_virtual\_path\_default\_set\_name
Dynamic Virtual path Default Set name using which the API operation should be performed.

*Type* : string


<a name="is\_auto"></a>
### is\_auto
To indicate that this is auto-generated

*Type* : boolean


<a name="name"></a>
### name
Class Name

*Type* : string


<a name="package\_name"></a>
### package\_name
Config package name using which the API operation should be performed.

*Type* : string


<a name="sustained\_share\_percent"></a>
### sustained\_share\_percent
The maximum share of Virtual Path bandwidth after the Initial Period, as a percentage

*Type* : integer


<a name="type"></a>
### type
Class Traffic Type

*Type* : string






# file\_management


<a name="overview"></a>
## Overview
This resource can be used for license file managemen.


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/license/  
*Schemes* : HTTP


### Tags

* file\_management : Operations related to file\_management 




<a name="paths"></a>
## Paths

<a name="file\_management-post"></a>
### POST operation for file\_management
```
POST /file_management
```


#### Description
Use this operation to unpload license file. This action expects multipart/form-data data like : -F filename=@LICENSE\_FILE\_NAME


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Query**|**action**  <br>*required*|Select if action is other that ADD|enum (upload\_license, delete\_license)|
|**Body**|**body**  <br>*optional*||[file\_management\_request\_schema](#file\_management\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[file\_management\_post\_success\_schema](#file\_management\_post\_success\_schema)|
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

* file\_management


<a name="file\_management-get"></a>
### Get operation for file\_management
```
GET /file_management
```


#### Description
Use this operation to get uploaded license files.


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[file\_management\_response\_schema](#file\_management\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* file\_management




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="file\_management"></a>
### file\_management

|Name|Schema|
|---|---|
|**filename**  <br>*optional*|[filename](#filename)|


<a name="file\_management\_delete\_success\_schema"></a>
### file\_management\_delete\_success\_schema

|Name|Schema|
|---|---|
|**file\_management**  <br>*optional*|[file\_management](#file\_management\_delete\_success\_schema-file\_management)|

<a name="file\_management\_delete\_success\_schema-file\_management"></a>
**file\_management**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="file\_management\_post\_success\_schema"></a>
### file\_management\_post\_success\_schema

|Name|Schema|
|---|---|
|**file\_management**  <br>*optional*|[file\_management](#file\_management\_post\_success\_schema-file\_management)|

<a name="file\_management\_post\_success\_schema-file\_management"></a>
**file\_management**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="file\_management\_put\_success\_schema"></a>
### file\_management\_put\_success\_schema

|Name|Schema|
|---|---|
|**file\_management**  <br>*optional*|[file\_management](#file\_management\_put\_success\_schema-file\_management)|

<a name="file\_management\_put\_success\_schema-file\_management"></a>
**file\_management**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="file\_management\_request\_schema"></a>
### file\_management\_request\_schema

|Name|Schema|
|---|---|
|**file\_management**  <br>*optional*|[file\_management](#file\_management)|


<a name="file\_management\_response\_schema"></a>
### file\_management\_response\_schema
*Type* : < [file\_management\_response\_schema](#file\_management\_response\_schema-inline) > array

<a name="file\_management\_response\_schema-inline"></a>
**file\_management\_response\_schema**

|Name|Schema|
|---|---|
|**filename**  <br>*optional*|[filename](#filename)|


<a name="filename"></a>
### filename
The filename of the license to be uploaded/deleted

*Type* : string






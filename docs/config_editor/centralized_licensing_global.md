# centralized\_licensing\_global


<a name="overview"></a>
## Overview
API to modify, get, global settings for centralized licensing


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* centralized\_licensing\_global : Operations related to centralized\_licensing\_global 




<a name="paths"></a>
## Paths

<a name="centralized\_licensing\_global-get"></a>
### Get operation for centralized\_licensing\_global
```
GET /centralized_licensing_global
```


#### Description
Use this operation to get global centralized license properties


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[centralized\_licensing\_global\_response\_schema](#centralized\_licensing\_global\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* centralized\_licensing\_global


<a name="centralized\_licensing\_global-put"></a>
### PUT operation for centralized\_licensing\_global
```
PUT /centralized_licensing_global
```


#### Description
Use this operation to modify global centralized license properties


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[centralized\_licensing\_global\_request\_schema](#centralized\_licensing\_global\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[centralized\_licensing\_global\_put\_success\_schema](#centralized\_licensing\_global\_put\_success\_schema)|
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

* centralized\_licensing\_global




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="centralized\_licensing\_global"></a>
### centralized\_licensing\_global

|Name|Schema|
|---|---|
|**enable**  <br>*optional*|[enable](#enable)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**remote\_server\_ip**  <br>*optional*|[remote\_server\_ip](#remote\_server\_ip)|
|**remote\_server\_port**  <br>*optional*|[remote\_server\_port](#remote\_server\_port)|


<a name="centralized\_licensing\_global\_delete\_success\_schema"></a>
### centralized\_licensing\_global\_delete\_success\_schema

|Name|Schema|
|---|---|
|**centralized\_licensing\_global**  <br>*optional*|[centralized\_licensing\_global](#centralized\_licensing\_global\_delete\_success\_schema-centralized\_licensing\_global)|

<a name="centralized\_licensing\_global\_delete\_success\_schema-centralized\_licensing\_global"></a>
**centralized\_licensing\_global**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="centralized\_licensing\_global\_post\_success\_schema"></a>
### centralized\_licensing\_global\_post\_success\_schema

|Name|Schema|
|---|---|
|**centralized\_licensing\_global**  <br>*optional*|[centralized\_licensing\_global](#centralized\_licensing\_global\_post\_success\_schema-centralized\_licensing\_global)|

<a name="centralized\_licensing\_global\_post\_success\_schema-centralized\_licensing\_global"></a>
**centralized\_licensing\_global**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="centralized\_licensing\_global\_put\_success\_schema"></a>
### centralized\_licensing\_global\_put\_success\_schema

|Name|Schema|
|---|---|
|**centralized\_licensing\_global**  <br>*optional*|[centralized\_licensing\_global](#centralized\_licensing\_global\_put\_success\_schema-centralized\_licensing\_global)|

<a name="centralized\_licensing\_global\_put\_success\_schema-centralized\_licensing\_global"></a>
**centralized\_licensing\_global**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="centralized\_licensing\_global\_request\_schema"></a>
### centralized\_licensing\_global\_request\_schema

|Name|Schema|
|---|---|
|**centralized\_licensing\_global**  <br>*optional*|[centralized\_licensing\_global](#centralized\_licensing\_global)|


<a name="centralized\_licensing\_global\_response\_schema"></a>
### centralized\_licensing\_global\_response\_schema
*Type* : < [centralized\_licensing\_global\_response\_schema](#centralized\_licensing\_global\_response\_schema-inline) > array

<a name="centralized\_licensing\_global\_response\_schema-inline"></a>
**centralized\_licensing\_global\_response\_schema**

|Name|Schema|
|---|---|
|**enable**  <br>*optional*|[enable](#enable)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**remote\_server\_ip**  <br>*optional*|[remote\_server\_ip](#remote\_server\_ip)|
|**remote\_server\_port**  <br>*optional*|[remote\_server\_port](#remote\_server\_port)|


<a name="enable"></a>
### enable
enable/disable centralized licensing

*Type* : boolean


<a name="package\_name"></a>
### package\_name
Config package name using which the licensing  API operation should be performed.

*Type* : string


<a name="remote\_server\_ip"></a>
### remote\_server\_ip
Remote licensing server ip address

*Type* : string


<a name="remote\_server\_port"></a>
### remote\_server\_port
Remote licensing server port

*Type* : integer






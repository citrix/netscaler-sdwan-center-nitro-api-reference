# ntp\_servers


<a name="overview"></a>
## Overview
Add, Delete or List NTP Servers through these APIs


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/system/  
*Schemes* : HTTP


### Tags

* ntp\_servers : Operations related to ntp\_servers 




<a name="paths"></a>
## Paths

<a name="ntp\_servers-post"></a>
### POST operation for ntp\_servers
```
POST /ntp_servers
```


#### Description
Use this operation to add a NTP server


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[ntp\_servers\_request\_schema](#ntp\_servers\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[ntp\_servers\_post\_success\_schema](#ntp\_servers\_post\_success\_schema)|
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

* ntp\_servers


<a name="ntp\_servers-get"></a>
### Get operation for ntp\_servers
```
GET /ntp_servers
```


#### Description
Use this operation to list all ntp servers


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[ntp\_servers\_response\_schema](#ntp\_servers\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* ntp\_servers


<a name="ntp\_servers-deletepathparam-delete"></a>
### DELETE operation for ntp\_servers
```
DELETE /ntp_servers/{deletePathParam}
```


#### Description
Use this operation to delete a NTP server


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[ntp\_servers\_delete\_success\_schema](#ntp\_servers\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* ntp\_servers




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="address"></a>
### address
Address for the NTP Server

*Type* : string


<a name="ntp\_servers"></a>
### ntp\_servers

|Name|Schema|
|---|---|
|**address**  <br>*optional*|[address](#address)|


<a name="ntp\_servers\_delete\_success\_schema"></a>
### ntp\_servers\_delete\_success\_schema

|Name|Schema|
|---|---|
|**ntp\_servers**  <br>*optional*|[ntp\_servers](#ntp\_servers\_delete\_success\_schema-ntp\_servers)|

<a name="ntp\_servers\_delete\_success\_schema-ntp\_servers"></a>
**ntp\_servers**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="ntp\_servers\_post\_success\_schema"></a>
### ntp\_servers\_post\_success\_schema

|Name|Schema|
|---|---|
|**ntp\_servers**  <br>*optional*|[ntp\_servers](#ntp\_servers\_post\_success\_schema-ntp\_servers)|

<a name="ntp\_servers\_post\_success\_schema-ntp\_servers"></a>
**ntp\_servers**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="ntp\_servers\_put\_success\_schema"></a>
### ntp\_servers\_put\_success\_schema

|Name|Schema|
|---|---|
|**ntp\_servers**  <br>*optional*|[ntp\_servers](#ntp\_servers\_put\_success\_schema-ntp\_servers)|

<a name="ntp\_servers\_put\_success\_schema-ntp\_servers"></a>
**ntp\_servers**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="ntp\_servers\_request\_schema"></a>
### ntp\_servers\_request\_schema

|Name|Schema|
|---|---|
|**ntp\_servers**  <br>*optional*|[ntp\_servers](#ntp\_servers)|


<a name="ntp\_servers\_response\_schema"></a>
### ntp\_servers\_response\_schema
*Type* : < [ntp\_servers\_response\_schema](#ntp\_servers\_response\_schema-inline) > array

<a name="ntp\_servers\_response\_schema-inline"></a>
**ntp\_servers\_response\_schema**

|Name|Schema|
|---|---|
|**address**  <br>*optional*|[address](#address)|






# discovery\_settings


<a name="overview"></a>
## Overview
This resource can be used to set and get the discovery settings.


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config/  
*Schemes* : HTTP


### Tags

* discovery\_settings : Operations related to discovery\_settings 




<a name="paths"></a>
## Paths

<a name="discovery\_settings-post"></a>
### POST operation for discovery\_settings
```
POST /discovery_settings
```


#### Description
Use this operation to set the Discovery settings.


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Query**|**action**  <br>*optional*|Select if action is other that ADD|enum (check\_discovery\_status, start\_discovery, test, check\_region\_discovery\_status, start\_region\_discovery)|
|**Body**|**body**  <br>*optional*||[discovery\_settings\_request\_schema](#discovery\_settings\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[discovery\_settings\_post\_success\_schema](#discovery\_settings\_post\_success\_schema)|
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

* discovery\_settings


<a name="discovery\_settings-get"></a>
### Get operation for discovery\_settings
```
GET /discovery_settings
```


#### Description
Use this operation to get the Discovery settings.


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[discovery\_settings\_response\_schema](#discovery\_settings\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* discovery\_settings




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="bandwidth\_limit"></a>
### bandwidth\_limit
The maximum amount of bandwidth--in aggregate for all Sites--that can be used to transmit statistics from the Virtual WAN, in kbps (100-1000000). Defaults to 1000 kbps.

*Type* : integer


<a name="discovery\_settings"></a>
### discovery\_settings

|Name|Schema|
|---|---|
|**bandwidth\_limit**  <br>*optional*|[bandwidth\_limit](#bandwidth\_limit)|
|**mcn\_ip**  <br>*optional*|[mcn\_ip](#mcn\_ip)|
|**poll\_interval**  <br>*optional*|[poll\_interval](#poll\_interval)|


<a name="discovery\_settings\_delete\_success\_schema"></a>
### discovery\_settings\_delete\_success\_schema

|Name|Schema|
|---|---|
|**discovery\_settings**  <br>*optional*|[discovery\_settings](#discovery\_settings\_delete\_success\_schema-discovery\_settings)|

<a name="discovery\_settings\_delete\_success\_schema-discovery\_settings"></a>
**discovery\_settings**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="discovery\_settings\_post\_success\_schema"></a>
### discovery\_settings\_post\_success\_schema

|Name|Schema|
|---|---|
|**discovery\_settings**  <br>*optional*|[discovery\_settings](#discovery\_settings\_post\_success\_schema-discovery\_settings)|

<a name="discovery\_settings\_post\_success\_schema-discovery\_settings"></a>
**discovery\_settings**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="discovery\_settings\_put\_success\_schema"></a>
### discovery\_settings\_put\_success\_schema

|Name|Schema|
|---|---|
|**discovery\_settings**  <br>*optional*|[discovery\_settings](#discovery\_settings\_put\_success\_schema-discovery\_settings)|

<a name="discovery\_settings\_put\_success\_schema-discovery\_settings"></a>
**discovery\_settings**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="discovery\_settings\_request\_schema"></a>
### discovery\_settings\_request\_schema

|Name|Schema|
|---|---|
|**discovery\_settings**  <br>*optional*|[discovery\_settings](#discovery\_settings)|


<a name="discovery\_settings\_response\_schema"></a>
### discovery\_settings\_response\_schema
*Type* : < [discovery\_settings\_response\_schema](#discovery\_settings\_response\_schema-inline) > array

<a name="discovery\_settings\_response\_schema-inline"></a>
**discovery\_settings\_response\_schema**

|Name|Schema|
|---|---|
|**bandwidth\_limit**  <br>*optional*|[bandwidth\_limit](#bandwidth\_limit)|
|**mcn\_ip**  <br>*optional*|[mcn\_ip](#mcn\_ip)|
|**poll\_interval**  <br>*optional*|[poll\_interval](#poll\_interval)|


<a name="mcn\_ip"></a>
### mcn\_ip
The Master Controller Node IP Address

*Type* : string


<a name="poll\_interval"></a>
### poll\_interval
The interval at which to collect statistics from Virtual WAN Appliances, in minutes (2-60). Defaults to 5 minutes.

*Type* : integer






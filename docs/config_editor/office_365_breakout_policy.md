# office\_365\_breakout\_policy


<a name="overview"></a>
## Overview
API to get, modify global Office 365 Breakout Policy.


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* office\_365\_breakout\_policy : Operations related to office\_365\_breakout\_policy 




<a name="paths"></a>
## Paths

<a name="office\_365\_breakout\_policy-get"></a>
### Get operation for office\_365\_breakout\_policy
```
GET /office_365_breakout_policy
```


#### Description
Use this operation to get the current values of Office 365 Breakout Policy


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[office\_365\_breakout\_policy\_response\_schema](#office\_365\_breakout\_policy\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* office\_365\_breakout\_policy


<a name="office\_365\_breakout\_policy-put"></a>
### PUT operation for office\_365\_breakout\_policy
```
PUT /office_365_breakout_policy
```


#### Description
Use this operation to modify the current values of Office 365 Breakout Policy


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[office\_365\_breakout\_policy\_request\_schema](#office\_365\_breakout\_policy\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[office\_365\_breakout\_policy\_put\_success\_schema](#office\_365\_breakout\_policy\_put\_success\_schema)|
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

* office\_365\_breakout\_policy




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="enable\_breakout\_from\_branch\_allow"></a>
### enable\_breakout\_from\_branch\_allow
Set to true to enable from branch for Allow O365 URL Category.

*Type* : boolean


<a name="enable\_breakout\_from\_branch\_default"></a>
### enable\_breakout\_from\_branch\_default
Set to true to enable from branch for Default O365 URL Category.

*Type* : boolean


<a name="enable\_breakout\_from\_branch\_optimize"></a>
### enable\_breakout\_from\_branch\_optimize
Set to true to enable breakout from branch for Optimize O365 URL Category.

*Type* : boolean


<a name="office\_365\_breakout\_policy"></a>
### office\_365\_breakout\_policy

|Name|Schema|
|---|---|
|**enable\_breakout\_from\_branch\_allow**  <br>*optional*|[enable\_breakout\_from\_branch\_allow](#enable\_breakout\_from\_branch\_allow)|
|**enable\_breakout\_from\_branch\_default**  <br>*optional*|[enable\_breakout\_from\_branch\_default](#enable\_breakout\_from\_branch\_default)|
|**enable\_breakout\_from\_branch\_optimize**  <br>*optional*|[enable\_breakout\_from\_branch\_optimize](#enable\_breakout\_from\_branch\_optimize)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|


<a name="office\_365\_breakout\_policy\_delete\_success\_schema"></a>
### office\_365\_breakout\_policy\_delete\_success\_schema

|Name|Schema|
|---|---|
|**office\_365\_breakout\_policy**  <br>*optional*|[office\_365\_breakout\_policy](#office\_365\_breakout\_policy\_delete\_success\_schema-office\_365\_breakout\_policy)|

<a name="office\_365\_breakout\_policy\_delete\_success\_schema-office\_365\_breakout\_policy"></a>
**office\_365\_breakout\_policy**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="office\_365\_breakout\_policy\_post\_success\_schema"></a>
### office\_365\_breakout\_policy\_post\_success\_schema

|Name|Schema|
|---|---|
|**office\_365\_breakout\_policy**  <br>*optional*|[office\_365\_breakout\_policy](#office\_365\_breakout\_policy\_post\_success\_schema-office\_365\_breakout\_policy)|

<a name="office\_365\_breakout\_policy\_post\_success\_schema-office\_365\_breakout\_policy"></a>
**office\_365\_breakout\_policy**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="office\_365\_breakout\_policy\_put\_success\_schema"></a>
### office\_365\_breakout\_policy\_put\_success\_schema

|Name|Schema|
|---|---|
|**office\_365\_breakout\_policy**  <br>*optional*|[office\_365\_breakout\_policy](#office\_365\_breakout\_policy\_put\_success\_schema-office\_365\_breakout\_policy)|

<a name="office\_365\_breakout\_policy\_put\_success\_schema-office\_365\_breakout\_policy"></a>
**office\_365\_breakout\_policy**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="office\_365\_breakout\_policy\_request\_schema"></a>
### office\_365\_breakout\_policy\_request\_schema

|Name|Schema|
|---|---|
|**office\_365\_breakout\_policy**  <br>*optional*|[office\_365\_breakout\_policy](#office\_365\_breakout\_policy)|


<a name="office\_365\_breakout\_policy\_response\_schema"></a>
### office\_365\_breakout\_policy\_response\_schema
*Type* : < [office\_365\_breakout\_policy\_response\_schema](#office\_365\_breakout\_policy\_response\_schema-inline) > array

<a name="office\_365\_breakout\_policy\_response\_schema-inline"></a>
**office\_365\_breakout\_policy\_response\_schema**

|Name|Schema|
|---|---|
|**enable\_breakout\_from\_branch\_allow**  <br>*optional*|[enable\_breakout\_from\_branch\_allow](#enable\_breakout\_from\_branch\_allow)|
|**enable\_breakout\_from\_branch\_default**  <br>*optional*|[enable\_breakout\_from\_branch\_default](#enable\_breakout\_from\_branch\_default)|
|**enable\_breakout\_from\_branch\_optimize**  <br>*optional*|[enable\_breakout\_from\_branch\_optimize](#enable\_breakout\_from\_branch\_optimize)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|


<a name="package\_name"></a>
### package\_name
Config package name using which the API operation should be performed.

*Type* : string






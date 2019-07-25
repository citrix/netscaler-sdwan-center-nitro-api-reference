# connections\_office\_365\_breakout\_policy


<a name="overview"></a>
## Overview
API to get, modify Connections Office 365 Breakout Policy.


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* connections\_office\_365\_breakout\_policy : Operations related to connections\_office\_365\_breakout\_policy 




<a name="paths"></a>
## Paths

<a name="connections\_office\_365\_breakout\_policy-get"></a>
### Get operation for connections\_office\_365\_breakout\_policy
```
GET /connections_office_365_breakout_policy
```


#### Description
Use this operation to get the current values of Connections Office 365 Breakout Policy


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[connections\_office\_365\_breakout\_policy\_response\_schema](#connections\_office\_365\_breakout\_policy\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* connections\_office\_365\_breakout\_policy


<a name="connections\_office\_365\_breakout\_policy-put"></a>
### PUT operation for connections\_office\_365\_breakout\_policy
```
PUT /connections_office_365_breakout_policy
```


#### Description
Use this operation to modify the current values of Connections Office 365 Breakout Policy


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[connections\_office\_365\_breakout\_policy\_request\_schema](#connections\_office\_365\_breakout\_policy\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[connections\_office\_365\_breakout\_policy\_put\_success\_schema](#connections\_office\_365\_breakout\_policy\_put\_success\_schema)|
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

* connections\_office\_365\_breakout\_policy




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="connections\_office\_365\_breakout\_policy"></a>
### connections\_office\_365\_breakout\_policy

|Name|Schema|
|---|---|
|**enable\_breakout\_from\_branch\_allow**  <br>*optional*|[enable\_breakout\_from\_branch\_allow](#enable\_breakout\_from\_branch\_allow)|
|**enable\_breakout\_from\_branch\_default**  <br>*optional*|[enable\_breakout\_from\_branch\_default](#enable\_breakout\_from\_branch\_default)|
|**enable\_breakout\_from\_branch\_optimize**  <br>*optional*|[enable\_breakout\_from\_branch\_optimize](#enable\_breakout\_from\_branch\_optimize)|
|**override\_global\_office\_365\_policy**  <br>*optional*|[override\_global\_office\_365\_policy](#override\_global\_office\_365\_policy)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|


<a name="connections\_office\_365\_breakout\_policy\_delete\_success\_schema"></a>
### connections\_office\_365\_breakout\_policy\_delete\_success\_schema

|Name|Schema|
|---|---|
|**connections\_office\_365\_breakout\_policy**  <br>*optional*|[connections\_office\_365\_breakout\_policy](#connections\_office\_365\_breakout\_policy\_delete\_success\_schema-connections\_office\_365\_breakout\_policy)|

<a name="connections\_office\_365\_breakout\_policy\_delete\_success\_schema-connections\_office\_365\_breakout\_policy"></a>
**connections\_office\_365\_breakout\_policy**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="connections\_office\_365\_breakout\_policy\_post\_success\_schema"></a>
### connections\_office\_365\_breakout\_policy\_post\_success\_schema

|Name|Schema|
|---|---|
|**connections\_office\_365\_breakout\_policy**  <br>*optional*|[connections\_office\_365\_breakout\_policy](#connections\_office\_365\_breakout\_policy\_post\_success\_schema-connections\_office\_365\_breakout\_policy)|

<a name="connections\_office\_365\_breakout\_policy\_post\_success\_schema-connections\_office\_365\_breakout\_policy"></a>
**connections\_office\_365\_breakout\_policy**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="connections\_office\_365\_breakout\_policy\_put\_success\_schema"></a>
### connections\_office\_365\_breakout\_policy\_put\_success\_schema

|Name|Schema|
|---|---|
|**connections\_office\_365\_breakout\_policy**  <br>*optional*|[connections\_office\_365\_breakout\_policy](#connections\_office\_365\_breakout\_policy\_put\_success\_schema-connections\_office\_365\_breakout\_policy)|

<a name="connections\_office\_365\_breakout\_policy\_put\_success\_schema-connections\_office\_365\_breakout\_policy"></a>
**connections\_office\_365\_breakout\_policy**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="connections\_office\_365\_breakout\_policy\_request\_schema"></a>
### connections\_office\_365\_breakout\_policy\_request\_schema

|Name|Schema|
|---|---|
|**connections\_office\_365\_breakout\_policy**  <br>*optional*|[connections\_office\_365\_breakout\_policy](#connections\_office\_365\_breakout\_policy)|


<a name="connections\_office\_365\_breakout\_policy\_response\_schema"></a>
### connections\_office\_365\_breakout\_policy\_response\_schema
*Type* : < [connections\_office\_365\_breakout\_policy\_response\_schema](#connections\_office\_365\_breakout\_policy\_response\_schema-inline) > array

<a name="connections\_office\_365\_breakout\_policy\_response\_schema-inline"></a>
**connections\_office\_365\_breakout\_policy\_response\_schema**

|Name|Schema|
|---|---|
|**enable\_breakout\_from\_branch\_allow**  <br>*optional*|[enable\_breakout\_from\_branch\_allow](#enable\_breakout\_from\_branch\_allow)|
|**enable\_breakout\_from\_branch\_default**  <br>*optional*|[enable\_breakout\_from\_branch\_default](#enable\_breakout\_from\_branch\_default)|
|**enable\_breakout\_from\_branch\_optimize**  <br>*optional*|[enable\_breakout\_from\_branch\_optimize](#enable\_breakout\_from\_branch\_optimize)|
|**override\_global\_office\_365\_policy**  <br>*optional*|[override\_global\_office\_365\_policy](#override\_global\_office\_365\_policy)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|


<a name="enable\_breakout\_from\_branch\_allow"></a>
### enable\_breakout\_from\_branch\_allow
Set to true to enable breakout from branch for Allow O365 URL Category.

*Type* : boolean


<a name="enable\_breakout\_from\_branch\_default"></a>
### enable\_breakout\_from\_branch\_default
Set to true to enable breakout from branch for Default O365 URL Category.

*Type* : boolean


<a name="enable\_breakout\_from\_branch\_optimize"></a>
### enable\_breakout\_from\_branch\_optimize
Set to true to enable breakout from branch for Optimize O365 URL Category.

*Type* : boolean


<a name="override\_global\_office\_365\_policy"></a>
### override\_global\_office\_365\_policy
Set to true to override global office 365 policy.

*Type* : boolean


<a name="package\_name"></a>
### package\_name
Config package name using which the API operation should be performed.

*Type* : string


<a name="site\_name"></a>
### site\_name
Site Name

*Type* : string






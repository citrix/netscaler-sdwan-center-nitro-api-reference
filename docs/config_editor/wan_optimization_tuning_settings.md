# wan\_optimization\_tuning\_settings


<a name="overview"></a>
## Overview
API to get, modify global WAN Optimization Tuning Settings.


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* wan\_optimization\_tuning\_settings : Operations related to wan\_optimization\_tuning\_settings 




<a name="paths"></a>
## Paths

<a name="wan\_optimization\_tuning\_settings-get"></a>
### Get operation for wan\_optimization\_tuning\_settings
```
GET /wan_optimization_tuning_settings
```


#### Description
Use this operation to get the current values of WAN Optimization tuning settings


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[wan\_optimization\_tuning\_settings\_response\_schema](#wan\_optimization\_tuning\_settings\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* wan\_optimization\_tuning\_settings


<a name="wan\_optimization\_tuning\_settings-put"></a>
### PUT operation for wan\_optimization\_tuning\_settings
```
PUT /wan_optimization_tuning_settings
```


#### Description
Use this operation to modify the current values of WAN Optimization tuning settings


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[wan\_optimization\_tuning\_settings\_request\_schema](#wan\_optimization\_tuning\_settings\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[wan\_optimization\_tuning\_settings\_put\_success\_schema](#wan\_optimization\_tuning\_settings\_put\_success\_schema)|
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

* wan\_optimization\_tuning\_settings




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="default\_mss"></a>
### default\_mss
Default value for MSS

*Type* : integer


<a name="enable\_connection\_timeout"></a>
### enable\_connection\_timeout
Set to true to enable connection timeout.

*Type* : boolean


<a name="idle\_timeout"></a>
### idle\_timeout
Idle Timeout

*Type* : number


<a name="maximum\_mss"></a>
### maximum\_mss
Maximum value for MSS

*Type* : integer


<a name="package\_name"></a>
### package\_name
Config package name using which the API operation should be performed.

*Type* : string


<a name="wan\_optimization\_tuning\_settings"></a>
### wan\_optimization\_tuning\_settings

|Name|Schema|
|---|---|
|**default\_mss**  <br>*optional*|[default\_mss](#default\_mss)|
|**enable\_connection\_timeout**  <br>*optional*|[enable\_connection\_timeout](#enable\_connection\_timeout)|
|**idle\_timeout**  <br>*optional*|[idle\_timeout](#idle\_timeout)|
|**maximum\_mss**  <br>*optional*|[maximum\_mss](#maximum\_mss)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|


<a name="wan\_optimization\_tuning\_settings\_delete\_success\_schema"></a>
### wan\_optimization\_tuning\_settings\_delete\_success\_schema

|Name|Schema|
|---|---|
|**wan\_optimization\_tuning\_settings**  <br>*optional*|[wan\_optimization\_tuning\_settings](#wan\_optimization\_tuning\_settings\_delete\_success\_schema-wan\_optimization\_tuning\_settings)|

<a name="wan\_optimization\_tuning\_settings\_delete\_success\_schema-wan\_optimization\_tuning\_settings"></a>
**wan\_optimization\_tuning\_settings**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="wan\_optimization\_tuning\_settings\_post\_success\_schema"></a>
### wan\_optimization\_tuning\_settings\_post\_success\_schema

|Name|Schema|
|---|---|
|**wan\_optimization\_tuning\_settings**  <br>*optional*|[wan\_optimization\_tuning\_settings](#wan\_optimization\_tuning\_settings\_post\_success\_schema-wan\_optimization\_tuning\_settings)|

<a name="wan\_optimization\_tuning\_settings\_post\_success\_schema-wan\_optimization\_tuning\_settings"></a>
**wan\_optimization\_tuning\_settings**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="wan\_optimization\_tuning\_settings\_put\_success\_schema"></a>
### wan\_optimization\_tuning\_settings\_put\_success\_schema

|Name|Schema|
|---|---|
|**wan\_optimization\_tuning\_settings**  <br>*optional*|[wan\_optimization\_tuning\_settings](#wan\_optimization\_tuning\_settings\_put\_success\_schema-wan\_optimization\_tuning\_settings)|

<a name="wan\_optimization\_tuning\_settings\_put\_success\_schema-wan\_optimization\_tuning\_settings"></a>
**wan\_optimization\_tuning\_settings**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="wan\_optimization\_tuning\_settings\_request\_schema"></a>
### wan\_optimization\_tuning\_settings\_request\_schema

|Name|Schema|
|---|---|
|**wan\_optimization\_tuning\_settings**  <br>*optional*|[wan\_optimization\_tuning\_settings](#wan\_optimization\_tuning\_settings)|


<a name="wan\_optimization\_tuning\_settings\_response\_schema"></a>
### wan\_optimization\_tuning\_settings\_response\_schema
*Type* : < [wan\_optimization\_tuning\_settings\_response\_schema](#wan\_optimization\_tuning\_settings\_response\_schema-inline) > array

<a name="wan\_optimization\_tuning\_settings\_response\_schema-inline"></a>
**wan\_optimization\_tuning\_settings\_response\_schema**

|Name|Schema|
|---|---|
|**default\_mss**  <br>*optional*|[default\_mss](#default\_mss)|
|**enable\_connection\_timeout**  <br>*optional*|[enable\_connection\_timeout](#enable\_connection\_timeout)|
|**idle\_timeout**  <br>*optional*|[idle\_timeout](#idle\_timeout)|
|**maximum\_mss**  <br>*optional*|[maximum\_mss](#maximum\_mss)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|






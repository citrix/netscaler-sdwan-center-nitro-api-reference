# enable\_polling


<a name="overview"></a>
## Overview
To enable/disable polling on Virtual WAN Appliances for statistics


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config/  
*Schemes* : HTTP


### Tags

* enable\_polling : Operations related to enable\_polling 




<a name="paths"></a>
## Paths

<a name="enable\_polling-post"></a>
### POST operation for enable\_polling
```
POST /enable_polling
```


#### Description
To enable/disable polling on Virtual WAN Appliances for statistics


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[enable\_polling\_request\_schema](#enable\_polling\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[enable\_polling\_post\_success\_schema](#enable\_polling\_post\_success\_schema)|
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

* enable\_polling




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="enable\_polling"></a>
### enable\_polling

|Name|Schema|
|---|---|
|**poll**  <br>*optional*|[poll](#poll)|
|**region\_name**  <br>*optional*|[region\_name](#region\_name)|
|**site**  <br>*optional*|[site](#site)|


<a name="enable\_polling\_delete\_success\_schema"></a>
### enable\_polling\_delete\_success\_schema

|Name|Schema|
|---|---|
|**enable\_polling**  <br>*optional*|[enable\_polling](#enable\_polling\_delete\_success\_schema-enable\_polling)|

<a name="enable\_polling\_delete\_success\_schema-enable\_polling"></a>
**enable\_polling**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="enable\_polling\_post\_success\_schema"></a>
### enable\_polling\_post\_success\_schema

|Name|Schema|
|---|---|
|**enable\_polling**  <br>*optional*|[enable\_polling](#enable\_polling\_post\_success\_schema-enable\_polling)|

<a name="enable\_polling\_post\_success\_schema-enable\_polling"></a>
**enable\_polling**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="enable\_polling\_put\_success\_schema"></a>
### enable\_polling\_put\_success\_schema

|Name|Schema|
|---|---|
|**enable\_polling**  <br>*optional*|[enable\_polling](#enable\_polling\_put\_success\_schema-enable\_polling)|

<a name="enable\_polling\_put\_success\_schema-enable\_polling"></a>
**enable\_polling**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="enable\_polling\_request\_schema"></a>
### enable\_polling\_request\_schema

|Name|Schema|
|---|---|
|**enable\_polling**  <br>*optional*|[enable\_polling](#enable\_polling)|


<a name="enable\_polling\_response\_schema"></a>
### enable\_polling\_response\_schema
*Type* : < [enable\_polling\_response\_schema](#enable\_polling\_response\_schema-inline) > array

<a name="enable\_polling\_response\_schema-inline"></a>
**enable\_polling\_response\_schema**

|Name|Schema|
|---|---|
|**poll**  <br>*optional*|[poll](#poll)|
|**region\_name**  <br>*optional*|[region\_name](#region\_name)|
|**site**  <br>*optional*|[site](#site)|


<a name="poll"></a>
### poll
Set to true to enable polling on a Virtual WAN appliance

*Type* : boolean


<a name="region\_name"></a>
### region\_name
Region name. The selection allows the corresponding region collector to poll the appliance.

*Type* : string


<a name="site"></a>
### site
Site name

*Type* : string






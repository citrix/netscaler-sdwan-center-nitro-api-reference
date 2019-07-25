# dynamic\_virtual\_path\_default\_set\_advanced\_settings


<a name="overview"></a>
## Overview
API to modify, get Dynamic Virtual Path Default Set Advanced settings


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* dynamic\_virtual\_path\_default\_set\_advanced\_settings : Operations related to dynamic\_virtual\_path\_default\_set\_advanced\_settings 




<a name="paths"></a>
## Paths

<a name="dynamic\_virtual\_path\_default\_set\_advanced\_settings-get"></a>
### Get operation for dynamic\_virtual\_path\_default\_set\_advanced\_settings
```
GET /dynamic_virtual_path_default_set_advanced_settings
```


#### Description
Use this operation to get the Dynamic Virtual Path Default Set Advanced settings


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[dynamic\_virtual\_path\_default\_set\_advanced\_settings\_response\_schema](#dynamic\_virtual\_path\_default\_set\_advanced\_settings\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* dynamic\_virtual\_path\_default\_set\_advanced\_settings


<a name="dynamic\_virtual\_path\_default\_set\_advanced\_settings-put"></a>
### PUT operation for dynamic\_virtual\_path\_default\_set\_advanced\_settings
```
PUT /dynamic_virtual_path_default_set_advanced_settings
```


#### Description
Use this operation to modify Dynamic Virtual Path Default Set Advanced settings


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[dynamic\_virtual\_path\_default\_set\_advanced\_settings\_request\_schema](#dynamic\_virtual\_path\_default\_set\_advanced\_settings\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[dynamic\_virtual\_path\_default\_set\_advanced\_settings\_put\_success\_schema](#dynamic\_virtual\_path\_default\_set\_advanced\_settings\_put\_success\_schema)|
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

* dynamic\_virtual\_path\_default\_set\_advanced\_settings




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="dynamic\_virtual\_path\_default\_set\_advanced\_settings"></a>
### dynamic\_virtual\_path\_default\_set\_advanced\_settings

|Name|Schema|
|---|---|
|**id**  <br>*optional*|[id](#id)|
|**override\_global\_on\_demand\_bandwidth\_limit**  <br>*optional*|[override\_global\_on\_demand\_bandwidth\_limit](#override\_global\_on\_demand\_bandwidth\_limit)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**standby\_bandwidth\_threshold\_percentage**  <br>*optional*|[standby\_bandwidth\_threshold\_percentage](#standby\_bandwidth\_threshold\_percentage)|


<a name="dynamic\_virtual\_path\_default\_set\_advanced\_settings\_delete\_success\_schema"></a>
### dynamic\_virtual\_path\_default\_set\_advanced\_settings\_delete\_success\_schema

|Name|Schema|
|---|---|
|**dynamic\_virtual\_path\_default\_set\_advanced\_settings**  <br>*optional*|[dynamic\_virtual\_path\_default\_set\_advanced\_settings](#dynamic\_virtual\_path\_default\_set\_advanced\_settings\_delete\_success\_schema-dynamic\_virtual\_path\_default\_set\_advanced\_settings)|

<a name="dynamic\_virtual\_path\_default\_set\_advanced\_settings\_delete\_success\_schema-dynamic\_virtual\_path\_default\_set\_advanced\_settings"></a>
**dynamic\_virtual\_path\_default\_set\_advanced\_settings**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="dynamic\_virtual\_path\_default\_set\_advanced\_settings\_post\_success\_schema"></a>
### dynamic\_virtual\_path\_default\_set\_advanced\_settings\_post\_success\_schema

|Name|Schema|
|---|---|
|**dynamic\_virtual\_path\_default\_set\_advanced\_settings**  <br>*optional*|[dynamic\_virtual\_path\_default\_set\_advanced\_settings](#dynamic\_virtual\_path\_default\_set\_advanced\_settings\_post\_success\_schema-dynamic\_virtual\_path\_default\_set\_advanced\_settings)|

<a name="dynamic\_virtual\_path\_default\_set\_advanced\_settings\_post\_success\_schema-dynamic\_virtual\_path\_default\_set\_advanced\_settings"></a>
**dynamic\_virtual\_path\_default\_set\_advanced\_settings**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="dynamic\_virtual\_path\_default\_set\_advanced\_settings\_put\_success\_schema"></a>
### dynamic\_virtual\_path\_default\_set\_advanced\_settings\_put\_success\_schema

|Name|Schema|
|---|---|
|**dynamic\_virtual\_path\_default\_set\_advanced\_settings**  <br>*optional*|[dynamic\_virtual\_path\_default\_set\_advanced\_settings](#dynamic\_virtual\_path\_default\_set\_advanced\_settings\_put\_success\_schema-dynamic\_virtual\_path\_default\_set\_advanced\_settings)|

<a name="dynamic\_virtual\_path\_default\_set\_advanced\_settings\_put\_success\_schema-dynamic\_virtual\_path\_default\_set\_advanced\_settings"></a>
**dynamic\_virtual\_path\_default\_set\_advanced\_settings**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="dynamic\_virtual\_path\_default\_set\_advanced\_settings\_request\_schema"></a>
### dynamic\_virtual\_path\_default\_set\_advanced\_settings\_request\_schema

|Name|Schema|
|---|---|
|**dynamic\_virtual\_path\_default\_set\_advanced\_settings**  <br>*optional*|[dynamic\_virtual\_path\_default\_set\_advanced\_settings](#dynamic\_virtual\_path\_default\_set\_advanced\_settings)|


<a name="dynamic\_virtual\_path\_default\_set\_advanced\_settings\_response\_schema"></a>
### dynamic\_virtual\_path\_default\_set\_advanced\_settings\_response\_schema
*Type* : < [dynamic\_virtual\_path\_default\_set\_advanced\_settings\_response\_schema](#dynamic\_virtual\_path\_default\_set\_advanced\_settings\_response\_schema-inline) > array

<a name="dynamic\_virtual\_path\_default\_set\_advanced\_settings\_response\_schema-inline"></a>
**dynamic\_virtual\_path\_default\_set\_advanced\_settings\_response\_schema**

|Name|Schema|
|---|---|
|**dynamic\_virtual\_path\_default\_set\_name**  <br>*optional*|[dynamic\_virtual\_path\_default\_set\_name](#dynamic\_virtual\_path\_default\_set\_name)|
|**id**  <br>*optional*|[id](#id)|
|**override\_global\_on\_demand\_bandwidth\_limit**  <br>*optional*|[override\_global\_on\_demand\_bandwidth\_limit](#override\_global\_on\_demand\_bandwidth\_limit)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**standby\_bandwidth\_threshold\_percentage**  <br>*optional*|[standby\_bandwidth\_threshold\_percentage](#standby\_bandwidth\_threshold\_percentage)|


<a name="dynamic\_virtual\_path\_default\_set\_name"></a>
### dynamic\_virtual\_path\_default\_set\_name
Virtual path default set name using which the API operation should be performed.

*Type* : string


<a name="id"></a>
### id
Auto-generated ID to uniquely identify Virtual Path Default Set Advanced setting

*Type* : integer


<a name="override\_global\_on\_demand\_bandwidth\_limit"></a>
### override\_global\_on\_demand\_bandwidth\_limit
Override the global on-demand bandwidth limit value for the Virtual Path

*Type* : boolean


<a name="package\_name"></a>
### package\_name
Config package name using which the API operation should be performed.

*Type* : string


<a name="standby\_bandwidth\_threshold\_percentage"></a>
### standby\_bandwidth\_threshold\_percentage
On-Demand standby links will not be activated when the WAN-to-LAN bandwidth exceeds this limit.

*Type* : integer






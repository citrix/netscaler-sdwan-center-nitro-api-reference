# proxy\_auto\_config\_file\_settings


<a name="overview"></a>
## Overview
API to get, modify global Proxy auto-config File Settings.


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* proxy\_auto\_config\_file\_settings : Operations related to proxy\_auto\_config\_file\_settings 




<a name="paths"></a>
## Paths

<a name="proxy\_auto\_config\_file\_settings-get"></a>
### Get operation for proxy\_auto\_config\_file\_settings
```
GET /proxy_auto_config_file_settings
```


#### Description
Use this operation to get the current values of Proxy auto-config file settings


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[proxy\_auto\_config\_file\_settings\_response\_schema](#proxy\_auto\_config\_file\_settings\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* proxy\_auto\_config\_file\_settings


<a name="proxy\_auto\_config\_file\_settings-put"></a>
### PUT operation for proxy\_auto\_config\_file\_settings
```
PUT /proxy_auto_config_file_settings
```


#### Description
Use this operation to modify the current values of Proxy auto-config file settings


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[proxy\_auto\_config\_file\_settings\_request\_schema](#proxy\_auto\_config\_file\_settings\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[proxy\_auto\_config\_file\_settings\_put\_success\_schema](#proxy\_auto\_config\_file\_settings\_put\_success\_schema)|
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

* proxy\_auto\_config\_file\_settings




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="enable\_pac\_file\_customization"></a>
### enable\_pac\_file\_customization
Set to true to enable Proxy auto-config file settings for Office 365 URLs.

*Type* : boolean


<a name="pac\_file\_url"></a>
### pac\_file\_url
Proxy Auto Config file URL.

*Type* : string


<a name="package\_name"></a>
### package\_name
Config package name using which the API operation should be performed.

*Type* : string


<a name="proxy\_auto\_config\_file\_settings"></a>
### proxy\_auto\_config\_file\_settings

|Name|Schema|
|---|---|
|**enable\_pac\_file\_customization**  <br>*optional*|[enable\_pac\_file\_customization](#enable\_pac\_file\_customization)|
|**pac\_file\_url**  <br>*optional*|[pac\_file\_url](#pac\_file\_url)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|


<a name="proxy\_auto\_config\_file\_settings\_delete\_success\_schema"></a>
### proxy\_auto\_config\_file\_settings\_delete\_success\_schema

|Name|Schema|
|---|---|
|**proxy\_auto\_config\_file\_settings**  <br>*optional*|[proxy\_auto\_config\_file\_settings](#proxy\_auto\_config\_file\_settings\_delete\_success\_schema-proxy\_auto\_config\_file\_settings)|

<a name="proxy\_auto\_config\_file\_settings\_delete\_success\_schema-proxy\_auto\_config\_file\_settings"></a>
**proxy\_auto\_config\_file\_settings**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="proxy\_auto\_config\_file\_settings\_post\_success\_schema"></a>
### proxy\_auto\_config\_file\_settings\_post\_success\_schema

|Name|Schema|
|---|---|
|**proxy\_auto\_config\_file\_settings**  <br>*optional*|[proxy\_auto\_config\_file\_settings](#proxy\_auto\_config\_file\_settings\_post\_success\_schema-proxy\_auto\_config\_file\_settings)|

<a name="proxy\_auto\_config\_file\_settings\_post\_success\_schema-proxy\_auto\_config\_file\_settings"></a>
**proxy\_auto\_config\_file\_settings**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="proxy\_auto\_config\_file\_settings\_put\_success\_schema"></a>
### proxy\_auto\_config\_file\_settings\_put\_success\_schema

|Name|Schema|
|---|---|
|**proxy\_auto\_config\_file\_settings**  <br>*optional*|[proxy\_auto\_config\_file\_settings](#proxy\_auto\_config\_file\_settings\_put\_success\_schema-proxy\_auto\_config\_file\_settings)|

<a name="proxy\_auto\_config\_file\_settings\_put\_success\_schema-proxy\_auto\_config\_file\_settings"></a>
**proxy\_auto\_config\_file\_settings**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="proxy\_auto\_config\_file\_settings\_request\_schema"></a>
### proxy\_auto\_config\_file\_settings\_request\_schema

|Name|Schema|
|---|---|
|**proxy\_auto\_config\_file\_settings**  <br>*optional*|[proxy\_auto\_config\_file\_settings](#proxy\_auto\_config\_file\_settings)|


<a name="proxy\_auto\_config\_file\_settings\_response\_schema"></a>
### proxy\_auto\_config\_file\_settings\_response\_schema
*Type* : < [proxy\_auto\_config\_file\_settings\_response\_schema](#proxy\_auto\_config\_file\_settings\_response\_schema-inline) > array

<a name="proxy\_auto\_config\_file\_settings\_response\_schema-inline"></a>
**proxy\_auto\_config\_file\_settings\_response\_schema**

|Name|Schema|
|---|---|
|**enable\_pac\_file\_customization**  <br>*optional*|[enable\_pac\_file\_customization](#enable\_pac\_file\_customization)|
|**pac\_file\_url**  <br>*optional*|[pac\_file\_url](#pac\_file\_url)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|






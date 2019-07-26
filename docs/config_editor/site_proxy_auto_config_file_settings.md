# site\_proxy\_auto\_config\_file\_settings


<a name="overview"></a>
## Overview
API to get, modify Proxy auto-config file Settings at site level.


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* site\_proxy\_auto\_config\_file\_settings : Operations related to site\_proxy\_auto\_config\_file\_settings 




<a name="paths"></a>
## Paths

<a name="site\_proxy\_auto\_config\_file\_settings-get"></a>
### Get operation for site\_proxy\_auto\_config\_file\_settings
```
GET /site_proxy_auto_config_file_settings
```


#### Description
Use this operation to get the current values of Proxy auto-config file settings


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[site\_proxy\_auto\_config\_file\_settings\_response\_schema](#site\_proxy\_auto\_config\_file\_settings\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* site\_proxy\_auto\_config\_file\_settings


<a name="site\_proxy\_auto\_config\_file\_settings-put"></a>
### PUT operation for site\_proxy\_auto\_config\_file\_settings
```
PUT /site_proxy_auto_config_file_settings
```


#### Description
Use this operation to modify the current values of Proxy auto-config file settings


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[site\_proxy\_auto\_config\_file\_settings\_request\_schema](#site\_proxy\_auto\_config\_file\_settings\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[site\_proxy\_auto\_config\_file\_settings\_put\_success\_schema](#site\_proxy\_auto\_config\_file\_settings\_put\_success\_schema)|
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

* site\_proxy\_auto\_config\_file\_settings




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


<a name="override\_global\_pac\_file\_settings"></a>
### override\_global\_pac\_file\_settings
Set to true to override global Proxy auto-config file settings.

*Type* : boolean


<a name="pac\_file\_url"></a>
### pac\_file\_url
Proxy auto-config file URL.

*Type* : string


<a name="package\_name"></a>
### package\_name
Config package name using which the API operation should be performed.

*Type* : string


<a name="site\_name"></a>
### site\_name
Site Name

*Type* : string


<a name="site\_proxy\_auto\_config\_file\_settings"></a>
### site\_proxy\_auto\_config\_file\_settings

|Name|Schema|
|---|---|
|**enable\_pac\_file\_customization**  <br>*optional*|[enable\_pac\_file\_customization](#enable\_pac\_file\_customization)|
|**override\_global\_pac\_file\_settings**  <br>*optional*|[override\_global\_pac\_file\_settings](#override\_global\_pac\_file\_settings)|
|**pac\_file\_url**  <br>*optional*|[pac\_file\_url](#pac\_file\_url)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|


<a name="site\_proxy\_auto\_config\_file\_settings\_delete\_success\_schema"></a>
### site\_proxy\_auto\_config\_file\_settings\_delete\_success\_schema

|Name|Schema|
|---|---|
|**site\_proxy\_auto\_config\_file\_settings**  <br>*optional*|[site\_proxy\_auto\_config\_file\_settings](#site\_proxy\_auto\_config\_file\_settings\_delete\_success\_schema-site\_proxy\_auto\_config\_file\_settings)|

<a name="site\_proxy\_auto\_config\_file\_settings\_delete\_success\_schema-site\_proxy\_auto\_config\_file\_settings"></a>
**site\_proxy\_auto\_config\_file\_settings**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="site\_proxy\_auto\_config\_file\_settings\_post\_success\_schema"></a>
### site\_proxy\_auto\_config\_file\_settings\_post\_success\_schema

|Name|Schema|
|---|---|
|**site\_proxy\_auto\_config\_file\_settings**  <br>*optional*|[site\_proxy\_auto\_config\_file\_settings](#site\_proxy\_auto\_config\_file\_settings\_post\_success\_schema-site\_proxy\_auto\_config\_file\_settings)|

<a name="site\_proxy\_auto\_config\_file\_settings\_post\_success\_schema-site\_proxy\_auto\_config\_file\_settings"></a>
**site\_proxy\_auto\_config\_file\_settings**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="site\_proxy\_auto\_config\_file\_settings\_put\_success\_schema"></a>
### site\_proxy\_auto\_config\_file\_settings\_put\_success\_schema

|Name|Schema|
|---|---|
|**site\_proxy\_auto\_config\_file\_settings**  <br>*optional*|[site\_proxy\_auto\_config\_file\_settings](#site\_proxy\_auto\_config\_file\_settings\_put\_success\_schema-site\_proxy\_auto\_config\_file\_settings)|

<a name="site\_proxy\_auto\_config\_file\_settings\_put\_success\_schema-site\_proxy\_auto\_config\_file\_settings"></a>
**site\_proxy\_auto\_config\_file\_settings**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="site\_proxy\_auto\_config\_file\_settings\_request\_schema"></a>
### site\_proxy\_auto\_config\_file\_settings\_request\_schema

|Name|Schema|
|---|---|
|**site\_proxy\_auto\_config\_file\_settings**  <br>*optional*|[site\_proxy\_auto\_config\_file\_settings](#site\_proxy\_auto\_config\_file\_settings)|


<a name="site\_proxy\_auto\_config\_file\_settings\_response\_schema"></a>
### site\_proxy\_auto\_config\_file\_settings\_response\_schema
*Type* : < [site\_proxy\_auto\_config\_file\_settings\_response\_schema](#site\_proxy\_auto\_config\_file\_settings\_response\_schema-inline) > array

<a name="site\_proxy\_auto\_config\_file\_settings\_response\_schema-inline"></a>
**site\_proxy\_auto\_config\_file\_settings\_response\_schema**

|Name|Schema|
|---|---|
|**enable\_pac\_file\_customization**  <br>*optional*|[enable\_pac\_file\_customization](#enable\_pac\_file\_customization)|
|**override\_global\_pac\_file\_settings**  <br>*optional*|[override\_global\_pac\_file\_settings](#override\_global\_pac\_file\_settings)|
|**pac\_file\_url**  <br>*optional*|[pac\_file\_url](#pac\_file\_url)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|






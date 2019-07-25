# site\_routing\_domain


<a name="overview"></a>
## Overview
API to get and modify site routing domains.


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* site\_routing\_domain : Operations related to site\_routing\_domain 




<a name="paths"></a>
## Paths

<a name="site\_routing\_domain-get"></a>
### Get operation for site\_routing\_domain
```
GET /site_routing_domain
```


#### Description
Use this operation to get the list of site routing domains


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[site\_routing\_domain\_response\_schema](#site\_routing\_domain\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* site\_routing\_domain


<a name="site\_routing\_domain-put"></a>
### PUT operation for site\_routing\_domain
```
PUT /site_routing_domain
```


#### Description
Use this operation to modify properties of site routing domain


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[site\_routing\_domain\_request\_schema](#site\_routing\_domain\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[site\_routing\_domain\_put\_success\_schema](#site\_routing\_domain\_put\_success\_schema)|
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

* site\_routing\_domain




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="name"></a>
### name
Site Routing Domain

*Type* : string


<a name="package\_name"></a>
### package\_name
Config package name using which the site API operation should be performed.

*Type* : string


<a name="site\_name"></a>
### site\_name
Site Name

*Type* : string


<a name="site\_routing\_domain"></a>
### site\_routing\_domain

|Name|Schema|
|---|---|
|**name**  <br>*optional*|[name](#name)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**site\_routing\_domain\_properties**  <br>*optional*|[site\_routing\_domain\_properties](#site\_routing\_domain\_properties)|


<a name="site\_routing\_domain\_delete\_success\_schema"></a>
### site\_routing\_domain\_delete\_success\_schema

|Name|Schema|
|---|---|
|**site\_routing\_domain**  <br>*optional*|[site\_routing\_domain](#site\_routing\_domain\_delete\_success\_schema-site\_routing\_domain)|

<a name="site\_routing\_domain\_delete\_success\_schema-site\_routing\_domain"></a>
**site\_routing\_domain**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="site\_routing\_domain\_post\_success\_schema"></a>
### site\_routing\_domain\_post\_success\_schema

|Name|Schema|
|---|---|
|**site\_routing\_domain**  <br>*optional*|[site\_routing\_domain](#site\_routing\_domain\_post\_success\_schema-site\_routing\_domain)|

<a name="site\_routing\_domain\_post\_success\_schema-site\_routing\_domain"></a>
**site\_routing\_domain**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="site\_routing\_domain\_properties"></a>
### site\_routing\_domain\_properties
Site Routing Domain properties

*Type* : < [site\_routing\_domain\_properties](#site\_routing\_domain\_properties-inline) > array

<a name="site\_routing\_domain\_properties-inline"></a>
**site\_routing\_domain\_properties**

|Name|Description|Schema|
|---|---|---|
|**enabled**  <br>*optional*|enable/disable routing domain to be available for the site  <br>**Default** : `true`|boolean|
|**is\_default**  <br>*optional*|enable/disable routing domain as default domain for the site  <br>**Default** : `false`|boolean|
|**redirect\_to\_wanop**  <br>*optional*|enable/disable optimizing of routing domain traffic  <br>**Default** : `false`|boolean|


<a name="site\_routing\_domain\_put\_success\_schema"></a>
### site\_routing\_domain\_put\_success\_schema

|Name|Schema|
|---|---|
|**site\_routing\_domain**  <br>*optional*|[site\_routing\_domain](#site\_routing\_domain\_put\_success\_schema-site\_routing\_domain)|

<a name="site\_routing\_domain\_put\_success\_schema-site\_routing\_domain"></a>
**site\_routing\_domain**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="site\_routing\_domain\_request\_schema"></a>
### site\_routing\_domain\_request\_schema

|Name|Schema|
|---|---|
|**site\_routing\_domain**  <br>*optional*|[site\_routing\_domain](#site\_routing\_domain)|


<a name="site\_routing\_domain\_response\_schema"></a>
### site\_routing\_domain\_response\_schema
*Type* : < [site\_routing\_domain\_response\_schema](#site\_routing\_domain\_response\_schema-inline) > array

<a name="site\_routing\_domain\_response\_schema-inline"></a>
**site\_routing\_domain\_response\_schema**

|Name|Schema|
|---|---|
|**name**  <br>*optional*|[name](#name)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**site\_routing\_domain\_properties**  <br>*optional*|[site\_routing\_domain\_properties](#site\_routing\_domain\_properties)|






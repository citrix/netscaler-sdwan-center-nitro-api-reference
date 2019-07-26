# site


<a name="overview"></a>
## Overview
API to add, modify, delete, and get sites.


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* site : Operations related to site 




<a name="paths"></a>
## Paths

<a name="site-post"></a>
### POST operation for site
```
POST /site
```


#### Description
Use this operation to add site


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[site\_request\_schema](#site\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[site\_post\_success\_schema](#site\_post\_success\_schema)|
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

* site


<a name="site-get"></a>
### Get operation for site
```
GET /site
```


#### Description
Use this operation to get the list of sites


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[site\_response\_schema](#site\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* site


<a name="site-put"></a>
### PUT operation for site
```
PUT /site
```


#### Description
Use this operation to modify site


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[site\_put\_success\_schema](#site\_put\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* site


<a name="site-deletepathparam-delete"></a>
### DELETE operation for site
```
DELETE /site/{deletePathParam}
```


#### Description
Use this operation to delete a site


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[site\_delete\_success\_schema](#site\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* site




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="mode"></a>
### mode
Operating mode of this site

*Type* : enum (primary\_mcn, secondary\_mcn, primary\_rcn, secondary\_rcn, client)


<a name="model"></a>
### model
site model

*Type* : enum (cb210, cb400, cb410, cb1000, cb2000, cb2100, cb4000, cb4100, cb5100, cbvpx, cbvpxl)


<a name="package\_name"></a>
### package\_name
Config package name using which the site API operation should be performed.

*Type* : string


<a name="persist\_ucast\_refresh\_time\_ms"></a>
### persist\_ucast\_refresh\_time\_ms
Gateway ARP Timer: (ms)

*Type* : integer


<a name="region"></a>
### region
Region to which the site belongs to

*Type* : string


<a name="secure\_key"></a>
### secure\_key
Hexadecimal secure key used for encryption and membership verification in the Virtual WAN network. This field is optional. If the value is not provided, API generates the secure key.

*Type* : string


<a name="site"></a>
### site

|Name|Schema|
|---|---|
|**mode**  <br>*optional*|[mode](#mode)|
|**model**  <br>*optional*|[model](#model)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**persist\_ucast\_refresh\_time\_ms**  <br>*optional*|[persist\_ucast\_refresh\_time\_ms](#persist\_ucast\_refresh\_time\_ms)|
|**region**  <br>*optional*|[region](#region)|
|**secure\_key**  <br>*optional*|[secure\_key](#secure\_key)|
|**site\_location**  <br>*optional*|[site\_location](#site\_location)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**user\_ucast\_refresh\_time\_ms**  <br>*optional*|[user\_ucast\_refresh\_time\_ms](#user\_ucast\_refresh\_time\_ms)|


<a name="site\_delete\_success\_schema"></a>
### site\_delete\_success\_schema

|Name|Schema|
|---|---|
|**site**  <br>*optional*|[site](#site\_delete\_success\_schema-site)|

<a name="site\_delete\_success\_schema-site"></a>
**site**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="site\_location"></a>
### site\_location
Site location.

*Type* : string


<a name="site\_name"></a>
### site\_name
Site Name

*Type* : string


<a name="site\_post\_success\_schema"></a>
### site\_post\_success\_schema

|Name|Schema|
|---|---|
|**site**  <br>*optional*|[site](#site\_post\_success\_schema-site)|

<a name="site\_post\_success\_schema-site"></a>
**site**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="site\_put\_success\_schema"></a>
### site\_put\_success\_schema

|Name|Schema|
|---|---|
|**site**  <br>*optional*|[site](#site\_put\_success\_schema-site)|

<a name="site\_put\_success\_schema-site"></a>
**site**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="site\_request\_schema"></a>
### site\_request\_schema

|Name|Schema|
|---|---|
|**site**  <br>*optional*|[site](#site)|


<a name="site\_response\_schema"></a>
### site\_response\_schema
*Type* : < [site\_response\_schema](#site\_response\_schema-inline) > array

<a name="site\_response\_schema-inline"></a>
**site\_response\_schema**

|Name|Schema|
|---|---|
|**mode**  <br>*optional*|[mode](#mode)|
|**model**  <br>*optional*|[model](#model)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**persist\_ucast\_refresh\_time\_ms**  <br>*optional*|[persist\_ucast\_refresh\_time\_ms](#persist\_ucast\_refresh\_time\_ms)|
|**region**  <br>*optional*|[region](#region)|
|**secure\_key**  <br>*optional*|[secure\_key](#secure\_key)|
|**site\_location**  <br>*optional*|[site\_location](#site\_location)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**user\_ucast\_refresh\_time\_ms**  <br>*optional*|[user\_ucast\_refresh\_time\_ms](#user\_ucast\_refresh\_time\_ms)|


<a name="user\_ucast\_refresh\_time\_ms"></a>
### user\_ucast\_refresh\_time\_ms
Host ARP Timer: (ms)

*Type* : integer






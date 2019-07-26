# centralized\_licensing\_site


<a name="overview"></a>
## Overview
API to modify, get, site settings for centralized licensing for sites


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* centralized\_licensing\_site : Operations related to centralized\_licensing\_site 




<a name="paths"></a>
## Paths

<a name="centralized\_licensing\_site-get"></a>
### Get operation for centralized\_licensing\_site
```
GET /centralized_licensing_site
```


#### Description
Use this operation to get the centralized licensing settings for this site


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[centralized\_licensing\_site\_response\_schema](#centralized\_licensing\_site\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* centralized\_licensing\_site


<a name="centralized\_licensing\_site-put"></a>
### PUT operation for centralized\_licensing\_site
```
PUT /centralized_licensing_site
```


#### Description
Use this operation to modify the centralized licensing settings for this site


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[centralized\_licensing\_site\_request\_schema](#centralized\_licensing\_site\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[centralized\_licensing\_site\_put\_success\_schema](#centralized\_licensing\_site\_put\_success\_schema)|
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

* centralized\_licensing\_site




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="appliance\_edition"></a>
### appliance\_edition
Edition of the appliance. SE is Stanadard Edition, EE is Enterprise Edition, PER-HOUR is on an hourly basis

*Type* : enum (SE, EE, PER-HOUR)


<a name="centralized\_licensing\_site"></a>
### centralized\_licensing\_site

|Name|Schema|
|---|---|
|**appliance\_edition**  <br>*optional*|[appliance\_edition](#appliance\_edition)|
|**license\_rate**  <br>*optional*|[license\_rate](#license\_rate)|
|**license\_server\_location**  <br>*optional*|[license\_server\_location](#license\_server\_location)|
|**override\_global**  <br>*optional*|[override\_global](#override\_global)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**remote\_server\_ip**  <br>*optional*|[remote\_server\_ip](#remote\_server\_ip)|
|**remote\_server\_port**  <br>*optional*|[remote\_server\_port](#remote\_server\_port)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|


<a name="centralized\_licensing\_site\_delete\_success\_schema"></a>
### centralized\_licensing\_site\_delete\_success\_schema

|Name|Schema|
|---|---|
|**centralized\_licensing\_site**  <br>*optional*|[centralized\_licensing\_site](#centralized\_licensing\_site\_delete\_success\_schema-centralized\_licensing\_site)|

<a name="centralized\_licensing\_site\_delete\_success\_schema-centralized\_licensing\_site"></a>
**centralized\_licensing\_site**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="centralized\_licensing\_site\_post\_success\_schema"></a>
### centralized\_licensing\_site\_post\_success\_schema

|Name|Schema|
|---|---|
|**centralized\_licensing\_site**  <br>*optional*|[centralized\_licensing\_site](#centralized\_licensing\_site\_post\_success\_schema-centralized\_licensing\_site)|

<a name="centralized\_licensing\_site\_post\_success\_schema-centralized\_licensing\_site"></a>
**centralized\_licensing\_site**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="centralized\_licensing\_site\_put\_success\_schema"></a>
### centralized\_licensing\_site\_put\_success\_schema

|Name|Schema|
|---|---|
|**centralized\_licensing\_site**  <br>*optional*|[centralized\_licensing\_site](#centralized\_licensing\_site\_put\_success\_schema-centralized\_licensing\_site)|

<a name="centralized\_licensing\_site\_put\_success\_schema-centralized\_licensing\_site"></a>
**centralized\_licensing\_site**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="centralized\_licensing\_site\_request\_schema"></a>
### centralized\_licensing\_site\_request\_schema

|Name|Schema|
|---|---|
|**centralized\_licensing\_site**  <br>*optional*|[centralized\_licensing\_site](#centralized\_licensing\_site)|


<a name="centralized\_licensing\_site\_response\_schema"></a>
### centralized\_licensing\_site\_response\_schema
*Type* : < [centralized\_licensing\_site\_response\_schema](#centralized\_licensing\_site\_response\_schema-inline) > array

<a name="centralized\_licensing\_site\_response\_schema-inline"></a>
**centralized\_licensing\_site\_response\_schema**

|Name|Schema|
|---|---|
|**appliance\_edition**  <br>*optional*|[appliance\_edition](#appliance\_edition)|
|**license\_rate**  <br>*optional*|[license\_rate](#license\_rate)|
|**license\_server\_location**  <br>*optional*|[license\_server\_location](#license\_server\_location)|
|**override\_global**  <br>*optional*|[override\_global](#override\_global)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**remote\_server\_ip**  <br>*optional*|[remote\_server\_ip](#remote\_server\_ip)|
|**remote\_server\_port**  <br>*optional*|[remote\_server\_port](#remote\_server\_port)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|


<a name="license\_rate"></a>
### license\_rate
License rate

*Type* : enum (10, 20, 50, 100, 150, 200, 250, 300, 500, 1000, 1500, 2000, 3000, 4000, 5000, auto)


<a name="license\_server\_location"></a>
### license\_server\_location
The location of the license server

*Type* : enum (LOCAL, CENTRAL)


<a name="override\_global"></a>
### override\_global
enable/disable overriding global centralized licensing settings

*Type* : boolean


<a name="package\_name"></a>
### package\_name
Config package name using which the centralized licensing operation should be performed.

*Type* : string


<a name="remote\_server\_ip"></a>
### remote\_server\_ip
Remote licensing server ip address

*Type* : string


<a name="remote\_server\_port"></a>
### remote\_server\_port
Remote server port

*Type* : integer


<a name="site\_name"></a>
### site\_name
Site Name for which centralized licensing properties need to be set

*Type* : string






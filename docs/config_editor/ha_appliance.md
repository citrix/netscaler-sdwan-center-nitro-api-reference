# ha\_appliance


<a name="overview"></a>
## Overview
API to add, get and modify HA Appliance.


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* ha\_appliance : Operations related to ha\_appliance 




<a name="paths"></a>
## Paths

<a name="ha\_appliance-get"></a>
### Get operation for ha\_appliance
```
GET /ha_appliance
```


#### Description
Use this operation to get HA Appliance


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[ha\_appliance\_response\_schema](#ha\_appliance\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* ha\_appliance


<a name="ha\_appliance-put"></a>
### PUT operation for ha\_appliance
```
PUT /ha_appliance
```


#### Description
Use this operation to modify HA Appliance


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[ha\_appliance\_request\_schema](#ha\_appliance\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[ha\_appliance\_put\_success\_schema](#ha\_appliance\_put\_success\_schema)|
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

* ha\_appliance




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="ha\_appliance"></a>
### ha\_appliance

|Name|Schema|
|---|---|
|**name**  <br>*optional*|[name](#name)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|


<a name="ha\_appliance\_delete\_success\_schema"></a>
### ha\_appliance\_delete\_success\_schema

|Name|Schema|
|---|---|
|**ha\_appliance**  <br>*optional*|[ha\_appliance](#ha\_appliance\_delete\_success\_schema-ha\_appliance)|

<a name="ha\_appliance\_delete\_success\_schema-ha\_appliance"></a>
**ha\_appliance**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="ha\_appliance\_post\_success\_schema"></a>
### ha\_appliance\_post\_success\_schema

|Name|Schema|
|---|---|
|**ha\_appliance**  <br>*optional*|[ha\_appliance](#ha\_appliance\_post\_success\_schema-ha\_appliance)|

<a name="ha\_appliance\_post\_success\_schema-ha\_appliance"></a>
**ha\_appliance**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="ha\_appliance\_put\_success\_schema"></a>
### ha\_appliance\_put\_success\_schema

|Name|Schema|
|---|---|
|**ha\_appliance**  <br>*optional*|[ha\_appliance](#ha\_appliance\_put\_success\_schema-ha\_appliance)|

<a name="ha\_appliance\_put\_success\_schema-ha\_appliance"></a>
**ha\_appliance**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="ha\_appliance\_request\_schema"></a>
### ha\_appliance\_request\_schema

|Name|Schema|
|---|---|
|**ha\_appliance**  <br>*optional*|[ha\_appliance](#ha\_appliance)|


<a name="ha\_appliance\_response\_schema"></a>
### ha\_appliance\_response\_schema
*Type* : < [ha\_appliance\_response\_schema](#ha\_appliance\_response\_schema-inline) > array

<a name="ha\_appliance\_response\_schema-inline"></a>
**ha\_appliance\_response\_schema**

|Name|Schema|
|---|---|
|**name**  <br>*optional*|[name](#name)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|


<a name="name"></a>
### name
The HA appliance name

*Type* : string


<a name="package\_name"></a>
### package\_name
Config package name using which the site API operation should be performed.

*Type* : string


<a name="site\_name"></a>
### site\_name
Site Name

*Type* : string






# wan\_links\_standby\_mode\_internal


<a name="overview"></a>
## Overview
API to get configuration for wan\_links\_standby\_mode\_internal


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* wan\_links\_standby\_mode\_internal : Operations related to wan\_links\_standby\_mode\_internal 




<a name="paths"></a>
## Paths

<a name="wan\_links\_standby\_mode\_internal-get"></a>
### Get operation for wan\_links\_standby\_mode\_internal
```
GET /wan_links_standby_mode_internal
```


#### Description
Use this operation to get the standby\_mode info for the wan links


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[wan\_links\_standby\_mode\_internal\_response\_schema](#wan\_links\_standby\_mode\_internal\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* wan\_links\_standby\_mode\_internal




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="package\_name"></a>
### package\_name
Config package name using which the ipsec\_tunnel API operation should be performed.

*Type* : string


<a name="site\_name"></a>
### site\_name
site name

*Type* : string


<a name="standby\_mode"></a>
### standby\_mode
Stand by mode value

*Type* : string


<a name="wan\_link\_name"></a>
### wan\_link\_name
Wan link name

*Type* : string


<a name="wan\_links\_standby\_mode\_internal"></a>
### wan\_links\_standby\_mode\_internal

|Name|Schema|
|---|---|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**standby\_mode**  <br>*optional*|[standby\_mode](#standby\_mode)|
|**wan\_link\_name**  <br>*optional*|[wan\_link\_name](#wan\_link\_name)|


<a name="wan\_links\_standby\_mode\_internal\_delete\_success\_schema"></a>
### wan\_links\_standby\_mode\_internal\_delete\_success\_schema

|Name|Schema|
|---|---|
|**wan\_links\_standby\_mode\_internal**  <br>*optional*|[wan\_links\_standby\_mode\_internal](#wan\_links\_standby\_mode\_internal\_delete\_success\_schema-wan\_links\_standby\_mode\_internal)|

<a name="wan\_links\_standby\_mode\_internal\_delete\_success\_schema-wan\_links\_standby\_mode\_internal"></a>
**wan\_links\_standby\_mode\_internal**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="wan\_links\_standby\_mode\_internal\_post\_success\_schema"></a>
### wan\_links\_standby\_mode\_internal\_post\_success\_schema

|Name|Schema|
|---|---|
|**wan\_links\_standby\_mode\_internal**  <br>*optional*|[wan\_links\_standby\_mode\_internal](#wan\_links\_standby\_mode\_internal\_post\_success\_schema-wan\_links\_standby\_mode\_internal)|

<a name="wan\_links\_standby\_mode\_internal\_post\_success\_schema-wan\_links\_standby\_mode\_internal"></a>
**wan\_links\_standby\_mode\_internal**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="wan\_links\_standby\_mode\_internal\_put\_success\_schema"></a>
### wan\_links\_standby\_mode\_internal\_put\_success\_schema

|Name|Schema|
|---|---|
|**wan\_links\_standby\_mode\_internal**  <br>*optional*|[wan\_links\_standby\_mode\_internal](#wan\_links\_standby\_mode\_internal\_put\_success\_schema-wan\_links\_standby\_mode\_internal)|

<a name="wan\_links\_standby\_mode\_internal\_put\_success\_schema-wan\_links\_standby\_mode\_internal"></a>
**wan\_links\_standby\_mode\_internal**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="wan\_links\_standby\_mode\_internal\_request\_schema"></a>
### wan\_links\_standby\_mode\_internal\_request\_schema

|Name|Schema|
|---|---|
|**wan\_links\_standby\_mode\_internal**  <br>*optional*|[wan\_links\_standby\_mode\_internal](#wan\_links\_standby\_mode\_internal)|


<a name="wan\_links\_standby\_mode\_internal\_response\_schema"></a>
### wan\_links\_standby\_mode\_internal\_response\_schema
*Type* : < [wan\_links\_standby\_mode\_internal\_response\_schema](#wan\_links\_standby\_mode\_internal\_response\_schema-inline) > array

<a name="wan\_links\_standby\_mode\_internal\_response\_schema-inline"></a>
**wan\_links\_standby\_mode\_internal\_response\_schema**

|Name|Schema|
|---|---|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**standby\_mode**  <br>*optional*|[standby\_mode](#standby\_mode)|
|**wan\_link\_name**  <br>*optional*|[wan\_link\_name](#wan\_link\_name)|






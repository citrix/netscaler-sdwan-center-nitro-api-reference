# object\_and\_properties


<a name="overview"></a>
## Overview
API to retrieve the available object names and properties which can be retrieved using the monitoring statistics api


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/monitoring/  
*Schemes* : HTTP


### Tags

* object\_and\_properties : Operations related to object\_and\_properties 




<a name="paths"></a>
## Paths

<a name="object\_and\_properties-get"></a>
### Get operation for object\_and\_properties
```
GET /object_and_properties
```


#### Description
Use this operation to get a list of available object names and properties


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[object\_and\_properties\_response\_schema](#object\_and\_properties\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* object\_and\_properties




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="available\_stats"></a>
### available\_stats
The available properties for each type of object

*Type* : < [available\_stats](#available\_stats-inline) > array

<a name="available\_stats-inline"></a>
**available\_stats**

|Name|Description|Schema|
|---|---|---|
|**lan\_to\_wan\_paths**  <br>*optional*  <br>*read-only*|The lan to wan path properties available|< string > array|
|**virtual\_path**  <br>*optional*  <br>*read-only*|The virtual path properties available|< string > array|
|**wan\_link**  <br>*optional*  <br>*read-only*|The wan link properties available|< string > array|
|**wan\_to\_lan\_paths**  <br>*optional*  <br>*read-only*|The wan to lan path properties available|< string > array|


<a name="object\_and\_properties\_delete\_success\_schema"></a>
### object\_and\_properties\_delete\_success\_schema

|Name|Schema|
|---|---|
|**object\_and\_properties**  <br>*optional*|[object\_and\_properties](#object\_and\_properties\_delete\_success\_schema-object\_and\_properties)|

<a name="object\_and\_properties\_delete\_success\_schema-object\_and\_properties"></a>
**object\_and\_properties**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="object\_and\_properties\_post\_success\_schema"></a>
### object\_and\_properties\_post\_success\_schema

|Name|Schema|
|---|---|
|**object\_and\_properties**  <br>*optional*|[object\_and\_properties](#object\_and\_properties\_post\_success\_schema-object\_and\_properties)|

<a name="object\_and\_properties\_post\_success\_schema-object\_and\_properties"></a>
**object\_and\_properties**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="object\_and\_properties\_put\_success\_schema"></a>
### object\_and\_properties\_put\_success\_schema

|Name|Schema|
|---|---|
|**object\_and\_properties**  <br>*optional*|[object\_and\_properties](#object\_and\_properties\_put\_success\_schema-object\_and\_properties)|

<a name="object\_and\_properties\_put\_success\_schema-object\_and\_properties"></a>
**object\_and\_properties**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="object\_and\_properties\_response\_schema"></a>
### object\_and\_properties\_response\_schema
*Type* : < [object\_and\_properties\_response\_schema](#object\_and\_properties\_response\_schema-inline) > array

<a name="object\_and\_properties\_response\_schema-inline"></a>
**object\_and\_properties\_response\_schema**

|Name|Schema|
|---|---|
|**available\_stats**  <br>*optional*|[available\_stats](#available\_stats)|
|**sites**  <br>*optional*|[sites](#sites)|


<a name="sites"></a>
### sites
The site and related object names

*Type* : < [sites](#sites-inline) > array

<a name="sites-inline"></a>
**sites**

|Name|Description|Schema|
|---|---|---|
|**name**  <br>*optional*  <br>*read-only*|The site name|string|
|**virtual\_paths**  <br>*optional*  <br>*read-only*|The virtual path and related path names associated with this site|< [virtual\_paths](#sites-virtual\_paths) > array|
|**wan\_links**  <br>*optional*  <br>*read-only*|The wan link names available for that site|< string > array|

<a name="sites-virtual\_paths"></a>
**virtual\_paths**

|Name|Description|Schema|
|---|---|---|
|**lan\_to\_wan\_paths**  <br>*optional*  <br>*read-only*|The LAN to WAN Path names available for this virtual path|string|
|**name**  <br>*optional*  <br>*read-only*|The virtual path name|string|
|**wan\_to\_lan\_paths**  <br>*optional*  <br>*read-only*|The WAN to LAN Path names available for this virtual path|string|






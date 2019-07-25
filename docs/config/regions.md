# regions


<a name="overview"></a>
## Overview
This resource can be used to get the region discovery configuration.


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config/  
*Schemes* : HTTP


### Tags

* regions : Operations related to regions 




<a name="paths"></a>
## Paths

<a name="regions-get"></a>
### Get operation for regions
```
GET /regions
```


#### Description
Use this operation to get the regions discovery configuration.


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[regions\_response\_schema](#regions\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* regions




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="collector\_ip"></a>
### collector\_ip
The IP address of the collector configured to work with the region

*Type* : string


<a name="region\_control\_node\_ip"></a>
### region\_control\_node\_ip
The primary region control node ip address

*Type* : string


<a name="region\_discovery\_status"></a>
### region\_discovery\_status
The status of discovery by Collector for the region appliances

*Type* : string


<a name="region\_name"></a>
### region\_name
The region name

*Type* : string


<a name="regions\_delete\_success\_schema"></a>
### regions\_delete\_success\_schema

|Name|Schema|
|---|---|
|**regions**  <br>*optional*|[regions](#regions\_delete\_success\_schema-regions)|

<a name="regions\_delete\_success\_schema-regions"></a>
**regions**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="regions\_post\_success\_schema"></a>
### regions\_post\_success\_schema

|Name|Schema|
|---|---|
|**regions**  <br>*optional*|[regions](#regions\_post\_success\_schema-regions)|

<a name="regions\_post\_success\_schema-regions"></a>
**regions**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="regions\_put\_success\_schema"></a>
### regions\_put\_success\_schema

|Name|Schema|
|---|---|
|**regions**  <br>*optional*|[regions](#regions\_put\_success\_schema-regions)|

<a name="regions\_put\_success\_schema-regions"></a>
**regions**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="regions\_response\_schema"></a>
### regions\_response\_schema
*Type* : < [regions\_response\_schema](#regions\_response\_schema-inline) > array

<a name="regions\_response\_schema-inline"></a>
**regions\_response\_schema**

|Name|Schema|
|---|---|
|**collector\_ip**  <br>*optional*|[collector\_ip](#collector\_ip)|
|**region\_control\_node\_ip**  <br>*optional*|[region\_control\_node\_ip](#region\_control\_node\_ip)|
|**region\_discovery\_status**  <br>*optional*|[region\_discovery\_status](#region\_discovery\_status)|
|**region\_name**  <br>*optional*|[region\_name](#region\_name)|






# services


<a name="overview"></a>
## Overview
API to get reports for services (bandwidth is in Kbps and data is in KB)


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/reports/  
*Schemes* : HTTP


### Tags

* services : Operations related to services 




<a name="paths"></a>
## Paths

<a name="services-get"></a>
### Get operation for services
```
GET /services
```


#### Description
Use this operation to get a report for services. The response payload also contains the meta\_data block.


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[services\_response\_schema](#services\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* services




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="data\_coverage"></a>
### data\_coverage
The amount in percent, of the selected time period for which there is data

*Type* : number


<a name="lan\_to\_wan\_bandwidth"></a>
### lan\_to\_wan\_bandwidth
The LAN to WAN Bandwidth for all packet types

*Type* : number


<a name="lan\_to\_wan\_packets"></a>
### lan\_to\_wan\_packets
The LAN to WAN packets for all packet types

*Type* : integer


<a name="lan\_to\_wan\_packets\_dropped"></a>
### lan\_to\_wan\_packets\_dropped
The LAN to WAN packets dropped

*Type* : integer


<a name="lan\_to\_wan\_percent\_drop"></a>
### lan\_to\_wan\_percent\_drop
The LAN to WAN drop, in percent

*Type* : number


<a name="name"></a>
### name
The site name

*Type* : string


<a name="region\_name"></a>
### region\_name
The region name

*Type* : string


<a name="service\_type"></a>
### service\_type
The Service Type (Virtual Path, Internet, Intranet or Passthrough)

*Type* : string


<a name="services\_delete\_success\_schema"></a>
### services\_delete\_success\_schema

|Name|Schema|
|---|---|
|**services**  <br>*optional*|[services](#services\_delete\_success\_schema-services)|

<a name="services\_delete\_success\_schema-services"></a>
**services**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="services\_post\_success\_schema"></a>
### services\_post\_success\_schema

|Name|Schema|
|---|---|
|**services**  <br>*optional*|[services](#services\_post\_success\_schema-services)|

<a name="services\_post\_success\_schema-services"></a>
**services**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="services\_put\_success\_schema"></a>
### services\_put\_success\_schema

|Name|Schema|
|---|---|
|**services**  <br>*optional*|[services](#services\_put\_success\_schema-services)|

<a name="services\_put\_success\_schema-services"></a>
**services**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="services\_response\_schema"></a>
### services\_response\_schema
*Type* : < [services\_response\_schema](#services\_response\_schema-inline) > array

<a name="services\_response\_schema-inline"></a>
**services\_response\_schema**

|Name|Schema|
|---|---|
|**data\_coverage**  <br>*optional*|[data\_coverage](#data\_coverage)|
|**lan\_to\_wan\_bandwidth**  <br>*optional*|[lan\_to\_wan\_bandwidth](#lan\_to\_wan\_bandwidth)|
|**lan\_to\_wan\_packets**  <br>*optional*|[lan\_to\_wan\_packets](#lan\_to\_wan\_packets)|
|**lan\_to\_wan\_packets\_dropped**  <br>*optional*|[lan\_to\_wan\_packets\_dropped](#lan\_to\_wan\_packets\_dropped)|
|**lan\_to\_wan\_percent\_drop**  <br>*optional*|[lan\_to\_wan\_percent\_drop](#lan\_to\_wan\_percent\_drop)|
|**name**  <br>*optional*|[name](#name)|
|**region\_name**  <br>*optional*|[region\_name](#region\_name)|
|**service\_type**  <br>*optional*|[service\_type](#service\_type)|
|**wan\_to\_lan\_bandwidth**  <br>*optional*|[wan\_to\_lan\_bandwidth](#wan\_to\_lan\_bandwidth)|
|**wan\_to\_lan\_packets**  <br>*optional*|[wan\_to\_lan\_packets](#wan\_to\_lan\_packets)|
|**wan\_to\_lan\_packets\_dropped**  <br>*optional*|[wan\_to\_lan\_packets\_dropped](#wan\_to\_lan\_packets\_dropped)|
|**wan\_to\_lan\_percent\_drop**  <br>*optional*|[wan\_to\_lan\_percent\_drop](#wan\_to\_lan\_percent\_drop)|


<a name="wan\_to\_lan\_bandwidth"></a>
### wan\_to\_lan\_bandwidth
The WAN to LAN bandwidth for all packet types

*Type* : number


<a name="wan\_to\_lan\_packets"></a>
### wan\_to\_lan\_packets
The WAN to LAN packets for all packet types

*Type* : integer


<a name="wan\_to\_lan\_packets\_dropped"></a>
### wan\_to\_lan\_packets\_dropped
The WAN to LAN packets dropped

*Type* : integer


<a name="wan\_to\_lan\_percent\_drop"></a>
### wan\_to\_lan\_percent\_drop
The WAN to LAN packets dropped

*Type* : number






# inventory\_status


<a name="overview"></a>
## Overview
This resource can be used for inventory and status


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config/  
*Schemes* : HTTP


### Tags

* inventory\_status : Operations related to inventory\_status 




<a name="paths"></a>
## Paths

<a name="inventory\_status-get"></a>
### Get operation for inventory\_status
```
GET /inventory_status
```


#### Description
Use this operation to get the inventory and status


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[inventory\_status\_response\_schema](#inventory\_status\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* inventory\_status




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="appliance\_identifier"></a>
### appliance\_identifier
HA identifier for an appliance. If it's 0 then HA primary, else HA secondary

*Type* : boolean


<a name="inventory\_status"></a>
### inventory\_status

|Name|Schema|
|---|---|
|**region\_name**  <br>*optional*|[region\_name](#region\_name)|


<a name="inventory\_status\_delete\_success\_schema"></a>
### inventory\_status\_delete\_success\_schema

|Name|Schema|
|---|---|
|**inventory\_status**  <br>*optional*|[inventory\_status](#inventory\_status\_delete\_success\_schema-inventory\_status)|

<a name="inventory\_status\_delete\_success\_schema-inventory\_status"></a>
**inventory\_status**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="inventory\_status\_post\_success\_schema"></a>
### inventory\_status\_post\_success\_schema

|Name|Schema|
|---|---|
|**inventory\_status**  <br>*optional*|[inventory\_status](#inventory\_status\_post\_success\_schema-inventory\_status)|

<a name="inventory\_status\_post\_success\_schema-inventory\_status"></a>
**inventory\_status**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="inventory\_status\_put\_success\_schema"></a>
### inventory\_status\_put\_success\_schema

|Name|Schema|
|---|---|
|**inventory\_status**  <br>*optional*|[inventory\_status](#inventory\_status\_put\_success\_schema-inventory\_status)|

<a name="inventory\_status\_put\_success\_schema-inventory\_status"></a>
**inventory\_status**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="inventory\_status\_request\_schema"></a>
### inventory\_status\_request\_schema

|Name|Schema|
|---|---|
|**inventory\_status**  <br>*optional*|[inventory\_status](#inventory\_status)|


<a name="inventory\_status\_response\_schema"></a>
### inventory\_status\_response\_schema
*Type* : < [inventory\_status\_response\_schema](#inventory\_status\_response\_schema-inline) > array

<a name="inventory\_status\_response\_schema-inline"></a>
**inventory\_status\_response\_schema**

|Name|Schema|
|---|---|
|**appliance\_identifier**  <br>*optional*|[appliance\_identifier](#appliance\_identifier)|
|**last\_successful\_poll**  <br>*optional*|[last\_successful\_poll](#last\_successful\_poll)|
|**latest\_record**  <br>*optional*|[latest\_record](#latest\_record)|
|**management\_ip**  <br>*optional*|[management\_ip](#management\_ip)|
|**model**  <br>*optional*|[model](#model)|
|**poll**  <br>*optional*|[poll](#poll)|
|**region\_name**  <br>*optional*|[region\_name](#region\_name)|
|**registry\_timestamp**  <br>*optional*|[registry\_timestamp](#registry\_timestamp)|
|**serial\_number**  <br>*optional*|[serial\_number](#serial\_number)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**software**  <br>*optional*|[software](#software)|
|**status**  <br>*optional*|[status](#status)|


<a name="last\_successful\_poll"></a>
### last\_successful\_poll
Time when SD-WAN Center successfully applied statistics from Virtual WAN Appliance

*Type* : string


<a name="latest\_record"></a>
### latest\_record
Timestamp of last record in statistics received from Virtual WAN Appliance

*Type* : string


<a name="management\_ip"></a>
### management\_ip
Management IP address of Virtual WAN Appliance obtained from the active Master Control Node

*Type* : string


<a name="model"></a>
### model
Virtual WAN model type

*Type* : string


<a name="poll"></a>
### poll
Shows whether an appliance is being polled or not

*Type* : boolean


<a name="region\_name"></a>
### region\_name
Region name

*Type* : string


<a name="registry\_timestamp"></a>
### registry\_timestamp
Timestamp of compiled config running on Virtual WAN Appliance

*Type* : string


<a name="serial\_number"></a>
### serial\_number
Virtual WAN serial number

*Type* : string


<a name="site\_name"></a>
### site\_name
Site name

*Type* : string


<a name="software"></a>
### software
Software version running on Virtual WAN Appliance

*Type* : string


<a name="status"></a>
### status
State of connection to Virtual WAN Appliances during polling or discovery process

*Type* : string






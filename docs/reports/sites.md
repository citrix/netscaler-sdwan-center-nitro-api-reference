# sites


<a name="overview"></a>
## Overview
API to get reports for sites (bandwidth is in Kbps and data is in KB)


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/reports/  
*Schemes* : HTTP


### Tags

* sites : Operations related to sites 




<a name="paths"></a>
## Paths

<a name="sites-get"></a>
### Get operation for sites
```
GET /sites
```


#### Description
Use this operation to get a report for sites. The response payload also contains the meta\_data block.


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[sites\_response\_schema](#sites\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* sites




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
The amount in percent of the selected time for which there is data

*Type* : number


<a name="lan\_to\_wan\_available\_bandwidth"></a>
### lan\_to\_wan\_available\_bandwidth
The LAN to WAN available Bandwidth

*Type* : number


<a name="lan\_to\_wan\_bandwidth"></a>
### lan\_to\_wan\_bandwidth
The LAN to WAN Bandwidth for all packet types

*Type* : number


<a name="lan\_to\_wan\_bulk\_bandwidth\_packets"></a>
### lan\_to\_wan\_bulk\_bandwidth\_packets
The LAN to WAN bulk Bandwidth packets

*Type* : integer


<a name="lan\_to\_wan\_bulk\_packets"></a>
### lan\_to\_wan\_bulk\_packets
The LAN to WAN bulk packets

*Type* : integer


<a name="lan\_to\_wan\_control\_bandwidth"></a>
### lan\_to\_wan\_control\_bandwidth
The LAN to WAN control Bandwidth

*Type* : number


<a name="lan\_to\_wan\_control\_packets"></a>
### lan\_to\_wan\_control\_packets
The LAN to WAN control packets

*Type* : integer


<a name="lan\_to\_wan\_data"></a>
### lan\_to\_wan\_data
The LAN to WAN data sent

*Type* : number


<a name="lan\_to\_wan\_interactive\_bandwidth"></a>
### lan\_to\_wan\_interactive\_bandwidth
The LAN to WAN interactive Bandwidth

*Type* : number


<a name="lan\_to\_wan\_interactive\_packets"></a>
### lan\_to\_wan\_interactive\_packets
The LAN to WAN interactive packets

*Type* : integer


<a name="lan\_to\_wan\_packets"></a>
### lan\_to\_wan\_packets
The LAN to WAN packets for all packet types

*Type* : integer


<a name="lan\_to\_wan\_permitted\_bandwidth"></a>
### lan\_to\_wan\_permitted\_bandwidth
The LAN to WAN permitted Bandwidth

*Type* : number


<a name="lan\_to\_wan\_realtime\_bandwidth"></a>
### lan\_to\_wan\_realtime\_bandwidth
The LAN to WAN real-time Bandwidth

*Type* : number


<a name="lan\_to\_wan\_realtime\_packets"></a>
### lan\_to\_wan\_realtime\_packets
The LAN to WAN real-time packets

*Type* : integer


<a name="region\_name"></a>
### region\_name
The region name

*Type* : string


<a name="site\_name"></a>
### site\_name
The site name

*Type* : string


<a name="sites\_delete\_success\_schema"></a>
### sites\_delete\_success\_schema

|Name|Schema|
|---|---|
|**sites**  <br>*optional*|[sites](#sites\_delete\_success\_schema-sites)|

<a name="sites\_delete\_success\_schema-sites"></a>
**sites**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="sites\_post\_success\_schema"></a>
### sites\_post\_success\_schema

|Name|Schema|
|---|---|
|**sites**  <br>*optional*|[sites](#sites\_post\_success\_schema-sites)|

<a name="sites\_post\_success\_schema-sites"></a>
**sites**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="sites\_put\_success\_schema"></a>
### sites\_put\_success\_schema

|Name|Schema|
|---|---|
|**sites**  <br>*optional*|[sites](#sites\_put\_success\_schema-sites)|

<a name="sites\_put\_success\_schema-sites"></a>
**sites**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="sites\_response\_schema"></a>
### sites\_response\_schema
*Type* : < [sites\_response\_schema](#sites\_response\_schema-inline) > array

<a name="sites\_response\_schema-inline"></a>
**sites\_response\_schema**

|Name|Schema|
|---|---|
|**data\_coverage**  <br>*optional*|[data\_coverage](#data\_coverage)|
|**lan\_to\_wan\_available\_bandwidth**  <br>*optional*|[lan\_to\_wan\_available\_bandwidth](#lan\_to\_wan\_available\_bandwidth)|
|**lan\_to\_wan\_bandwidth**  <br>*optional*|[lan\_to\_wan\_bandwidth](#lan\_to\_wan\_bandwidth)|
|**lan\_to\_wan\_bulk\_bandwidth\_packets**  <br>*optional*|[lan\_to\_wan\_bulk\_bandwidth\_packets](#lan\_to\_wan\_bulk\_bandwidth\_packets)|
|**lan\_to\_wan\_bulk\_packets**  <br>*optional*|[lan\_to\_wan\_bulk\_packets](#lan\_to\_wan\_bulk\_packets)|
|**lan\_to\_wan\_control\_bandwidth**  <br>*optional*|[lan\_to\_wan\_control\_bandwidth](#lan\_to\_wan\_control\_bandwidth)|
|**lan\_to\_wan\_control\_packets**  <br>*optional*|[lan\_to\_wan\_control\_packets](#lan\_to\_wan\_control\_packets)|
|**lan\_to\_wan\_data**  <br>*optional*|[lan\_to\_wan\_data](#lan\_to\_wan\_data)|
|**lan\_to\_wan\_interactive\_bandwidth**  <br>*optional*|[lan\_to\_wan\_interactive\_bandwidth](#lan\_to\_wan\_interactive\_bandwidth)|
|**lan\_to\_wan\_interactive\_packets**  <br>*optional*|[lan\_to\_wan\_interactive\_packets](#lan\_to\_wan\_interactive\_packets)|
|**lan\_to\_wan\_packets**  <br>*optional*|[lan\_to\_wan\_packets](#lan\_to\_wan\_packets)|
|**lan\_to\_wan\_permitted\_bandwidth**  <br>*optional*|[lan\_to\_wan\_permitted\_bandwidth](#lan\_to\_wan\_permitted\_bandwidth)|
|**lan\_to\_wan\_realtime\_bandwidth**  <br>*optional*|[lan\_to\_wan\_realtime\_bandwidth](#lan\_to\_wan\_realtime\_bandwidth)|
|**lan\_to\_wan\_realtime\_packets**  <br>*optional*|[lan\_to\_wan\_realtime\_packets](#lan\_to\_wan\_realtime\_packets)|
|**region\_name**  <br>*optional*|[region\_name](#region\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**total\_available\_bandwidth**  <br>*optional*|[total\_available\_bandwidth](#total\_available\_bandwidth)|
|**total\_bandwidth**  <br>*optional*|[total\_bandwidth](#total\_bandwidth)|
|**total\_data**  <br>*optional*|[total\_data](#total\_data)|
|**total\_permitted\_bandwidth**  <br>*optional*|[total\_permitted\_bandwidth](#total\_permitted\_bandwidth)|
|**wan\_to\_lan\_available\_bandwidth**  <br>*optional*|[wan\_to\_lan\_available\_bandwidth](#wan\_to\_lan\_available\_bandwidth)|
|**wan\_to\_lan\_bandwidth**  <br>*optional*|[wan\_to\_lan\_bandwidth](#wan\_to\_lan\_bandwidth)|
|**wan\_to\_lan\_data**  <br>*optional*|[wan\_to\_lan\_data](#wan\_to\_lan\_data)|
|**wan\_to\_lan\_packets**  <br>*optional*|[wan\_to\_lan\_packets](#wan\_to\_lan\_packets)|
|**wan\_to\_lan\_permitted\_bandwidth**  <br>*optional*|[wan\_to\_lan\_permitted\_bandwidth](#wan\_to\_lan\_permitted\_bandwidth)|


<a name="total\_available\_bandwidth"></a>
### total\_available\_bandwidth
The total available bandwidth

*Type* : number


<a name="total\_bandwidth"></a>
### total\_bandwidth
The total bandwidth

*Type* : number


<a name="total\_data"></a>
### total\_data
The total data

*Type* : number


<a name="total\_permitted\_bandwidth"></a>
### total\_permitted\_bandwidth
The total permitted bandwidth

*Type* : number


<a name="wan\_to\_lan\_available\_bandwidth"></a>
### wan\_to\_lan\_available\_bandwidth
The WAN to LAN available Bandwidth

*Type* : number


<a name="wan\_to\_lan\_bandwidth"></a>
### wan\_to\_lan\_bandwidth
The WAN to LAN Bandwidth for all packet types

*Type* : number


<a name="wan\_to\_lan\_data"></a>
### wan\_to\_lan\_data
The WAN to LAN data received

*Type* : number


<a name="wan\_to\_lan\_packets"></a>
### wan\_to\_lan\_packets
The WAN to LAN packets for all packet types

*Type* : integer


<a name="wan\_to\_lan\_permitted\_bandwidth"></a>
### wan\_to\_lan\_permitted\_bandwidth
The WAN to LAN Permitted Bandwidth

*Type* : number






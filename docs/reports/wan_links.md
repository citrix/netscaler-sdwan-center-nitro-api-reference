# wan\_links


<a name="overview"></a>
## Overview
API to get reports for WAN links (bandwidth is in Kbps and data is in KB)


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/reports/  
*Schemes* : HTTP


### Tags

* wan\_links : Operations related to wan\_links 




<a name="paths"></a>
## Paths

<a name="wan\_links-get"></a>
### Get operation for wan\_links
```
GET /wan_links
```


#### Description
Use this operation to get a report for WAN Links. The response payload also contains the meta\_data block.


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[wan\_links\_response\_schema](#wan\_links\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* wan\_links




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
The amount, in percent of the selected time period for which there is data

*Type* : number


<a name="lan\_to\_wan\_available\_bandwidth"></a>
### lan\_to\_wan\_available\_bandwidth
The LAN to WAN available Bandwidth

*Type* : number


<a name="lan\_to\_wan\_bandwidth"></a>
### lan\_to\_wan\_bandwidth
The LAN to WAN bandwidth for all packet types

*Type* : number


<a name="lan\_to\_wan\_bulk\_bandwidth"></a>
### lan\_to\_wan\_bulk\_bandwidth
The LAN to WAN bulk bandwidth

*Type* : number


<a name="lan\_to\_wan\_bulk\_packets"></a>
### lan\_to\_wan\_bulk\_packets
The LAN to WAN bulk packets

*Type* : integer


<a name="lan\_to\_wan\_control\_bandwidth"></a>
### lan\_to\_wan\_control\_bandwidth
The LAN to WAN control bandwidth

*Type* : number


<a name="lan\_to\_wan\_control\_packets"></a>
### lan\_to\_wan\_control\_packets
The LAN to WAN control packets

*Type* : integer


<a name="lan\_to\_wan\_interactive\_bandwidth"></a>
### lan\_to\_wan\_interactive\_bandwidth
The LAN to WAN interactive bandwidth

*Type* : number


<a name="lan\_to\_wan\_interactive\_packets"></a>
### lan\_to\_wan\_interactive\_packets
The LAN to WAN interactive packets

*Type* : integer


<a name="lan\_to\_wan\_max\_bandwidth"></a>
### lan\_to\_wan\_max\_bandwidth
The maximum LAN to WAN Bandwidth for all packet types

*Type* : number


<a name="lan\_to\_wan\_min\_bandwidth"></a>
### lan\_to\_wan\_min\_bandwidth
The minimum LAN to WAN Bandwidth for all packet types

*Type* : number


<a name="lan\_to\_wan\_mismatched\_bandwidth"></a>
### lan\_to\_wan\_mismatched\_bandwidth
The LAN to WAN Bandwidth not matching an MPLS Queue

*Type* : number


<a name="lan\_to\_wan\_mismatched\_packets"></a>
### lan\_to\_wan\_mismatched\_packets
The LAN to WAN packets not matching an MPLS Queue

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
The LAN to WAN real-time bandwidth

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


<a name="total\_available\_bandwidth"></a>
### total\_available\_bandwidth
Total available bandwidth

*Type* : number


<a name="total\_bandwidth"></a>
### total\_bandwidth
Total bandwidth

*Type* : number


<a name="total\_data"></a>
### total\_data
Total data

*Type* : number


<a name="total\_permitted\_bandwidth"></a>
### total\_permitted\_bandwidth
Total permitted bandwidth

*Type* : number


<a name="wan\_link\_name"></a>
### wan\_link\_name
The WAN link name

*Type* : string


<a name="wan\_links\_delete\_success\_schema"></a>
### wan\_links\_delete\_success\_schema

|Name|Schema|
|---|---|
|**wan\_links**  <br>*optional*|[wan\_links](#wan\_links\_delete\_success\_schema-wan\_links)|

<a name="wan\_links\_delete\_success\_schema-wan\_links"></a>
**wan\_links**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="wan\_links\_post\_success\_schema"></a>
### wan\_links\_post\_success\_schema

|Name|Schema|
|---|---|
|**wan\_links**  <br>*optional*|[wan\_links](#wan\_links\_post\_success\_schema-wan\_links)|

<a name="wan\_links\_post\_success\_schema-wan\_links"></a>
**wan\_links**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="wan\_links\_put\_success\_schema"></a>
### wan\_links\_put\_success\_schema

|Name|Schema|
|---|---|
|**wan\_links**  <br>*optional*|[wan\_links](#wan\_links\_put\_success\_schema-wan\_links)|

<a name="wan\_links\_put\_success\_schema-wan\_links"></a>
**wan\_links**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="wan\_links\_response\_schema"></a>
### wan\_links\_response\_schema
*Type* : < [wan\_links\_response\_schema](#wan\_links\_response\_schema-inline) > array

<a name="wan\_links\_response\_schema-inline"></a>
**wan\_links\_response\_schema**

|Name|Schema|
|---|---|
|**data\_coverage**  <br>*optional*|[data\_coverage](#data\_coverage)|
|**lan\_to\_wan\_available\_bandwidth**  <br>*optional*|[lan\_to\_wan\_available\_bandwidth](#lan\_to\_wan\_available\_bandwidth)|
|**lan\_to\_wan\_bandwidth**  <br>*optional*|[lan\_to\_wan\_bandwidth](#lan\_to\_wan\_bandwidth)|
|**lan\_to\_wan\_bulk\_bandwidth**  <br>*optional*|[lan\_to\_wan\_bulk\_bandwidth](#lan\_to\_wan\_bulk\_bandwidth)|
|**lan\_to\_wan\_bulk\_packets**  <br>*optional*|[lan\_to\_wan\_bulk\_packets](#lan\_to\_wan\_bulk\_packets)|
|**lan\_to\_wan\_control\_bandwidth**  <br>*optional*|[lan\_to\_wan\_control\_bandwidth](#lan\_to\_wan\_control\_bandwidth)|
|**lan\_to\_wan\_control\_packets**  <br>*optional*|[lan\_to\_wan\_control\_packets](#lan\_to\_wan\_control\_packets)|
|**lan\_to\_wan\_interactive\_bandwidth**  <br>*optional*|[lan\_to\_wan\_interactive\_bandwidth](#lan\_to\_wan\_interactive\_bandwidth)|
|**lan\_to\_wan\_interactive\_packets**  <br>*optional*|[lan\_to\_wan\_interactive\_packets](#lan\_to\_wan\_interactive\_packets)|
|**lan\_to\_wan\_max\_bandwidth**  <br>*optional*|[lan\_to\_wan\_max\_bandwidth](#lan\_to\_wan\_max\_bandwidth)|
|**lan\_to\_wan\_min\_bandwidth**  <br>*optional*|[lan\_to\_wan\_min\_bandwidth](#lan\_to\_wan\_min\_bandwidth)|
|**lan\_to\_wan\_mismatched\_bandwidth**  <br>*optional*|[lan\_to\_wan\_mismatched\_bandwidth](#lan\_to\_wan\_mismatched\_bandwidth)|
|**lan\_to\_wan\_mismatched\_packets**  <br>*optional*|[lan\_to\_wan\_mismatched\_packets](#lan\_to\_wan\_mismatched\_packets)|
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
|**wan\_link\_name**  <br>*optional*|[wan\_link\_name](#wan\_link\_name)|
|**wan\_to\_lan\_available\_bandwidth**  <br>*optional*|[wan\_to\_lan\_available\_bandwidth](#wan\_to\_lan\_available\_bandwidth)|
|**wan\_to\_lan\_bandwidth**  <br>*optional*|[wan\_to\_lan\_bandwidth](#wan\_to\_lan\_bandwidth)|
|**wan\_to\_lan\_best\_one\_way\_time\_latency**  <br>*optional*|[wan\_to\_lan\_best\_one\_way\_time\_latency](#wan\_to\_lan\_best\_one\_way\_time\_latency)|
|**wan\_to\_lan\_best\_one\_way\_time\_max\_latency\_ms**  <br>*optional*|[wan\_to\_lan\_best\_one\_way\_time\_max\_latency\_ms](#wan\_to\_lan\_best\_one\_way\_time\_max\_latency\_ms)|
|**wan\_to\_lan\_best\_one\_way\_time\_min\_latency\_ms**  <br>*optional*|[wan\_to\_lan\_best\_one\_way\_time\_min\_latency\_ms](#wan\_to\_lan\_best\_one\_way\_time\_min\_latency\_ms)|
|**wan\_to\_lan\_congestion**  <br>*optional*|[wan\_to\_lan\_congestion](#wan\_to\_lan\_congestion)|
|**wan\_to\_lan\_jitter**  <br>*optional*|[wan\_to\_lan\_jitter](#wan\_to\_lan\_jitter)|
|**wan\_to\_lan\_loss\_percent**  <br>*optional*|[wan\_to\_lan\_loss\_percent](#wan\_to\_lan\_loss\_percent)|
|**wan\_to\_lan\_max\_bandwidth**  <br>*optional*|[wan\_to\_lan\_max\_bandwidth](#wan\_to\_lan\_max\_bandwidth)|
|**wan\_to\_lan\_max\_loss\_percent**  <br>*optional*|[wan\_to\_lan\_max\_loss\_percent](#wan\_to\_lan\_max\_loss\_percent)|
|**wan\_to\_lan\_min\_bandwidth**  <br>*optional*|[wan\_to\_lan\_min\_bandwidth](#wan\_to\_lan\_min\_bandwidth)|
|**wan\_to\_lan\_min\_jitter\_ms**  <br>*optional*|[wan\_to\_lan\_min\_jitter\_ms](#wan\_to\_lan\_min\_jitter\_ms)|
|**wan\_to\_lan\_min\_loss\_percent**  <br>*optional*|[wan\_to\_lan\_min\_loss\_percent](#wan\_to\_lan\_min\_loss\_percent)|
|**wan\_to\_lan\_mismatched\_bandwidth**  <br>*optional*|[wan\_to\_lan\_mismatched\_bandwidth](#wan\_to\_lan\_mismatched\_bandwidth)|
|**wan\_to\_lan\_mismatched\_packets**  <br>*optional*|[wan\_to\_lan\_mismatched\_packets](#wan\_to\_lan\_mismatched\_packets)|
|**wan\_to\_lan\_ooo\_percent**  <br>*optional*|[wan\_to\_lan\_ooo\_percent](#wan\_to\_lan\_ooo\_percent)|
|**wan\_to\_lan\_packets**  <br>*optional*|[wan\_to\_lan\_packets](#wan\_to\_lan\_packets)|
|**wan\_to\_lan\_packets\_lost**  <br>*optional*|[wan\_to\_lan\_packets\_lost](#wan\_to\_lan\_packets\_lost)|
|**wan\_to\_lan\_packets\_ooo**  <br>*optional*|[wan\_to\_lan\_packets\_ooo](#wan\_to\_lan\_packets\_ooo)|
|**wan\_to\_lan\_permitted\_bandwidth**  <br>*optional*|[wan\_to\_lan\_permitted\_bandwidth](#wan\_to\_lan\_permitted\_bandwidth)|


<a name="wan\_to\_lan\_available\_bandwidth"></a>
### wan\_to\_lan\_available\_bandwidth
The WAN to LAN available bandwidth

*Type* : number


<a name="wan\_to\_lan\_bandwidth"></a>
### wan\_to\_lan\_bandwidth
The WAN to LAN bandwidth for all packet types

*Type* : number


<a name="wan\_to\_lan\_best\_one\_way\_time\_latency"></a>
### wan\_to\_lan\_best\_one\_way\_time\_latency
The WAN to LAN best one way time latency, in milliseconds

*Type* : integer


<a name="wan\_to\_lan\_best\_one\_way\_time\_max\_latency\_ms"></a>
### wan\_to\_lan\_best\_one\_way\_time\_max\_latency\_ms
The maximum WAN to LAN best one way time latency in milliseconds

*Type* : integer


<a name="wan\_to\_lan\_best\_one\_way\_time\_min\_latency\_ms"></a>
### wan\_to\_lan\_best\_one\_way\_time\_min\_latency\_ms
The minimum WAN to LAN best one way time latency in milliseconds

*Type* : integer


<a name="wan\_to\_lan\_congestion"></a>
### wan\_to\_lan\_congestion
Congestion detected due to increased, unexpected packet flow in the WAN

*Type* : string


<a name="wan\_to\_lan\_jitter"></a>
### wan\_to\_lan\_jitter
Maximum WAN to LAN jitter, in milliseconds

*Type* : integer


<a name="wan\_to\_lan\_loss\_percent"></a>
### wan\_to\_lan\_loss\_percent
The WAN to LAN loss, in percent

*Type* : number


<a name="wan\_to\_lan\_max\_bandwidth"></a>
### wan\_to\_lan\_max\_bandwidth
The maximum WAN to LAN bandwidth for all packet types

*Type* : number


<a name="wan\_to\_lan\_max\_loss\_percent"></a>
### wan\_to\_lan\_max\_loss\_percent
The maximum WAN to LAN loss, in percent

*Type* : number


<a name="wan\_to\_lan\_min\_bandwidth"></a>
### wan\_to\_lan\_min\_bandwidth
The minimum WAN to LAN bandwidth for all packet types

*Type* : number


<a name="wan\_to\_lan\_min\_jitter\_ms"></a>
### wan\_to\_lan\_min\_jitter\_ms
The minimum WAN to LAN jitter in milliseconds

*Type* : integer


<a name="wan\_to\_lan\_min\_loss\_percent"></a>
### wan\_to\_lan\_min\_loss\_percent
The minimum WAN to LAN loss, in percent

*Type* : number


<a name="wan\_to\_lan\_mismatched\_bandwidth"></a>
### wan\_to\_lan\_mismatched\_bandwidth
The WAN to LAN bandwidth not matching an MPLS Queue

*Type* : number


<a name="wan\_to\_lan\_mismatched\_packets"></a>
### wan\_to\_lan\_mismatched\_packets
The WAN to LAN packets not matching an MPLS Queue

*Type* : integer


<a name="wan\_to\_lan\_ooo\_percent"></a>
### wan\_to\_lan\_ooo\_percent
The WAN to LAN out-of-order, in percent

*Type* : number


<a name="wan\_to\_lan\_packets"></a>
### wan\_to\_lan\_packets
The WAN to LAN packets for all packet types

*Type* : integer


<a name="wan\_to\_lan\_packets\_lost"></a>
### wan\_to\_lan\_packets\_lost
The WAN to LAN packet loss

*Type* : integer


<a name="wan\_to\_lan\_packets\_ooo"></a>
### wan\_to\_lan\_packets\_ooo
The WAN to LAN packets out-of-order

*Type* : integer


<a name="wan\_to\_lan\_permitted\_bandwidth"></a>
### wan\_to\_lan\_permitted\_bandwidth
The WAN to LAN permitted bandwidth

*Type* : number






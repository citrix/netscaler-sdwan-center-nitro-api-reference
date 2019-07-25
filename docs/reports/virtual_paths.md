# virtual\_paths


<a name="overview"></a>
## Overview
API to get reports for virtual paths (bandwidth is in Kbps and data is in KB)


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/reports/  
*Schemes* : HTTP


### Tags

* virtual\_paths : Operations related to virtual\_paths 




<a name="paths"></a>
## Paths

<a name="virtual\_paths-get"></a>
### Get operation for virtual\_paths
```
GET /virtual_paths
```


#### Description
Use this operation to get a report for virtual paths. The response payload also contains the meta\_data block.


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[virtual\_paths\_response\_schema](#virtual\_paths\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* virtual\_paths




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="bad\_time"></a>
### bad\_time
The time that the service was bad, in seconds

*Type* : string


<a name="bad\_time\_percent"></a>
### bad\_time\_percent
The time, in percent that the service was bad

*Type* : number


<a name="data\_coverage"></a>
### data\_coverage
The amount, in percent of the selected time period for which there is data

*Type* : number


<a name="down\_time"></a>
### down\_time
The time that the service was unusable, in seconds

*Type* : string


<a name="down\_time\_percent"></a>
### down\_time\_percent
The time, in percent that the service was unusable

*Type* : number


<a name="good\_time"></a>
### good\_time
The time that the service was good, in seconds

*Type* : string


<a name="good\_time\_percent"></a>
### good\_time\_percent
The time, in percent that the service was good

*Type* : number


<a name="ipsec\_worst\_state"></a>
### ipsec\_worst\_state
The IPsec tunnel worst state observed during the time period

*Type* : string


<a name="lan\_to\_wan\_bandwidth"></a>
### lan\_to\_wan\_bandwidth
The LAN to WAN Bandwidth for all packet types

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
The LAN to WAN Control Bandwidth

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


<a name="lan\_to\_wan\_packets"></a>
### lan\_to\_wan\_packets
The LAN to WAN packets for all packet types

*Type* : integer


<a name="lan\_to\_wan\_permitted-bandwidth"></a>
### lan\_to\_wan\_permitted bandwidth
The LAN to WAN permitted bandwidth

*Type* : number


<a name="lan\_to\_wan\_realtime\_bandwidth"></a>
### lan\_to\_wan\_realtime\_bandwidth
The LAN to WAN Realtime Bandwidth

*Type* : number


<a name="lan\_to\_wan\_realtime\_packets"></a>
### lan\_to\_wan\_realtime\_packets
The LAN to WAN real-time packets

*Type* : integer


<a name="percent\_up\_time"></a>
### percent\_up\_time
The time, in percent that the service was usable

*Type* : number


<a name="region\_name"></a>
### region\_name
The region name

*Type* : string


<a name="site\_name"></a>
### site\_name
The site name

*Type* : string


<a name="up\_time"></a>
### up\_time
The time that the service was usable, in seconds

*Type* : string


<a name="virtual\_path\_name"></a>
### virtual\_path\_name
The virtual path name

*Type* : string


<a name="virtual\_path\_type"></a>
### virtual\_path\_type
Virtual path type ( static or dynamic)

*Type* : string


<a name="virtual\_paths\_delete\_success\_schema"></a>
### virtual\_paths\_delete\_success\_schema

|Name|Schema|
|---|---|
|**virtual\_paths**  <br>*optional*|[virtual\_paths](#virtual\_paths\_delete\_success\_schema-virtual\_paths)|

<a name="virtual\_paths\_delete\_success\_schema-virtual\_paths"></a>
**virtual\_paths**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="virtual\_paths\_post\_success\_schema"></a>
### virtual\_paths\_post\_success\_schema

|Name|Schema|
|---|---|
|**virtual\_paths**  <br>*optional*|[virtual\_paths](#virtual\_paths\_post\_success\_schema-virtual\_paths)|

<a name="virtual\_paths\_post\_success\_schema-virtual\_paths"></a>
**virtual\_paths**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="virtual\_paths\_put\_success\_schema"></a>
### virtual\_paths\_put\_success\_schema

|Name|Schema|
|---|---|
|**virtual\_paths**  <br>*optional*|[virtual\_paths](#virtual\_paths\_put\_success\_schema-virtual\_paths)|

<a name="virtual\_paths\_put\_success\_schema-virtual\_paths"></a>
**virtual\_paths**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="virtual\_paths\_response\_schema"></a>
### virtual\_paths\_response\_schema
*Type* : < [virtual\_paths\_response\_schema](#virtual\_paths\_response\_schema-inline) > array

<a name="virtual\_paths\_response\_schema-inline"></a>
**virtual\_paths\_response\_schema**

|Name|Schema|
|---|---|
|**bad\_time**  <br>*optional*|[bad\_time](#bad\_time)|
|**bad\_time\_percent**  <br>*optional*|[bad\_time\_percent](#bad\_time\_percent)|
|**data\_coverage**  <br>*optional*|[data\_coverage](#data\_coverage)|
|**down\_time**  <br>*optional*|[down\_time](#down\_time)|
|**down\_time\_percent**  <br>*optional*|[down\_time\_percent](#down\_time\_percent)|
|**good\_time**  <br>*optional*|[good\_time](#good\_time)|
|**good\_time\_percent**  <br>*optional*|[good\_time\_percent](#good\_time\_percent)|
|**ipsec\_worst\_state**  <br>*optional*|[ipsec\_worst\_state](#ipsec\_worst\_state)|
|**lan\_to\_wan\_bandwidth**  <br>*optional*|[lan\_to\_wan\_bandwidth](#lan\_to\_wan\_bandwidth)|
|**lan\_to\_wan\_bulk\_bandwidth**  <br>*optional*|[lan\_to\_wan\_bulk\_bandwidth](#lan\_to\_wan\_bulk\_bandwidth)|
|**lan\_to\_wan\_bulk\_packets**  <br>*optional*|[lan\_to\_wan\_bulk\_packets](#lan\_to\_wan\_bulk\_packets)|
|**lan\_to\_wan\_control\_bandwidth**  <br>*optional*|[lan\_to\_wan\_control\_bandwidth](#lan\_to\_wan\_control\_bandwidth)|
|**lan\_to\_wan\_control\_packets**  <br>*optional*|[lan\_to\_wan\_control\_packets](#lan\_to\_wan\_control\_packets)|
|**lan\_to\_wan\_interactive\_bandwidth**  <br>*optional*|[lan\_to\_wan\_interactive\_bandwidth](#lan\_to\_wan\_interactive\_bandwidth)|
|**lan\_to\_wan\_interactive\_packets**  <br>*optional*|[lan\_to\_wan\_interactive\_packets](#lan\_to\_wan\_interactive\_packets)|
|**lan\_to\_wan\_max\_bandwidth**  <br>*optional*|[lan\_to\_wan\_max\_bandwidth](#lan\_to\_wan\_max\_bandwidth)|
|**lan\_to\_wan\_min\_bandwidth**  <br>*optional*|[lan\_to\_wan\_min\_bandwidth](#lan\_to\_wan\_min\_bandwidth)|
|**lan\_to\_wan\_packets**  <br>*optional*|[lan\_to\_wan\_packets](#lan\_to\_wan\_packets)|
|**lan\_to\_wan\_permitted bandwidth**  <br>*optional*|[lan\_to\_wan\_permitted bandwidth](#lan\_to\_wan\_permitted-bandwidth)|
|**lan\_to\_wan\_realtime\_bandwidth**  <br>*optional*|[lan\_to\_wan\_realtime\_bandwidth](#lan\_to\_wan\_realtime\_bandwidth)|
|**lan\_to\_wan\_realtime\_packets**  <br>*optional*|[lan\_to\_wan\_realtime\_packets](#lan\_to\_wan\_realtime\_packets)|
|**percent\_up\_time**  <br>*optional*|[percent\_up\_time](#percent\_up\_time)|
|**region\_name**  <br>*optional*|[region\_name](#region\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**up\_time**  <br>*optional*|[up\_time](#up\_time)|
|**virtual\_path\_name**  <br>*optional*|[virtual\_path\_name](#virtual\_path\_name)|
|**virtual\_path\_type**  <br>*optional*|[virtual\_path\_type](#virtual\_path\_type)|
|**wan\_to\_lan\_bandwidth**  <br>*optional*|[wan\_to\_lan\_bandwidth](#wan\_to\_lan\_bandwidth)|
|**wan\_to\_lan\_best\_one\_way\_time\_latency\_ms**  <br>*optional*|[wan\_to\_lan\_best\_one\_way\_time\_latency\_ms](#wan\_to\_lan\_best\_one\_way\_time\_latency\_ms)|
|**wan\_to\_lan\_best\_one\_way\_time\_max\_latency\_ms**  <br>*optional*|[wan\_to\_lan\_best\_one\_way\_time\_max\_latency\_ms](#wan\_to\_lan\_best\_one\_way\_time\_max\_latency\_ms)|
|**wan\_to\_lan\_best\_one\_way\_time\_min\_latency\_ms**  <br>*optional*|[wan\_to\_lan\_best\_one\_way\_time\_min\_latency\_ms](#wan\_to\_lan\_best\_one\_way\_time\_min\_latency\_ms)|
|**wan\_to\_lan\_congestion\_count**  <br>*optional*|[wan\_to\_lan\_congestion\_count](#wan\_to\_lan\_congestion\_count)|
|**wan\_to\_lan\_max\_bandwidth**  <br>*optional*|[wan\_to\_lan\_max\_bandwidth](#wan\_to\_lan\_max\_bandwidth)|
|**wan\_to\_lan\_max\_jitter\_ms**  <br>*optional*|[wan\_to\_lan\_max\_jitter\_ms](#wan\_to\_lan\_max\_jitter\_ms)|
|**wan\_to\_lan\_max\_percent\_loss**  <br>*optional*|[wan\_to\_lan\_max\_percent\_loss](#wan\_to\_lan\_max\_percent\_loss)|
|**wan\_to\_lan\_min\_bandwidth**  <br>*optional*|[wan\_to\_lan\_min\_bandwidth](#wan\_to\_lan\_min\_bandwidth)|
|**wan\_to\_lan\_min\_jitter\_ms**  <br>*optional*|[wan\_to\_lan\_min\_jitter\_ms](#wan\_to\_lan\_min\_jitter\_ms)|
|**wan\_to\_lan\_min\_percent\_loss**  <br>*optional*|[wan\_to\_lan\_min\_percent\_loss](#wan\_to\_lan\_min\_percent\_loss)|
|**wan\_to\_lan\_mismatched\_bandwidth**  <br>*optional*|[wan\_to\_lan\_mismatched\_bandwidth](#wan\_to\_lan\_mismatched\_bandwidth)|
|**wan\_to\_lan\_mismtached\_packets**  <br>*optional*|[wan\_to\_lan\_mismtached\_packets](#wan\_to\_lan\_mismtached\_packets)|
|**wan\_to\_lan\_packets**  <br>*optional*|[wan\_to\_lan\_packets](#wan\_to\_lan\_packets)|
|**wan\_to\_lan\_packets\_loss**  <br>*optional*|[wan\_to\_lan\_packets\_loss](#wan\_to\_lan\_packets\_loss)|
|**wan\_to\_lan\_packets\_ooo**  <br>*optional*|[wan\_to\_lan\_packets\_ooo](#wan\_to\_lan\_packets\_ooo)|
|**wan\_to\_lan\_percent\_loss**  <br>*optional*|[wan\_to\_lan\_percent\_loss](#wan\_to\_lan\_percent\_loss)|
|**wan\_to\_lan\_percent\_ooo**  <br>*optional*|[wan\_to\_lan\_percent\_ooo](#wan\_to\_lan\_percent\_ooo)|
|**wan\_to\_lan\_permitted\_bandwidth**  <br>*optional*|[wan\_to\_lan\_permitted\_bandwidth](#wan\_to\_lan\_permitted\_bandwidth)|
|**worst\_state**  <br>*optional*|[worst\_state](#worst\_state)|


<a name="wan\_to\_lan\_bandwidth"></a>
### wan\_to\_lan\_bandwidth
The WAN to LAN bandwidth for all packet types

*Type* : number


<a name="wan\_to\_lan\_best\_one\_way\_time\_latency\_ms"></a>
### wan\_to\_lan\_best\_one\_way\_time\_latency\_ms
The WAN to LAN best one way time latency in milliseconds

*Type* : integer


<a name="wan\_to\_lan\_best\_one\_way\_time\_max\_latency\_ms"></a>
### wan\_to\_lan\_best\_one\_way\_time\_max\_latency\_ms
The maximum WAN to LAN best one way time latency in milliseconds

*Type* : integer


<a name="wan\_to\_lan\_best\_one\_way\_time\_min\_latency\_ms"></a>
### wan\_to\_lan\_best\_one\_way\_time\_min\_latency\_ms
The minimum WAN to LAN best one way time latency in milliseconds

*Type* : integer


<a name="wan\_to\_lan\_congestion\_count"></a>
### wan\_to\_lan\_congestion\_count
Congestion detected due to increased, unexpected delay in packet flow in the WAN

*Type* : string


<a name="wan\_to\_lan\_max\_bandwidth"></a>
### wan\_to\_lan\_max\_bandwidth
The maximum WAN to LAN bandwidth for all packet types

*Type* : number


<a name="wan\_to\_lan\_max\_jitter\_ms"></a>
### wan\_to\_lan\_max\_jitter\_ms
The maximum WAN to LAN jitter in milliseconds

*Type* : integer


<a name="wan\_to\_lan\_max\_percent\_loss"></a>
### wan\_to\_lan\_max\_percent\_loss
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


<a name="wan\_to\_lan\_min\_percent\_loss"></a>
### wan\_to\_lan\_min\_percent\_loss
The minimum WAN to LAN loss, in percent

*Type* : number


<a name="wan\_to\_lan\_mismatched\_bandwidth"></a>
### wan\_to\_lan\_mismatched\_bandwidth
The WAN to LAN bandwidth not matching an MPLS Queue

*Type* : number


<a name="wan\_to\_lan\_mismtached\_packets"></a>
### wan\_to\_lan\_mismtached\_packets
The WAN to LAN packets not matching an MPLS Queue

*Type* : integer


<a name="wan\_to\_lan\_packets"></a>
### wan\_to\_lan\_packets
The WAN to LAN packets for all packet types

*Type* : integer


<a name="wan\_to\_lan\_packets\_loss"></a>
### wan\_to\_lan\_packets\_loss
The WAN to LAN packets lost

*Type* : integer


<a name="wan\_to\_lan\_packets\_ooo"></a>
### wan\_to\_lan\_packets\_ooo
The WAN to LAN packets out-of-order

*Type* : integer


<a name="wan\_to\_lan\_percent\_loss"></a>
### wan\_to\_lan\_percent\_loss
The WAN to LAN loss, in percent

*Type* : number


<a name="wan\_to\_lan\_percent\_ooo"></a>
### wan\_to\_lan\_percent\_ooo
The WAN to LAN out-of-order in percent

*Type* : number


<a name="wan\_to\_lan\_permitted\_bandwidth"></a>
### wan\_to\_lan\_permitted\_bandwidth
The WAN to LAN permitted bandwidth

*Type* : number


<a name="worst\_state"></a>
### worst\_state
The worst state observed during the time period

*Type* : string






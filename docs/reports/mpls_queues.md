# mpls\_queues


<a name="overview"></a>
## Overview
API to get reports for MPLS Queues (bandwidth is in Kbps and data is in KB)


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/reports/  
*Schemes* : HTTP


### Tags

* mpls\_queues : Operations related to mpls\_queues 




<a name="paths"></a>
## Paths

<a name="mpls\_queues-get"></a>
### Get operation for mpls\_queues
```
GET /mpls_queues
```


#### Description
Use this operation to get a report for MPLS Queues. The response payload also contains the meta\_data block.


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[mpls\_queues\_response\_schema](#mpls\_queues\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* mpls\_queues




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


<a name="mpls\_queues\_delete\_success\_schema"></a>
### mpls\_queues\_delete\_success\_schema

|Name|Schema|
|---|---|
|**mpls\_queues**  <br>*optional*|[mpls\_queues](#mpls\_queues\_delete\_success\_schema-mpls\_queues)|

<a name="mpls\_queues\_delete\_success\_schema-mpls\_queues"></a>
**mpls\_queues**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="mpls\_queues\_post\_success\_schema"></a>
### mpls\_queues\_post\_success\_schema

|Name|Schema|
|---|---|
|**mpls\_queues**  <br>*optional*|[mpls\_queues](#mpls\_queues\_post\_success\_schema-mpls\_queues)|

<a name="mpls\_queues\_post\_success\_schema-mpls\_queues"></a>
**mpls\_queues**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="mpls\_queues\_put\_success\_schema"></a>
### mpls\_queues\_put\_success\_schema

|Name|Schema|
|---|---|
|**mpls\_queues**  <br>*optional*|[mpls\_queues](#mpls\_queues\_put\_success\_schema-mpls\_queues)|

<a name="mpls\_queues\_put\_success\_schema-mpls\_queues"></a>
**mpls\_queues**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="mpls\_queues\_response\_schema"></a>
### mpls\_queues\_response\_schema
*Type* : < [mpls\_queues\_response\_schema](#mpls\_queues\_response\_schema-inline) > array

<a name="mpls\_queues\_response\_schema-inline"></a>
**mpls\_queues\_response\_schema**

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
|**lan\_to\_wan\_mismatched\_bandwidth**  <br>*optional*|[lan\_to\_wan\_mismatched\_bandwidth](#lan\_to\_wan\_mismatched\_bandwidth)|
|**lan\_to\_wan\_mismatched\_packets**  <br>*optional*|[lan\_to\_wan\_mismatched\_packets](#lan\_to\_wan\_mismatched\_packets)|
|**lan\_to\_wan\_packets**  <br>*optional*|[lan\_to\_wan\_packets](#lan\_to\_wan\_packets)|
|**lan\_to\_wan\_permitted\_bandwidth**  <br>*optional*|[lan\_to\_wan\_permitted\_bandwidth](#lan\_to\_wan\_permitted\_bandwidth)|
|**lan\_to\_wan\_realtime\_bandwidth**  <br>*optional*|[lan\_to\_wan\_realtime\_bandwidth](#lan\_to\_wan\_realtime\_bandwidth)|
|**lan\_to\_wan\_realtime\_packets**  <br>*optional*|[lan\_to\_wan\_realtime\_packets](#lan\_to\_wan\_realtime\_packets)|
|**mpls\_wan\_link**  <br>*optional*|[mpls\_wan\_link](#mpls\_wan\_link)|
|**name**  <br>*optional*|[name](#name)|
|**region\_name**  <br>*optional*|[region\_name](#region\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**total\_available\_bandwidth**  <br>*optional*|[total\_available\_bandwidth](#total\_available\_bandwidth)|
|**total\_bandwidth**  <br>*optional*|[total\_bandwidth](#total\_bandwidth)|
|**total\_data**  <br>*optional*|[total\_data](#total\_data)|
|**total\_permitted\_bandwidth**  <br>*optional*|[total\_permitted\_bandwidth](#total\_permitted\_bandwidth)|
|**wan\_to\_lan\_available\_bandwidth**  <br>*optional*|[wan\_to\_lan\_available\_bandwidth](#wan\_to\_lan\_available\_bandwidth)|
|**wan\_to\_lan\_bandwidth**  <br>*optional*|[wan\_to\_lan\_bandwidth](#wan\_to\_lan\_bandwidth)|
|**wan\_to\_lan\_best\_one\_way\_time\_latency**  <br>*optional*|[wan\_to\_lan\_best\_one\_way\_time\_latency](#wan\_to\_lan\_best\_one\_way\_time\_latency)|
|**wan\_to\_lan\_congestion**  <br>*optional*|[wan\_to\_lan\_congestion](#wan\_to\_lan\_congestion)|
|**wan\_to\_lan\_jitter**  <br>*optional*|[wan\_to\_lan\_jitter](#wan\_to\_lan\_jitter)|
|**wan\_to\_lan\_loss\_percent**  <br>*optional*|[wan\_to\_lan\_loss\_percent](#wan\_to\_lan\_loss\_percent)|
|**wan\_to\_lan\_mismatched\_bandwidth**  <br>*optional*|[wan\_to\_lan\_mismatched\_bandwidth](#wan\_to\_lan\_mismatched\_bandwidth)|
|**wan\_to\_lan\_mismatched\_packets**  <br>*optional*|[wan\_to\_lan\_mismatched\_packets](#wan\_to\_lan\_mismatched\_packets)|
|**wan\_to\_lan\_ooo\_percent**  <br>*optional*|[wan\_to\_lan\_ooo\_percent](#wan\_to\_lan\_ooo\_percent)|
|**wan\_to\_lan\_packets**  <br>*optional*|[wan\_to\_lan\_packets](#wan\_to\_lan\_packets)|
|**wan\_to\_lan\_packets\_lost**  <br>*optional*|[wan\_to\_lan\_packets\_lost](#wan\_to\_lan\_packets\_lost)|
|**wan\_to\_lan\_packets\_ooo**  <br>*optional*|[wan\_to\_lan\_packets\_ooo](#wan\_to\_lan\_packets\_ooo)|
|**wan\_to\_lan\_permitted\_bandwidth**  <br>*optional*|[wan\_to\_lan\_permitted\_bandwidth](#wan\_to\_lan\_permitted\_bandwidth)|


<a name="mpls\_wan\_link"></a>
### mpls\_wan\_link
Name of the MPLS WAN link the MPLS Queue is a member of

*Type* : string


<a name="name"></a>
### name
The MPLS Queue name

*Type* : string


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






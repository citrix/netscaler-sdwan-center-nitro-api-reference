# paths


<a name="overview"></a>
## Overview
API to get reports for paths (bandwidth is in Kbps and data is in KB)


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/reports/  
*Schemes* : HTTP


### Tags

* paths : Operations related to paths 




<a name="paths"></a>
## Paths

<a name="paths-get"></a>
### Get operation for paths
```
GET /paths
```


#### Description
Use this operation to get a report for paths. The response payload also contains the meta\_data block.


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[paths\_response\_schema](#paths\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* paths




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="from\_external\_source\_port"></a>
### from\_external\_source\_port
The external source UDP port, as observed by remote sites

*Type* : integer


<a name="from\_site\_name"></a>
### from\_site\_name
From site name

*Type* : string


<a name="from\_source\_port"></a>
### from\_source\_port
The configured source UDP port

*Type* : integer


<a name="from\_wanlink\_name"></a>
### from\_wanlink\_name
From wanlink name

*Type* : string


<a name="lan\_to\_wan\_bad\_time"></a>
### lan\_to\_wan\_bad\_time
The total time in the selected time period that the service was bad, in seconds

*Type* : string


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


<a name="lan\_to\_wan\_congestion"></a>
### lan\_to\_wan\_congestion
Congestion detected due to increased, unexpected delay in packet flow in the WAN

*Type* : string


<a name="lan\_to\_wan\_control\_bandwidth"></a>
### lan\_to\_wan\_control\_bandwidth
The LAN to WAN control bandwidth

*Type* : number


<a name="lan\_to\_wan\_control\_packets"></a>
### lan\_to\_wan\_control\_packets
The LAN to WAN control packets

*Type* : integer


<a name="lan\_to\_wan\_data\_coverage"></a>
### lan\_to\_wan\_data\_coverage
The amount, in percent of the selected time period for which there is data

*Type* : number


<a name="lan\_to\_wan\_dead\_peer\_time"></a>
### lan\_to\_wan\_dead\_peer\_time
The total time in the selected time period that the service was dead because notified by peer, in seconds

*Type* : string


<a name="lan\_to\_wan\_down\_time"></a>
### lan\_to\_wan\_down\_time
The total time in the selected time period that the service was unusable, in seconds

*Type* : string


<a name="lan\_to\_wan\_good\_time"></a>
### lan\_to\_wan\_good\_time
The total time in the selected time period that the service was good, in seconds

*Type* : string


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
LAN to WAN packets for all packet types

*Type* : integer


<a name="lan\_to\_wan\_percent\_bad\_peer\_time"></a>
### lan\_to\_wan\_percent\_bad\_peer\_time
The time, in percent that the service was bad because notified by peer

*Type* : string


<a name="lan\_to\_wan\_percent\_bad\_silence\_time"></a>
### lan\_to\_wan\_percent\_bad\_silence\_time
The time, in percent that the service was bad because silence time exceeded threshold

*Type* : string


<a name="lan\_to\_wan\_percent\_bad\_time"></a>
### lan\_to\_wan\_percent\_bad\_time
The time, in percent that the service was bad

*Type* : string


<a name="lan\_to\_wan\_percent\_dead\_peer\_time"></a>
### lan\_to\_wan\_percent\_dead\_peer\_time
The time, in percent that the service was dead because notified by peer

*Type* : string


<a name="lan\_to\_wan\_percent\_dead\_silence\_time"></a>
### lan\_to\_wan\_percent\_dead\_silence\_time
The time, in percent that the service was dead because silence time exceeded threshold

*Type* : string


<a name="lan\_to\_wan\_percent\_down\_time"></a>
### lan\_to\_wan\_percent\_down\_time
The time, in percent that the service was unusable

*Type* : string


<a name="lan\_to\_wan\_percent\_good\_time"></a>
### lan\_to\_wan\_percent\_good\_time
The time, in percent that the service was good

*Type* : string


<a name="lan\_to\_wan\_percent\_up\_time"></a>
### lan\_to\_wan\_percent\_up\_time
The time, in percent that the service was usable

*Type* : string


<a name="lan\_to\_wan\_realtime\_bandwidth"></a>
### lan\_to\_wan\_realtime\_bandwidth
The LAN to WAN real-time bandwidth

*Type* : number


<a name="lan\_to\_wan\_realtime\_packets"></a>
### lan\_to\_wan\_realtime\_packets
The LAN to WAN real-time packets

*Type* : integer


<a name="lan\_to\_wan\_state\_bad\_peer\_time"></a>
### lan\_to\_wan\_state\_bad\_peer\_time
The total time in the selected time period that the service was bad because notified by peer, in seconds

*Type* : string


<a name="lan\_to\_wan\_state\_bad\_silence\_time"></a>
### lan\_to\_wan\_state\_bad\_silence\_time
The total time in the selected time period that the service was bad because silence time exceeded threshold, in seconds

*Type* : string


<a name="lan\_to\_wan\_state\_dead\_silence\_time"></a>
### lan\_to\_wan\_state\_dead\_silence\_time
The total time in the selected time period that the service was dead because silence time exceeded threshold, in seconds

*Type* : string


<a name="lan\_to\_wan\_up\_time"></a>
### lan\_to\_wan\_up\_time
The total time in the selected time period that the service was usable, in seconds

*Type* : string


<a name="lan\_to\_wan\_worst\_state"></a>
### lan\_to\_wan\_worst\_state
The worst LAN to WAN state observed during the time period

*Type* : string


<a name="lan\_to\_wan\_worst\_state\_reason"></a>
### lan\_to\_wan\_worst\_state\_reason
The reason for the worst state observed during the time period

*Type* : string


<a name="maximum\_transmission\_unit"></a>
### maximum\_transmission\_unit
The maximum transmission unit, in  bytes

*Type* : integer


<a name="path\_name"></a>
### path\_name
The path name

*Type* : string


<a name="paths\_delete\_success\_schema"></a>
### paths\_delete\_success\_schema

|Name|Schema|
|---|---|
|**paths**  <br>*optional*|[paths](#paths\_delete\_success\_schema-paths)|

<a name="paths\_delete\_success\_schema-paths"></a>
**paths**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="paths\_post\_success\_schema"></a>
### paths\_post\_success\_schema

|Name|Schema|
|---|---|
|**paths**  <br>*optional*|[paths](#paths\_post\_success\_schema-paths)|

<a name="paths\_post\_success\_schema-paths"></a>
**paths**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="paths\_put\_success\_schema"></a>
### paths\_put\_success\_schema

|Name|Schema|
|---|---|
|**paths**  <br>*optional*|[paths](#paths\_put\_success\_schema-paths)|

<a name="paths\_put\_success\_schema-paths"></a>
**paths**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="paths\_response\_schema"></a>
### paths\_response\_schema
*Type* : < [paths\_response\_schema](#paths\_response\_schema-inline) > array

<a name="paths\_response\_schema-inline"></a>
**paths\_response\_schema**

|Name|Schema|
|---|---|
|**from\_external\_source\_port**  <br>*optional*|[from\_external\_source\_port](#from\_external\_source\_port)|
|**from\_site\_name**  <br>*optional*|[from\_site\_name](#from\_site\_name)|
|**from\_source\_port**  <br>*optional*|[from\_source\_port](#from\_source\_port)|
|**from\_wanlink\_name**  <br>*optional*|[from\_wanlink\_name](#from\_wanlink\_name)|
|**lan\_to\_wan\_bad\_time**  <br>*optional*|[lan\_to\_wan\_bad\_time](#lan\_to\_wan\_bad\_time)|
|**lan\_to\_wan\_bandwidth**  <br>*optional*|[lan\_to\_wan\_bandwidth](#lan\_to\_wan\_bandwidth)|
|**lan\_to\_wan\_bulk\_bandwidth**  <br>*optional*|[lan\_to\_wan\_bulk\_bandwidth](#lan\_to\_wan\_bulk\_bandwidth)|
|**lan\_to\_wan\_bulk\_packets**  <br>*optional*|[lan\_to\_wan\_bulk\_packets](#lan\_to\_wan\_bulk\_packets)|
|**lan\_to\_wan\_congestion**  <br>*optional*|[lan\_to\_wan\_congestion](#lan\_to\_wan\_congestion)|
|**lan\_to\_wan\_control\_bandwidth**  <br>*optional*|[lan\_to\_wan\_control\_bandwidth](#lan\_to\_wan\_control\_bandwidth)|
|**lan\_to\_wan\_control\_packets**  <br>*optional*|[lan\_to\_wan\_control\_packets](#lan\_to\_wan\_control\_packets)|
|**lan\_to\_wan\_data\_coverage**  <br>*optional*|[lan\_to\_wan\_data\_coverage](#lan\_to\_wan\_data\_coverage)|
|**lan\_to\_wan\_dead\_peer\_time**  <br>*optional*|[lan\_to\_wan\_dead\_peer\_time](#lan\_to\_wan\_dead\_peer\_time)|
|**lan\_to\_wan\_down\_time**  <br>*optional*|[lan\_to\_wan\_down\_time](#lan\_to\_wan\_down\_time)|
|**lan\_to\_wan\_good\_time**  <br>*optional*|[lan\_to\_wan\_good\_time](#lan\_to\_wan\_good\_time)|
|**lan\_to\_wan\_interactive\_bandwidth**  <br>*optional*|[lan\_to\_wan\_interactive\_bandwidth](#lan\_to\_wan\_interactive\_bandwidth)|
|**lan\_to\_wan\_interactive\_packets**  <br>*optional*|[lan\_to\_wan\_interactive\_packets](#lan\_to\_wan\_interactive\_packets)|
|**lan\_to\_wan\_max\_bandwidth**  <br>*optional*|[lan\_to\_wan\_max\_bandwidth](#lan\_to\_wan\_max\_bandwidth)|
|**lan\_to\_wan\_min\_bandwidth**  <br>*optional*|[lan\_to\_wan\_min\_bandwidth](#lan\_to\_wan\_min\_bandwidth)|
|**lan\_to\_wan\_packets**  <br>*optional*|[lan\_to\_wan\_packets](#lan\_to\_wan\_packets)|
|**lan\_to\_wan\_percent\_bad\_peer\_time**  <br>*optional*|[lan\_to\_wan\_percent\_bad\_peer\_time](#lan\_to\_wan\_percent\_bad\_peer\_time)|
|**lan\_to\_wan\_percent\_bad\_silence\_time**  <br>*optional*|[lan\_to\_wan\_percent\_bad\_silence\_time](#lan\_to\_wan\_percent\_bad\_silence\_time)|
|**lan\_to\_wan\_percent\_bad\_time**  <br>*optional*|[lan\_to\_wan\_percent\_bad\_time](#lan\_to\_wan\_percent\_bad\_time)|
|**lan\_to\_wan\_percent\_dead\_peer\_time**  <br>*optional*|[lan\_to\_wan\_percent\_dead\_peer\_time](#lan\_to\_wan\_percent\_dead\_peer\_time)|
|**lan\_to\_wan\_percent\_dead\_silence\_time**  <br>*optional*|[lan\_to\_wan\_percent\_dead\_silence\_time](#lan\_to\_wan\_percent\_dead\_silence\_time)|
|**lan\_to\_wan\_percent\_down\_time**  <br>*optional*|[lan\_to\_wan\_percent\_down\_time](#lan\_to\_wan\_percent\_down\_time)|
|**lan\_to\_wan\_percent\_good\_time**  <br>*optional*|[lan\_to\_wan\_percent\_good\_time](#lan\_to\_wan\_percent\_good\_time)|
|**lan\_to\_wan\_percent\_up\_time**  <br>*optional*|[lan\_to\_wan\_percent\_up\_time](#lan\_to\_wan\_percent\_up\_time)|
|**lan\_to\_wan\_realtime\_bandwidth**  <br>*optional*|[lan\_to\_wan\_realtime\_bandwidth](#lan\_to\_wan\_realtime\_bandwidth)|
|**lan\_to\_wan\_realtime\_packets**  <br>*optional*|[lan\_to\_wan\_realtime\_packets](#lan\_to\_wan\_realtime\_packets)|
|**lan\_to\_wan\_state\_bad\_peer\_time**  <br>*optional*|[lan\_to\_wan\_state\_bad\_peer\_time](#lan\_to\_wan\_state\_bad\_peer\_time)|
|**lan\_to\_wan\_state\_bad\_silence\_time**  <br>*optional*|[lan\_to\_wan\_state\_bad\_silence\_time](#lan\_to\_wan\_state\_bad\_silence\_time)|
|**lan\_to\_wan\_state\_dead\_silence\_time**  <br>*optional*|[lan\_to\_wan\_state\_dead\_silence\_time](#lan\_to\_wan\_state\_dead\_silence\_time)|
|**lan\_to\_wan\_up\_time**  <br>*optional*|[lan\_to\_wan\_up\_time](#lan\_to\_wan\_up\_time)|
|**lan\_to\_wan\_worst\_state**  <br>*optional*|[lan\_to\_wan\_worst\_state](#lan\_to\_wan\_worst\_state)|
|**lan\_to\_wan\_worst\_state\_reason**  <br>*optional*|[lan\_to\_wan\_worst\_state\_reason](#lan\_to\_wan\_worst\_state\_reason)|
|**maximum\_transmission\_unit**  <br>*optional*|[maximum\_transmission\_unit](#maximum\_transmission\_unit)|
|**path\_name**  <br>*optional*|[path\_name](#path\_name)|
|**region\_name**  <br>*optional*|[region\_name](#region\_name)|
|**to\_destination\_port**  <br>*optional*|[to\_destination\_port](#to\_destination\_port)|
|**to\_external\_destination\_port**  <br>*optional*|[to\_external\_destination\_port](#to\_external\_destination\_port)|
|**to\_site\_name**  <br>*optional*|[to\_site\_name](#to\_site\_name)|
|**to\_wanlink\_name**  <br>*optional*|[to\_wanlink\_name](#to\_wanlink\_name)|
|**wan\_to\_lan\_bad\_loss\_time**  <br>*optional*|[wan\_to\_lan\_bad\_loss\_time](#wan\_to\_lan\_bad\_loss\_time)|
|**wan\_to\_lan\_bad\_silence\_time**  <br>*optional*|[wan\_to\_lan\_bad\_silence\_time](#wan\_to\_lan\_bad\_silence\_time)|
|**wan\_to\_lan\_bad\_time**  <br>*optional*|[wan\_to\_lan\_bad\_time](#wan\_to\_lan\_bad\_time)|
|**wan\_to\_lan\_bandwidth**  <br>*optional*|[wan\_to\_lan\_bandwidth](#wan\_to\_lan\_bandwidth)|
|**wan\_to\_lan\_best\_one\_way\_time\_latency\_ms**  <br>*optional*|[wan\_to\_lan\_best\_one\_way\_time\_latency\_ms](#wan\_to\_lan\_best\_one\_way\_time\_latency\_ms)|
|**wan\_to\_lan\_best\_one\_way\_time\_max\_latency\_ms**  <br>*optional*|[wan\_to\_lan\_best\_one\_way\_time\_max\_latency\_ms](#wan\_to\_lan\_best\_one\_way\_time\_max\_latency\_ms)|
|**wan\_to\_lan\_best\_one\_way\_time\_min\_latency\_ms**  <br>*optional*|[wan\_to\_lan\_best\_one\_way\_time\_min\_latency\_ms](#wan\_to\_lan\_best\_one\_way\_time\_min\_latency\_ms)|
|**wan\_to\_lan\_congestion**  <br>*optional*|[wan\_to\_lan\_congestion](#wan\_to\_lan\_congestion)|
|**wan\_to\_lan\_data\_coverage**  <br>*optional*|[wan\_to\_lan\_data\_coverage](#wan\_to\_lan\_data\_coverage)|
|**wan\_to\_lan\_down\_time**  <br>*optional*|[wan\_to\_lan\_down\_time](#wan\_to\_lan\_down\_time)|
|**wan\_to\_lan\_good\_time**  <br>*optional*|[wan\_to\_lan\_good\_time](#wan\_to\_lan\_good\_time)|
|**wan\_to\_lan\_jitter\_ms**  <br>*optional*|[wan\_to\_lan\_jitter\_ms](#wan\_to\_lan\_jitter\_ms)|
|**wan\_to\_lan\_max\_bandwidth**  <br>*optional*|[wan\_to\_lan\_max\_bandwidth](#wan\_to\_lan\_max\_bandwidth)|
|**wan\_to\_lan\_max\_percent\_loss**  <br>*optional*|[wan\_to\_lan\_max\_percent\_loss](#wan\_to\_lan\_max\_percent\_loss)|
|**wan\_to\_lan\_min\_bandwidth**  <br>*optional*|[wan\_to\_lan\_min\_bandwidth](#wan\_to\_lan\_min\_bandwidth)|
|**wan\_to\_lan\_min\_jitter\_ms**  <br>*optional*|[wan\_to\_lan\_min\_jitter\_ms](#wan\_to\_lan\_min\_jitter\_ms)|
|**wan\_to\_lan\_min\_percent\_loss**  <br>*optional*|[wan\_to\_lan\_min\_percent\_loss](#wan\_to\_lan\_min\_percent\_loss)|
|**wan\_to\_lan\_mismatched\_bandwidth**  <br>*optional*|[wan\_to\_lan\_mismatched\_bandwidth](#wan\_to\_lan\_mismatched\_bandwidth)|
|**wan\_to\_lan\_mismatched\_packets**  <br>*optional*|[wan\_to\_lan\_mismatched\_packets](#wan\_to\_lan\_mismatched\_packets)|
|**wan\_to\_lan\_packets**  <br>*optional*|[wan\_to\_lan\_packets](#wan\_to\_lan\_packets)|
|**wan\_to\_lan\_packets\_lost**  <br>*optional*|[wan\_to\_lan\_packets\_lost](#wan\_to\_lan\_packets\_lost)|
|**wan\_to\_lan\_packets\_ooo**  <br>*optional*|[wan\_to\_lan\_packets\_ooo](#wan\_to\_lan\_packets\_ooo)|
|**wan\_to\_lan\_percent\_bad\_loss\_time**  <br>*optional*|[wan\_to\_lan\_percent\_bad\_loss\_time](#wan\_to\_lan\_percent\_bad\_loss\_time)|
|**wan\_to\_lan\_percent\_bad\_silence\_time**  <br>*optional*|[wan\_to\_lan\_percent\_bad\_silence\_time](#wan\_to\_lan\_percent\_bad\_silence\_time)|
|**wan\_to\_lan\_percent\_bad\_time**  <br>*optional*|[wan\_to\_lan\_percent\_bad\_time](#wan\_to\_lan\_percent\_bad\_time)|
|**wan\_to\_lan\_percent\_dead\_silence\_time**  <br>*optional*|[wan\_to\_lan\_percent\_dead\_silence\_time](#wan\_to\_lan\_percent\_dead\_silence\_time)|
|**wan\_to\_lan\_percent\_down\_time**  <br>*optional*|[wan\_to\_lan\_percent\_down\_time](#wan\_to\_lan\_percent\_down\_time)|
|**wan\_to\_lan\_percent\_good\_time**  <br>*optional*|[wan\_to\_lan\_percent\_good\_time](#wan\_to\_lan\_percent\_good\_time)|
|**wan\_to\_lan\_percent\_loss**  <br>*optional*|[wan\_to\_lan\_percent\_loss](#wan\_to\_lan\_percent\_loss)|
|**wan\_to\_lan\_percent\_ooo**  <br>*optional*|[wan\_to\_lan\_percent\_ooo](#wan\_to\_lan\_percent\_ooo)|
|**wan\_to\_lan\_percent\_up\_time**  <br>*optional*|[wan\_to\_lan\_percent\_up\_time](#wan\_to\_lan\_percent\_up\_time)|
|**wan\_to\_lan\_state\_dead\_silence\_time**  <br>*optional*|[wan\_to\_lan\_state\_dead\_silence\_time](#wan\_to\_lan\_state\_dead\_silence\_time)|
|**wan\_to\_lan\_up\_time**  <br>*optional*|[wan\_to\_lan\_up\_time](#wan\_to\_lan\_up\_time)|
|**wan\_to\_lan\_worst\_state**  <br>*optional*|[wan\_to\_lan\_worst\_state](#wan\_to\_lan\_worst\_state)|
|**wan\_to\_lan\_worst\_state\_reason**  <br>*optional*|[wan\_to\_lan\_worst\_state\_reason](#wan\_to\_lan\_worst\_state\_reason)|


<a name="region\_name"></a>
### region\_name
The region name

*Type* : string


<a name="to\_destination\_port"></a>
### to\_destination\_port
The configured Destination UDP port

*Type* : integer


<a name="to\_external\_destination\_port"></a>
### to\_external\_destination\_port
The external destination UDP port, as observed by remote sites

*Type* : integer


<a name="to\_site\_name"></a>
### to\_site\_name
To site name

*Type* : string


<a name="to\_wanlink\_name"></a>
### to\_wanlink\_name
To wanlink name

*Type* : string


<a name="wan\_to\_lan\_bad\_loss\_time"></a>
### wan\_to\_lan\_bad\_loss\_time
The total time in the selected time period that the service was bad because packet loss exceeded threshold, in seconds

*Type* : string


<a name="wan\_to\_lan\_bad\_silence\_time"></a>
### wan\_to\_lan\_bad\_silence\_time
The total time in the selected time period that the service was bad because silence time exceeded threshold, in seconds

*Type* : string


<a name="wan\_to\_lan\_bad\_time"></a>
### wan\_to\_lan\_bad\_time
The total time in the selected time period that the service was bad, in seconds

*Type* : string


<a name="wan\_to\_lan\_bandwidth"></a>
### wan\_to\_lan\_bandwidth
WAN to LAN bandwidth for all packet types

*Type* : number


<a name="wan\_to\_lan\_best\_one\_way\_time\_latency\_ms"></a>
### wan\_to\_lan\_best\_one\_way\_time\_latency\_ms
WAN to LAN best one way time latency in milliseconds

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
Congestion detected due to increased, unexpected delay in packet flow in the WAN

*Type* : string


<a name="wan\_to\_lan\_data\_coverage"></a>
### wan\_to\_lan\_data\_coverage
The amount, in percent of the selected time period for which there is data

*Type* : number


<a name="wan\_to\_lan\_down\_time"></a>
### wan\_to\_lan\_down\_time
The total time in the selected time period that the service was unusable, in seconds

*Type* : string


<a name="wan\_to\_lan\_good\_time"></a>
### wan\_to\_lan\_good\_time
The total time in the selected time period that the service was good, in seconds

*Type* : string


<a name="wan\_to\_lan\_jitter\_ms"></a>
### wan\_to\_lan\_jitter\_ms
WAN to LAN jitter in milliseconds

*Type* : integer


<a name="wan\_to\_lan\_max\_bandwidth"></a>
### wan\_to\_lan\_max\_bandwidth
The maximum WAN to LAN bandwidth for all packet types

*Type* : number


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
WAN to LAN bandwidth not matching an MPLS Queue

*Type* : number


<a name="wan\_to\_lan\_mismatched\_packets"></a>
### wan\_to\_lan\_mismatched\_packets
WAN to LAN packets not matching an MPLS Queue

*Type* : integer


<a name="wan\_to\_lan\_packets"></a>
### wan\_to\_lan\_packets
WAN to LAN packets for all packet types

*Type* : string


<a name="wan\_to\_lan\_packets\_lost"></a>
### wan\_to\_lan\_packets\_lost
WAN to LAN packets lost

*Type* : integer


<a name="wan\_to\_lan\_packets\_ooo"></a>
### wan\_to\_lan\_packets\_ooo
WAN to LAN packets out-of-order

*Type* : integer


<a name="wan\_to\_lan\_percent\_bad\_loss\_time"></a>
### wan\_to\_lan\_percent\_bad\_loss\_time
The time, in percent that the service was bad because packet loss exceeded threshold

*Type* : string


<a name="wan\_to\_lan\_percent\_bad\_silence\_time"></a>
### wan\_to\_lan\_percent\_bad\_silence\_time
The time, in percent that the service was bad because silence time exceeded threshold

*Type* : string


<a name="wan\_to\_lan\_percent\_bad\_time"></a>
### wan\_to\_lan\_percent\_bad\_time
The time, in percent that the service was bad

*Type* : string


<a name="wan\_to\_lan\_percent\_dead\_silence\_time"></a>
### wan\_to\_lan\_percent\_dead\_silence\_time
The time, in percent that the service was dead because silence time exceeded threshold

*Type* : string


<a name="wan\_to\_lan\_percent\_down\_time"></a>
### wan\_to\_lan\_percent\_down\_time
The time, in percent that the service was unusable

*Type* : string


<a name="wan\_to\_lan\_percent\_good\_time"></a>
### wan\_to\_lan\_percent\_good\_time
The time, in percent that the service was good

*Type* : string


<a name="wan\_to\_lan\_percent\_loss"></a>
### wan\_to\_lan\_percent\_loss
WAN to LAN loss, in percent

*Type* : number


<a name="wan\_to\_lan\_percent\_ooo"></a>
### wan\_to\_lan\_percent\_ooo
WAN to LAN out-of-order, in percent

*Type* : number


<a name="wan\_to\_lan\_percent\_up\_time"></a>
### wan\_to\_lan\_percent\_up\_time
The time, in percent that the service was usable

*Type* : string


<a name="wan\_to\_lan\_state\_dead\_silence\_time"></a>
### wan\_to\_lan\_state\_dead\_silence\_time
The total time in the selected time period that the service was dead because silence time exceeded threshold, in seconds

*Type* : string


<a name="wan\_to\_lan\_up\_time"></a>
### wan\_to\_lan\_up\_time
The total time in the selected time period that the service was usable, in seconds

*Type* : string


<a name="wan\_to\_lan\_worst\_state"></a>
### wan\_to\_lan\_worst\_state
The worst WAN to LAN state observed during the time period

*Type* : string


<a name="wan\_to\_lan\_worst\_state\_reason"></a>
### wan\_to\_lan\_worst\_state\_reason
The reason for the worst state observed during the time period

*Type* : string






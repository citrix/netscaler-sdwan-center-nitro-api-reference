# gre\_tunnels


<a name="overview"></a>
## Overview
API to get reports for GRE Tunnels (bandwidth is in Kbps and data is in KB)


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/reports/  
*Schemes* : HTTP


### Tags

* gre\_tunnels : Operations related to gre\_tunnels 




<a name="paths"></a>
## Paths

<a name="gre\_tunnels-get"></a>
### Get operation for gre\_tunnels
```
GET /gre_tunnels
```


#### Description
Use this operation to get a report for GRE Tunnels. The response payload also contains the meta\_data block.


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[gre\_tunnels\_response\_schema](#gre\_tunnels\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* gre\_tunnels




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="bandwidth\_received"></a>
### bandwidth\_received
Receive bandwidth

*Type* : number


<a name="bandwidth\_transmitted"></a>
### bandwidth\_transmitted
Transmit bandwidth

*Type* : number


<a name="data\_coverage"></a>
### data\_coverage
The amount, in percent of the selected time period for which there is data

*Type* : number


<a name="gre\_tunnel\_name"></a>
### gre\_tunnel\_name
The GRE Tunnel name

*Type* : string


<a name="gre\_tunnels\_delete\_success\_schema"></a>
### gre\_tunnels\_delete\_success\_schema

|Name|Schema|
|---|---|
|**gre\_tunnels**  <br>*optional*|[gre\_tunnels](#gre\_tunnels\_delete\_success\_schema-gre\_tunnels)|

<a name="gre\_tunnels\_delete\_success\_schema-gre\_tunnels"></a>
**gre\_tunnels**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="gre\_tunnels\_post\_success\_schema"></a>
### gre\_tunnels\_post\_success\_schema

|Name|Schema|
|---|---|
|**gre\_tunnels**  <br>*optional*|[gre\_tunnels](#gre\_tunnels\_post\_success\_schema-gre\_tunnels)|

<a name="gre\_tunnels\_post\_success\_schema-gre\_tunnels"></a>
**gre\_tunnels**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="gre\_tunnels\_put\_success\_schema"></a>
### gre\_tunnels\_put\_success\_schema

|Name|Schema|
|---|---|
|**gre\_tunnels**  <br>*optional*|[gre\_tunnels](#gre\_tunnels\_put\_success\_schema-gre\_tunnels)|

<a name="gre\_tunnels\_put\_success\_schema-gre\_tunnels"></a>
**gre\_tunnels**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="gre\_tunnels\_response\_schema"></a>
### gre\_tunnels\_response\_schema
*Type* : < [gre\_tunnels\_response\_schema](#gre\_tunnels\_response\_schema-inline) > array

<a name="gre\_tunnels\_response\_schema-inline"></a>
**gre\_tunnels\_response\_schema**

|Name|Schema|
|---|---|
|**bandwidth\_received**  <br>*optional*|[bandwidth\_received](#bandwidth\_received)|
|**bandwidth\_transmitted**  <br>*optional*|[bandwidth\_transmitted](#bandwidth\_transmitted)|
|**data\_coverage**  <br>*optional*|[data\_coverage](#data\_coverage)|
|**gre\_tunnel\_name**  <br>*optional*|[gre\_tunnel\_name](#gre\_tunnel\_name)|
|**link\_state**  <br>*optional*|[link\_state](#link\_state)|
|**mtu**  <br>*optional*|[mtu](#mtu)|
|**packets\_dropped**  <br>*optional*|[packets\_dropped](#packets\_dropped)|
|**packets\_fragmented**  <br>*optional*|[packets\_fragmented](#packets\_fragmented)|
|**packets\_received**  <br>*optional*|[packets\_received](#packets\_received)|
|**packets\_transmitted**  <br>*optional*|[packets\_transmitted](#packets\_transmitted)|
|**region\_name**  <br>*optional*|[region\_name](#region\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|


<a name="link\_state"></a>
### link\_state
The worst state observed during the time period

*Type* : string


<a name="mtu"></a>
### mtu
The maximum transmission unit

*Type* : string


<a name="packets\_dropped"></a>
### packets\_dropped
Packets dropped

*Type* : integer


<a name="packets\_fragmented"></a>
### packets\_fragmented
Packets fragmented

*Type* : string


<a name="packets\_received"></a>
### packets\_received
Packets received

*Type* : integer


<a name="packets\_transmitted"></a>
### packets\_transmitted
Packets transmitted

*Type* : integer


<a name="region\_name"></a>
### region\_name
The region name

*Type* : string


<a name="site\_name"></a>
### site\_name
The site name

*Type* : string






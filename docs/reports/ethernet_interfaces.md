# ethernet\_interfaces


<a name="overview"></a>
## Overview
API to get reports for Ethernet Interfaces (bandwidth is in Kbps and data is in KB)


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/reports/  
*Schemes* : HTTP


### Tags

* ethernet\_interfaces : Operations related to ethernet\_interfaces 




<a name="paths"></a>
## Paths

<a name="ethernet\_interfaces-get"></a>
### Get operation for ethernet\_interfaces
```
GET /ethernet_interfaces
```


#### Description
Use this operation to get a report for Ethernet interfaces. The response payload also contains the meta\_data block.


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[ethernet\_interfaces\_response\_schema](#ethernet\_interfaces\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* ethernet\_interfaces




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


<a name="errors"></a>
### errors
Errors

*Type* : integer


<a name="ethernet\_interface\_name"></a>
### ethernet\_interface\_name
The name

*Type* : string


<a name="ethernet\_interfaces\_delete\_success\_schema"></a>
### ethernet\_interfaces\_delete\_success\_schema

|Name|Schema|
|---|---|
|**ethernet\_interfaces**  <br>*optional*|[ethernet\_interfaces](#ethernet\_interfaces\_delete\_success\_schema-ethernet\_interfaces)|

<a name="ethernet\_interfaces\_delete\_success\_schema-ethernet\_interfaces"></a>
**ethernet\_interfaces**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="ethernet\_interfaces\_post\_success\_schema"></a>
### ethernet\_interfaces\_post\_success\_schema

|Name|Schema|
|---|---|
|**ethernet\_interfaces**  <br>*optional*|[ethernet\_interfaces](#ethernet\_interfaces\_post\_success\_schema-ethernet\_interfaces)|

<a name="ethernet\_interfaces\_post\_success\_schema-ethernet\_interfaces"></a>
**ethernet\_interfaces**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="ethernet\_interfaces\_put\_success\_schema"></a>
### ethernet\_interfaces\_put\_success\_schema

|Name|Schema|
|---|---|
|**ethernet\_interfaces**  <br>*optional*|[ethernet\_interfaces](#ethernet\_interfaces\_put\_success\_schema-ethernet\_interfaces)|

<a name="ethernet\_interfaces\_put\_success\_schema-ethernet\_interfaces"></a>
**ethernet\_interfaces**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="ethernet\_interfaces\_response\_schema"></a>
### ethernet\_interfaces\_response\_schema
*Type* : < [ethernet\_interfaces\_response\_schema](#ethernet\_interfaces\_response\_schema-inline) > array

<a name="ethernet\_interfaces\_response\_schema-inline"></a>
**ethernet\_interfaces\_response\_schema**

|Name|Schema|
|---|---|
|**bandwidth\_received**  <br>*optional*|[bandwidth\_received](#bandwidth\_received)|
|**bandwidth\_transmitted**  <br>*optional*|[bandwidth\_transmitted](#bandwidth\_transmitted)|
|**data\_coverage**  <br>*optional*|[data\_coverage](#data\_coverage)|
|**errors**  <br>*optional*|[errors](#errors)|
|**ethernet\_interface\_name**  <br>*optional*|[ethernet\_interface\_name](#ethernet\_interface\_name)|
|**link\_state**  <br>*optional*|[link\_state](#link\_state)|
|**packets\_received**  <br>*optional*|[packets\_received](#packets\_received)|
|**packets\_transmitted**  <br>*optional*|[packets\_transmitted](#packets\_transmitted)|
|**region\_name**  <br>*optional*|[region\_name](#region\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|


<a name="link\_state"></a>
### link\_state
The worst state observed during the time period

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






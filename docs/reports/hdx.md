# hdx


<a name="overview"></a>
## Overview
API to get reports for HDX (bandwidth is in Kbps and data is in KB)


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/reports/  
*Schemes* : HTTP


### Tags

* hdx : Operations related to hdx 




<a name="paths"></a>
## Paths

<a name="hdx-get"></a>
### Get operation for hdx
```
GET /hdx
```


#### Description
Use this operation to get a report for HDX. The response payload also contains the meta\_data block.


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[hdx\_response\_schema](#hdx\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* hdx




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="hdx\_delete\_success\_schema"></a>
### hdx\_delete\_success\_schema

|Name|Schema|
|---|---|
|**hdx**  <br>*optional*|[hdx](#hdx\_delete\_success\_schema-hdx)|

<a name="hdx\_delete\_success\_schema-hdx"></a>
**hdx**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="hdx\_post\_success\_schema"></a>
### hdx\_post\_success\_schema

|Name|Schema|
|---|---|
|**hdx**  <br>*optional*|[hdx](#hdx\_post\_success\_schema-hdx)|

<a name="hdx\_post\_success\_schema-hdx"></a>
**hdx**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="hdx\_put\_success\_schema"></a>
### hdx\_put\_success\_schema

|Name|Schema|
|---|---|
|**hdx**  <br>*optional*|[hdx](#hdx\_put\_success\_schema-hdx)|

<a name="hdx\_put\_success\_schema-hdx"></a>
**hdx**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="hdx\_response\_schema"></a>
### hdx\_response\_schema
*Type* : < [hdx\_response\_schema](#hdx\_response\_schema-inline) > array

<a name="hdx\_response\_schema-inline"></a>
**hdx\_response\_schema**

|Name|Schema|
|---|---|
|**qoe\_index**  <br>*optional*|[qoe\_index](#qoe\_index)|
|**region\_name**  <br>*optional*|[region\_name](#region\_name)|
|**sessions**  <br>*optional*|[sessions](#sessions)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**tcp\_flows**  <br>*optional*|[tcp\_flows](#tcp\_flows)|
|**udp\_flows**  <br>*optional*|[udp\_flows](#udp\_flows)|
|**users**  <br>*optional*|[users](#users)|


<a name="qoe\_index"></a>
### qoe\_index
Quality of experience index

*Type* : integer


<a name="region\_name"></a>
### region\_name
The region name

*Type* : string


<a name="sessions"></a>
### sessions
Sessions

*Type* : integer


<a name="site\_name"></a>
### site\_name
The site name

*Type* : string


<a name="tcp\_flows"></a>
### tcp\_flows
TCP Flows

*Type* : integer


<a name="udp\_flows"></a>
### udp\_flows
UDP Flows

*Type* : integer


<a name="users"></a>
### users
Users

*Type* : integer






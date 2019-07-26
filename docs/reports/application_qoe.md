# application\_qoe


<a name="overview"></a>
## Overview
API to get reports for Application QoE


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/reports/  
*Schemes* : HTTP


### Tags

* application\_qoe : Operations related to application\_qoe 




<a name="paths"></a>
## Paths

<a name="application\_qoe-get"></a>
### Get operation for application\_qoe
```
GET /application_qoe
```


#### Description
Use this operation to get a report for application QoE. The response payload also contains the meta\_data block.


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[application\_qoe\_response\_schema](#application\_qoe\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* application\_qoe




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="application\_name"></a>
### application\_name
The application name

*Type* : string


<a name="application\_qoe\_delete\_success\_schema"></a>
### application\_qoe\_delete\_success\_schema

|Name|Schema|
|---|---|
|**application\_qoe**  <br>*optional*|[application\_qoe](#application\_qoe\_delete\_success\_schema-application\_qoe)|

<a name="application\_qoe\_delete\_success\_schema-application\_qoe"></a>
**application\_qoe**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="application\_qoe\_post\_success\_schema"></a>
### application\_qoe\_post\_success\_schema

|Name|Schema|
|---|---|
|**application\_qoe**  <br>*optional*|[application\_qoe](#application\_qoe\_post\_success\_schema-application\_qoe)|

<a name="application\_qoe\_post\_success\_schema-application\_qoe"></a>
**application\_qoe**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="application\_qoe\_put\_success\_schema"></a>
### application\_qoe\_put\_success\_schema

|Name|Schema|
|---|---|
|**application\_qoe**  <br>*optional*|[application\_qoe](#application\_qoe\_put\_success\_schema-application\_qoe)|

<a name="application\_qoe\_put\_success\_schema-application\_qoe"></a>
**application\_qoe**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="application\_qoe\_response\_schema"></a>
### application\_qoe\_response\_schema
*Type* : < [application\_qoe\_response\_schema](#application\_qoe\_response\_schema-inline) > array

<a name="application\_qoe\_response\_schema-inline"></a>
**application\_qoe\_response\_schema**

|Name|Schema|
|---|---|
|**application\_name**  <br>*optional*|[application\_name](#application\_name)|
|**interactive\_jitter**  <br>*optional*|[interactive\_jitter](#interactive\_jitter)|
|**interactive\_latency**  <br>*optional*|[interactive\_latency](#interactive\_latency)|
|**interactive\_loss**  <br>*optional*|[interactive\_loss](#interactive\_loss)|
|**interactive\_qoe**  <br>*optional*|[interactive\_qoe](#interactive\_qoe)|
|**realtime\_jitter**  <br>*optional*|[realtime\_jitter](#realtime\_jitter)|
|**realtime\_latency**  <br>*optional*|[realtime\_latency](#realtime\_latency)|
|**realtime\_loss**  <br>*optional*|[realtime\_loss](#realtime\_loss)|
|**realtime\_qoe**  <br>*optional*|[realtime\_qoe](#realtime\_qoe)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**virtual\_service**  <br>*optional*|[virtual\_service](#virtual\_service)|


<a name="interactive\_jitter"></a>
### interactive\_jitter
The interactive jitter value

*Type* : string


<a name="interactive\_latency"></a>
### interactive\_latency
The interactive latency value

*Type* : string


<a name="interactive\_loss"></a>
### interactive\_loss
The interactive loss value

*Type* : string


<a name="interactive\_qoe"></a>
### interactive\_qoe
The interactive qoe

*Type* : string


<a name="realtime\_jitter"></a>
### realtime\_jitter
The realtime jitter value

*Type* : string


<a name="realtime\_latency"></a>
### realtime\_latency
The realtime latency value

*Type* : string


<a name="realtime\_loss"></a>
### realtime\_loss
The realtime loss value

*Type* : string


<a name="realtime\_qoe"></a>
### realtime\_qoe
The realtime qoe

*Type* : string


<a name="site\_name"></a>
### site\_name
The site name

*Type* : string


<a name="virtual\_service"></a>
### virtual\_service
The virtual service name

*Type* : string






# events


<a name="overview"></a>
## Overview
API to get reports for Events (bandwidth is in Kbps and data is in KB)


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/reports/  
*Schemes* : HTTP


### Tags

* events : Operations related to events 




<a name="paths"></a>
## Paths

<a name="events-get"></a>
### Get operation for events
```
GET /events
```


#### Description
Use this operation to get a report for Events. The response payload also contains the meta\_data block.


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[events\_response\_schema](#events\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* events




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="alert\_events"></a>
### alert\_events
The number of alert events that have occured

*Type* : integer


<a name="critical\_events"></a>
### critical\_events
The number of critical events that have occured

*Type* : integer


<a name="debug\_events"></a>
### debug\_events
The number of debugging events that have occured

*Type* : string


<a name="emergency\_events"></a>
### emergency\_events
The number of emergency events that have occured

*Type* : integer


<a name="error\_events"></a>
### error\_events
The number of error events that have occured

*Type* : integer


<a name="events\_delete\_success\_schema"></a>
### events\_delete\_success\_schema

|Name|Schema|
|---|---|
|**events**  <br>*optional*|[events](#events\_delete\_success\_schema-events)|

<a name="events\_delete\_success\_schema-events"></a>
**events**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="events\_post\_success\_schema"></a>
### events\_post\_success\_schema

|Name|Schema|
|---|---|
|**events**  <br>*optional*|[events](#events\_post\_success\_schema-events)|

<a name="events\_post\_success\_schema-events"></a>
**events**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="events\_put\_success\_schema"></a>
### events\_put\_success\_schema

|Name|Schema|
|---|---|
|**events**  <br>*optional*|[events](#events\_put\_success\_schema-events)|

<a name="events\_put\_success\_schema-events"></a>
**events**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="events\_response\_schema"></a>
### events\_response\_schema
*Type* : < [events\_response\_schema](#events\_response\_schema-inline) > array

<a name="events\_response\_schema-inline"></a>
**events\_response\_schema**

|Name|Schema|
|---|---|
|**alert\_events**  <br>*optional*|[alert\_events](#alert\_events)|
|**critical\_events**  <br>*optional*|[critical\_events](#critical\_events)|
|**debug\_events**  <br>*optional*|[debug\_events](#debug\_events)|
|**emergency\_events**  <br>*optional*|[emergency\_events](#emergency\_events)|
|**error\_events**  <br>*optional*|[error\_events](#error\_events)|
|**info\_events**  <br>*optional*|[info\_events](#info\_events)|
|**notice\_events**  <br>*optional*|[notice\_events](#notice\_events)|
|**region\_name**  <br>*optional*|[region\_name](#region\_name)|
|**warning\_events**  <br>*optional*|[warning\_events](#warning\_events)|


<a name="info\_events"></a>
### info\_events
The number of informational events that have occured

*Type* : string


<a name="notice\_events"></a>
### notice\_events
The number of notice events that have occured

*Type* : string


<a name="region\_name"></a>
### region\_name
The region name

*Type* : string


<a name="warning\_events"></a>
### warning\_events
The number of warning events that have occured

*Type* : integer






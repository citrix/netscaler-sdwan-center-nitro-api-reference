# event\_viewer


<a name="overview"></a>
## Overview
API to get events information from all discovered appliances in the network


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/fault/  
*Schemes* : HTTP


### Tags

* event\_viewer : Operations related to event\_viewer 




<a name="paths"></a>
## Paths

<a name="event\_viewer-get"></a>
### Get operation for event\_viewer
```
GET /event_viewer
```


#### Description
Use this operation to get events information from all discovered appliances in the network. The response payload also contains the meta\_data block. Without using filters, events provided will be an empty list, Please use filter 'last\_by' or 'start\_at' and 'end\_at' to get the events under specified time interval


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[event\_viewer\_response\_schema](#event\_viewer\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* event\_viewer




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="appliance\_id"></a>
### appliance\_id
Specifies whether the appliance from which the event originated is a primary (0) or secondary (1) appliance

*Type* : string


<a name="current\_state"></a>
### current\_state
The state of object at the time of the event

*Type* : string


<a name="description"></a>
### description
Text description of the event

*Type* : string


<a name="event\_viewer\_delete\_success\_schema"></a>
### event\_viewer\_delete\_success\_schema

|Name|Schema|
|---|---|
|**event\_viewer**  <br>*optional*|[event\_viewer](#event\_viewer\_delete\_success\_schema-event\_viewer)|

<a name="event\_viewer\_delete\_success\_schema-event\_viewer"></a>
**event\_viewer**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="event\_viewer\_post\_success\_schema"></a>
### event\_viewer\_post\_success\_schema

|Name|Schema|
|---|---|
|**event\_viewer**  <br>*optional*|[event\_viewer](#event\_viewer\_post\_success\_schema-event\_viewer)|

<a name="event\_viewer\_post\_success\_schema-event\_viewer"></a>
**event\_viewer**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="event\_viewer\_put\_success\_schema"></a>
### event\_viewer\_put\_success\_schema

|Name|Schema|
|---|---|
|**event\_viewer**  <br>*optional*|[event\_viewer](#event\_viewer\_put\_success\_schema-event\_viewer)|

<a name="event\_viewer\_put\_success\_schema-event\_viewer"></a>
**event\_viewer**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="event\_viewer\_response\_schema"></a>
### event\_viewer\_response\_schema
*Type* : < [event\_viewer\_response\_schema](#event\_viewer\_response\_schema-inline) > array

<a name="event\_viewer\_response\_schema-inline"></a>
**event\_viewer\_response\_schema**

|Name|Schema|
|---|---|
|**appliance\_id**  <br>*optional*|[appliance\_id](#appliance\_id)|
|**current\_state**  <br>*optional*|[current\_state](#current\_state)|
|**description**  <br>*optional*|[description](#description)|
|**object\_name**  <br>*optional*|[object\_name](#object\_name)|
|**object\_type**  <br>*optional*|[object\_type](#object\_type)|
|**previous\_state**  <br>*optional*|[previous\_state](#previous\_state)|
|**severity**  <br>*optional*|[severity](#severity)|
|**site**  <br>*optional*|[site](#site)|
|**time**  <br>*optional*|[time](#time)|


<a name="object\_name"></a>
### object\_name
The name of object generating the event

*Type* : string


<a name="object\_type"></a>
### object\_type
The type of object generating the event

*Type* : string


<a name="previous\_state"></a>
### previous\_state
The state of object before the event. The state will be listed as unknown if not applicable

*Type* : string


<a name="severity"></a>
### severity
The severity level of the event

*Type* : string


<a name="site"></a>
### site
The site name on which the event originated

*Type* : string


<a name="time"></a>
### time
The time when event was generated

*Type* : string






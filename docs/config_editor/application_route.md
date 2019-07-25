# application\_route


<a name="overview"></a>
## Overview
API to add, modify, delete, and get configuration for application routes


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* application\_route : Operations related to application\_route 




<a name="paths"></a>
## Paths

<a name="application\_route-post"></a>
### POST operation for application\_route
```
POST /application_route
```


#### Description
Use this operation to add zen branch map entry


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[application\_route\_post\_success\_schema](#application\_route\_post\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* application\_route


<a name="application\_route-get"></a>
### Get operation for application\_route
```
GET /application_route
```


#### Description
Use this operation to get the list of zen branch map entry


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[application\_route\_response\_schema](#application\_route\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* application\_route


<a name="application\_route-put"></a>
### PUT operation for application\_route
```
PUT /application_route
```


#### Description
Use this operation to modify a zen branch map entry


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[application\_route\_request\_schema](#application\_route\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[application\_route\_put\_success\_schema](#application\_route\_put\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* application\_route


<a name="application\_route-deletepathparam-delete"></a>
### DELETE operation for application\_route
```
DELETE /application_route/{deletePathParam}
```


#### Description
Use this operation to delete a zen branch map entry


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[application\_route\_delete\_success\_schema](#application\_route\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* application\_route




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="application\_match\_name"></a>
### application\_match\_name
application object name

*Type* : string


<a name="application\_route"></a>
### application\_route

|Name|Schema|
|---|---|
|**application\_match\_name**  <br>*optional*|[application\_match\_name](#application\_match\_name)|
|**cost**  <br>*optional*|[cost](#cost)|
|**eligibility\_based\_on\_gateway**  <br>*optional*|[eligibility\_based\_on\_gateway](#eligibility\_based\_on\_gateway)|
|**eligibility\_based\_on\_path**  <br>*optional*|[eligibility\_based\_on\_path](#eligibility\_based\_on\_path)|
|**eligibility\_based\_on\_tunnel**  <br>*optional*|[eligibility\_based\_on\_tunnel](#eligibility\_based\_on\_tunnel)|
|**gateway\_ip\_addr**  <br>*optional*|[gateway\_ip\_addr](#gateway\_ip\_addr)|
|**id**  <br>*optional*|[id](#id)|
|**intranet\_service\_name**  <br>*optional*|[intranet\_service\_name](#intranet\_service\_name)|
|**ipsec\_tunnel**  <br>*optional*|[ipsec\_tunnel](#ipsec\_tunnel)|
|**next\_hop\_site**  <br>*optional*|[next\_hop\_site](#next\_hop\_site)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**path**  <br>*optional*|[path](#path)|
|**route\_eligibility\_from\_wan\_link**  <br>*optional*|[route\_eligibility\_from\_wan\_link](#route\_eligibility\_from\_wan\_link)|
|**route\_eligibility\_to\_wan\_link**  <br>*optional*|[route\_eligibility\_to\_wan\_link](#route\_eligibility\_to\_wan\_link)|
|**routing\_domain**  <br>*optional*|[routing\_domain](#routing\_domain)|
|**service\_type**  <br>*optional*|[service\_type](#service\_type)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|


<a name="application\_route\_delete\_success\_schema"></a>
### application\_route\_delete\_success\_schema

|Name|Schema|
|---|---|
|**application\_route**  <br>*optional*|[application\_route](#application\_route\_delete\_success\_schema-application\_route)|

<a name="application\_route\_delete\_success\_schema-application\_route"></a>
**application\_route**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="application\_route\_post\_success\_schema"></a>
### application\_route\_post\_success\_schema

|Name|Schema|
|---|---|
|**application\_route**  <br>*optional*|[application\_route](#application\_route\_post\_success\_schema-application\_route)|

<a name="application\_route\_post\_success\_schema-application\_route"></a>
**application\_route**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="application\_route\_put\_success\_schema"></a>
### application\_route\_put\_success\_schema

|Name|Schema|
|---|---|
|**application\_route**  <br>*optional*|[application\_route](#application\_route\_put\_success\_schema-application\_route)|

<a name="application\_route\_put\_success\_schema-application\_route"></a>
**application\_route**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="application\_route\_request\_schema"></a>
### application\_route\_request\_schema

|Name|Schema|
|---|---|
|**application\_route**  <br>*optional*|[application\_route](#application\_route)|


<a name="application\_route\_response\_schema"></a>
### application\_route\_response\_schema
*Type* : < [application\_route\_response\_schema](#application\_route\_response\_schema-inline) > array

<a name="application\_route\_response\_schema-inline"></a>
**application\_route\_response\_schema**

|Name|Schema|
|---|---|
|**application\_match\_name**  <br>*optional*|[application\_match\_name](#application\_match\_name)|
|**cost**  <br>*optional*|[cost](#cost)|
|**eligibility\_based\_on\_gateway**  <br>*optional*|[eligibility\_based\_on\_gateway](#eligibility\_based\_on\_gateway)|
|**eligibility\_based\_on\_path**  <br>*optional*|[eligibility\_based\_on\_path](#eligibility\_based\_on\_path)|
|**eligibility\_based\_on\_tunnel**  <br>*optional*|[eligibility\_based\_on\_tunnel](#eligibility\_based\_on\_tunnel)|
|**gateway\_ip\_addr**  <br>*optional*|[gateway\_ip\_addr](#gateway\_ip\_addr)|
|**id**  <br>*optional*|[id](#id)|
|**intranet\_service\_name**  <br>*optional*|[intranet\_service\_name](#intranet\_service\_name)|
|**ipsec\_tunnel**  <br>*optional*|[ipsec\_tunnel](#ipsec\_tunnel)|
|**next\_hop\_site**  <br>*optional*|[next\_hop\_site](#next\_hop\_site)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**path**  <br>*optional*|[path](#path)|
|**route\_eligibility\_from\_wan\_link**  <br>*optional*|[route\_eligibility\_from\_wan\_link](#route\_eligibility\_from\_wan\_link)|
|**route\_eligibility\_to\_wan\_link**  <br>*optional*|[route\_eligibility\_to\_wan\_link](#route\_eligibility\_to\_wan\_link)|
|**routing\_domain**  <br>*optional*|[routing\_domain](#routing\_domain)|
|**service\_type**  <br>*optional*|[service\_type](#service\_type)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|


<a name="cost"></a>
### cost
cost of route

*Type* : integer


<a name="eligibility\_based\_on\_gateway"></a>
### eligibility\_based\_on\_gateway
route eligibility on gateway

*Type* : string


<a name="eligibility\_based\_on\_path"></a>
### eligibility\_based\_on\_path
route eligibility based on path

*Type* : string


<a name="eligibility\_based\_on\_tunnel"></a>
### eligibility\_based\_on\_tunnel
route eligibility on tunnel

*Type* : string


<a name="gateway\_ip\_addr"></a>
### gateway\_ip\_addr
gateway ip address

*Type* : string


<a name="id"></a>
### id
Auto-generated ID. Use this ID to modify or delete a zen\_branch\_map

*Type* : integer


<a name="intranet\_service\_name"></a>
### intranet\_service\_name
intranet service name

*Type* : string


<a name="ipsec\_tunnel"></a>
### ipsec\_tunnel
LAN Ipsec tunnel name

*Type* : string


<a name="next\_hop\_site"></a>
### next\_hop\_site
next hop site name

*Type* : string


<a name="package\_name"></a>
### package\_name
Config package name using which the application route API operation should be performed.

*Type* : string


<a name="path"></a>
### path
Path from which to determine Route eligibility. Path should be given when eligibilty\_based\_on\_path is set to true

*Type* : string


<a name="route\_eligibility\_from\_wan\_link"></a>
### route\_eligibility\_from\_wan\_link
route eligibility from wanlink

*Type* : string


<a name="route\_eligibility\_to\_wan\_link"></a>
### route\_eligibility\_to\_wan\_link
route eligibility to wanlink

*Type* : string


<a name="routing\_domain"></a>
### routing\_domain
routing domain

*Type* : string


<a name="service\_type"></a>
### service\_type
service type

*Type* : string


<a name="site\_name"></a>
### site\_name
Sitename

*Type* : string






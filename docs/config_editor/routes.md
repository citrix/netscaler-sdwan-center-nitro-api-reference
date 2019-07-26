# routes


<a name="overview"></a>
## Overview
API to add, delete, get, modify routes


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* routes : Operations related to routes 




<a name="paths"></a>
## Paths

<a name="routes-post"></a>
### POST operation for routes
```
POST /routes
```


#### Description
Use this operation to add routes


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[routes\_request\_schema](#routes\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[routes\_post\_success\_schema](#routes\_post\_success\_schema)|
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

* routes


<a name="routes-get"></a>
### Get operation for routes
```
GET /routes
```


#### Description
Use this operation to get routes


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[routes\_response\_schema](#routes\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* routes


<a name="routes-put"></a>
### PUT operation for routes
```
PUT /routes
```


#### Description
Use this operation to modify routes


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[routes\_put\_success\_schema](#routes\_put\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* routes


<a name="routes-deletepathparam-delete"></a>
### DELETE operation for routes
```
DELETE /routes/{deletePathParam}
```


#### Description
Use this operation to delete routes


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[routes\_delete\_success\_schema](#routes\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* routes




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="cost"></a>
### cost
A weight to determine Route priority. Lower-cost Routes will be preferred over higher-cost Routes.

*Type* : integer


<a name="eligibility\_based\_on\_gateway"></a>
### eligibility\_based\_on\_gateway
If enabled, the Route will not receive traffic when the Gateway is unreachable

*Type* : boolean


<a name="eligibility\_based\_on\_path"></a>
### eligibility\_based\_on\_path
If enabled, the Route will not receive traffic when the selected Path is down

*Type* : boolean


<a name="eligibility\_based\_on\_tunnel"></a>
### eligibility\_based\_on\_tunnel
If enabled, the Route will not receive traffic when the associated Tunnel is unreachable

*Type* : boolean


<a name="export\_route"></a>
### export\_route
If enabled, this route will be exported to other connected Sites. Intranet and Internet routes will only be exported when WAN-to-WAN forwarding is also enabled

*Type* : boolean


<a name="gateway\_ip\_addr"></a>
### gateway\_ip\_addr
Gateway. For GRE tunnel route, this must be in the tunnel's subnet

*Type* : string


<a name="id"></a>
### id
Auto-generated ID to uniquely identify Routes

*Type* : integer


<a name="ipsec\_tunnel"></a>
### ipsec\_tunnel
The IPsec Tunnel to use for this Route

*Type* : string


<a name="network\_ip\_address"></a>
### network\_ip\_address
Network IP Address

*Type* : string


<a name="next\_hop\_site"></a>
### next\_hop\_site
The remote Site to which Virtual Path packets will be directed

*Type* : string


<a name="package\_name"></a>
### package\_name
Config package name using which the site API operation should be performed.

*Type* : string


<a name="path"></a>
### path
Path from which to determine Route eligibility. Path should be given when eligibilty\_based\_on\_path is set to true

*Type* : string


<a name="routes"></a>
### routes

|Name|Schema|
|---|---|
|**cost**  <br>*optional*|[cost](#cost)|
|**eligibility\_based\_on\_gateway**  <br>*optional*|[eligibility\_based\_on\_gateway](#eligibility\_based\_on\_gateway)|
|**eligibility\_based\_on\_path**  <br>*optional*|[eligibility\_based\_on\_path](#eligibility\_based\_on\_path)|
|**eligibility\_based\_on\_tunnel**  <br>*optional*|[eligibility\_based\_on\_tunnel](#eligibility\_based\_on\_tunnel)|
|**export\_route**  <br>*optional*|[export\_route](#export\_route)|
|**gateway\_ip\_addr**  <br>*optional*|[gateway\_ip\_addr](#gateway\_ip\_addr)|
|**id**  <br>*optional*|[id](#id)|
|**ipsec\_tunnel**  <br>*optional*|[ipsec\_tunnel](#ipsec\_tunnel)|
|**network\_ip\_address**  <br>*optional*|[network\_ip\_address](#network\_ip\_address)|
|**next\_hop\_site**  <br>*optional*|[next\_hop\_site](#next\_hop\_site)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**path**  <br>*optional*|[path](#path)|
|**routing\_domain**  <br>*optional*|[routing\_domain](#routing\_domain)|
|**service\_name**  <br>*optional*|[service\_name](#service\_name)|
|**service\_type**  <br>*optional*|[service\_type](#service\_type)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**summary\_route**  <br>*optional*|[summary\_route](#summary\_route)|


<a name="routes\_delete\_success\_schema"></a>
### routes\_delete\_success\_schema

|Name|Schema|
|---|---|
|**routes**  <br>*optional*|[routes](#routes\_delete\_success\_schema-routes)|

<a name="routes\_delete\_success\_schema-routes"></a>
**routes**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="routes\_post\_success\_schema"></a>
### routes\_post\_success\_schema

|Name|Schema|
|---|---|
|**routes**  <br>*optional*|[routes](#routes\_post\_success\_schema-routes)|

<a name="routes\_post\_success\_schema-routes"></a>
**routes**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="routes\_put\_success\_schema"></a>
### routes\_put\_success\_schema

|Name|Schema|
|---|---|
|**routes**  <br>*optional*|[routes](#routes\_put\_success\_schema-routes)|

<a name="routes\_put\_success\_schema-routes"></a>
**routes**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="routes\_request\_schema"></a>
### routes\_request\_schema

|Name|Schema|
|---|---|
|**routes**  <br>*optional*|[routes](#routes)|


<a name="routes\_response\_schema"></a>
### routes\_response\_schema
*Type* : < [routes\_response\_schema](#routes\_response\_schema-inline) > array

<a name="routes\_response\_schema-inline"></a>
**routes\_response\_schema**

|Name|Schema|
|---|---|
|**cost**  <br>*optional*|[cost](#cost)|
|**eligibility\_based\_on\_gateway**  <br>*optional*|[eligibility\_based\_on\_gateway](#eligibility\_based\_on\_gateway)|
|**eligibility\_based\_on\_path**  <br>*optional*|[eligibility\_based\_on\_path](#eligibility\_based\_on\_path)|
|**eligibility\_based\_on\_tunnel**  <br>*optional*|[eligibility\_based\_on\_tunnel](#eligibility\_based\_on\_tunnel)|
|**export\_route**  <br>*optional*|[export\_route](#export\_route)|
|**gateway\_ip\_addr**  <br>*optional*|[gateway\_ip\_addr](#gateway\_ip\_addr)|
|**id**  <br>*optional*|[id](#id)|
|**ipsec\_tunnel**  <br>*optional*|[ipsec\_tunnel](#ipsec\_tunnel)|
|**network\_ip\_address**  <br>*optional*|[network\_ip\_address](#network\_ip\_address)|
|**next\_hop\_site**  <br>*optional*|[next\_hop\_site](#next\_hop\_site)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**path**  <br>*optional*|[path](#path)|
|**routing\_domain**  <br>*optional*|[routing\_domain](#routing\_domain)|
|**service\_name**  <br>*optional*|[service\_name](#service\_name)|
|**service\_type**  <br>*optional*|[service\_type](#service\_type)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**summary\_route**  <br>*optional*|[summary\_route](#summary\_route)|


<a name="routing\_domain"></a>
### routing\_domain
One of the configured routing domains

*Type* : string


<a name="service\_name"></a>
### service\_name
Service name

*Type* : string


<a name="service\_type"></a>
### service\_type
Service Type

*Type* : enum (virtual\_path, internet, intranet, passthrough, local, lan\_gre\_tunnel, lan\_ipsec\_tunnel, discard)


<a name="site\_name"></a>
### site\_name
Site Name

*Type* : string


<a name="summary\_route"></a>
### summary\_route
If enabled, this route will be advertised to other connected instead of individual summarized routes

*Type* : boolean






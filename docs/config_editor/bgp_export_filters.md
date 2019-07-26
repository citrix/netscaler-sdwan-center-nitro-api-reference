# bgp\_export\_filters


<a name="overview"></a>
## Overview
API to add, delete, get, modify BGP Export Filters. To set any property value to wildcard, use *.


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* bgp\_export\_filters : Operations related to bgp\_export\_filters 




<a name="paths"></a>
## Paths

<a name="bgp\_export\_filters-post"></a>
### POST operation for bgp\_export\_filters
```
POST /bgp_export_filters
```


#### Description
Use this operation to add BGP Export Filters


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[bgp\_export\_filters\_request\_schema](#bgp\_export\_filters\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[bgp\_export\_filters\_post\_success\_schema](#bgp\_export\_filters\_post\_success\_schema)|
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

* bgp\_export\_filters


<a name="bgp\_export\_filters-get"></a>
### Get operation for bgp\_export\_filters
```
GET /bgp_export_filters
```


#### Description
Use this operation to get the BGP Export Filters


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[bgp\_export\_filters\_response\_schema](#bgp\_export\_filters\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* bgp\_export\_filters


<a name="bgp\_export\_filters-put"></a>
### PUT operation for bgp\_export\_filters
```
PUT /bgp_export_filters
```


#### Description
Use this operation to modify BGP Export Filters


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[bgp\_export\_filters\_put\_success\_schema](#bgp\_export\_filters\_put\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* bgp\_export\_filters


<a name="bgp\_export\_filters-deletepathparam-delete"></a>
### DELETE operation for bgp\_export\_filters
```
DELETE /bgp_export_filters/{deletePathParam}
```


#### Description
Use this operation to delete BGP Export Filters


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[bgp\_export\_filters\_delete\_success\_schema](#bgp\_export\_filters\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* bgp\_export\_filters




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="bgp\_export\_filters"></a>
### bgp\_export\_filters

|Name|Schema|
|---|---|
|**cost**  <br>*optional*|[cost](#cost)|
|**cost\_match\_type**  <br>*optional*|[cost\_match\_type](#cost\_match\_type)|
|**enabled**  <br>*optional*|[enabled](#enabled)|
|**export\_ospf\_route\_type**  <br>*optional*|[export\_ospf\_route\_type](#export\_ospf\_route\_type)|
|**export\_ospf\_route\_weight**  <br>*optional*|[export\_ospf\_route\_weight](#export\_ospf\_route\_weight)|
|**gateway\_ip\_address**  <br>*optional*|[gateway\_ip\_address](#gateway\_ip\_address)|
|**id**  <br>*optional*|[id](#id)|
|**include**  <br>*optional*|[include](#include)|
|**network\_ip\_address**  <br>*optional*|[network\_ip\_address](#network\_ip\_address)|
|**network\_object\_name**  <br>*optional*|[network\_object\_name](#network\_object\_name)|
|**order**  <br>*optional*|[order](#order)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**prefix**  <br>*optional*|[prefix](#prefix)|
|**prefix\_match\_type**  <br>*optional*|[prefix\_match\_type](#prefix\_match\_type)|
|**routing\_domain**  <br>*optional*|[routing\_domain](#routing\_domain)|
|**service\_type**  <br>*optional*|[service\_type](#service\_type)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**site\_or\_service\_name**  <br>*optional*|[site\_or\_service\_name](#site\_or\_service\_name)|


<a name="bgp\_export\_filters\_delete\_success\_schema"></a>
### bgp\_export\_filters\_delete\_success\_schema

|Name|Schema|
|---|---|
|**bgp\_export\_filters**  <br>*optional*|[bgp\_export\_filters](#bgp\_export\_filters\_delete\_success\_schema-bgp\_export\_filters)|

<a name="bgp\_export\_filters\_delete\_success\_schema-bgp\_export\_filters"></a>
**bgp\_export\_filters**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="bgp\_export\_filters\_post\_success\_schema"></a>
### bgp\_export\_filters\_post\_success\_schema

|Name|Schema|
|---|---|
|**bgp\_export\_filters**  <br>*optional*|[bgp\_export\_filters](#bgp\_export\_filters\_post\_success\_schema-bgp\_export\_filters)|

<a name="bgp\_export\_filters\_post\_success\_schema-bgp\_export\_filters"></a>
**bgp\_export\_filters**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="bgp\_export\_filters\_put\_success\_schema"></a>
### bgp\_export\_filters\_put\_success\_schema

|Name|Schema|
|---|---|
|**bgp\_export\_filters**  <br>*optional*|[bgp\_export\_filters](#bgp\_export\_filters\_put\_success\_schema-bgp\_export\_filters)|

<a name="bgp\_export\_filters\_put\_success\_schema-bgp\_export\_filters"></a>
**bgp\_export\_filters**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="bgp\_export\_filters\_request\_schema"></a>
### bgp\_export\_filters\_request\_schema

|Name|Schema|
|---|---|
|**bgp\_export\_filters**  <br>*optional*|[bgp\_export\_filters](#bgp\_export\_filters)|


<a name="bgp\_export\_filters\_response\_schema"></a>
### bgp\_export\_filters\_response\_schema
*Type* : < [bgp\_export\_filters\_response\_schema](#bgp\_export\_filters\_response\_schema-inline) > array

<a name="bgp\_export\_filters\_response\_schema-inline"></a>
**bgp\_export\_filters\_response\_schema**

|Name|Schema|
|---|---|
|**cost**  <br>*optional*|[cost](#cost)|
|**cost\_match\_type**  <br>*optional*|[cost\_match\_type](#cost\_match\_type)|
|**enabled**  <br>*optional*|[enabled](#enabled)|
|**export\_ospf\_route\_type**  <br>*optional*|[export\_ospf\_route\_type](#export\_ospf\_route\_type)|
|**export\_ospf\_route\_weight**  <br>*optional*|[export\_ospf\_route\_weight](#export\_ospf\_route\_weight)|
|**gateway\_ip\_address**  <br>*optional*|[gateway\_ip\_address](#gateway\_ip\_address)|
|**id**  <br>*optional*|[id](#id)|
|**include**  <br>*optional*|[include](#include)|
|**is\_auto**  <br>*optional*|[is\_auto](#is\_auto)|
|**network\_ip\_address**  <br>*optional*|[network\_ip\_address](#network\_ip\_address)|
|**network\_object\_name**  <br>*optional*|[network\_object\_name](#network\_object\_name)|
|**order**  <br>*optional*|[order](#order)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**prefix**  <br>*optional*|[prefix](#prefix)|
|**prefix\_match\_type**  <br>*optional*|[prefix\_match\_type](#prefix\_match\_type)|
|**routing\_domain**  <br>*optional*|[routing\_domain](#routing\_domain)|
|**service\_type**  <br>*optional*|[service\_type](#service\_type)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**site\_or\_service\_name**  <br>*optional*|[site\_or\_service\_name](#site\_or\_service\_name)|


<a name="cost"></a>
### cost
The route cost

*Type* : string


<a name="cost\_match\_type"></a>
### cost\_match\_type
Choose a method to match the route’s cost from the list of predicates (eq, lt, le, gt, or ge)

*Type* : enum (eq, lt, le, gt, ge)


<a name="enabled"></a>
### enabled
Set to true to Enable the filter. A filter that is not enabled has no effect.

*Type* : boolean


<a name="export\_ospf\_route\_type"></a>
### export\_ospf\_route\_type
Advertise the NetScaler SD-WAN route to OSPF neighbors as type 1 Intra-area route or type 5 External route. Default route is always advertised as type-5 External route to normal areas and type-3 summary route to stub areas.

*Type* : enum (type1\_intra\_area, type5\_as\_external)


<a name="export\_ospf\_route\_weight"></a>
### export\_ospf\_route\_weight
When export NetScaler SD-WAN routes to OSPF, add the weight to each route's NetScaler SD-WAN cost as total cost.

*Type* : integer


<a name="gateway\_ip\_address"></a>
### gateway\_ip\_address
The IP address of the gateway

*Type* : string


<a name="id"></a>
### id
Auto-generated ID to uniquely identify BGP Export Filter

*Type* : integer


<a name="include"></a>
### include
Set to true to include routes that match this filter. Otherwise matching routes are ignored.

*Type* : boolean


<a name="is\_auto"></a>
### is\_auto
to indicate that this is auto-generated

*Type* : boolean


<a name="network\_ip\_address"></a>
### network\_ip\_address
The IP address describing a route's destination

*Type* : string


<a name="network\_object\_name"></a>
### network\_object\_name
The Network Object describing a route's network. To set it to manual, pass manual as the value. To use an existing network object, pass its name

*Type* : string


<a name="order"></a>
### order
The Order in which filters are prioritized. Once filters are applied, they are automatically sorted by Order.

*Type* : integer


<a name="package\_name"></a>
### package\_name
Config package name using which the API operation should be performed.

*Type* : string


<a name="prefix"></a>
### prefix
The prefix used to match route's prefix

*Type* : string


<a name="prefix\_match\_type"></a>
### prefix\_match\_type
The method used to match a route's prefix

*Type* : enum (eq, lt, le, gt, ge)


<a name="routing\_domain"></a>
### routing\_domain
Choose one of the configured Routing Domains. Leave blank or any for Any Routing Domain

*Type* : string


<a name="service\_type"></a>
### service\_type
The service type

*Type* : enum (local, internet, intranet, gre\_tunnel, virtual\_path, lan\_ipsec\_tunnel, ip\_host)


<a name="site\_name"></a>
### site\_name
Site for which the feature is being configured

*Type* : string


<a name="site\_or\_service\_name"></a>
### site\_or\_service\_name
The name of the Service or Site (for Virtual Paths)

*Type* : string






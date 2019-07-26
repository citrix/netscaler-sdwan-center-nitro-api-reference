# ospf\_import\_filters


<a name="overview"></a>
## Overview
API to add, delete, get, modify OSPF Import Filters


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* ospf\_import\_filters : Operations related to ospf\_import\_filters 




<a name="paths"></a>
## Paths

<a name="ospf\_import\_filters-post"></a>
### POST operation for ospf\_import\_filters
```
POST /ospf_import_filters
```


#### Description
Use this operation to add OSPF Import Filters


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[ospf\_import\_filters\_request\_schema](#ospf\_import\_filters\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[ospf\_import\_filters\_post\_success\_schema](#ospf\_import\_filters\_post\_success\_schema)|
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

* ospf\_import\_filters


<a name="ospf\_import\_filters-get"></a>
### Get operation for ospf\_import\_filters
```
GET /ospf_import_filters
```


#### Description
Use this operation to get the OSPF Import Filters


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[ospf\_import\_filters\_response\_schema](#ospf\_import\_filters\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* ospf\_import\_filters


<a name="ospf\_import\_filters-put"></a>
### PUT operation for ospf\_import\_filters
```
PUT /ospf_import_filters
```


#### Description
Use this operation to modify OSPF Import Filters


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[ospf\_import\_filters\_put\_success\_schema](#ospf\_import\_filters\_put\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* ospf\_import\_filters


<a name="ospf\_import\_filters-deletepathparam-delete"></a>
### DELETE operation for ospf\_import\_filters
```
DELETE /ospf_import_filters/{deletePathParam}
```


#### Description
Use this operation to delete OSPF Import Filters


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[ospf\_import\_filters\_delete\_success\_schema](#ospf\_import\_filters\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* ospf\_import\_filters




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
The cost used to match routes (OSPF only)

*Type* : string


<a name="cost\_match\_type"></a>
### cost\_match\_type
Choose a method to match the route’s cost from the list of predicates (eq, lt, le, gt, or ge)

*Type* : enum (eq, lt, le, gt, ge)


<a name="destination\_ip\_address"></a>
### destination\_ip\_address
The IP address with prefix, describing a route's destination

*Type* : string


<a name="destination\_network\_object\_name"></a>
### destination\_network\_object\_name
The Network Object describing a route's destination. To set it to manual, pass manual as the value. To use an existing network object, pass its name

*Type* : string


<a name="eligibility\_based\_on\_gateway"></a>
### eligibility\_based\_on\_gateway
Set to true to ensure that traffic is not sent to matching routes if the Gateway is unreachable.

*Type* : boolean


<a name="eligibility\_based\_on\_path"></a>
### eligibility\_based\_on\_path
Set to true to allow eligibility based on path

*Type* : boolean


<a name="enabled"></a>
### enabled
Set to true to Enable the filter. A filter that is not enabled has no effect.

*Type* : boolean


<a name="export\_route\_to\_appliance"></a>
### export\_route\_to\_appliance
Set to true to export matching routes to Citrix Appliances at other Sites. This functionality is enabled by default and only applies for the following Service Types: Local, LAN GRE Tunnel.

*Type* : boolean


<a name="id"></a>
### id
Auto-generated ID to uniquely identify OSPF Import Filters

*Type* : integer


<a name="include"></a>
### include
Set to true to include routes that match this filter. Otherwise matching routes are ignored.

*Type* : boolean


<a name="is\_auto"></a>
### is\_auto
to indicate that this is auto-generated

*Type* : boolean


<a name="next\_hop"></a>
### next\_hop
The IP address of the next hop

*Type* : string


<a name="order"></a>
### order
The Order in which filters are prioritized. Once filters are applied, they are automatically sorted by Order.

*Type* : integer


<a name="ospf\_import\_filters"></a>
### ospf\_import\_filters

|Name|Schema|
|---|---|
|**cost**  <br>*optional*|[cost](#cost)|
|**cost\_match\_type**  <br>*optional*|[cost\_match\_type](#cost\_match\_type)|
|**destination\_ip\_address**  <br>*optional*|[destination\_ip\_address](#destination\_ip\_address)|
|**destination\_network\_object\_name**  <br>*optional*|[destination\_network\_object\_name](#destination\_network\_object\_name)|
|**eligibility\_based\_on\_gateway**  <br>*optional*|[eligibility\_based\_on\_gateway](#eligibility\_based\_on\_gateway)|
|**eligibility\_based\_on\_path**  <br>*optional*|[eligibility\_based\_on\_path](#eligibility\_based\_on\_path)|
|**enabled**  <br>*optional*|[enabled](#enabled)|
|**export\_route\_to\_appliance**  <br>*optional*|[export\_route\_to\_appliance](#export\_route\_to\_appliance)|
|**id**  <br>*optional*|[id](#id)|
|**include**  <br>*optional*|[include](#include)|
|**next\_hop**  <br>*optional*|[next\_hop](#next\_hop)|
|**order**  <br>*optional*|[order](#order)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**path**  <br>*optional*|[path](#path)|
|**prefix**  <br>*optional*|[prefix](#prefix)|
|**prefix\_match\_type**  <br>*optional*|[prefix\_match\_type](#prefix\_match\_type)|
|**protocol**  <br>*optional*|[protocol](#protocol)|
|**route\_tag**  <br>*optional*|[route\_tag](#route\_tag)|
|**routing\_domain**  <br>*optional*|[routing\_domain](#routing\_domain)|
|**sdwan\_cost**  <br>*optional*|[sdwan\_cost](#sdwan\_cost)|
|**service\_name**  <br>*optional*|[service\_name](#service\_name)|
|**service\_type**  <br>*optional*|[service\_type](#service\_type)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**source\_router\_ip\_address**  <br>*optional*|[source\_router\_ip\_address](#source\_router\_ip\_address)|
|**use\_ospf\_route\_cost**  <br>*optional*|[use\_ospf\_route\_cost](#use\_ospf\_route\_cost)|


<a name="ospf\_import\_filters\_delete\_success\_schema"></a>
### ospf\_import\_filters\_delete\_success\_schema

|Name|Schema|
|---|---|
|**ospf\_import\_filters**  <br>*optional*|[ospf\_import\_filters](#ospf\_import\_filters\_delete\_success\_schema-ospf\_import\_filters)|

<a name="ospf\_import\_filters\_delete\_success\_schema-ospf\_import\_filters"></a>
**ospf\_import\_filters**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="ospf\_import\_filters\_post\_success\_schema"></a>
### ospf\_import\_filters\_post\_success\_schema

|Name|Schema|
|---|---|
|**ospf\_import\_filters**  <br>*optional*|[ospf\_import\_filters](#ospf\_import\_filters\_post\_success\_schema-ospf\_import\_filters)|

<a name="ospf\_import\_filters\_post\_success\_schema-ospf\_import\_filters"></a>
**ospf\_import\_filters**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="ospf\_import\_filters\_put\_success\_schema"></a>
### ospf\_import\_filters\_put\_success\_schema

|Name|Schema|
|---|---|
|**ospf\_import\_filters**  <br>*optional*|[ospf\_import\_filters](#ospf\_import\_filters\_put\_success\_schema-ospf\_import\_filters)|

<a name="ospf\_import\_filters\_put\_success\_schema-ospf\_import\_filters"></a>
**ospf\_import\_filters**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="ospf\_import\_filters\_request\_schema"></a>
### ospf\_import\_filters\_request\_schema

|Name|Schema|
|---|---|
|**ospf\_import\_filters**  <br>*optional*|[ospf\_import\_filters](#ospf\_import\_filters)|


<a name="ospf\_import\_filters\_response\_schema"></a>
### ospf\_import\_filters\_response\_schema
*Type* : < [ospf\_import\_filters\_response\_schema](#ospf\_import\_filters\_response\_schema-inline) > array

<a name="ospf\_import\_filters\_response\_schema-inline"></a>
**ospf\_import\_filters\_response\_schema**

|Name|Schema|
|---|---|
|**cost**  <br>*optional*|[cost](#cost)|
|**cost\_match\_type**  <br>*optional*|[cost\_match\_type](#cost\_match\_type)|
|**destination\_ip\_address**  <br>*optional*|[destination\_ip\_address](#destination\_ip\_address)|
|**destination\_network\_object\_name**  <br>*optional*|[destination\_network\_object\_name](#destination\_network\_object\_name)|
|**eligibility\_based\_on\_gateway**  <br>*optional*|[eligibility\_based\_on\_gateway](#eligibility\_based\_on\_gateway)|
|**eligibility\_based\_on\_path**  <br>*optional*|[eligibility\_based\_on\_path](#eligibility\_based\_on\_path)|
|**enabled**  <br>*optional*|[enabled](#enabled)|
|**export\_route\_to\_appliance**  <br>*optional*|[export\_route\_to\_appliance](#export\_route\_to\_appliance)|
|**id**  <br>*optional*|[id](#id)|
|**include**  <br>*optional*|[include](#include)|
|**is\_auto**  <br>*optional*|[is\_auto](#is\_auto)|
|**next\_hop**  <br>*optional*|[next\_hop](#next\_hop)|
|**order**  <br>*optional*|[order](#order)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**path**  <br>*optional*|[path](#path)|
|**prefix**  <br>*optional*|[prefix](#prefix)|
|**prefix\_match\_type**  <br>*optional*|[prefix\_match\_type](#prefix\_match\_type)|
|**protocol**  <br>*optional*|[protocol](#protocol)|
|**route\_tag**  <br>*optional*|[route\_tag](#route\_tag)|
|**routing\_domain**  <br>*optional*|[routing\_domain](#routing\_domain)|
|**sdwan\_cost**  <br>*optional*|[sdwan\_cost](#sdwan\_cost)|
|**service\_name**  <br>*optional*|[service\_name](#service\_name)|
|**service\_type**  <br>*optional*|[service\_type](#service\_type)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**source\_router\_ip\_address**  <br>*optional*|[source\_router\_ip\_address](#source\_router\_ip\_address)|
|**use\_ospf\_route\_cost**  <br>*optional*|[use\_ospf\_route\_cost](#use\_ospf\_route\_cost)|


<a name="package\_name"></a>
### package\_name
Config package name using which the site API operation should be performed.

*Type* : string


<a name="path"></a>
### path
Path from which to determine Route eligibility

*Type* : string


<a name="prefix"></a>
### prefix
The prefix used to match route's prefix

*Type* : string


<a name="prefix\_match\_type"></a>
### prefix\_match\_type
The method used to match a route's prefix

*Type* : enum (eq, lt, le, gt, ge)


<a name="protocol"></a>
### protocol
Choose the protocol to learn routes from.

*Type* : enum (any, ospf, bgp)


<a name="route\_tag"></a>
### route\_tag
Enter the route tag that this filter will match or leave blank in order to not specify a route tag.

*Type* : string


<a name="routing\_domain"></a>
### routing\_domain
Choose one of the configured Routing Domains. Leave blank or any for Any Routing Domain

*Type* : string


<a name="sdwan\_cost"></a>
### sdwan\_cost
This cost will be applied to the matched routes when importing into Citrix Appliance route table(the default is 6).

*Type* : integer


<a name="service\_name"></a>
### service\_name
The name of the service that matching routes will use.

*Type* : string


<a name="service\_type"></a>
### service\_type
The service type

*Type* : enum (local, internet, intranet, gre\_tunnel, passthrough)


<a name="site\_name"></a>
### site\_name
Site Name

*Type* : string


<a name="source\_router\_ip\_address"></a>
### source\_router\_ip\_address
Enter the IP address of the Source Router, valid for iBGP only.

*Type* : string


<a name="use\_ospf\_route\_cost"></a>
### use\_ospf\_route\_cost
Enable this option for OSPF routes to prevent overriding OSPF cost with SD-WAN cost

*Type* : boolean






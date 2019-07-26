# interface\_groups


<a name="overview"></a>
## Overview
API to add, modify, delete, and get interface groups.


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* interface\_groups : Operations related to interface\_groups 




<a name="paths"></a>
## Paths

<a name="interface\_groups-post"></a>
### POST operation for interface\_groups
```
POST /interface_groups
```


#### Description
Use this operation to add interface group


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[interface\_groups\_post\_success\_schema](#interface\_groups\_post\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* interface\_groups


<a name="interface\_groups-get"></a>
### Get operation for interface\_groups
```
GET /interface_groups
```


#### Description
Use this operation to get the list of interface groups


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[interface\_groups\_response\_schema](#interface\_groups\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* interface\_groups


<a name="interface\_groups-put"></a>
### PUT operation for interface\_groups
```
PUT /interface_groups
```


#### Description
Use this operation to modify a Virtual IP address


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[interface\_groups\_request\_schema](#interface\_groups\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[interface\_groups\_put\_success\_schema](#interface\_groups\_put\_success\_schema)|
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

* interface\_groups


<a name="interface\_groups-deletepathparam-delete"></a>
### DELETE operation for interface\_groups
```
DELETE /interface_groups/{deletePathParam}
```


#### Description
Use this operation to delete an interface group.


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[interface\_groups\_delete\_success\_schema](#interface\_groups\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* interface\_groups




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="bridge\_pair"></a>
### bridge\_pair
Add brige pair associated with the group

*Type* : < [bridge\_pair](#bridge\_pair-inline) > array

<a name="bridge\_pair-inline"></a>
**bridge\_pair**

|Name|Description|Schema|
|---|---|---|
|**device\_one**  <br>*optional*|device one which forms the bridge pair|string|
|**device\_two**  <br>*optional*|device two which forms the bridge pair|string|
|**lsp\_enabled**  <br>*optional*|If enabled, the link state of the bridge pair are synchronized|boolean|


<a name="bypass\_mode"></a>
### bypass\_mode
The behavior of bridge-paired interfaces in the Interface Group in the event of Appliance/Service restart or failure.

*Type* : enum (fail\_to\_wire, fail\_to\_block)


<a name="eth\_interfaces"></a>
### eth\_interfaces
Give interface id to be included in ethernet interface

*Type* : < string > array


<a name="id"></a>
### id
*Type* : integer


<a name="interface\_groups"></a>
### interface\_groups

|Name|Schema|
|---|---|
|**bridge\_pair**  <br>*optional*|[bridge\_pair](#bridge\_pair)|
|**bypass\_mode**  <br>*optional*|[bypass\_mode](#bypass\_mode)|
|**eth\_interfaces**  <br>*optional*|[eth\_interfaces](#eth\_interfaces)|
|**id**  <br>*optional*|[id](#id)|
|**is\_bridged**  <br>*optional*|[is\_bridged](#is\_bridged)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**security**  <br>*optional*|[security](#security)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**virtual\_interfaces**  <br>*optional*|[virtual\_interfaces](#virtual\_interfaces)|
|**wccp**  <br>*optional*|[wccp](#wccp)|


<a name="interface\_groups\_delete\_success\_schema"></a>
### interface\_groups\_delete\_success\_schema

|Name|Schema|
|---|---|
|**interface\_groups**  <br>*optional*|[interface\_groups](#interface\_groups\_delete\_success\_schema-interface\_groups)|

<a name="interface\_groups\_delete\_success\_schema-interface\_groups"></a>
**interface\_groups**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="interface\_groups\_post\_success\_schema"></a>
### interface\_groups\_post\_success\_schema

|Name|Schema|
|---|---|
|**interface\_groups**  <br>*optional*|[interface\_groups](#interface\_groups\_post\_success\_schema-interface\_groups)|

<a name="interface\_groups\_post\_success\_schema-interface\_groups"></a>
**interface\_groups**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="interface\_groups\_put\_success\_schema"></a>
### interface\_groups\_put\_success\_schema

|Name|Schema|
|---|---|
|**interface\_groups**  <br>*optional*|[interface\_groups](#interface\_groups\_put\_success\_schema-interface\_groups)|

<a name="interface\_groups\_put\_success\_schema-interface\_groups"></a>
**interface\_groups**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="interface\_groups\_request\_schema"></a>
### interface\_groups\_request\_schema

|Name|Schema|
|---|---|
|**interface\_groups**  <br>*optional*|[interface\_groups](#interface\_groups)|


<a name="interface\_groups\_response\_schema"></a>
### interface\_groups\_response\_schema
*Type* : < [interface\_groups\_response\_schema](#interface\_groups\_response\_schema-inline) > array

<a name="interface\_groups\_response\_schema-inline"></a>
**interface\_groups\_response\_schema**

|Name|Schema|
|---|---|
|**bridge\_pair**  <br>*optional*|[bridge\_pair](#bridge\_pair)|
|**bypass\_mode**  <br>*optional*|[bypass\_mode](#bypass\_mode)|
|**eth\_interfaces**  <br>*optional*|[eth\_interfaces](#eth\_interfaces)|
|**id**  <br>*optional*|[id](#id)|
|**is\_bridged**  <br>*optional*|[is\_bridged](#is\_bridged)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**security**  <br>*optional*|[security](#security)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**virtual\_interfaces**  <br>*optional*|[virtual\_interfaces](#virtual\_interfaces)|
|**wccp**  <br>*optional*|[wccp](#wccp)|


<a name="is\_bridged"></a>
### is\_bridged
Enable bridge pairs between the selected interfaces.

*Type* : boolean


<a name="package\_name"></a>
### package\_name
Config package name using which the site API operation should be performed.

*Type* : string


<a name="security"></a>
### security
The security of the Interface Group's network segment. Trusted segments are generally protected by a firewall.

*Type* : enum (trusted, untrusted)


<a name="site\_name"></a>
### site\_name
Site Name in which interface group should be added.

*Type* : string


<a name="virtual\_interfaces"></a>
### virtual\_interfaces
List of virtual interfaces associated with the interface group.

*Type* : < [virtual\_interfaces](#virtual\_interfaces-inline) > array

<a name="virtual\_interfaces-inline"></a>
**virtual\_interfaces**

|Name|Description|Schema|
|---|---|---|
|**client\_mode**  <br>*optional*|The client mode can be DHCP, Static/Dynamic PPPOE for this interface.|string|
|**dhcp\_client**  <br>*optional*|The client mode can be DHCP, Static/Dynamic PPPOE for this interface.|boolean|
|**firewall\_zone**  <br>*optional*|Firewall zone|string|
|**name**  <br>*optional*|A name by which the Virtual Interface will be referenced.|string|
|**pppoe\_ac\_name**  <br>*optional*|PPPOE Account Name|string|
|**pppoe\_auth\_type**  <br>*optional*|PPPOE Authentication type can be auto, pap, chap, eap|string|
|**pppoe\_password**  <br>*optional*|PPPOE user password|string|
|**pppoe\_reconnect\_hold\_off\_time**  <br>*optional*|Wait time in seconds after which PPPOE sessions try to reconnect|integer|
|**pppoe\_service\_name**  <br>*optional*|PPPOE service name|string|
|**pppoe\_username**  <br>*optional*|PPPOE user name|string|
|**routing\_domain**  <br>*optional*|routing domain|string|
|**vlan\_id**  <br>*optional*|The ID for identifying and marking traffic to and from the Virtual Interface. An ID of '0' may be used for native/untagged traffic.|integer|


<a name="wccp"></a>
### wccp
Enabling this feature will cause the corresponding routing domain's TCP traffic to be redirected to the SD-WAN Optimization appliance for optimization. The listener should be enabled on interface groups with only ONE ethernet interface.

*Type* : boolean






# firewall\_policy\_template


<a name="overview"></a>
## Overview
API to add, modify, delete, and get configuration for Firewall policy templates


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* firewall\_policy\_template : Operations related to firewall\_policy\_template 




<a name="paths"></a>
## Paths

<a name="firewall\_policy\_template-post"></a>
### POST operation for firewall\_policy\_template
```
POST /firewall_policy_template
```


#### Description
Use this operation to add Firewall policy templates


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[firewall\_policy\_template\_request\_schema](#firewall\_policy\_template\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[firewall\_policy\_template\_post\_success\_schema](#firewall\_policy\_template\_post\_success\_schema)|
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

* firewall\_policy\_template


<a name="firewall\_policy\_template-get"></a>
### Get operation for firewall\_policy\_template
```
GET /firewall_policy_template
```


#### Description
Use this operation to get the Firewall policy templates


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[firewall\_policy\_template\_response\_schema](#firewall\_policy\_template\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* firewall\_policy\_template


<a name="firewall\_policy\_template-put"></a>
### PUT operation for firewall\_policy\_template
```
PUT /firewall_policy_template
```


#### Description
Use this operation to modify the Firewall policy templates


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[firewall\_policy\_template\_put\_success\_schema](#firewall\_policy\_template\_put\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* firewall\_policy\_template


<a name="firewall\_policy\_template-deletepathparam-delete"></a>
### DELETE operation for firewall\_policy\_template
```
DELETE /firewall_policy_template/{deletePathParam}
```


#### Description
Use this operation to delete Firewall policy templates


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[firewall\_policy\_template\_delete\_success\_schema](#firewall\_policy\_template\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* firewall\_policy\_template




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="firewall\_policy\_template"></a>
### firewall\_policy\_template

|Name|Schema|
|---|---|
|**firewall\_policy\_template\_name**  <br>*optional*|[firewall\_policy\_template\_name](#firewall\_policy\_template\_name)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**post\_appliance\_policies**  <br>*optional*|[post\_appliance\_policies](#post\_appliance\_policies)|
|**pre\_appliance\_policies**  <br>*optional*|[pre\_appliance\_policies](#pre\_appliance\_policies)|


<a name="firewall\_policy\_template\_delete\_success\_schema"></a>
### firewall\_policy\_template\_delete\_success\_schema

|Name|Schema|
|---|---|
|**firewall\_policy\_template**  <br>*optional*|[firewall\_policy\_template](#firewall\_policy\_template\_delete\_success\_schema-firewall\_policy\_template)|

<a name="firewall\_policy\_template\_delete\_success\_schema-firewall\_policy\_template"></a>
**firewall\_policy\_template**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="firewall\_policy\_template\_name"></a>
### firewall\_policy\_template\_name
Firewall policy template name

*Type* : string


<a name="firewall\_policy\_template\_post\_success\_schema"></a>
### firewall\_policy\_template\_post\_success\_schema

|Name|Schema|
|---|---|
|**firewall\_policy\_template**  <br>*optional*|[firewall\_policy\_template](#firewall\_policy\_template\_post\_success\_schema-firewall\_policy\_template)|

<a name="firewall\_policy\_template\_post\_success\_schema-firewall\_policy\_template"></a>
**firewall\_policy\_template**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="firewall\_policy\_template\_put\_success\_schema"></a>
### firewall\_policy\_template\_put\_success\_schema

|Name|Schema|
|---|---|
|**firewall\_policy\_template**  <br>*optional*|[firewall\_policy\_template](#firewall\_policy\_template\_put\_success\_schema-firewall\_policy\_template)|

<a name="firewall\_policy\_template\_put\_success\_schema-firewall\_policy\_template"></a>
**firewall\_policy\_template**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="firewall\_policy\_template\_request\_schema"></a>
### firewall\_policy\_template\_request\_schema

|Name|Schema|
|---|---|
|**firewall\_policy\_template**  <br>*optional*|[firewall\_policy\_template](#firewall\_policy\_template)|


<a name="firewall\_policy\_template\_response\_schema"></a>
### firewall\_policy\_template\_response\_schema
*Type* : < [firewall\_policy\_template\_response\_schema](#firewall\_policy\_template\_response\_schema-inline) > array

<a name="firewall\_policy\_template\_response\_schema-inline"></a>
**firewall\_policy\_template\_response\_schema**

|Name|Schema|
|---|---|
|**firewall\_policy\_template\_name**  <br>*optional*|[firewall\_policy\_template\_name](#firewall\_policy\_template\_name)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**post\_appliance\_policies**  <br>*optional*|[post\_appliance\_policies](#post\_appliance\_policies)|
|**pre\_appliance\_policies**  <br>*optional*|[pre\_appliance\_policies](#pre\_appliance\_policies)|


<a name="package\_name"></a>
### package\_name
Config package name using which the firewall policy template API operation should be performed.

*Type* : string


<a name="post\_appliance\_policies"></a>
### post\_appliance\_policies
Post appliance policies

*Type* : < [post\_appliance\_policies](#post\_appliance\_policies-inline) > array

<a name="post\_appliance\_policies-inline"></a>
**post\_appliance\_policies**

|Name|Description|Schema|
|---|---|---|
|**action**  <br>*optional*|The Action to take for each packet matching the Filter.  <br>**Default** : `"allow"`|enum (allow, drop, reject, count\_and\_continue)|
|**allow\_fragments**  <br>*optional*|To allow fragmented packets matching the Filter.  <br>**Default** : `true`|boolean|
|**application**  <br>*optional*|The Application used as match criteria for this Filter.|string|
|**application\_family**  <br>*optional*|The Application used as match criteria for this Filter.|string|
|**application\_objects**  <br>*optional*|The Application used as match criteria for this Filter.  <br>**Default** : `"any"`|string|
|**destination\_ip\_address**  <br>*optional*|The Destination IP Address and Subnet Mask that the Filter will match.|string|
|**destination\_port**  <br>*optional*|The Destination Port or Port Range that the Filter will match.|integer|
|**destination\_service\_name**  <br>*optional*|The Destination service that the filter will match  <br>**Default** : `"any"`|string|
|**destination\_service\_type**  <br>*optional*|The Destination Service Type that the Filter will match.  <br>**Default** : `"any"`|enum (any, local, virtual\_path, internet, intranet, gre\_tunnel, lan\_ipsec\_tunnel, ip\_host, multicast)|
|**from\_zones**  <br>*optional*|Select to filter on the zone the packet originated from  <br>**Default** : `"any"`|enum (any, default\_lan\_zone, internet\_zone, untrusted\_internet\_zone)|
|**ip\_dscp**  <br>*optional*|The time, in seconds, to wait for new packets before closing a UDP session that has not seen traffic in both directions.  <br>**Default** : `"ANY"`|enum (ANY, DEFAULT, af11, af12, af13, af21, af22, af23, af31, af32, af33, af41, af42, af43, cs1, cs2, cs3, cs4, cs5, cs6, cs7, ef)|
|**ip\_protocol\_num**  <br>*optional*|The IP Protocol that the Filter will match.|integer|
|**log\_connection\_end**  <br>*optional*|To generate a log when a Connection matching this Filter is deleted.  <br>**Default** : `false`|boolean|
|**log\_connection\_start**  <br>*optional*|To generate a log when a new Connection is created by a packet matching this Filter.  <br>**Default** : `false`|boolean|
|**log\_interval**  <br>*optional*|The time, in seconds, between logging the number of packets matching the filter (0 = disabled, valid settings are 60-600).|integer|
|**match\_established**  <br>*optional*|To match incoming packets for a Connection to which outgoing packets were allowed.  <br>**Default** : `false`|boolean|
|**match\_type**  <br>*optional*|The Application used as match criteria for this Filter.  <br>**Default** : `"any;"`|enum (ip\_protocol, application, application\_family, application\_objects)|
|**priority**  <br>*optional*  <br>*read-only*|The order/precedence in which Filters are applied (automatically redistributed).|integer|
|**reverse\_also**  <br>*optional*|Click the checkbox to automatically add a copy of this Filter with the Source and Destination settings reversed.  <br>**Default** : `false`|boolean|
|**source\_ip\_address**  <br>*optional*|The Source IP Address and Subnet Mask that the Filter will match.|string|
|**source\_port**  <br>*optional*|The Source Port or Port Range that the Filter will match.|integer|
|**source\_service\_name**  <br>*optional*|The Source service that the filter will match  <br>**Default** : `"any"`|string|
|**source\_service\_type**  <br>*optional*|The Source Service Type that the Filter will match.  <br>**Default** : `"any"`|enum (any, local, virtual\_path, internet, intranet, gre\_tunnel, lan\_ipsec\_tunnel, ip\_host, multicast)|
|**to\_zones**  <br>*optional*|Select to filter on the zone the packet is destined to  <br>**Default** : `"any"`|enum (any, default\_lan\_zone, internet\_zone, untrusted\_internet\_zone)|
|**track\_connection**  <br>*optional*|Whether or not to enable bidirectional connection state tracking for TCP, UDP and ICMP packets matching this Filter. This feature will block flows which appear illegitimate, due to asymmetric routing or failure of checksum, protocol specific validation -- proceed with caution if NetScaler SD-WAN is not fully inline.  <br>**Default** : `true`|boolean|


<a name="pre\_appliance\_policies"></a>
### pre\_appliance\_policies
Pre appliance policies

*Type* : < [pre\_appliance\_policies](#pre\_appliance\_policies-inline) > array

<a name="pre\_appliance\_policies-inline"></a>
**pre\_appliance\_policies**

|Name|Description|Schema|
|---|---|---|
|**action**  <br>*optional*|The Action to take for each packet matching the Filter.  <br>**Default** : `"allow"`|enum (allow, drop, reject, count\_and\_continue)|
|**allow\_fragments**  <br>*optional*|To allow fragmented packets matching the Filter.  <br>**Default** : `true`|boolean|
|**application**  <br>*optional*|The Application used as match criteria for this Filter.|string|
|**application\_family**  <br>*optional*|The Application used as match criteria for this Filter.|string|
|**application\_objects**  <br>*optional*|The Application used as match criteria for this Filter.  <br>**Default** : `"any"`|string|
|**destination\_ip\_address**  <br>*optional*|The Destination IP Address and Subnet Mask that the Filter will match.|string|
|**destination\_port**  <br>*optional*|The Destination Port or Port Range that the Filter will match.|integer|
|**destination\_service\_name**  <br>*optional*|The Destination service that the filter will match  <br>**Default** : `"any"`|string|
|**destination\_service\_type**  <br>*optional*|The Destination Service Type that the Filter will match.  <br>**Default** : `"any"`|enum (any, local, virtual\_path, internet, intranet, gre\_tunnel, lan\_ipsec\_tunnel, ip\_host, multicast)|
|**from\_zones**  <br>*optional*|Select to filter on the zone the packet originated from  <br>**Default** : `"any"`|enum (any, default\_lan\_zone, internet\_zone, untrusted\_internet\_zone)|
|**ip\_dscp**  <br>*optional*|The time, in seconds, to wait for new packets before closing a UDP session that has not seen traffic in both directions.  <br>**Default** : `"ANY"`|enum (ANY, DEFAULT, af11, af12, af13, af21, af22, af23, af31, af32, af33, af41, af42, af43, cs1, cs2, cs3, cs4, cs5, cs6, cs7, ef)|
|**ip\_protocol\_num**  <br>*optional*|The IP Protocol that the Filter will match.|integer|
|**log\_connection\_end**  <br>*optional*|To generate a log when a Connection matching this Filter is deleted.  <br>**Default** : `false`|boolean|
|**log\_connection\_start**  <br>*optional*|To generate a log when a new Connection is created by a packet matching this Filter.  <br>**Default** : `false`|boolean|
|**log\_interval**  <br>*optional*|The time, in seconds, between logging the number of packets matching the filter (0 = disabled, valid settings are 60-600).|integer|
|**match\_established**  <br>*optional*|To match incoming packets for a Connection to which outgoing packets were allowed.  <br>**Default** : `false`|boolean|
|**match\_type**  <br>*optional*|The Application used as match criteria for this Filter.  <br>**Default** : `"any;"`|enum (ip\_protocol, application, application\_family, application\_objects)|
|**priority**  <br>*optional*  <br>*read-only*|The order/precedence in which Filters are applied (automatically redistributed).|integer|
|**reverse\_also**  <br>*optional*|Click the checkbox to automatically add a copy of this Filter with the Source and Destination settings reversed.  <br>**Default** : `false`|boolean|
|**source\_ip\_address**  <br>*optional*|The Source IP Address and Subnet Mask that the Filter will match.|string|
|**source\_port**  <br>*optional*|The Source Port or Port Range that the Filter will match.|integer|
|**source\_service\_name**  <br>*optional*|The Source service that the filter will match  <br>**Default** : `"any"`|string|
|**source\_service\_type**  <br>*optional*|The Source Service Type that the Filter will match.  <br>**Default** : `"any"`|enum (any, local, virtual\_path, internet, intranet, gre\_tunnel, lan\_ipsec\_tunnel, ip\_host, multicast)|
|**to\_zones**  <br>*optional*|Select to filter on the zone the packet is destined to  <br>**Default** : `"any"`|enum (any, default\_lan\_zone, internet\_zone, untrusted\_internet\_zone)|
|**track\_connection**  <br>*optional*|Whether or not to enable bidirectional connection state tracking for TCP, UDP and ICMP packets matching this Filter. This feature will block flows which appear illegitimate, due to asymmetric routing or failure of checksum, protocol specific validation -- proceed with caution if NetScaler SD-WAN is not fully inline.  <br>**Default** : `true`|boolean|






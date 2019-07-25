# firewall


<a name="overview"></a>
## Overview
API to add, modify, delete, and get configuration for Firewall settings


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* firewall : Operations related to firewall 




<a name="paths"></a>
## Paths

<a name="firewall-post"></a>
### POST operation for firewall
```
POST /firewall
```


#### Description
Use this operation to add the firewall settings


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[firewall\_request\_schema](#firewall\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[firewall\_post\_success\_schema](#firewall\_post\_success\_schema)|
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

* firewall


<a name="firewall-get"></a>
### Get operation for firewall
```
GET /firewall
```


#### Description
Use this operation to get the firewall settings


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[firewall\_response\_schema](#firewall\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* firewall


<a name="firewall-put"></a>
### PUT operation for firewall
```
PUT /firewall
```


#### Description
Use this operation to modify the firewall settings


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[firewall\_put\_success\_schema](#firewall\_put\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* firewall


<a name="firewall-deletepathparam-delete"></a>
### DELETE operation for firewall
```
DELETE /firewall/{deletePathParam}
```


#### Description
Use this operation to delete the firewall settings


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[firewall\_delete\_success\_schema](#firewall\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* firewall




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="firewall"></a>
### firewall

|Name|Schema|
|---|---|
|**firewall\_destination\_nat\_policy**  <br>*optional*|[firewall\_destination\_nat\_policy](#firewall\_destination\_nat\_policy)|
|**firewall\_dynamic\_nat\_policy**  <br>*optional*|[firewall\_dynamic\_nat\_policy](#firewall\_dynamic\_nat\_policy)|
|**firewall\_local\_policy**  <br>*optional*|[firewall\_local\_policy](#firewall\_local\_policy)|
|**firewall\_settings**  <br>*optional*|[firewall\_settings](#firewall\_settings)|
|**firewall\_static\_nat\_policy**  <br>*optional*|[firewall\_static\_nat\_policy](#firewall\_static\_nat\_policy)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|


<a name="firewall\_delete\_success\_schema"></a>
### firewall\_delete\_success\_schema

|Name|Schema|
|---|---|
|**firewall**  <br>*optional*|[firewall](#firewall\_delete\_success\_schema-firewall)|

<a name="firewall\_delete\_success\_schema-firewall"></a>
**firewall**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="firewall\_destination\_nat\_policy"></a>
### firewall\_destination\_nat\_policy
Destination NAT Policy for firewall

*Type* : < [firewall\_destination\_nat\_policy](#firewall\_destination\_nat\_policy-inline) > array

<a name="firewall\_destination\_nat\_policy-inline"></a>
**firewall\_destination\_nat\_policy**

|Name|Description|Schema|
|---|---|---|
|**direction**  <br>*optional*|The direction, from the Service or Virtual Interface perspective, the translation will operate.  <br>**Default** : `"outbound"`|enum (inbound, outbound)|
|**id**  <br>*optional*|Firewall destination NATs policy id|integer|
|**inside\_network\_ip\_address**  <br>*optional*|The Inside IP Address and Prefix to translate (Destination IP Address in the direction selected).|string|
|**inside\_port**  <br>*optional*|The Inside Port or port range to translate (Destination port/port range in the direction selected).  <br>**Default** : `"1-65535"`|string|
|**outside\_network\_ip\_address**  <br>*optional*|The Outside IP Address packets will be translated to (Destination IP Address in the direction selected).|string|
|**outside\_port**  <br>*optional*|The Outside Port packets will be translated to (Destination port in the direction selected(0: do not NAT the Port)).|integer|
|**priority**  <br>*optional*  <br>*read-only*|The order/precedence in which Filters are applied (automatically redistributed).|integer|
|**service\_name**  <br>*optional*|The Service Name that the translation applies to.|string|
|**service\_type**  <br>*optional*|The Service Type that the translation applies to.|enum (local, internet, intranet)|


<a name="firewall\_dynamic\_nat\_policy"></a>
### firewall\_dynamic\_nat\_policy
Dynamic NAT Policy for firewall

*Type* : < [firewall\_dynamic\_nat\_policy](#firewall\_dynamic\_nat\_policy-inline) > array

<a name="firewall\_dynamic\_nat\_policy-inline"></a>
**firewall\_dynamic\_nat\_policy**

|Name|Description|Schema|
|---|---|---|
|**allow\_related**  <br>*optional*|To allow packets related to a Connection (ICMP error packets).  <br>**Default** : `false`|boolean|
|**bind\_responder\_route**  <br>*optional*|If enabled, the route for the responder's traffic will be bound to the Source Service.  <br>**Default** : `false`|boolean|
|**direction**  <br>*optional*|The direction, from the Service or Virtual Interface perspective, the translation will operate.  <br>**Default** : `"outbound"`|enum (inbound, outbound)|
|**enable\_gre\_pptp\_passthrough**  <br>*optional*|To allow a GRE/PPTP session to be translated. Only a single session from the inside network will be permitted.  <br>**Default** : `false`|boolean|
|**enable\_ipsec\_passthrough**  <br>*optional*|To allow an IPsec (AH/ESP) session to be translated. Only a single session from the inside network will be permitted.  <br>**Default** : `false`|boolean|
|**id**  <br>*optional*|Firewall dynamic NATs policy id|integer|
|**inside\_network\_ip\_address**  <br>*optional*|The Inside IP Address and Prefix to translate (Source IP Address in the direction selected).|string|
|**inside\_zone**  <br>*optional*|The Inside Zone to translate.  <br>**Default** : `"any"`|enum (any, Internet\_Zone, Untrusted\_Internet\_Zone, Default\_LAN\_Zone)|
|**outside\_network\_ip\_address**  <br>*optional*|The Outside IP Address and Subnet Mask packets will be translated to (Source IP Address in the direction selected).|string|
|**outside\_zone**  <br>*optional*|The Zone a packet must be destined for to allow translation.|enum (Internet\_Zone, Untrusted\_Internet\_Zone, Default\_LAN\_Zone)|
|**port\_forwarding\_rules**  <br>*optional*|Port Forwarding Rules|< [port\_forwarding\_rules](#firewall\_dynamic\_nat\_policy-port\_forwarding\_rules) > array|
|**port\_parity**  <br>*optional*|If enabled, outside ports for NAT connections will maintain parity (even if inside port is even, odd if outside port is odd).  <br>**Default** : `false`|boolean|
|**priority**  <br>*optional*  <br>*read-only*|The order/precedence in which Filters are applied (automatically redistributed).|integer|
|**service\_name**  <br>*optional*|The Service Name that the translation applies to.|string|
|**service\_type**  <br>*optional*|The Service Type that the translation applies to.|enum (local, internet, intranet)|
|**type**  <br>*optional*|The type of Dynamic NAT to perform.  <br>**Default** : `"port_restricted"`|enum (port\_restricted, symmetric)|

<a name="firewall\_dynamic\_nat\_policy-port\_forwarding\_rules"></a>
**port\_forwarding\_rules**

|Name|Description|Schema|
|---|---|---|
|**allow\_fragments**  <br>*optional*|To enable forwarding of packet fragments.  <br>**Default** : `true`|boolean|
|**inside\_network\_ip\_address**  <br>*optional*|The Inside IP address to forward to.|string|
|**inside\_port**  <br>*optional*|The Inside port or port range to forward to. If a range is configured, it must define the name number of ports as the Outside Port.  <br>**Default** : `"1-65535"`|string|
|**log\_connection\_end**  <br>*optional*|To generate a log when a Connection matching this Rule is deleted.  <br>**Default** : `false`|boolean|
|**log\_connection\_start**  <br>*optional*|To generate a log when a new Connection is created by a packet matching this Rule.  <br>**Default** : `false`|boolean|
|**log\_interval**  <br>*optional*|The time, in seconds, between logging the number of packets matching the rule (0 = disabled, valid settings are 60-600).|integer|
|**outside\_port**  <br>*optional*|The Outside port or port range to forward.  <br>**Default** : `"1-65535"`|string|
|**protocol**  <br>*optional*|The IP protocol to forward.  <br>**Default** : `"both"`|enum (both, TCP, UDP)|
|**track\_connection**  <br>*optional*|Whether or not to enable bidirectional connection state tracking for TCP, UDP and ICMP packets matching this Rule. This feature will block flows which appear illegitimate, due to asymmetric routing or failure of checksum, protocol specific validation -- proceed with caution if NetScaler SD-WAN is not fully inline.  <br>**Default** : `true`|boolean|


<a name="firewall\_local\_policy"></a>
### firewall\_local\_policy
Local policy for firewall

*Type* : < [firewall\_local\_policy](#firewall\_local\_policy-inline) > array

<a name="firewall\_local\_policy-inline"></a>
**firewall\_local\_policy**

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
|**id**  <br>*optional*|Firewall local policy id|integer|
|**ip\_dscp**  <br>*optional*|The time, in seconds, to wait for new packets before closing a UDP session that has not seen traffic in both directions.  <br>**Default** : `"ANY"`|enum (ANY, DEFAULT, af11, af12, af13, af21, af22, af23, af31, af32, af33, af41, af42, af43, cs1, cs2, cs3, cs4, cs5, cs6, cs7, ef)|
|**ip\_protocol\_num**  <br>*optional*|The IP Protocol that the Filter will match.|integer|
|**log\_connection\_end**  <br>*optional*|To generate a log when a Connection matching this Filter is deleted.  <br>**Default** : `false`|boolean|
|**log\_connection\_start**  <br>*optional*|To generate a log when a new Connection is created by a packet matching this Filter.  <br>**Default** : `false`|boolean|
|**log\_interval**  <br>*optional*|The time, in seconds, between logging the number of packets matching the filter (0 = disabled, valid settings are 60-600).|integer|
|**match\_established**  <br>*optional*|To match incoming packets for a Connection to which outgoing packets were allowed.  <br>**Default** : `false`|boolean|
|**match\_type**  <br>*optional*|The Application used as match criteria for this Filter.  <br>**Default** : `"any;"`|enum (ip\_protocol, application, application\_family, application\_objects)|
|**priority**  <br>*optional*|The order/precedence in which Filters are applied (automatically redistributed).|integer|
|**reverse\_also**  <br>*optional*|Click the checkbox to automatically add a copy of this Filter with the Source and Destination settings reversed.  <br>**Default** : `false`|boolean|
|**source\_ip\_address**  <br>*optional*|The Source IP Address and Subnet Mask that the Filter will match.|string|
|**source\_port**  <br>*optional*|The Source Port or Port Range that the Filter will match.|integer|
|**source\_service\_name**  <br>*optional*|The Source service that the filter will match  <br>**Default** : `"any"`|string|
|**source\_service\_type**  <br>*optional*|The Source Service Type that the Filter will match.  <br>**Default** : `"any"`|enum (any, local, virtual\_path, internet, intranet, gre\_tunnel, lan\_ipsec\_tunnel, ip\_host, multicast)|
|**to\_zones**  <br>*optional*|Select to filter on the zone the packet is destined to  <br>**Default** : `"any"`|enum (any, default\_lan\_zone, internet\_zone, untrusted\_internet\_zone)|
|**track\_connection**  <br>*optional*|Whether or not to enable bidirectional connection state tracking for TCP, UDP and ICMP packets matching this Filter. This feature will block flows which appear illegitimate, due to asymmetric routing or failure of checksum, protocol specific validation -- proceed with caution if NetScaler SD-WAN is not fully inline.  <br>**Default** : `true`|boolean|


<a name="firewall\_post\_success\_schema"></a>
### firewall\_post\_success\_schema

|Name|Schema|
|---|---|
|**firewall**  <br>*optional*|[firewall](#firewall\_post\_success\_schema-firewall)|

<a name="firewall\_post\_success\_schema-firewall"></a>
**firewall**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="firewall\_put\_success\_schema"></a>
### firewall\_put\_success\_schema

|Name|Schema|
|---|---|
|**firewall**  <br>*optional*|[firewall](#firewall\_put\_success\_schema-firewall)|

<a name="firewall\_put\_success\_schema-firewall"></a>
**firewall**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="firewall\_request\_schema"></a>
### firewall\_request\_schema

|Name|Schema|
|---|---|
|**firewall**  <br>*optional*|[firewall](#firewall)|


<a name="firewall\_response\_schema"></a>
### firewall\_response\_schema
*Type* : < [firewall\_response\_schema](#firewall\_response\_schema-inline) > array

<a name="firewall\_response\_schema-inline"></a>
**firewall\_response\_schema**

|Name|Schema|
|---|---|
|**firewall\_destination\_nat\_policy**  <br>*optional*|[firewall\_destination\_nat\_policy](#firewall\_destination\_nat\_policy)|
|**firewall\_dynamic\_nat\_policy**  <br>*optional*|[firewall\_dynamic\_nat\_policy](#firewall\_dynamic\_nat\_policy)|
|**firewall\_local\_policy**  <br>*optional*|[firewall\_local\_policy](#firewall\_local\_policy)|
|**firewall\_settings**  <br>*optional*|[firewall\_settings](#firewall\_settings)|
|**firewall\_static\_nat\_policy**  <br>*optional*|[firewall\_static\_nat\_policy](#firewall\_static\_nat\_policy)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|


<a name="firewall\_settings"></a>
### firewall\_settings
Basic settings for firewall

*Type* : < [firewall\_settings](#firewall\_settings-inline) > array

<a name="firewall\_settings-inline"></a>
**firewall\_settings**

|Name|Description|Schema|
|---|---|---|
|**default\_firewall\_action**  <br>*optional*|The action for packets that do not match a policy.  <br>**Default** : `"allow"`|enum (allow, drop)|
|**default\_track\_connection**  <br>*optional*|Whether or not to enable bidirectional connection state tracking for TCP, UDP and ICMP packets that do not match a filter policy or NAT rule. This feature will block flows which appear illegitimate, due to asymmetric routing or failure of checksum, protocol specific validation -- proceed with caution if NetScaler SD-WAN is not fully inline.  <br>**Default** : `true`|boolean|
|**generic\_idle\_timeout\_seconds**  <br>*optional*|The time, in seconds, to wait for new packets before closing an active generic session.|integer|
|**generic\_initial\_timeout\_seconds**  <br>*optional*|The time, in seconds, to wait for new packets before closing a generic session that has not seen traffic in both directions.|integer|
|**icmp\_idle\_timeout\_seconds**  <br>*optional*|The time, in seconds, to wait for new packets before closing an active ICMP session.|integer|
|**icmp\_initial\_timeout\_seconds**  <br>*optional*|The time, in seconds, to wait for new packets before closing an ICMP session that has not seen traffic in both directions.|integer|
|**max\_new\_connections\_per\_source**  <br>*optional*|The maximum number of non-established Connections to allow per Source IP Address. 0 = unlimited.|integer|
|**policy\_template\_name**  <br>*optional*|This is the name of the Policy Template defined globally whose filters will be included in this site's collection of firewall filters.|string|
|**priority**  <br>*optional*  <br>*read-only*|The order/precedence in which Filters are applied (automatically redistributed).|integer|
|**source\_route\_validation**  <br>*optional*|If enabled, packets will be dropped when received on an interface that differs from the packet's route, as determined by the Source IP address.  <br>**Default** : `false`|boolean|
|**tcp\_closed\_timeout\_seconds**  <br>*optional*|The time, in seconds, to wait for new packets before closing an aborted TCP session.|integer|
|**tcp\_closing\_timeout\_seconds**  <br>*optional*|The time, in seconds, to wait for new packets before closing a TCP session after a request to terminate.|integer|
|**tcp\_idle\_timeout\_seconds**  <br>*optional*|The time, in seconds, to wait for new packets before closing an active TCP session.|integer|
|**tcp\_initial\_timeout\_seconds**  <br>*optional*|The time, in seconds, to wait for new packets before closing a TCP session that has not completed a handshake.|integer|
|**tcp\_timewait\_seconds**  <br>*optional*|The time, in seconds, to wait for new packets before closing a terminated TCP session.|integer|
|**udp\_idle\_timeout\_seconds**  <br>*optional*|The time, in seconds, to wait for new packets before closing an active UDP session.|integer|
|**udp\_initial\_timeout\_seconds**  <br>*optional*|The time, in seconds, to wait for new packets before closing a UDP session that has not seen traffic in both directions.|integer|
|**untracked\_and\_denied\_timeout\_seconds**  <br>*optional*|The time, in seconds, to wait for new packets before closing Untracked or Denied Connections.|integer|


<a name="firewall\_static\_nat\_policy"></a>
### firewall\_static\_nat\_policy
Static NAT Policy for firewall

*Type* : < [firewall\_static\_nat\_policy](#firewall\_static\_nat\_policy-inline) > array

<a name="firewall\_static\_nat\_policy-inline"></a>
**firewall\_static\_nat\_policy**

|Name|Description|Schema|
|---|---|---|
|**bind\_responder\_route**  <br>*optional*|If enabled, the route for the responder's traffic will be bound to the Source Service.  <br>**Default** : `false`|boolean|
|**direction**  <br>*optional*|The direction, from the Service or Virtual Interface perspective, the translation will operate.  <br>**Default** : `"outbound"`|enum (inbound, outbound)|
|**id**  <br>*optional*|Firewall local policy id|integer|
|**inside\_network\_ip\_address**  <br>*optional*|The Inside IP Address and Prefix to translate (Source IP Address in the direction selected).|string|
|**inside\_zone**  <br>*optional*|The Zone a packet must be from to allow translation.  <br>**Default** : `"Internet_Zone"`|enum (Internet\_Zone, Untrusted\_Internet\_Zone, Default\_LAN\_Zone)|
|**outside\_network\_ip\_address**  <br>*optional*|The Outside IP Address and Subnet Mask packets will be translated to (Source IP Address in the direction selected).|string|
|**outside\_zone**  <br>*optional*|The Zone a packet must be destined for to allow translation.  <br>**Default** : `"Default_LAN_Zone"`|enum (Internet\_Zone, Untrusted\_Internet\_Zone, Default\_LAN\_Zone)|
|**priority**  <br>*optional*  <br>*read-only*|The order/precedence in which Filters are applied (automatically redistributed).|integer|
|**service\_name**  <br>*optional*|The Service Name that the translation applies to.|string|
|**service\_type**  <br>*optional*|The Service Type that the translation applies to.|enum (local, internet, intranet)|


<a name="package\_name"></a>
### package\_name
Config package name using which the firewall API operation should be performed.

*Type* : string


<a name="site\_name"></a>
### site\_name
Site Name

*Type* : string






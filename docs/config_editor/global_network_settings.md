# global\_network\_settings


<a name="overview"></a>
## Overview
API to get, modify global Network Settings.


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* global\_network\_settings : Operations related to global\_network\_settings 




<a name="paths"></a>
## Paths

<a name="global\_network\_settings-get"></a>
### Get operation for global\_network\_settings
```
GET /global_network_settings
```


#### Description
Use this operation to get the current values of Global Network settings


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[global\_network\_settings\_response\_schema](#global\_network\_settings\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* global\_network\_settings


<a name="global\_network\_settings-put"></a>
### PUT operation for global\_network\_settings
```
PUT /global_network_settings
```


#### Description
Use this operation to modify the current values of Global Network settings


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[global\_network\_settings\_request\_schema](#global\_network\_settings\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[global\_network\_settings\_put\_success\_schema](#global\_network\_settings\_put\_success\_schema)|
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

* global\_network\_settings




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="default\_connection\_state\_tracking"></a>
### default\_connection\_state\_tracking
Set to true to enable bidirectional connection state tracking for TCP, UDP and ICMP flows that do not match a filter policy or NAT rule. Asymmetric flows will be blocked when this is enabled even when there are no Firewall policies defined. The settings may be defined at the site level which will override the global setting. If there is the possibility of asymmetric flows at a site, the recommendation is to enable this at a site or policy level and not globally.

*Type* : boolean


<a name="default\_firewall\_action"></a>
### default\_firewall\_action
The action for packets the do not match a policy. This policy may be overridden at an Appliance.

*Type* : enum (allow, drop)


<a name="denied\_timeout"></a>
### denied\_timeout
The time, in seconds, to wait for new packets before closing Denied Connections.

*Type* : integer


<a name="enable\_encryption\_key\_rotation"></a>
### enable\_encryption\_key\_rotation
Set to true to enable encryption key rotation. If enabled, Encryption Keys are rotated at intervals of 10-15 minutes

*Type* : boolean


<a name="enable\_extended\_packet\_authentication\_trailer"></a>
### enable\_extended\_packet\_authentication\_trailer
Set to true to enable extended packet authentication trailer. If enabled, an authentication code is appended to the contents of encrypted traffic to verify the message is delivered unaltered

*Type* : boolean


<a name="enable\_extended\_packet\_encryption\_header"></a>
### enable\_extended\_packet\_encryption\_header
Set to true to enable extended packet encryption header. If enabled, a 16 byte encrypted counter is prepended to encrypted traffic to serve as an Initialization Vector and randomize packet encryption

*Type* : boolean


<a name="enable\_fips\_mode"></a>
### enable\_fips\_mode
Set to true to enable FIPS mode. If enabled, a strict FIPS compliance checking is enforced to meet requirements for all sites

*Type* : boolean


<a name="extended\_packet\_authentication\_trailer\_type"></a>
### extended\_packet\_authentication\_trailer\_type
The type of trailer used to validate packet contents

*Type* : enum (32-Bit Checksum, SHA-256)


<a name="generic\_idle\_timeout"></a>
### generic\_idle\_timeout
The time, in seconds, to wait for new packets before closing an active generic session.

*Type* : integer


<a name="generic\_initial\_timeout"></a>
### generic\_initial\_timeout
The time, in seconds, to wait for new packets before closing a generic session that has not seen traffic in both directions.

*Type* : integer


<a name="global\_network\_settings"></a>
### global\_network\_settings

|Name|Schema|
|---|---|
|**default\_connection\_state\_tracking**  <br>*optional*|[default\_connection\_state\_tracking](#default\_connection\_state\_tracking)|
|**default\_firewall\_action**  <br>*optional*|[default\_firewall\_action](#default\_firewall\_action)|
|**denied\_timeout**  <br>*optional*|[denied\_timeout](#denied\_timeout)|
|**enable\_encryption\_key\_rotation**  <br>*optional*|[enable\_encryption\_key\_rotation](#enable\_encryption\_key\_rotation)|
|**enable\_extended\_packet\_authentication\_trailer**  <br>*optional*|[enable\_extended\_packet\_authentication\_trailer](#enable\_extended\_packet\_authentication\_trailer)|
|**enable\_extended\_packet\_encryption\_header**  <br>*optional*|[enable\_extended\_packet\_encryption\_header](#enable\_extended\_packet\_encryption\_header)|
|**enable\_fips\_mode**  <br>*optional*|[enable\_fips\_mode](#enable\_fips\_mode)|
|**extended\_packet\_authentication\_trailer\_type**  <br>*optional*|[extended\_packet\_authentication\_trailer\_type](#extended\_packet\_authentication\_trailer\_type)|
|**generic\_idle\_timeout**  <br>*optional*|[generic\_idle\_timeout](#generic\_idle\_timeout)|
|**generic\_initial\_timeout**  <br>*optional*|[generic\_initial\_timeout](#generic\_initial\_timeout)|
|**global\_policy\_template**  <br>*optional*|[global\_policy\_template](#global\_policy\_template)|
|**icmp\_idle\_timeout**  <br>*optional*|[icmp\_idle\_timeout](#icmp\_idle\_timeout)|
|**icmp\_initial\_timeout**  <br>*optional*|[icmp\_initial\_timeout](#icmp\_initial\_timeout)|
|**network\_encryption\_mode**  <br>*optional*|[network\_encryption\_mode](#network\_encryption\_mode)|
|**on\_demand\_bandwidth\_limit\_percent**  <br>*optional*|[on\_demand\_bandwidth\_limit\_percent](#on\_demand\_bandwidth\_limit\_percent)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**tcp\_closed\_timeout**  <br>*optional*|[tcp\_closed\_timeout](#tcp\_closed\_timeout)|
|**tcp\_closing\_timeout**  <br>*optional*|[tcp\_closing\_timeout](#tcp\_closing\_timeout)|
|**tcp\_idle\_timeout**  <br>*optional*|[tcp\_idle\_timeout](#tcp\_idle\_timeout)|
|**tcp\_initial\_timeout**  <br>*optional*|[tcp\_initial\_timeout](#tcp\_initial\_timeout)|
|**tcp\_time\_wait\_timeout**  <br>*optional*|[tcp\_time\_wait\_timeout](#tcp\_time\_wait\_timeout)|
|**udp\_idle\_timeout**  <br>*optional*|[udp\_idle\_timeout](#udp\_idle\_timeout)|
|**udp\_initial\_timeout**  <br>*optional*|[udp\_initial\_timeout](#udp\_initial\_timeout)|


<a name="global\_network\_settings\_delete\_success\_schema"></a>
### global\_network\_settings\_delete\_success\_schema

|Name|Schema|
|---|---|
|**global\_network\_settings**  <br>*optional*|[global\_network\_settings](#global\_network\_settings\_delete\_success\_schema-global\_network\_settings)|

<a name="global\_network\_settings\_delete\_success\_schema-global\_network\_settings"></a>
**global\_network\_settings**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="global\_network\_settings\_post\_success\_schema"></a>
### global\_network\_settings\_post\_success\_schema

|Name|Schema|
|---|---|
|**global\_network\_settings**  <br>*optional*|[global\_network\_settings](#global\_network\_settings\_post\_success\_schema-global\_network\_settings)|

<a name="global\_network\_settings\_post\_success\_schema-global\_network\_settings"></a>
**global\_network\_settings**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="global\_network\_settings\_put\_success\_schema"></a>
### global\_network\_settings\_put\_success\_schema

|Name|Schema|
|---|---|
|**global\_network\_settings**  <br>*optional*|[global\_network\_settings](#global\_network\_settings\_put\_success\_schema-global\_network\_settings)|

<a name="global\_network\_settings\_put\_success\_schema-global\_network\_settings"></a>
**global\_network\_settings**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="global\_network\_settings\_request\_schema"></a>
### global\_network\_settings\_request\_schema

|Name|Schema|
|---|---|
|**global\_network\_settings**  <br>*optional*|[global\_network\_settings](#global\_network\_settings)|


<a name="global\_network\_settings\_response\_schema"></a>
### global\_network\_settings\_response\_schema
*Type* : < [global\_network\_settings\_response\_schema](#global\_network\_settings\_response\_schema-inline) > array

<a name="global\_network\_settings\_response\_schema-inline"></a>
**global\_network\_settings\_response\_schema**

|Name|Schema|
|---|---|
|**default\_connection\_state\_tracking**  <br>*optional*|[default\_connection\_state\_tracking](#default\_connection\_state\_tracking)|
|**default\_firewall\_action**  <br>*optional*|[default\_firewall\_action](#default\_firewall\_action)|
|**denied\_timeout**  <br>*optional*|[denied\_timeout](#denied\_timeout)|
|**enable\_encryption\_key\_rotation**  <br>*optional*|[enable\_encryption\_key\_rotation](#enable\_encryption\_key\_rotation)|
|**enable\_extended\_packet\_authentication\_trailer**  <br>*optional*|[enable\_extended\_packet\_authentication\_trailer](#enable\_extended\_packet\_authentication\_trailer)|
|**enable\_extended\_packet\_encryption\_header**  <br>*optional*|[enable\_extended\_packet\_encryption\_header](#enable\_extended\_packet\_encryption\_header)|
|**enable\_fips\_mode**  <br>*optional*|[enable\_fips\_mode](#enable\_fips\_mode)|
|**extended\_packet\_authentication\_trailer\_type**  <br>*optional*|[extended\_packet\_authentication\_trailer\_type](#extended\_packet\_authentication\_trailer\_type)|
|**generic\_idle\_timeout**  <br>*optional*|[generic\_idle\_timeout](#generic\_idle\_timeout)|
|**generic\_initial\_timeout**  <br>*optional*|[generic\_initial\_timeout](#generic\_initial\_timeout)|
|**global\_policy\_template**  <br>*optional*|[global\_policy\_template](#global\_policy\_template)|
|**icmp\_idle\_timeout**  <br>*optional*|[icmp\_idle\_timeout](#icmp\_idle\_timeout)|
|**icmp\_initial\_timeout**  <br>*optional*|[icmp\_initial\_timeout](#icmp\_initial\_timeout)|
|**network\_encryption\_mode**  <br>*optional*|[network\_encryption\_mode](#network\_encryption\_mode)|
|**on\_demand\_bandwidth\_limit\_percent**  <br>*optional*|[on\_demand\_bandwidth\_limit\_percent](#on\_demand\_bandwidth\_limit\_percent)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**tcp\_closed\_timeout**  <br>*optional*|[tcp\_closed\_timeout](#tcp\_closed\_timeout)|
|**tcp\_closing\_timeout**  <br>*optional*|[tcp\_closing\_timeout](#tcp\_closing\_timeout)|
|**tcp\_idle\_timeout**  <br>*optional*|[tcp\_idle\_timeout](#tcp\_idle\_timeout)|
|**tcp\_initial\_timeout**  <br>*optional*|[tcp\_initial\_timeout](#tcp\_initial\_timeout)|
|**tcp\_time\_wait\_timeout**  <br>*optional*|[tcp\_time\_wait\_timeout](#tcp\_time\_wait\_timeout)|
|**udp\_idle\_timeout**  <br>*optional*|[udp\_idle\_timeout](#udp\_idle\_timeout)|
|**udp\_initial\_timeout**  <br>*optional*|[udp\_initial\_timeout](#udp\_initial\_timeout)|


<a name="global\_policy\_template"></a>
### global\_policy\_template
A Firewall Policy template to be applied to all Appliances in the Citrix SD-WAN Network

*Type* : string


<a name="icmp\_idle\_timeout"></a>
### icmp\_idle\_timeout
The time, in seconds, to wait for new packets before closing an active ICMP session.

*Type* : integer


<a name="icmp\_initial\_timeout"></a>
### icmp\_initial\_timeout
The time, in seconds, to wait for new packets before closing an ICMP session that has not seen traffic in both directions.

*Type* : integer


<a name="network\_encryption\_mode"></a>
### network\_encryption\_mode
The encryption algorithm used for encrypted Paths

*Type* : enum (AES 128-Bit, AES 256-Bit)


<a name="on\_demand\_bandwidth\_limit\_percent"></a>
### on\_demand\_bandwidth\_limit\_percent
Default maximum total WAN-to-LAN bandwidth, as a percentage of bandwidth provided by non-standby WAN links in the Virtual Path (%).

*Type* : integer


<a name="package\_name"></a>
### package\_name
Config package name using which the API operation should be performed.

*Type* : string


<a name="tcp\_closed\_timeout"></a>
### tcp\_closed\_timeout
The time, in seconds, to wait for new packets before closing an aborted TCP session.

*Type* : integer


<a name="tcp\_closing\_timeout"></a>
### tcp\_closing\_timeout
The time, in seconds, to wait for new packets before closing a TCP session after a request to terminate.

*Type* : integer


<a name="tcp\_idle\_timeout"></a>
### tcp\_idle\_timeout
The time, in seconds, to wait for new packets before closing an active TCP session.

*Type* : integer


<a name="tcp\_initial\_timeout"></a>
### tcp\_initial\_timeout
The time, in seconds, to wait for new packets before closing a TCP session that has not completed a handshake.

*Type* : integer


<a name="tcp\_time\_wait\_timeout"></a>
### tcp\_time\_wait\_timeout
The time, in seconds, to wait for new packets before closing a terminated TCP session.

*Type* : integer


<a name="udp\_idle\_timeout"></a>
### udp\_idle\_timeout
The time, in seconds, to wait for new packets before closing an active UDP session.

*Type* : integer


<a name="udp\_initial\_timeout"></a>
### udp\_initial\_timeout
The time, in seconds, to wait for new packets before closing a UDP session that has not seen traffic in both directions.

*Type* : integer






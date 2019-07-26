# intranet\_service\_rules


<a name="overview"></a>
## Overview
API to add, modify, delete, and get Intranet Services Rules


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* intranet\_service\_rules : Operations related to intranet\_service\_rules 




<a name="paths"></a>
## Paths

<a name="intranet\_service\_rules-post"></a>
### POST operation for intranet\_service\_rules
```
POST /intranet_service_rules
```


#### Description
Use this operation to add Intranet Services Rules


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[intranet\_service\_rules\_request\_schema](#intranet\_service\_rules\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[intranet\_service\_rules\_post\_success\_schema](#intranet\_service\_rules\_post\_success\_schema)|
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

* intranet\_service\_rules


<a name="intranet\_service\_rules-get"></a>
### Get operation for intranet\_service\_rules
```
GET /intranet_service_rules
```


#### Description
Use this operation to get Intranet Services Rules


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[intranet\_service\_rules\_response\_schema](#intranet\_service\_rules\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* intranet\_service\_rules


<a name="intranet\_service\_rules-put"></a>
### PUT operation for intranet\_service\_rules
```
PUT /intranet_service_rules
```


#### Description
Use this operation to modify Intranet Services Rules


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[intranet\_service\_rules\_put\_success\_schema](#intranet\_service\_rules\_put\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* intranet\_service\_rules


<a name="intranet\_service\_rules-deletepathparam-delete"></a>
### DELETE operation for intranet\_service\_rules
```
DELETE /intranet_service_rules/{deletePathParam}
```


#### Description
Use this operation to delete Intranet Services Rules


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[intranet\_service\_rules\_delete\_success\_schema](#intranet\_service\_rules\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* intranet\_service\_rules




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="id"></a>
### id
Id of rule

*Type* : integer


<a name="intranet\_service\_name"></a>
### intranet\_service\_name
Intranet Service Name

*Type* : string


<a name="intranet\_service\_rules"></a>
### intranet\_service\_rules

|Name|Schema|
|---|---|
|**id**  <br>*optional*|[id](#id)|
|**intranet\_service\_name**  <br>*optional*|[intranet\_service\_name](#intranet\_service\_name)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**properties**  <br>*optional*|[properties](#properties)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|


<a name="intranet\_service\_rules\_delete\_success\_schema"></a>
### intranet\_service\_rules\_delete\_success\_schema

|Name|Schema|
|---|---|
|**intranet\_service\_rules**  <br>*optional*|[intranet\_service\_rules](#intranet\_service\_rules\_delete\_success\_schema-intranet\_service\_rules)|

<a name="intranet\_service\_rules\_delete\_success\_schema-intranet\_service\_rules"></a>
**intranet\_service\_rules**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="intranet\_service\_rules\_post\_success\_schema"></a>
### intranet\_service\_rules\_post\_success\_schema

|Name|Schema|
|---|---|
|**intranet\_service\_rules**  <br>*optional*|[intranet\_service\_rules](#intranet\_service\_rules\_post\_success\_schema-intranet\_service\_rules)|

<a name="intranet\_service\_rules\_post\_success\_schema-intranet\_service\_rules"></a>
**intranet\_service\_rules**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="intranet\_service\_rules\_put\_success\_schema"></a>
### intranet\_service\_rules\_put\_success\_schema

|Name|Schema|
|---|---|
|**intranet\_service\_rules**  <br>*optional*|[intranet\_service\_rules](#intranet\_service\_rules\_put\_success\_schema-intranet\_service\_rules)|

<a name="intranet\_service\_rules\_put\_success\_schema-intranet\_service\_rules"></a>
**intranet\_service\_rules**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="intranet\_service\_rules\_request\_schema"></a>
### intranet\_service\_rules\_request\_schema

|Name|Schema|
|---|---|
|**intranet\_service\_rules**  <br>*optional*|[intranet\_service\_rules](#intranet\_service\_rules)|


<a name="intranet\_service\_rules\_response\_schema"></a>
### intranet\_service\_rules\_response\_schema
*Type* : < [intranet\_service\_rules\_response\_schema](#intranet\_service\_rules\_response\_schema-inline) > array

<a name="intranet\_service\_rules\_response\_schema-inline"></a>
**intranet\_service\_rules\_response\_schema**

|Name|Schema|
|---|---|
|**id**  <br>*optional*|[id](#id)|
|**intranet\_service\_name**  <br>*optional*|[intranet\_service\_name](#intranet\_service\_name)|
|**order**  <br>*optional*|[order](#order)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**properties**  <br>*optional*|[properties](#properties)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|


<a name="order"></a>
### order
The order/precedence in which Rules are applied (automatically redistributed)

*Type* : integer


<a name="package\_name"></a>
### package\_name
Package name to add rule to

*Type* : string


<a name="properties"></a>
### properties
Intranet Service Rules Properties


|Name|Description|Schema|
|---|---|---|
|**destination\_ip\_address**  <br>*optional*|The Destination IP Address and subnet mask that this rule will match.|string|
|**destination\_port**  <br>*optional*|If set, the Destination Port or Port range (eg: 2345-2457) that this rule will match.|integer|
|**dscp**  <br>*optional*|The DSCP tag in the IP header that this rule will match.  <br>**Default** : `"any"`|enum (any, af11, af12, af13, af21, af22, af23, af31, af32, af33, af41, af42, af43, cs1, cs2, cs3, cs4, cs5, cs6, cs7, default, ef)|
|**enable\_passive\_ftp\_detection**  <br>*optional*|If enabled, this parameter will make processing decisions based upon user data.|boolean|
|**override\_service**  <br>*optional*|The destination service that flows should go to|enum (internet, passthrough, discard)|
|**protocol**  <br>*optional*|The Protocol Name that this filter will match.  <br>**Default** : `"ANY"`|enum (FTP, SMTP, POP3, IMAP, HTTP, TELNET, ICMP, HTTPS, ALTHTTP, SSH, DNS, NTP, SNMP, SNMPTRAP, RPC, RDP, IPSEC, SIP, ICACGPUDP, ICAUDP, ICACGP, ICA, IPERF, CIFS, LDAP, NETBIOS, RTP, RTCP, DHCP, NFS, GRE, TCP, UDP, Number, ANY)|
|**protocol\_num**  <br>*optional*|The Protocol Number that this filter will match.|integer|
|**rebind\_flow\_on\_change**  <br>*optional*|If enabled, flows which are otherwise identical in terms of match criteria will be treated as separate if their DSCP fields differ.|boolean|
|**rule\_group\_name**  <br>*optional*|A name given to a rule that will allow rule statistics to be summed in groups when they are displayed. All rule statistics for rules with the same Rule Group Name can be viewed together.  <br>**Default** : `"ANY"`|enum (ANY, FTP, SMTP, POP3, IMAP, HTTP, TELNET, ICMP, HTTPS, ALTHTTP, SSH, DNS, SNMP, NTP, SNMPTRAP, RDP, IPSEC, RPC, SIP, ICACGPPUDP, ICAUDP, ICACGP, ICA, IPERF, CIFS, LDAP, NETBIOS, GRE, TCP, UDP, Number, RTP, RTCP, DHCP, NFS)|
|**source\_ip\_address**  <br>*optional*|The Source IP Address and subnet mask that this rule will match.|string|
|**source\_port**  <br>*optional*|If set, the Source or Destination Port or Port range (eg: 2345-2457) that this rule will match.|integer|
|**vlan\_id**  <br>*optional*|The Ethernet VLAN tag that this rule will match.|integer|


<a name="site\_name"></a>
### site\_name
Site name to which the rule belongs

*Type* : string






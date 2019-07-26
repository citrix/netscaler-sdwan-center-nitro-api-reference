# internet\_service\_rules


<a name="overview"></a>
## Overview
API to add, modify, delete, and get Internet Services Rules


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* internet\_service\_rules : Operations related to internet\_service\_rules 




<a name="paths"></a>
## Paths

<a name="internet\_service\_rules-post"></a>
### POST operation for internet\_service\_rules
```
POST /internet_service_rules
```


#### Description
Use this operation to add Internet Services Rules


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[internet\_service\_rules\_request\_schema](#internet\_service\_rules\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[internet\_service\_rules\_post\_success\_schema](#internet\_service\_rules\_post\_success\_schema)|
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

* internet\_service\_rules


<a name="internet\_service\_rules-get"></a>
### Get operation for internet\_service\_rules
```
GET /internet_service_rules
```


#### Description
Use this operation to get Internet Services Rules


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[internet\_service\_rules\_response\_schema](#internet\_service\_rules\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* internet\_service\_rules


<a name="internet\_service\_rules-put"></a>
### PUT operation for internet\_service\_rules
```
PUT /internet_service_rules
```


#### Description
Use this operation to modify Internet Services Rules


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[internet\_service\_rules\_put\_success\_schema](#internet\_service\_rules\_put\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* internet\_service\_rules


<a name="internet\_service\_rules-deletepathparam-delete"></a>
### DELETE operation for internet\_service\_rules
```
DELETE /internet_service_rules/{deletePathParam}
```


#### Description
Use this operation to delete Internet Services Rules


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[internet\_service\_rules\_delete\_success\_schema](#internet\_service\_rules\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* internet\_service\_rules




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


<a name="internet\_service\_rules"></a>
### internet\_service\_rules

|Name|Schema|
|---|---|
|**id**  <br>*optional*|[id](#id)|
|**order**  <br>*optional*|[order](#order)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**properties**  <br>*optional*|[properties](#properties)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|


<a name="internet\_service\_rules\_delete\_success\_schema"></a>
### internet\_service\_rules\_delete\_success\_schema

|Name|Schema|
|---|---|
|**internet\_service\_rules**  <br>*optional*|[internet\_service\_rules](#internet\_service\_rules\_delete\_success\_schema-internet\_service\_rules)|

<a name="internet\_service\_rules\_delete\_success\_schema-internet\_service\_rules"></a>
**internet\_service\_rules**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="internet\_service\_rules\_post\_success\_schema"></a>
### internet\_service\_rules\_post\_success\_schema

|Name|Schema|
|---|---|
|**internet\_service\_rules**  <br>*optional*|[internet\_service\_rules](#internet\_service\_rules\_post\_success\_schema-internet\_service\_rules)|

<a name="internet\_service\_rules\_post\_success\_schema-internet\_service\_rules"></a>
**internet\_service\_rules**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="internet\_service\_rules\_put\_success\_schema"></a>
### internet\_service\_rules\_put\_success\_schema

|Name|Schema|
|---|---|
|**internet\_service\_rules**  <br>*optional*|[internet\_service\_rules](#internet\_service\_rules\_put\_success\_schema-internet\_service\_rules)|

<a name="internet\_service\_rules\_put\_success\_schema-internet\_service\_rules"></a>
**internet\_service\_rules**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="internet\_service\_rules\_request\_schema"></a>
### internet\_service\_rules\_request\_schema

|Name|Schema|
|---|---|
|**internet\_service\_rules**  <br>*optional*|[internet\_service\_rules](#internet\_service\_rules)|


<a name="internet\_service\_rules\_response\_schema"></a>
### internet\_service\_rules\_response\_schema
*Type* : < [internet\_service\_rules\_response\_schema](#internet\_service\_rules\_response\_schema-inline) > array

<a name="internet\_service\_rules\_response\_schema-inline"></a>
**internet\_service\_rules\_response\_schema**

|Name|Schema|
|---|---|
|**id**  <br>*optional*|[id](#id)|
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
Internet Service Rules Properties


|Name|Description|Schema|
|---|---|---|
|**destination\_ip\_address**  <br>*optional*|The Destination IP Address and subnet mask that this rule will match.|string|
|**destination\_port**  <br>*optional*|If set, the Destination Port or Port range (eg: 2345-2457) that this rule will match.|string|
|**dscp**  <br>*optional*|The DSCP tag in the IP header that this rule will match.  <br>**Default** : `"any"`|enum (any, af11, af12, af13, af21, af22, af23, af31, af32, af33, af41, af42, af43, cs1, cs2, cs3, cs4, cs5, cs6, cs7, default, ef)|
|**enable\_passive\_ftp\_detection**  <br>*optional*|If enabled, this parameter will make processing decisions based upon user data.|boolean|
|**mode**  <br>*optional*|The destination service that flows should go to  <br>**Default** : `"wan_link"`|enum (override\_service, wan\_link)|
|**override\_service**  <br>*optional*|The destination service that flows should go to|string|
|**protocol**  <br>*optional*|The Protocol Name that this filter will match.  <br>**Default** : `"ANY"`|enum (FTP, SMTP, POP3, IMAP, HTTP, TELNET, ICMP, HTTPS, ALTHTTP, SSH, DNS, NTP, SNMP, SNMPTRAP, RPC, RDP, IPSEC, SIP, ICACGPUDP, ICAUDP, ICACGP, ICA, IPERF, CIFS, LDAP, NETBIOS, RTP, RTCP, DHCP, NFS, GRE, TCP, UDP, Number, ANY)|
|**protocol\_num**  <br>*optional*|The Protocol Number that this filter will match.|integer|
|**rebind\_flow\_on\_change**  <br>*optional*|If enabled, flows which are otherwise identical in terms of match criteria will be treated as separate if their DSCP fields differ.|boolean|
|**routing\_domain**  <br>*optional*|Choose one of the configured Routing Domains. Leave blank or any for Any Routing Domain|string|
|**rule\_group\_name**  <br>*optional*|A name given to a rule that will allow rule statistics to be summed in groups when they are displayed. All rule statistics for rules with the same Rule Group Name can be viewed together.  <br>**Default** : `"NONE"`|enum (NONE, FTP, SMTP, POP3, IMAP, HTTP, TELNET, ICMP, HTTPS, ALTHTTP, SSH, DNS, SNMP, NTP, SNMPTRAP, RDP, IPSEC, RPC, SIP, ICACGPPUDP, ICAUDP, ICACGP, ICA, IPERF, CIFS, LDAP, NETBIOS, GRE, TCP, UDP, Number, RTP, RTCP, DHCP, NFS)|
|**source\_ip\_address**  <br>*optional*|The Source IP Address and subnet mask that this rule will match.|string|
|**source\_port**  <br>*optional*|If set, the Source or Destination Port or Port range (eg: 2345-2457) that this rule will match.|string|
|**vlan\_id**  <br>*optional*|The Ethernet VLAN tag that this rule will match.|string|
|**wan\_link**  <br>*optional*|The destination service that flows should go to|string|


<a name="site\_name"></a>
### site\_name
Site name to which the rule belongs

*Type* : string






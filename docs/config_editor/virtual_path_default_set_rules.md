# virtual\_path\_default\_set\_rules


<a name="overview"></a>
## Overview
API to modify, get Virtual Path Default Set Rules


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* virtual\_path\_default\_set\_rules : Operations related to virtual\_path\_default\_set\_rules 




<a name="paths"></a>
## Paths

<a name="virtual\_path\_default\_set\_rules-post"></a>
### POST operation for virtual\_path\_default\_set\_rules
```
POST /virtual_path_default_set_rules
```


#### Description
Use this operation to add Virtual Path Default Set Rules


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[virtual\_path\_default\_set\_rules\_request\_schema](#virtual\_path\_default\_set\_rules\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[virtual\_path\_default\_set\_rules\_post\_success\_schema](#virtual\_path\_default\_set\_rules\_post\_success\_schema)|
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

* virtual\_path\_default\_set\_rules


<a name="virtual\_path\_default\_set\_rules-get"></a>
### Get operation for virtual\_path\_default\_set\_rules
```
GET /virtual_path_default_set_rules
```


#### Description
Use this operation to get the Virtual Path Default Set Rules


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[virtual\_path\_default\_set\_rules\_response\_schema](#virtual\_path\_default\_set\_rules\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* virtual\_path\_default\_set\_rules


<a name="virtual\_path\_default\_set\_rules-put"></a>
### PUT operation for virtual\_path\_default\_set\_rules
```
PUT /virtual_path_default_set_rules
```


#### Description
Use this operation to modify Virtual Path Default Set Rules


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[virtual\_path\_default\_set\_rules\_put\_success\_schema](#virtual\_path\_default\_set\_rules\_put\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* virtual\_path\_default\_set\_rules


<a name="virtual\_path\_default\_set\_rules-deletepathparam-delete"></a>
### DELETE operation for virtual\_path\_default\_set\_rules
```
DELETE /virtual_path_default_set_rules/{deletePathParam}
```


#### Description
Use this operation to delete Virtual Path Default Set Rules


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[virtual\_path\_default\_set\_rules\_delete\_success\_schema](#virtual\_path\_default\_set\_rules\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* virtual\_path\_default\_set\_rules




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
Auto-generated ID to uniquely identify Virtual Path Default Set Rules

*Type* : integer


<a name="match\_properties"></a>
### match\_properties
Rule match properties


|Name|Description|Schema|
|---|---|---|
|**destination\_ip\_address**  <br>*optional*|The Destination IP Address and subnet mask that this rule will match. Give IP Address with subnet|string|
|**destination\_port**  <br>*optional*|If set, the Destination Port or Port range (eg: 2345-2457) that this rule will match.|string|
|**dscp**  <br>*optional*|The DSCP tag in the IP header that this rule will match.  <br>**Default** : `"any"`|enum (any, af11, af12, af13, af21, af22, af23, af31, af32, af33, af41, af42, af43, cs1, cs2, cs3, cs4, cs5, cs6, cs7, default, ef)|
|**protocol**  <br>*optional*|The Protocol Name that this filter will match.  <br>**Default** : `"ANY"`|enum (FTP, SMTP, POP3, IMAP, HTTP, TELNET, ICMP, HTTPS, ALTHTTP, SSH, DNS, NTP, SNMP, SNMPTRAP, RPC, RDP, IPSEC, SIP, ICACGPUDP, ICAUDP, ICACGP, ICA, IPERF, CIFS, LDAP, NETBIOS, RTP, RTCP, DHCP, NFS, GRE, TCP, UDP, Number, ANY)|
|**protocol\_num**  <br>*optional*|The Protocol Number that this filter will match.|integer|
|**rebind\_flow\_on\_change**  <br>*optional*|If enabled, flows which are otherwise identical in terms of match criteria will be treated as separate if their DSCP fields differ.|boolean|
|**routing\_domain**  <br>*optional*|routing domain|string|
|**source\_ip\_address**  <br>*optional*|The Source IP Address and subnet mask that this rule will match. Give IP Address with subnet|string|
|**source\_port**  <br>*optional*|If set, the Source or Destination Port or Port range (eg: 2345-2457) that this rule will match.|string|
|**vlan\_id**  <br>*optional*|The Ethernet VLAN tag that this rule will match.|integer|


<a name="order"></a>
### order
The order/precedence in which Rules are applied (automatically redistributed)

*Type* : integer


<a name="package\_name"></a>
### package\_name
Config package name using which the API operation should be performed.

*Type* : string


<a name="rule\_properties"></a>
### rule\_properties
Rule properties


|Name|Description|Schema|
|---|---|---|
|**enable\_gre**  <br>*optional*|If enabled, header compression will be used for GRE packets|boolean|
|**enable\_ip\_tcp\_udp\_compression**  <br>*optional*|If enabled, header compression will be used for IP, TCP and UDP packets|boolean|
|**enable\_packet\_aggregation**  <br>*optional*|If enabled, small packets on this flow will be aggregated together into larger packets|boolean|
|**enable\_passive\_ftp\_detection**  <br>*optional*|If enabled, processing decisions will be based upon user data. The rule will learn the port used for the FTP data transfer and apply the rule properties to the learned port|boolean|
|**enable\_tcp\_termination**  <br>*optional*|If enabled, flows matching this rule will be sent using reliable service to the remote appliance and any packets lost will be retransmitted|boolean|
|**lan\_to\_wan\_class\_id**  <br>*optional*|The Class that is to service traffic flows that match this Rule. The default is Class 9|string|
|**lan\_to\_wan\_drop\_depth**  <br>*optional*|If the queue depth exceeds this threshold, the packet will be discarded and statistics will be counted|integer|
|**lan\_to\_wan\_drop\_limit**  <br>*optional*|The maximum amount of estimated time that packets smaller than the Large Packet Size will have to wait in the class scheduler. If the estimated time exceeds this threshold, the packet will be discarded and statistics will be counted. Not valid for Bulk classes.|integer|
|**lan\_to\_wan\_duplicate\_packets\_disable\_depth**  <br>*optional*|The queue depth of the class scheduler at which point duplicate packets will not be generated|integer|
|**lan\_to\_wan\_duplicate\_packets\_disable\_limit**  <br>*optional*|The amount of time a packet may wait in the queue before duplication is not performed, which prevents duplicate packets from consuming bandwidth when bandwidth is limited|integer|
|**lan\_to\_wan\_enable\_red**  <br>*optional*|If enabled, Random Early Detection (RED) will discard packets uniformly when congestion is detected.|boolean|
|**lan\_to\_wan\_large\_packet\_size**  <br>*optional*|Packets destined for this class which are larger than or equal to this size will follow large packet drop policy. Packets which are smaller than this size will follow small packet drop policy. If this size is set to 0, all packets will be treated as small packets.|integer|
|**lan\_to\_wan\_large\_packets\_drop\_depth**  <br>*optional*|If the queue depth exceeds this threshold, the packet will be discarded and statistics will be counted.|integer|
|**lan\_to\_wan\_large\_packets\_drop\_limit**  <br>*optional*|The maximum amount of estimated time that packets larger than or equal to the Large Packet Size will have to wait in the class scheduler. If the estimated time exceeds this threshold, the packet will be discarded and statistics will be counted. Not valid for Bulk classes.|integer|
|**lan\_to\_wan\_reassign\_class\_id**  <br>*optional*|The Class to which flows will be reassigned if the size specified is exceeded. If the default option is selected, packets will not be assigned to an alternate class based on packet size, and will continue to be mapped to the class specified in the General section.|string|
|**lan\_to\_wan\_reassign\_drop\_depth**  <br>*optional*|If the queue depth exceeds this threshold, the packet will be discarded and statistics will be counted|integer|
|**lan\_to\_wan\_reassign\_drop\_limit**  <br>*optional*|If the estimated time exceeds this threshold, the packet will be discarded and statistics will be counted. Not valid for Bulk classes.|integer|
|**lan\_to\_wan\_reassign\_duplicate\_packets\_disable\_depth**  <br>*optional*|The queue depth of the class scheduler at which point duplicate packets will not be generated.|integer|
|**lan\_to\_wan\_reassign\_duplicate\_packets\_disable\_limit**  <br>*optional*|Designates the amount of time a packet may wait in the queue before duplication is not performed, which prevents duplicate packets from consuming bandwidth when bandwidth is limited.|integer|
|**lan\_to\_wan\_reassign\_enable\_red**  <br>*optional*|If enabled, Random Early Detection (RED) will discard packets uniformly when congestion is detected.|boolean|
|**lan\_to\_wan\_reassign\_large\_packet\_size**  <br>*optional*|Packets destined for this class which are larger than or equal to this size will follow large packet drop policy. Packets which are smaller than this size will follow small packet drop policy. If this size is set to 0, all packets will be treated as small packets.|integer|
|**lan\_to\_wan\_reassign\_large\_packets\_drop\_depth**  <br>*optional*|If the queue depth exceeds this threshold, the packet will be discarded and statistics will be counted.|integer|
|**lan\_to\_wan\_reassign\_large\_packets\_drop\_limit**  <br>*optional*|If the estimated time exceeds this threshold, the packet will be discarded and statistics will be counted. Not valid for Bulk classes.|integer|
|**lan\_to\_wan\_reassign\_size**  <br>*optional*|After a flow is established, if a packet that exceeds this size is detected on the LAN to WAN, then the flow will be moved to the class indicated|integer|
|**lan\_to\_wan\_tcp\_standalone\_ack\_class\_id**  <br>*optional*|The Class that will be used for standalone TCP ACKs. This has no effect on packets that are piggyback ACKs with payload. If the default option is selected, TCP Standalone ACKs will continue to be mapped to the class specified in the General section.|string|
|**lan\_to\_wan\_tcp\_standalone\_ack\_drop\_depth**  <br>*optional*|If the queue depth exceeds this threshold, the packet will be discarded and statistics will be counted|integer|
|**lan\_to\_wan\_tcp\_standalone\_ack\_drop\_limit**  <br>*optional*|If the estimated time exceeds this threshold, the packet will be discarded and statistics will be counted. Not valid for Bulk classes.|integer|
|**lan\_to\_wan\_tcp\_standalone\_ack\_large\_packet\_size**  <br>*optional*|Packets destined for this class which are larger than or equal to this size will follow large packet drop policy. Packets which are smaller than this size will follow small packet drop policy. If this size is set to 0, all packets will be treated as small packets.|integer|
|**lan\_to\_wan\_tcp\_standalone\_ack\_large\_packets\_drop\_depth**  <br>*optional*|If the queue depth exceeds this threshold, the packet will be discarded and statistics will be counted|integer|
|**lan\_to\_wan\_tcp\_standalone\_ack\_large\_packets\_drop\_limit**  <br>*optional*|If the estimated time exceeds this threshold, the packet will be discarded and statistics will be counted. Not valid for Bulk classes.|integer|
|**override\_service**  <br>*optional*|The destination service that flows should go to|boolean|
|**persistent\_impedance**  <br>*optional*|Use the same path until wait time on the path is longer than the configured value|integer|
|**retransmit\_lost\_packets**  <br>*optional*|If enabled, flows matching this rule will be sent using reliable service to the remote appliance and any packets lost will be retransmitted|boolean|
|**rule\_group\_name**  <br>*optional*|A name given to a rule that will allow rule statistics to be summed in groups when they are displayed. All rule statistics for rules with the same Rule Group Name can be viewed together.|string|
|**track\_performance**  <br>*optional*|If enabled, performance of a rule over time will be recorded in a session DB, including loss, latency, jitter and bandwidth used.|boolean|
|**transmit\_mode**  <br>*optional*|The method of transmitting and receiving packets|enum (load\_balance\_paths, persistent\_paths, duplicate\_paths, override\_service)|
|**wan\_to\_lan\_discard\_late\_resequence\_packets**  <br>*optional*|After a packets sequence timer has expired for a dependent packet, and the packets were permitted to the LAN: If a late packet arrives at WAN to LAN, this property defines what is to be done with it. Enable this checkbox to discard, disable this checkbox to forward.|boolean|
|**wan\_to\_lan\_dscp\_tag**  <br>*optional*|The DSCP tag that will be applied to packets that match this rule on WAN to LAN, before they are sent to the LAN  <br>**Default** : `"any"`|enum (any, af11, af12, af13, af21, af22, af23, af31, af32, af33, af41, af42, af43, cs1, cs2, cs3, cs4, cs5, cs6, cs7, default, ef)|
|**wan\_to\_lan\_enable\_packet\_resequencing**  <br>*optional*|If enabled, traffic flows that match this rule should be tagged for sequence order, and the packets should be reordered (if necessary) at the WAN to LAN appliance.|boolean|
|**wan\_to\_lan\_hold\_time**  <br>*optional*|The maximum delay that a packet may be held awaiting re-sequence. When the timer expires the packet will be sent to the LAN without waiting any further for the pre-requisite sequence numbers. <br /><u>DEFAULTS</u>: If this rule has a transmit mode of duplicate paths, the default hold time is 80ms. Otherwise, the default is 900ms for TCP rules and 250ms for NON TCP rules.|integer|


<a name="virtual\_path\_default\_set\_name"></a>
### virtual\_path\_default\_set\_name
Virtual path Default Set name using which the API operation should be performed.

*Type* : string


<a name="virtual\_path\_default\_set\_rules"></a>
### virtual\_path\_default\_set\_rules

|Name|Schema|
|---|---|
|**id**  <br>*optional*|[id](#id)|
|**match\_properties**  <br>*optional*|[match\_properties](#match\_properties)|
|**order**  <br>*optional*|[order](#order)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**rule\_properties**  <br>*optional*|[rule\_properties](#rule\_properties)|
|**virtual\_path\_default\_set\_name**  <br>*optional*|[virtual\_path\_default\_set\_name](#virtual\_path\_default\_set\_name)|


<a name="virtual\_path\_default\_set\_rules\_delete\_success\_schema"></a>
### virtual\_path\_default\_set\_rules\_delete\_success\_schema

|Name|Schema|
|---|---|
|**virtual\_path\_default\_set\_rules**  <br>*optional*|[virtual\_path\_default\_set\_rules](#virtual\_path\_default\_set\_rules\_delete\_success\_schema-virtual\_path\_default\_set\_rules)|

<a name="virtual\_path\_default\_set\_rules\_delete\_success\_schema-virtual\_path\_default\_set\_rules"></a>
**virtual\_path\_default\_set\_rules**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="virtual\_path\_default\_set\_rules\_post\_success\_schema"></a>
### virtual\_path\_default\_set\_rules\_post\_success\_schema

|Name|Schema|
|---|---|
|**virtual\_path\_default\_set\_rules**  <br>*optional*|[virtual\_path\_default\_set\_rules](#virtual\_path\_default\_set\_rules\_post\_success\_schema-virtual\_path\_default\_set\_rules)|

<a name="virtual\_path\_default\_set\_rules\_post\_success\_schema-virtual\_path\_default\_set\_rules"></a>
**virtual\_path\_default\_set\_rules**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="virtual\_path\_default\_set\_rules\_put\_success\_schema"></a>
### virtual\_path\_default\_set\_rules\_put\_success\_schema

|Name|Schema|
|---|---|
|**virtual\_path\_default\_set\_rules**  <br>*optional*|[virtual\_path\_default\_set\_rules](#virtual\_path\_default\_set\_rules\_put\_success\_schema-virtual\_path\_default\_set\_rules)|

<a name="virtual\_path\_default\_set\_rules\_put\_success\_schema-virtual\_path\_default\_set\_rules"></a>
**virtual\_path\_default\_set\_rules**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="virtual\_path\_default\_set\_rules\_request\_schema"></a>
### virtual\_path\_default\_set\_rules\_request\_schema

|Name|Schema|
|---|---|
|**virtual\_path\_default\_set\_rules**  <br>*optional*|[virtual\_path\_default\_set\_rules](#virtual\_path\_default\_set\_rules)|


<a name="virtual\_path\_default\_set\_rules\_response\_schema"></a>
### virtual\_path\_default\_set\_rules\_response\_schema
*Type* : < [virtual\_path\_default\_set\_rules\_response\_schema](#virtual\_path\_default\_set\_rules\_response\_schema-inline) > array

<a name="virtual\_path\_default\_set\_rules\_response\_schema-inline"></a>
**virtual\_path\_default\_set\_rules\_response\_schema**

|Name|Schema|
|---|---|
|**id**  <br>*optional*|[id](#id)|
|**match\_properties**  <br>*optional*|[match\_properties](#match\_properties)|
|**order**  <br>*optional*|[order](#order)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**rule\_properties**  <br>*optional*|[rule\_properties](#rule\_properties)|
|**virtual\_path\_default\_set\_name**  <br>*optional*|[virtual\_path\_default\_set\_name](#virtual\_path\_default\_set\_name)|






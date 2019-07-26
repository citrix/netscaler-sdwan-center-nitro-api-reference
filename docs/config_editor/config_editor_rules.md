# config\_editor\_rules


<a name="overview"></a>
## Overview
API to add, modify, delete, and get configuration for Rules


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* config\_editor\_rules : Operations related to config\_editor\_rules 




<a name="paths"></a>
## Paths

<a name="config\_editor\_rules-post"></a>
### POST operation for config\_editor\_rules
```
POST /config_editor_rules
```


#### Description
Use this operation to add the Rules


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[config\_editor\_rules\_request\_schema](#config\_editor\_rules\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[config\_editor\_rules\_post\_success\_schema](#config\_editor\_rules\_post\_success\_schema)|
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

* config\_editor\_rules


<a name="config\_editor\_rules-get"></a>
### Get operation for config\_editor\_rules
```
GET /config_editor_rules
```


#### Description
Use this operation to get the Rules


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[config\_editor\_rules\_response\_schema](#config\_editor\_rules\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* config\_editor\_rules


<a name="config\_editor\_rules-put"></a>
### PUT operation for config\_editor\_rules
```
PUT /config_editor_rules
```


#### Description
Use this operation to modify the Rules


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[config\_editor\_rules\_put\_success\_schema](#config\_editor\_rules\_put\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* config\_editor\_rules


<a name="config\_editor\_rules-deletepathparam-delete"></a>
### DELETE operation for config\_editor\_rules
```
DELETE /config_editor_rules/{deletePathParam}
```


#### Description
Use this operation to delete the Rules


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[config\_editor\_rules\_delete\_success\_schema](#config\_editor\_rules\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* config\_editor\_rules




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="config\_editor\_rules"></a>
### config\_editor\_rules

|Name|Schema|
|---|---|
|**deep\_packet\_inspection\_enable\_passive\_ftp\_detection**  <br>*optional*|[deep\_packet\_inspection\_enable\_passive\_ftp\_detection](#deep\_packet\_inspection\_enable\_passive\_ftp\_detection)|
|**id**  <br>*optional*|[id](#id)|
|**lan\_to\_wan\_drop\_general\_large\_packets\_drop\_depth**  <br>*optional*|[lan\_to\_wan\_drop\_general\_large\_packets\_drop\_depth](#lan\_to\_wan\_drop\_general\_large\_packets\_drop\_depth)|
|**lan\_to\_wan\_drop\_reassign\_large\_packets\_drop\_depth**  <br>*optional*|[lan\_to\_wan\_drop\_reassign\_large\_packets\_drop\_depth](#lan\_to\_wan\_drop\_reassign\_large\_packets\_drop\_depth)|
|**lan\_to\_wan\_drop\_tcp\_standalone\_ack\_large\_packets\_drop\_depth**  <br>*optional*|[lan\_to\_wan\_drop\_tcp\_standalone\_ack\_large\_packets\_drop\_depth](#lan\_to\_wan\_drop\_tcp\_standalone\_ack\_large\_packets\_drop\_depth)|
|**lan\_to\_wan\_general\_class**  <br>*optional*|[lan\_to\_wan\_general\_class](#lan\_to\_wan\_general\_class)|
|**lan\_to\_wan\_general\_drop\_depth**  <br>*optional*|[lan\_to\_wan\_general\_drop\_depth](#lan\_to\_wan\_general\_drop\_depth)|
|**lan\_to\_wan\_general\_drop\_limit**  <br>*optional*|[lan\_to\_wan\_general\_drop\_limit](#lan\_to\_wan\_general\_drop\_limit)|
|**lan\_to\_wan\_general\_duplicate\_packets\_disable\_depth**  <br>*optional*|[lan\_to\_wan\_general\_duplicate\_packets\_disable\_depth](#lan\_to\_wan\_general\_duplicate\_packets\_disable\_depth)|
|**lan\_to\_wan\_general\_duplicate\_packets\_disable\_limit**  <br>*optional*|[lan\_to\_wan\_general\_duplicate\_packets\_disable\_limit](#lan\_to\_wan\_general\_duplicate\_packets\_disable\_limit)|
|**lan\_to\_wan\_general\_enable\_red**  <br>*optional*|[lan\_to\_wan\_general\_enable\_red](#lan\_to\_wan\_general\_enable\_red)|
|**lan\_to\_wan\_general\_large\_packet\_size\_bytes**  <br>*optional*|[lan\_to\_wan\_general\_large\_packet\_size\_bytes](#lan\_to\_wan\_general\_large\_packet\_size\_bytes)|
|**lan\_to\_wan\_general\_large\_packets\_drop\_limit**  <br>*optional*|[lan\_to\_wan\_general\_large\_packets\_drop\_limit](#lan\_to\_wan\_general\_large\_packets\_drop\_limit)|
|**lan\_to\_wan\_reassign\_class**  <br>*optional*|[lan\_to\_wan\_reassign\_class](#lan\_to\_wan\_reassign\_class)|
|**lan\_to\_wan\_reassign\_drop\_depth**  <br>*optional*|[lan\_to\_wan\_reassign\_drop\_depth](#lan\_to\_wan\_reassign\_drop\_depth)|
|**lan\_to\_wan\_reassign\_drop\_limit**  <br>*optional*|[lan\_to\_wan\_reassign\_drop\_limit](#lan\_to\_wan\_reassign\_drop\_limit)|
|**lan\_to\_wan\_reassign\_duplicate\_packets\_disable\_depth**  <br>*optional*|[lan\_to\_wan\_reassign\_duplicate\_packets\_disable\_depth](#lan\_to\_wan\_reassign\_duplicate\_packets\_disable\_depth)|
|**lan\_to\_wan\_reassign\_duplicate\_packets\_disable\_limit**  <br>*optional*|[lan\_to\_wan\_reassign\_duplicate\_packets\_disable\_limit](#lan\_to\_wan\_reassign\_duplicate\_packets\_disable\_limit)|
|**lan\_to\_wan\_reassign\_enable\_red**  <br>*optional*|[lan\_to\_wan\_reassign\_enable\_red](#lan\_to\_wan\_reassign\_enable\_red)|
|**lan\_to\_wan\_reassign\_large\_packet\_size\_bytes**  <br>*optional*|[lan\_to\_wan\_reassign\_large\_packet\_size\_bytes](#lan\_to\_wan\_reassign\_large\_packet\_size\_bytes)|
|**lan\_to\_wan\_reassign\_large\_packets\_drop\_limit**  <br>*optional*|[lan\_to\_wan\_reassign\_large\_packets\_drop\_limit](#lan\_to\_wan\_reassign\_large\_packets\_drop\_limit)|
|**lan\_to\_wan\_reassign\_size**  <br>*optional*|[lan\_to\_wan\_reassign\_size](#lan\_to\_wan\_reassign\_size)|
|**lan\_to\_wan\_tcp\_standalone\_ack\_class**  <br>*optional*|[lan\_to\_wan\_tcp\_standalone\_ack\_class](#lan\_to\_wan\_tcp\_standalone\_ack\_class)|
|**lan\_to\_wan\_tcp\_standalone\_ack\_drop\_depth**  <br>*optional*|[lan\_to\_wan\_tcp\_standalone\_ack\_drop\_depth](#lan\_to\_wan\_tcp\_standalone\_ack\_drop\_depth)|
|**lan\_to\_wan\_tcp\_standalone\_ack\_drop\_limit**  <br>*optional*|[lan\_to\_wan\_tcp\_standalone\_ack\_drop\_limit](#lan\_to\_wan\_tcp\_standalone\_ack\_drop\_limit)|
|**lan\_to\_wan\_tcp\_standalone\_ack\_enable\_red**  <br>*optional*|[lan\_to\_wan\_tcp\_standalone\_ack\_enable\_red](#lan\_to\_wan\_tcp\_standalone\_ack\_enable\_red)|
|**lan\_to\_wan\_tcp\_standalone\_ack\_large\_packet\_size\_bytes**  <br>*optional*|[lan\_to\_wan\_tcp\_standalone\_ack\_large\_packet\_size\_bytes](#lan\_to\_wan\_tcp\_standalone\_ack\_large\_packet\_size\_bytes)|
|**lan\_to\_wan\_tcp\_standalone\_ack\_large\_packets\_drop\_limit**  <br>*optional*|[lan\_to\_wan\_tcp\_standalone\_ack\_large\_packets\_drop\_limit](#lan\_to\_wan\_tcp\_standalone\_ack\_large\_packets\_drop\_limit)|
|**match\_properties**  <br>*optional*|[match\_properties](#match\_properties)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**priority**  <br>*optional*|[priority](#priority)|
|**rule\_group\_name**  <br>*optional*|[rule\_group\_name](#rule\_group\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**virtual\_path\_name**  <br>*optional*|[virtual\_path\_name](#virtual\_path\_name)|
|**wan\_enable\_header\_compression\_gre**  <br>*optional*|[wan\_enable\_header\_compression\_gre](#wan\_enable\_header\_compression\_gre)|
|**wan\_enable\_header\_compression\_ip\_tcp\_udp**  <br>*optional*|[wan\_enable\_header\_compression\_ip\_tcp\_udp](#wan\_enable\_header\_compression\_ip\_tcp\_udp)|
|**wan\_enable\_packet\_aggregation**  <br>*optional*|[wan\_enable\_packet\_aggregation](#wan\_enable\_packet\_aggregation)|
|**wan\_enable\_tcp\_termination**  <br>*optional*|[wan\_enable\_tcp\_termination](#wan\_enable\_tcp\_termination)|
|**wan\_override\_service**  <br>*optional*|[wan\_override\_service](#wan\_override\_service)|
|**wan\_persistent\_impedance**  <br>*optional*|[wan\_persistent\_impedance](#wan\_persistent\_impedance)|
|**wan\_preferred\_wan\_link**  <br>*optional*|[wan\_preferred\_wan\_link](#wan\_preferred\_wan\_link)|
|**wan\_retransmit\_lost\_packets**  <br>*optional*|[wan\_retransmit\_lost\_packets](#wan\_retransmit\_lost\_packets)|
|**wan\_to\_lan\_discard\_late\_resequenced\_packets**  <br>*optional*|[wan\_to\_lan\_discard\_late\_resequenced\_packets](#wan\_to\_lan\_discard\_late\_resequenced\_packets)|
|**wan\_to\_lan\_dscp\_tag**  <br>*optional*|[wan\_to\_lan\_dscp\_tag](#wan\_to\_lan\_dscp\_tag)|
|**wan\_to\_lan\_enable\_packet\_resequencing**  <br>*optional*|[wan\_to\_lan\_enable\_packet\_resequencing](#wan\_to\_lan\_enable\_packet\_resequencing)|
|**wan\_to\_lan\_resequence\_hold\_time**  <br>*optional*|[wan\_to\_lan\_resequence\_hold\_time](#wan\_to\_lan\_resequence\_hold\_time)|
|**wan\_track\_performance**  <br>*optional*|[wan\_track\_performance](#wan\_track\_performance)|
|**wan\_transmit\_mode**  <br>*optional*|[wan\_transmit\_mode](#wan\_transmit\_mode)|


<a name="config\_editor\_rules\_delete\_success\_schema"></a>
### config\_editor\_rules\_delete\_success\_schema

|Name|Schema|
|---|---|
|**config\_editor\_rules**  <br>*optional*|[config\_editor\_rules](#config\_editor\_rules\_delete\_success\_schema-config\_editor\_rules)|

<a name="config\_editor\_rules\_delete\_success\_schema-config\_editor\_rules"></a>
**config\_editor\_rules**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="config\_editor\_rules\_post\_success\_schema"></a>
### config\_editor\_rules\_post\_success\_schema

|Name|Schema|
|---|---|
|**config\_editor\_rules**  <br>*optional*|[config\_editor\_rules](#config\_editor\_rules\_post\_success\_schema-config\_editor\_rules)|

<a name="config\_editor\_rules\_post\_success\_schema-config\_editor\_rules"></a>
**config\_editor\_rules**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="config\_editor\_rules\_put\_success\_schema"></a>
### config\_editor\_rules\_put\_success\_schema

|Name|Schema|
|---|---|
|**config\_editor\_rules**  <br>*optional*|[config\_editor\_rules](#config\_editor\_rules\_put\_success\_schema-config\_editor\_rules)|

<a name="config\_editor\_rules\_put\_success\_schema-config\_editor\_rules"></a>
**config\_editor\_rules**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="config\_editor\_rules\_request\_schema"></a>
### config\_editor\_rules\_request\_schema

|Name|Schema|
|---|---|
|**config\_editor\_rules**  <br>*optional*|[config\_editor\_rules](#config\_editor\_rules)|


<a name="config\_editor\_rules\_response\_schema"></a>
### config\_editor\_rules\_response\_schema
*Type* : < [config\_editor\_rules\_response\_schema](#config\_editor\_rules\_response\_schema-inline) > array

<a name="config\_editor\_rules\_response\_schema-inline"></a>
**config\_editor\_rules\_response\_schema**

|Name|Schema|
|---|---|
|**deep\_packet\_inspection\_enable\_passive\_ftp\_detection**  <br>*optional*|[deep\_packet\_inspection\_enable\_passive\_ftp\_detection](#deep\_packet\_inspection\_enable\_passive\_ftp\_detection)|
|**id**  <br>*optional*|[id](#id)|
|**lan\_to\_wan\_drop\_general\_large\_packets\_drop\_depth**  <br>*optional*|[lan\_to\_wan\_drop\_general\_large\_packets\_drop\_depth](#lan\_to\_wan\_drop\_general\_large\_packets\_drop\_depth)|
|**lan\_to\_wan\_drop\_reassign\_large\_packets\_drop\_depth**  <br>*optional*|[lan\_to\_wan\_drop\_reassign\_large\_packets\_drop\_depth](#lan\_to\_wan\_drop\_reassign\_large\_packets\_drop\_depth)|
|**lan\_to\_wan\_drop\_tcp\_standalone\_ack\_large\_packets\_drop\_depth**  <br>*optional*|[lan\_to\_wan\_drop\_tcp\_standalone\_ack\_large\_packets\_drop\_depth](#lan\_to\_wan\_drop\_tcp\_standalone\_ack\_large\_packets\_drop\_depth)|
|**lan\_to\_wan\_general\_class**  <br>*optional*|[lan\_to\_wan\_general\_class](#lan\_to\_wan\_general\_class)|
|**lan\_to\_wan\_general\_drop\_depth**  <br>*optional*|[lan\_to\_wan\_general\_drop\_depth](#lan\_to\_wan\_general\_drop\_depth)|
|**lan\_to\_wan\_general\_drop\_limit**  <br>*optional*|[lan\_to\_wan\_general\_drop\_limit](#lan\_to\_wan\_general\_drop\_limit)|
|**lan\_to\_wan\_general\_duplicate\_packets\_disable\_depth**  <br>*optional*|[lan\_to\_wan\_general\_duplicate\_packets\_disable\_depth](#lan\_to\_wan\_general\_duplicate\_packets\_disable\_depth)|
|**lan\_to\_wan\_general\_duplicate\_packets\_disable\_limit**  <br>*optional*|[lan\_to\_wan\_general\_duplicate\_packets\_disable\_limit](#lan\_to\_wan\_general\_duplicate\_packets\_disable\_limit)|
|**lan\_to\_wan\_general\_enable\_red**  <br>*optional*|[lan\_to\_wan\_general\_enable\_red](#lan\_to\_wan\_general\_enable\_red)|
|**lan\_to\_wan\_general\_large\_packet\_size\_bytes**  <br>*optional*|[lan\_to\_wan\_general\_large\_packet\_size\_bytes](#lan\_to\_wan\_general\_large\_packet\_size\_bytes)|
|**lan\_to\_wan\_general\_large\_packets\_drop\_limit**  <br>*optional*|[lan\_to\_wan\_general\_large\_packets\_drop\_limit](#lan\_to\_wan\_general\_large\_packets\_drop\_limit)|
|**lan\_to\_wan\_reassign\_class**  <br>*optional*|[lan\_to\_wan\_reassign\_class](#lan\_to\_wan\_reassign\_class)|
|**lan\_to\_wan\_reassign\_drop\_depth**  <br>*optional*|[lan\_to\_wan\_reassign\_drop\_depth](#lan\_to\_wan\_reassign\_drop\_depth)|
|**lan\_to\_wan\_reassign\_drop\_limit**  <br>*optional*|[lan\_to\_wan\_reassign\_drop\_limit](#lan\_to\_wan\_reassign\_drop\_limit)|
|**lan\_to\_wan\_reassign\_duplicate\_packets\_disable\_depth**  <br>*optional*|[lan\_to\_wan\_reassign\_duplicate\_packets\_disable\_depth](#lan\_to\_wan\_reassign\_duplicate\_packets\_disable\_depth)|
|**lan\_to\_wan\_reassign\_duplicate\_packets\_disable\_limit**  <br>*optional*|[lan\_to\_wan\_reassign\_duplicate\_packets\_disable\_limit](#lan\_to\_wan\_reassign\_duplicate\_packets\_disable\_limit)|
|**lan\_to\_wan\_reassign\_enable\_red**  <br>*optional*|[lan\_to\_wan\_reassign\_enable\_red](#lan\_to\_wan\_reassign\_enable\_red)|
|**lan\_to\_wan\_reassign\_large\_packet\_size\_bytes**  <br>*optional*|[lan\_to\_wan\_reassign\_large\_packet\_size\_bytes](#lan\_to\_wan\_reassign\_large\_packet\_size\_bytes)|
|**lan\_to\_wan\_reassign\_large\_packets\_drop\_limit**  <br>*optional*|[lan\_to\_wan\_reassign\_large\_packets\_drop\_limit](#lan\_to\_wan\_reassign\_large\_packets\_drop\_limit)|
|**lan\_to\_wan\_reassign\_size**  <br>*optional*|[lan\_to\_wan\_reassign\_size](#lan\_to\_wan\_reassign\_size)|
|**lan\_to\_wan\_tcp\_standalone\_ack\_class**  <br>*optional*|[lan\_to\_wan\_tcp\_standalone\_ack\_class](#lan\_to\_wan\_tcp\_standalone\_ack\_class)|
|**lan\_to\_wan\_tcp\_standalone\_ack\_drop\_depth**  <br>*optional*|[lan\_to\_wan\_tcp\_standalone\_ack\_drop\_depth](#lan\_to\_wan\_tcp\_standalone\_ack\_drop\_depth)|
|**lan\_to\_wan\_tcp\_standalone\_ack\_drop\_limit**  <br>*optional*|[lan\_to\_wan\_tcp\_standalone\_ack\_drop\_limit](#lan\_to\_wan\_tcp\_standalone\_ack\_drop\_limit)|
|**lan\_to\_wan\_tcp\_standalone\_ack\_enable\_red**  <br>*optional*|[lan\_to\_wan\_tcp\_standalone\_ack\_enable\_red](#lan\_to\_wan\_tcp\_standalone\_ack\_enable\_red)|
|**lan\_to\_wan\_tcp\_standalone\_ack\_large\_packet\_size\_bytes**  <br>*optional*|[lan\_to\_wan\_tcp\_standalone\_ack\_large\_packet\_size\_bytes](#lan\_to\_wan\_tcp\_standalone\_ack\_large\_packet\_size\_bytes)|
|**lan\_to\_wan\_tcp\_standalone\_ack\_large\_packets\_drop\_limit**  <br>*optional*|[lan\_to\_wan\_tcp\_standalone\_ack\_large\_packets\_drop\_limit](#lan\_to\_wan\_tcp\_standalone\_ack\_large\_packets\_drop\_limit)|
|**match\_properties**  <br>*optional*|[match\_properties](#match\_properties)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**priority**  <br>*optional*|[priority](#priority)|
|**rule\_group\_name**  <br>*optional*|[rule\_group\_name](#rule\_group\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**virtual\_path\_name**  <br>*optional*|[virtual\_path\_name](#virtual\_path\_name)|
|**wan\_enable\_header\_compression\_gre**  <br>*optional*|[wan\_enable\_header\_compression\_gre](#wan\_enable\_header\_compression\_gre)|
|**wan\_enable\_header\_compression\_ip\_tcp\_udp**  <br>*optional*|[wan\_enable\_header\_compression\_ip\_tcp\_udp](#wan\_enable\_header\_compression\_ip\_tcp\_udp)|
|**wan\_enable\_packet\_aggregation**  <br>*optional*|[wan\_enable\_packet\_aggregation](#wan\_enable\_packet\_aggregation)|
|**wan\_enable\_tcp\_termination**  <br>*optional*|[wan\_enable\_tcp\_termination](#wan\_enable\_tcp\_termination)|
|**wan\_override\_service**  <br>*optional*|[wan\_override\_service](#wan\_override\_service)|
|**wan\_persistent\_impedance**  <br>*optional*|[wan\_persistent\_impedance](#wan\_persistent\_impedance)|
|**wan\_preferred\_wan\_link**  <br>*optional*|[wan\_preferred\_wan\_link](#wan\_preferred\_wan\_link)|
|**wan\_retransmit\_lost\_packets**  <br>*optional*|[wan\_retransmit\_lost\_packets](#wan\_retransmit\_lost\_packets)|
|**wan\_to\_lan\_discard\_late\_resequenced\_packets**  <br>*optional*|[wan\_to\_lan\_discard\_late\_resequenced\_packets](#wan\_to\_lan\_discard\_late\_resequenced\_packets)|
|**wan\_to\_lan\_dscp\_tag**  <br>*optional*|[wan\_to\_lan\_dscp\_tag](#wan\_to\_lan\_dscp\_tag)|
|**wan\_to\_lan\_enable\_packet\_resequencing**  <br>*optional*|[wan\_to\_lan\_enable\_packet\_resequencing](#wan\_to\_lan\_enable\_packet\_resequencing)|
|**wan\_to\_lan\_resequence\_hold\_time**  <br>*optional*|[wan\_to\_lan\_resequence\_hold\_time](#wan\_to\_lan\_resequence\_hold\_time)|
|**wan\_track\_performance**  <br>*optional*|[wan\_track\_performance](#wan\_track\_performance)|
|**wan\_transmit\_mode**  <br>*optional*|[wan\_transmit\_mode](#wan\_transmit\_mode)|


<a name="deep\_packet\_inspection\_enable\_passive\_ftp\_detection"></a>
### deep\_packet\_inspection\_enable\_passive\_ftp\_detection
If enabled, processing decisions will be based upon user data. The rule will learn the port used for the FTP data transfer and apply the rule properties to the learned port

*Type* : boolean


<a name="id"></a>
### id
Id of rule

*Type* : integer


<a name="lan\_to\_wan\_drop\_general\_large\_packets\_drop\_depth"></a>
### lan\_to\_wan\_drop\_general\_large\_packets\_drop\_depth
If the queue depth exceeds this threshold, the packet will be discarded and statistics will be counted.

*Type* : integer


<a name="lan\_to\_wan\_drop\_reassign\_large\_packets\_drop\_depth"></a>
### lan\_to\_wan\_drop\_reassign\_large\_packets\_drop\_depth
If the queue depth exceeds this threshold, the packet will be discarded and statistics will be counted.

*Type* : integer


<a name="lan\_to\_wan\_drop\_tcp\_standalone\_ack\_large\_packets\_drop\_depth"></a>
### lan\_to\_wan\_drop\_tcp\_standalone\_ack\_large\_packets\_drop\_depth
If the queue depth exceeds this threshold, the packet will be discarded and statistics will be counted.

*Type* : integer


<a name="lan\_to\_wan\_general\_class"></a>
### lan\_to\_wan\_general\_class
The Class that is to service traffic flows that match this application. The default is Class 9

*Type* : integer


<a name="lan\_to\_wan\_general\_drop\_depth"></a>
### lan\_to\_wan\_general\_drop\_depth
If the queue depth exceeds this threshold, the packet will be discarded and statistics will be counted (value is in bytes)

*Type* : integer


<a name="lan\_to\_wan\_general\_drop\_limit"></a>
### lan\_to\_wan\_general\_drop\_limit
The maximum amount of estimated time that packets will have to wait in the class scheduler. If the estimated time exceeds this threshold, the packet will be discarded and statistics will be counted. Not valid for Bulk classes (Value is in ms)

*Type* : integer


<a name="lan\_to\_wan\_general\_duplicate\_packets\_disable\_depth"></a>
### lan\_to\_wan\_general\_duplicate\_packets\_disable\_depth
The queue depth of the class scheduler at which point duplicate packets will not be generated (value is in bytes)

*Type* : integer


<a name="lan\_to\_wan\_general\_duplicate\_packets\_disable\_limit"></a>
### lan\_to\_wan\_general\_duplicate\_packets\_disable\_limit
The amount of time a packet may wait in the queue before duplication is not performed, which prevents duplicate packets from consuming bandwidth when bandwidth is limited (value is in ms)

*Type* : integer


<a name="lan\_to\_wan\_general\_enable\_red"></a>
### lan\_to\_wan\_general\_enable\_red
If enabled, Random Early Detection (RED) will discard packets uniformly when congestion is detected.

*Type* : boolean


<a name="lan\_to\_wan\_general\_large\_packet\_size\_bytes"></a>
### lan\_to\_wan\_general\_large\_packet\_size\_bytes
Packets destined for this class which are larger than or equal to this size will follow large packet drop policy. Packets which are smaller than this size will follow small packet drop policy. If this size is set to 0, all packets will be treated as small packets.

*Type* : integer


<a name="lan\_to\_wan\_general\_large\_packets\_drop\_limit"></a>
### lan\_to\_wan\_general\_large\_packets\_drop\_limit
The maximum amount of estimated time that packets larger than or equal to the Large Packet Size will have to wait in the class scheduler. If the estimated time exceeds this threshold, the packet will be discarded and statistics will be counted. Not valid for Bulk classes.

*Type* : integer


<a name="lan\_to\_wan\_reassign\_class"></a>
### lan\_to\_wan\_reassign\_class
The Class to which flows will be reassigned if the size specified is exceeded. If the default option is selected, packets will not be assigned to an alternate class based on packet size, and will continue to be mapped to the class specified in the General section.

*Type* : integer


<a name="lan\_to\_wan\_reassign\_drop\_depth"></a>
### lan\_to\_wan\_reassign\_drop\_depth
If the queue depth exceeds this threshold, the packet will be discarded and statistics will be counted

*Type* : integer


<a name="lan\_to\_wan\_reassign\_drop\_limit"></a>
### lan\_to\_wan\_reassign\_drop\_limit
If the estimated time exceeds this threshold, the packet will be discarded and statistics will be counted. Not valid for Bulk classes.

*Type* : integer


<a name="lan\_to\_wan\_reassign\_duplicate\_packets\_disable\_depth"></a>
### lan\_to\_wan\_reassign\_duplicate\_packets\_disable\_depth
The queue depth of the class scheduler at which point duplicate packets will not be generated (value is in bytes)

*Type* : integer


<a name="lan\_to\_wan\_reassign\_duplicate\_packets\_disable\_limit"></a>
### lan\_to\_wan\_reassign\_duplicate\_packets\_disable\_limit
Designates the amount of time a packet may wait in the queue before duplication is not performed, which prevents duplicate packets from consuming bandwidth when bandwidth is limited.

*Type* : integer


<a name="lan\_to\_wan\_reassign\_enable\_red"></a>
### lan\_to\_wan\_reassign\_enable\_red
If enabled, Random Early Detection (RED) will discard packets uniformly when congestion is detected.

*Type* : boolean


<a name="lan\_to\_wan\_reassign\_large\_packet\_size\_bytes"></a>
### lan\_to\_wan\_reassign\_large\_packet\_size\_bytes
Packets destined for this class which are larger than or equal to this size will follow large packet drop policy. Packets which are smaller than this size will follow small packet drop policy. If this size is set to 0, all packets will be treated as small packets.

*Type* : integer


<a name="lan\_to\_wan\_reassign\_large\_packets\_drop\_limit"></a>
### lan\_to\_wan\_reassign\_large\_packets\_drop\_limit
If the estimated time exceeds this threshold, the packet will be discarded and statistics will be counted. Not valid for Bulk classes.

*Type* : integer


<a name="lan\_to\_wan\_reassign\_size"></a>
### lan\_to\_wan\_reassign\_size
After a flow is established, if a packet that exceeds this size is detected on the LAN to WAN, then the flow will be moved to the class indicated

*Type* : integer


<a name="lan\_to\_wan\_tcp\_standalone\_ack\_class"></a>
### lan\_to\_wan\_tcp\_standalone\_ack\_class
The Class that will be used for standalone TCP ACKs. This has no effect on packets that are piggyback ACKs with payload. If the default option is selected, TCP Standalone ACKs will continue to be mapped to the class specified in the General section.

*Type* : integer


<a name="lan\_to\_wan\_tcp\_standalone\_ack\_drop\_depth"></a>
### lan\_to\_wan\_tcp\_standalone\_ack\_drop\_depth
If the queue depth exceeds this threshold, the packet will be discarded and statistics will be counted

*Type* : integer


<a name="lan\_to\_wan\_tcp\_standalone\_ack\_drop\_limit"></a>
### lan\_to\_wan\_tcp\_standalone\_ack\_drop\_limit
If the estimated time exceeds this threshold, the packet will be discarded and statistics will be counted. Not valid for Bulk classes.

*Type* : integer


<a name="lan\_to\_wan\_tcp\_standalone\_ack\_enable\_red"></a>
### lan\_to\_wan\_tcp\_standalone\_ack\_enable\_red
If enabled, Random Early Detection (RED) will discard packets uniformly when congestion is detected.

*Type* : boolean


<a name="lan\_to\_wan\_tcp\_standalone\_ack\_large\_packet\_size\_bytes"></a>
### lan\_to\_wan\_tcp\_standalone\_ack\_large\_packet\_size\_bytes
Packets destined for this class which are larger than or equal to this size will follow large packet drop policy. Packets which are smaller than this size will follow small packet drop policy. If this size is set to 0, all packets will be treated as small packets.

*Type* : integer


<a name="lan\_to\_wan\_tcp\_standalone\_ack\_large\_packets\_drop\_limit"></a>
### lan\_to\_wan\_tcp\_standalone\_ack\_large\_packets\_drop\_limit
If the estimated time exceeds this threshold, the packet will be discarded and statistics will be counted. Not valid for Bulk classes.

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


<a name="package\_name"></a>
### package\_name
Package name to add rule to

*Type* : string


<a name="priority"></a>
### priority
The order/precedence in which Rules are applied (automatically redistributed)

*Type* : integer


<a name="rule\_group\_name"></a>
### rule\_group\_name
A name given to a rule that will allow rule statistics to be summed in groups when they are displayed. All rule statistics for rules with the same Rule Group Name can be viewed together.

*Type* : string


<a name="site\_name"></a>
### site\_name
Site name to which the rule belongs

*Type* : string


<a name="virtual\_path\_name"></a>
### virtual\_path\_name
virtual path name to which the rule belongs to

*Type* : string


<a name="wan\_enable\_header\_compression\_gre"></a>
### wan\_enable\_header\_compression\_gre
If enabled, header compression will be used for GRE packets

*Type* : boolean


<a name="wan\_enable\_header\_compression\_ip\_tcp\_udp"></a>
### wan\_enable\_header\_compression\_ip\_tcp\_udp
If enabled, header compression will be used for IP, TCP and UDP packets

*Type* : boolean


<a name="wan\_enable\_packet\_aggregation"></a>
### wan\_enable\_packet\_aggregation
If enabled, small packets on this flow will be aggregated together into larger packets

*Type* : boolean


<a name="wan\_enable\_tcp\_termination"></a>
### wan\_enable\_tcp\_termination
Traffic for this flow will be TCP terminated locally to improve throughput, reducing the round-trip times for acknowledgement packets. If enabled, TCP Termination feature will be used on flows matching this rule. The default is off.

*Type* : string


<a name="wan\_override\_service"></a>
### wan\_override\_service
The destination service that flows should go to

*Type* : string


<a name="wan\_persistent\_impedance"></a>
### wan\_persistent\_impedance
Use the same path until wait time on the path is longer than the configured value

*Type* : integer


<a name="wan\_preferred\_wan\_link"></a>
### wan\_preferred\_wan\_link
The WAN link that flows should use first

*Type* : boolean


<a name="wan\_retransmit\_lost\_packets"></a>
### wan\_retransmit\_lost\_packets
If enabled, flows matching this rule will be sent using reliable service to the remote appliance and any packets lost will be retransmitted

*Type* : boolean


<a name="wan\_to\_lan\_discard\_late\_resequenced\_packets"></a>
### wan\_to\_lan\_discard\_late\_resequenced\_packets
After a packets sequence timer has expired for a dependent packet, and the packets were permitted to the LAN: If a late packet arrives at WAN to LAN, this property defines what is to be done with it. Enable this to discard, disable this to forward.

*Type* : boolean


<a name="wan\_to\_lan\_dscp\_tag"></a>
### wan\_to\_lan\_dscp\_tag
The DSCP tag that will be applied to packets that match this rule on WAN to LAN, before they are sent to the LAN

*Type* : string


<a name="wan\_to\_lan\_enable\_packet\_resequencing"></a>
### wan\_to\_lan\_enable\_packet\_resequencing
If enabled, traffic flows that match this application should be tagged for sequence order, and the packets should be reordered (if necessary) at the WAN to LAN appliance.

*Type* : boolean


<a name="wan\_to\_lan\_resequence\_hold\_time"></a>
### wan\_to\_lan\_resequence\_hold\_time
The maximum delay that a packet may be held awaiting re-sequence. When the timer expires the packet will be sent to the LAN without waiting any further for the pre-requisite sequence numbers (value is in ms)

*Type* : integer


<a name="wan\_track\_performance"></a>
### wan\_track\_performance
If enabled, performance of a rule over time will be recorded in a session DB, including loss, latency, jitter and bandwidth used.

*Type* : integer


<a name="wan\_transmit\_mode"></a>
### wan\_transmit\_mode
The method of transmitting and receiving packets

*Type* : enum (persistent\_path, load\_balanced\_paths, duplicate\_paths, override\_service)






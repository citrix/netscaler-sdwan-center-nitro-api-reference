# application\_qos


<a name="overview"></a>
## Overview
API to add, modify, delete, and get configuration for Application QoS


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* application\_qos : Operations related to application\_qos 




<a name="paths"></a>
## Paths

<a name="application\_qos-post"></a>
### POST operation for application\_qos
```
POST /application_qos
```


#### Description
Use this operation to add the Application QoS


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[application\_qos\_request\_schema](#application\_qos\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[application\_qos\_post\_success\_schema](#application\_qos\_post\_success\_schema)|
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

* application\_qos


<a name="application\_qos-get"></a>
### Get operation for application\_qos
```
GET /application_qos
```


#### Description
Use this operation to get the Application QoS settings


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[application\_qos\_response\_schema](#application\_qos\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* application\_qos


<a name="application\_qos-put"></a>
### PUT operation for application\_qos
```
PUT /application_qos
```


#### Description
Use this operation to modify the Application QoS


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[application\_qos\_put\_success\_schema](#application\_qos\_put\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* application\_qos


<a name="application\_qos-deletepathparam-delete"></a>
### DELETE operation for application\_qos
```
DELETE /application_qos/{deletePathParam}
```


#### Description
Use this operation to delete the Application QoS


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[application\_qos\_delete\_success\_schema](#application\_qos\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* application\_qos




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="application"></a>
### application
The Application  is a pre-defined application, as specified in the Global - Applications section of this configuration.

*Type* : string


<a name="application\_family"></a>
### application\_family
The Application Family Object is a user-defined application family

*Type* : string


<a name="application\_id"></a>
### application\_id
The Application ID is a pre-defined application, as specified in the Global - Applications section of this configuration.

*Type* : integer


<a name="application\_objects"></a>
### application\_objects
The Application Object is a user-defined application, as specified in the Global - Applications section of this configuration.

*Type* : string


<a name="application\_qos"></a>
### application\_qos

|Name|Schema|
|---|---|
|**application**  <br>*optional*|[application](#application)|
|**application\_family**  <br>*optional*|[application\_family](#application\_family)|
|**application\_id**  <br>*optional*|[application\_id](#application\_id)|
|**application\_objects**  <br>*optional*|[application\_objects](#application\_objects)|
|**destination\_ip\_address**  <br>*optional*|[destination\_ip\_address](#destination\_ip\_address)|
|**destination\_port**  <br>*optional*|[destination\_port](#destination\_port)|
|**dscp\_tag**  <br>*optional*|[dscp\_tag](#dscp\_tag)|
|**duplicate\_packets\_disable\_depth**  <br>*optional*|[duplicate\_packets\_disable\_depth](#duplicate\_packets\_disable\_depth)|
|**duplicate\_packets\_disable\_limit**  <br>*optional*|[duplicate\_packets\_disable\_limit](#duplicate\_packets\_disable\_limit)|
|**id**  <br>*optional*|[id](#id)|
|**ip\_address**  <br>*optional*|[ip\_address](#ip\_address)|
|**is\_auto**  <br>*optional*|[is\_auto](#is\_auto)|
|**lan\_to\_wan\_class**  <br>*optional*|[lan\_to\_wan\_class](#lan\_to\_wan\_class)|
|**lan\_to\_wan\_drop\_depth**  <br>*optional*|[lan\_to\_wan\_drop\_depth](#lan\_to\_wan\_drop\_depth)|
|**lan\_to\_wan\_drop\_limit**  <br>*optional*|[lan\_to\_wan\_drop\_limit](#lan\_to\_wan\_drop\_limit)|
|**lan\_to\_wan\_enable\_red**  <br>*optional*|[lan\_to\_wan\_enable\_red](#lan\_to\_wan\_enable\_red)|
|**match\_type**  <br>*optional*|[match\_type](#match\_type)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**persistent\_impedance**  <br>*optional*|[persistent\_impedance](#persistent\_impedance)|
|**preferred\_wan\_link**  <br>*optional*|[preferred\_wan\_link](#preferred\_wan\_link)|
|**priority**  <br>*optional*|[priority](#priority)|
|**retransmit\_lost\_packets**  <br>*optional*|[retransmit\_lost\_packets](#retransmit\_lost\_packets)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**source\_ip\_address**  <br>*optional*|[source\_ip\_address](#source\_ip\_address)|
|**source\_port**  <br>*optional*|[source\_port](#source\_port)|
|**transmit\_mode**  <br>*optional*|[transmit\_mode](#transmit\_mode)|
|**virtual\_path\_name**  <br>*optional*|[virtual\_path\_name](#virtual\_path\_name)|
|**wan\_to\_lan\_discard\_late\_resequenced\_packets**  <br>*optional*|[wan\_to\_lan\_discard\_late\_resequenced\_packets](#wan\_to\_lan\_discard\_late\_resequenced\_packets)|
|**wan\_to\_lan\_enable\_packet\_resequencing**  <br>*optional*|[wan\_to\_lan\_enable\_packet\_resequencing](#wan\_to\_lan\_enable\_packet\_resequencing)|
|**wan\_to\_lan\_resequence\_hold\_time**  <br>*optional*|[wan\_to\_lan\_resequence\_hold\_time](#wan\_to\_lan\_resequence\_hold\_time)|


<a name="application\_qos\_delete\_success\_schema"></a>
### application\_qos\_delete\_success\_schema

|Name|Schema|
|---|---|
|**application\_qos**  <br>*optional*|[application\_qos](#application\_qos\_delete\_success\_schema-application\_qos)|

<a name="application\_qos\_delete\_success\_schema-application\_qos"></a>
**application\_qos**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="application\_qos\_post\_success\_schema"></a>
### application\_qos\_post\_success\_schema

|Name|Schema|
|---|---|
|**application\_qos**  <br>*optional*|[application\_qos](#application\_qos\_post\_success\_schema-application\_qos)|

<a name="application\_qos\_post\_success\_schema-application\_qos"></a>
**application\_qos**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="application\_qos\_put\_success\_schema"></a>
### application\_qos\_put\_success\_schema

|Name|Schema|
|---|---|
|**application\_qos**  <br>*optional*|[application\_qos](#application\_qos\_put\_success\_schema-application\_qos)|

<a name="application\_qos\_put\_success\_schema-application\_qos"></a>
**application\_qos**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="application\_qos\_request\_schema"></a>
### application\_qos\_request\_schema

|Name|Schema|
|---|---|
|**application\_qos**  <br>*optional*|[application\_qos](#application\_qos)|


<a name="application\_qos\_response\_schema"></a>
### application\_qos\_response\_schema
*Type* : < [application\_qos\_response\_schema](#application\_qos\_response\_schema-inline) > array

<a name="application\_qos\_response\_schema-inline"></a>
**application\_qos\_response\_schema**

|Name|Schema|
|---|---|
|**application**  <br>*optional*|[application](#application)|
|**application\_family**  <br>*optional*|[application\_family](#application\_family)|
|**application\_id**  <br>*optional*|[application\_id](#application\_id)|
|**application\_objects**  <br>*optional*|[application\_objects](#application\_objects)|
|**destination\_ip\_address**  <br>*optional*|[destination\_ip\_address](#destination\_ip\_address)|
|**destination\_port**  <br>*optional*|[destination\_port](#destination\_port)|
|**dscp\_tag**  <br>*optional*|[dscp\_tag](#dscp\_tag)|
|**duplicate\_packets\_disable\_depth**  <br>*optional*|[duplicate\_packets\_disable\_depth](#duplicate\_packets\_disable\_depth)|
|**duplicate\_packets\_disable\_limit**  <br>*optional*|[duplicate\_packets\_disable\_limit](#duplicate\_packets\_disable\_limit)|
|**id**  <br>*optional*|[id](#id)|
|**ip\_address**  <br>*optional*|[ip\_address](#ip\_address)|
|**is\_auto**  <br>*optional*|[is\_auto](#is\_auto)|
|**lan\_to\_wan\_class**  <br>*optional*|[lan\_to\_wan\_class](#lan\_to\_wan\_class)|
|**lan\_to\_wan\_drop\_depth**  <br>*optional*|[lan\_to\_wan\_drop\_depth](#lan\_to\_wan\_drop\_depth)|
|**lan\_to\_wan\_drop\_limit**  <br>*optional*|[lan\_to\_wan\_drop\_limit](#lan\_to\_wan\_drop\_limit)|
|**lan\_to\_wan\_enable\_red**  <br>*optional*|[lan\_to\_wan\_enable\_red](#lan\_to\_wan\_enable\_red)|
|**match\_type**  <br>*optional*|[match\_type](#match\_type)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**persistent\_impedance**  <br>*optional*|[persistent\_impedance](#persistent\_impedance)|
|**preferred\_wan\_link**  <br>*optional*|[preferred\_wan\_link](#preferred\_wan\_link)|
|**priority**  <br>*optional*|[priority](#priority)|
|**retransmit\_lost\_packets**  <br>*optional*|[retransmit\_lost\_packets](#retransmit\_lost\_packets)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**source\_ip\_address**  <br>*optional*|[source\_ip\_address](#source\_ip\_address)|
|**source\_port**  <br>*optional*|[source\_port](#source\_port)|
|**transmit\_mode**  <br>*optional*|[transmit\_mode](#transmit\_mode)|
|**virtual\_path\_name**  <br>*optional*|[virtual\_path\_name](#virtual\_path\_name)|
|**wan\_to\_lan\_discard\_late\_resequenced\_packets**  <br>*optional*|[wan\_to\_lan\_discard\_late\_resequenced\_packets](#wan\_to\_lan\_discard\_late\_resequenced\_packets)|
|**wan\_to\_lan\_enable\_packet\_resequencing**  <br>*optional*|[wan\_to\_lan\_enable\_packet\_resequencing](#wan\_to\_lan\_enable\_packet\_resequencing)|
|**wan\_to\_lan\_resequence\_hold\_time**  <br>*optional*|[wan\_to\_lan\_resequence\_hold\_time](#wan\_to\_lan\_resequence\_hold\_time)|


<a name="destination\_ip\_address"></a>
### destination\_ip\_address
The Destination IP Address and subnet mask that this rule will match

*Type* : string


<a name="destination\_port"></a>
### destination\_port
If set, the Destination Port or Port range (eg: 2345-2457) that this rule will match

*Type* : string


<a name="dscp\_tag"></a>
### dscp\_tag
The DSCP tag that will be applied to packets that match this rule on WAN to LAN, before they are sent to the LAN

*Type* : enum (any, af11, af12, af13, af21, af22, af23, af31, af32, af33, af41, af42, af43, cs1, cs2, cs3, cs4, cs5, cs6, cs7, default, ef)


<a name="duplicate\_packets\_disable\_depth"></a>
### duplicate\_packets\_disable\_depth
The queue depth of the class scheduler at which point duplicate packets will not be generated (value is in bytes)

*Type* : integer


<a name="duplicate\_packets\_disable\_limit"></a>
### duplicate\_packets\_disable\_limit
The amount of time a packet may wait in the queue before duplication is not performed, which prevents duplicate packets from consuming bandwidth when bandwidth is limited (value is in ms)

*Type* : integer


<a name="id"></a>
### id
Object id for application qos

*Type* : integer


<a name="ip\_address"></a>
### ip\_address
The Source or Destination IP Address and subnet mask that this application will match

*Type* : string


<a name="is\_auto"></a>
### is\_auto
If set to true, it is a default Application QoS

*Type* : boolean


<a name="lan\_to\_wan\_class"></a>
### lan\_to\_wan\_class
The Class that is to service traffic flows that match this application. The default is Class 9

*Type* : integer


<a name="lan\_to\_wan\_drop\_depth"></a>
### lan\_to\_wan\_drop\_depth
If the queue depth exceeds this threshold, the packet will be discarded and statistics will be counted (value is in bytes)

*Type* : integer


<a name="lan\_to\_wan\_drop\_limit"></a>
### lan\_to\_wan\_drop\_limit
The maximum amount of estimated time that packets will have to wait in the class scheduler. If the estimated time exceeds this threshold, the packet will be discarded and statistics will be counted. Not valid for Bulk classes (Value is in ms)

*Type* : integer


<a name="lan\_to\_wan\_enable\_red"></a>
### lan\_to\_wan\_enable\_red
If enabled, Random Early Detection (RED) will discard packets uniformly when congestion is detected.

*Type* : boolean


<a name="match\_type"></a>
### match\_type
The mechanism through which this application will be matched (Either a user-defined application, pre-defined applications or groupings of applications)

*Type* : enum (application\_objects, application, application\_family)


<a name="package\_name"></a>
### package\_name
Package name to add application qos to

*Type* : string


<a name="persistent\_impedance"></a>
### persistent\_impedance
Use the same path until wait time on the path is longer than the configured value

*Type* : integer


<a name="preferred\_wan\_link"></a>
### preferred\_wan\_link
The WAN link that flows should use first

*Type* : string


<a name="priority"></a>
### priority
Order of evaluation of the application rule

*Type* : integer


<a name="retransmit\_lost\_packets"></a>
### retransmit\_lost\_packets
If enabled, flows matching this application will be sent using reliable service to the remote appliance and any packets lost will be retransmitted

*Type* : boolean


<a name="site\_name"></a>
### site\_name
Site name to which the application qos belongs

*Type* : string


<a name="source\_ip\_address"></a>
### source\_ip\_address
The Source IP Address and subnet mask that this application will match

*Type* : string


<a name="source\_port"></a>
### source\_port
If set, the Source Port or Port range (eg: 2345-2457) that this rule will match

*Type* : string


<a name="transmit\_mode"></a>
### transmit\_mode
The method of transmitting and receiving packets

*Type* : enum (load\_balance\_paths, persistent\_path, duplicate\_paths)


<a name="virtual\_path\_name"></a>
### virtual\_path\_name
virtual path name to which the application qos belongs to

*Type* : string


<a name="wan\_to\_lan\_discard\_late\_resequenced\_packets"></a>
### wan\_to\_lan\_discard\_late\_resequenced\_packets
After a packets sequence timer has expired for a dependent packet, and the packets were permitted to the LAN: If a late packet arrives at WAN to LAN, this property defines what is to be done with it. Enable this checkbox to discard, disable this checkbox to forward.

*Type* : boolean


<a name="wan\_to\_lan\_enable\_packet\_resequencing"></a>
### wan\_to\_lan\_enable\_packet\_resequencing
If enabled, traffic flows that match this application should be tagged for sequence order, and the packets should be reordered (if necessary) at the WAN to LAN appliance.

*Type* : boolean


<a name="wan\_to\_lan\_resequence\_hold\_time"></a>
### wan\_to\_lan\_resequence\_hold\_time
The maximum delay that a packet may be held awaiting re-sequence. When the timer expires the packet will be sent to the LAN without waiting any further for the pre-requisite sequence numbers (value is in ms)

*Type* : integer






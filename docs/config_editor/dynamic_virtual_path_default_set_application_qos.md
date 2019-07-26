# dynamic\_virtual\_path\_default\_set\_application\_qos


<a name="overview"></a>
## Overview
API to add, modify, delete, and get configuration for Dynamic Virtual Path Default Set Application QoS


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* dynamic\_virtual\_path\_default\_set\_application\_qos : Operations related to dynamic\_virtual\_path\_default\_set\_application\_qos 




<a name="paths"></a>
## Paths

<a name="dynamic\_virtual\_path\_default\_set\_application\_qos-post"></a>
### POST operation for dynamic\_virtual\_path\_default\_set\_application\_qos
```
POST /dynamic_virtual_path_default_set_application_qos
```


#### Description
Use this operation to add the Dynamic Virtual Path Default Set Application QoS


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[dynamic\_virtual\_path\_default\_set\_application\_qos\_post\_success\_schema](#dynamic\_virtual\_path\_default\_set\_application\_qos\_post\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* dynamic\_virtual\_path\_default\_set\_application\_qos


<a name="dynamic\_virtual\_path\_default\_set\_application\_qos-get"></a>
### Get operation for dynamic\_virtual\_path\_default\_set\_application\_qos
```
GET /dynamic_virtual_path_default_set_application_qos
```


#### Description
Use this operation to get the Dynamic Virtual Path Default Set Application QoS


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[dynamic\_virtual\_path\_default\_set\_application\_qos\_response\_schema](#dynamic\_virtual\_path\_default\_set\_application\_qos\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* dynamic\_virtual\_path\_default\_set\_application\_qos


<a name="dynamic\_virtual\_path\_default\_set\_application\_qos-put"></a>
### PUT operation for dynamic\_virtual\_path\_default\_set\_application\_qos
```
PUT /dynamic_virtual_path_default_set_application_qos
```


#### Description
Use this operation to modify the Dynamic Virtual Path Default Set Application QoS


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[dynamic\_virtual\_path\_default\_set\_application\_qos\_request\_schema](#dynamic\_virtual\_path\_default\_set\_application\_qos\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[dynamic\_virtual\_path\_default\_set\_application\_qos\_put\_success\_schema](#dynamic\_virtual\_path\_default\_set\_application\_qos\_put\_success\_schema)|
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

* dynamic\_virtual\_path\_default\_set\_application\_qos


<a name="dynamic\_virtual\_path\_default\_set\_application\_qos-deletepathparam-delete"></a>
### DELETE operation for dynamic\_virtual\_path\_default\_set\_application\_qos
```
DELETE /dynamic_virtual_path_default_set_application_qos/{deletePathParam}
```


#### Description
Use this operation to delete the Dynamic Virtual Path Default Set Application QoS


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[dynamic\_virtual\_path\_default\_set\_application\_qos\_delete\_success\_schema](#dynamic\_virtual\_path\_default\_set\_application\_qos\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* dynamic\_virtual\_path\_default\_set\_application\_qos




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="dynamic\_virtual\_path\_default\_set\_application\_qos"></a>
### dynamic\_virtual\_path\_default\_set\_application\_qos

|Name|Schema|
|---|---|
|**dynamic\_virtual\_path\_default\_set\_name**  <br>*optional*|[dynamic\_virtual\_path\_default\_set\_name](#dynamic\_virtual\_path\_default\_set\_name)|
|**id**  <br>*optional*|[id](#id)|
|**match\_properties**  <br>*optional*|[match\_properties](#match\_properties)|
|**order**  <br>*optional*|[order](#order)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**wan\_properties**  <br>*optional*|[wan\_properties](#wan\_properties)|


<a name="dynamic\_virtual\_path\_default\_set\_application\_qos\_delete\_success\_schema"></a>
### dynamic\_virtual\_path\_default\_set\_application\_qos\_delete\_success\_schema

|Name|Schema|
|---|---|
|**dynamic\_virtual\_path\_default\_set\_application\_qos**  <br>*optional*|[dynamic\_virtual\_path\_default\_set\_application\_qos](#dynamic\_virtual\_path\_default\_set\_application\_qos\_delete\_success\_schema-dynamic\_virtual\_path\_default\_set\_application\_qos)|

<a name="dynamic\_virtual\_path\_default\_set\_application\_qos\_delete\_success\_schema-dynamic\_virtual\_path\_default\_set\_application\_qos"></a>
**dynamic\_virtual\_path\_default\_set\_application\_qos**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="dynamic\_virtual\_path\_default\_set\_application\_qos\_post\_success\_schema"></a>
### dynamic\_virtual\_path\_default\_set\_application\_qos\_post\_success\_schema

|Name|Schema|
|---|---|
|**dynamic\_virtual\_path\_default\_set\_application\_qos**  <br>*optional*|[dynamic\_virtual\_path\_default\_set\_application\_qos](#dynamic\_virtual\_path\_default\_set\_application\_qos\_post\_success\_schema-dynamic\_virtual\_path\_default\_set\_application\_qos)|

<a name="dynamic\_virtual\_path\_default\_set\_application\_qos\_post\_success\_schema-dynamic\_virtual\_path\_default\_set\_application\_qos"></a>
**dynamic\_virtual\_path\_default\_set\_application\_qos**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="dynamic\_virtual\_path\_default\_set\_application\_qos\_put\_success\_schema"></a>
### dynamic\_virtual\_path\_default\_set\_application\_qos\_put\_success\_schema

|Name|Schema|
|---|---|
|**dynamic\_virtual\_path\_default\_set\_application\_qos**  <br>*optional*|[dynamic\_virtual\_path\_default\_set\_application\_qos](#dynamic\_virtual\_path\_default\_set\_application\_qos\_put\_success\_schema-dynamic\_virtual\_path\_default\_set\_application\_qos)|

<a name="dynamic\_virtual\_path\_default\_set\_application\_qos\_put\_success\_schema-dynamic\_virtual\_path\_default\_set\_application\_qos"></a>
**dynamic\_virtual\_path\_default\_set\_application\_qos**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="dynamic\_virtual\_path\_default\_set\_application\_qos\_request\_schema"></a>
### dynamic\_virtual\_path\_default\_set\_application\_qos\_request\_schema

|Name|Schema|
|---|---|
|**dynamic\_virtual\_path\_default\_set\_application\_qos**  <br>*optional*|[dynamic\_virtual\_path\_default\_set\_application\_qos](#dynamic\_virtual\_path\_default\_set\_application\_qos)|


<a name="dynamic\_virtual\_path\_default\_set\_application\_qos\_response\_schema"></a>
### dynamic\_virtual\_path\_default\_set\_application\_qos\_response\_schema
*Type* : < [dynamic\_virtual\_path\_default\_set\_application\_qos\_response\_schema](#dynamic\_virtual\_path\_default\_set\_application\_qos\_response\_schema-inline) > array

<a name="dynamic\_virtual\_path\_default\_set\_application\_qos\_response\_schema-inline"></a>
**dynamic\_virtual\_path\_default\_set\_application\_qos\_response\_schema**

|Name|Schema|
|---|---|
|**dynamic\_virtual\_path\_default\_set\_name**  <br>*optional*|[dynamic\_virtual\_path\_default\_set\_name](#dynamic\_virtual\_path\_default\_set\_name)|
|**id**  <br>*optional*|[id](#id)|
|**match\_properties**  <br>*optional*|[match\_properties](#match\_properties)|
|**order**  <br>*optional*|[order](#order)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**wan\_properties**  <br>*optional*|[wan\_properties](#wan\_properties)|


<a name="dynamic\_virtual\_path\_default\_set\_name"></a>
### dynamic\_virtual\_path\_default\_set\_name
Dynamic Virtual path Default Set name using which the API operation should be performed.

*Type* : string


<a name="id"></a>
### id
Id for application qos

*Type* : integer


<a name="match\_properties"></a>
### match\_properties
Application QoS match properties


|Name|Description|Schema|
|---|---|---|
|**application**  <br>*optional*|The Application is a pre-defined application, as specified in the Global - Applications section of this configuration.  <br>**Default** : `"any"`|string|
|**application\_family**  <br>*optional*|The Application Family Object is a user-defined application family  <br>**Default** : `"any"`|string|
|**application\_object**  <br>*optional*|The Application Object is a user-defined application, as specified in the Global - Applications section of this configuration.  <br>**Default** : `"any"`|string|
|**destination\_ip\_address**  <br>*optional*|The Destination IP Address and subnet mask that this rule will match|string|
|**destination\_port**  <br>*optional*|If set, the Destination Port or Port range (eg: 2345-2457) that this rule will match|string|
|**match\_type**  <br>*optional*|The mechanism through which this application will be matched (Either a user-defined application, pre-defined applications or groupings of applications)|enum (application\_objects, application, application\_family)|
|**source\_ip\_address**  <br>*optional*|The Source IP Address and subnet mask that this application will match|string|
|**source\_port**  <br>*optional*|If set, the Source Port or Port range (eg: 2345-2457) that this rule will match|string|


<a name="order"></a>
### order
The order/precedence in which applications are matched (automatically redistributed)

*Type* : integer


<a name="package\_name"></a>
### package\_name
Package name to add application qos to

*Type* : string


<a name="wan\_properties"></a>
### wan\_properties
Application QoS WAN properties


|Name|Description|Schema|
|---|---|---|
|**lan\_to\_wan\_class\_id**  <br>*optional*|The Class that is to service traffic flows that match this application. The default is Class 9  <br>**Default** : `"9"`|string|
|**lan\_to\_wan\_drop\_depth**  <br>*optional*|If the queue depth exceeds this threshold, the packet will be discarded and statistics will be counted (value is in bytes)|integer|
|**lan\_to\_wan\_drop\_limit**  <br>*optional*|The maximum amount of estimated time that packets will have to wait in the class scheduler. If the estimated time exceeds this threshold, the packet will be discarded and statistics will be counted. Not valid for Bulk classes (Value is in ms)|integer|
|**lan\_to\_wan\_duplicate\_packets\_disable\_depth**  <br>*optional*|The queue depth of the class scheduler at which point duplicate packets will not be generated (value is in bytes)|integer|
|**lan\_to\_wan\_duplicate\_packets\_disable\_limit**  <br>*optional*|The amount of time a packet may wait in the queue before duplication is not performed, which prevents duplicate packets from consuming bandwidth when bandwidth is limited (value is in ms)|integer|
|**lan\_to\_wan\_enable\_red**  <br>*optional*|If enabled, Random Early Detection (RED) will discard packets uniformly when congestion is detected.  <br>**Default** : `false`|boolean|
|**persistent\_impedance**  <br>*optional*|Use the same path until wait time on the path is longer than the configured value|integer|
|**retransmit\_lost\_packets**  <br>*optional*|If enabled, flows matching this application will be sent using reliable service to the remote appliance and any packets lost will be retransmitted  <br>**Default** : `false`|boolean|
|**rule\_group\_name**  <br>*optional*|A name given to a rule that will allow rule statistics to be summed in groups when they are displayed. All rule statistics for rules with the same Application Name can be viewed together.|string|
|**transmit\_mode**  <br>*optional*|The method of transmitting and receiving packets  <br>**Default** : `"load_balance_paths"`|enum (load\_balance\_paths, persistent\_paths, duplicate\_paths)|
|**wan\_to\_lan\_discard\_late\_resequenced\_packets**  <br>*optional*|After a packets sequence timer has expired for a dependent packet, and the packets were permitted to the LAN: If a late packet arrives at WAN to LAN, this property defines what is to be done with it. Enable this checkbox to discard, disable this checkbox to forward.  <br>**Default** : `true`|boolean|
|**wan\_to\_lan\_dscp\_tag**  <br>*optional*|The DSCP tag that will be applied to packets that match this rule on WAN to LAN, before they are sent to the LAN|enum (any, af11, af12, af13, af21, af22, af23, af31, af32, af33, af41, af42, af43, cs1, cs2, cs3, cs4, cs5, cs6, cs7, default, ef)|
|**wan\_to\_lan\_enable\_packet\_resequencing**  <br>*optional*|If enabled, traffic flows that match this application should be tagged for sequence order, and the packets should be reordered (if necessary) at the WAN to LAN appliance.  <br>**Default** : `false`|boolean|
|**wan\_to\_lan\_resequence\_hold\_time**  <br>*optional*|The maximum delay that a packet may be held awaiting re-sequence. When the timer expires the packet will be sent to the LAN without waiting any further for the pre-requisite sequence numbers (value is in ms)|integer|






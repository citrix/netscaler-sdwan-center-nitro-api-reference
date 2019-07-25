# virtualpaths


<a name="overview"></a>
## Overview
API to add, modify, delete, and get virtual paths


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* virtualpaths : Operations related to virtualpaths 




<a name="paths"></a>
## Paths

<a name="virtualpaths-post"></a>
### POST operation for virtualpaths
```
POST /virtualpaths
```


#### Description
Use this operation to add virtual paths


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[virtualpaths\_request\_schema](#virtualpaths\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[virtualpaths\_post\_success\_schema](#virtualpaths\_post\_success\_schema)|
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

* virtualpaths


<a name="virtualpaths-get"></a>
### Get operation for virtualpaths
```
GET /virtualpaths
```


#### Description
Use this operation to get the list of virtual paths


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[virtualpaths\_response\_schema](#virtualpaths\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* virtualpaths


<a name="virtualpaths-put"></a>
### PUT operation for virtualpaths
```
PUT /virtualpaths
```


#### Description
Use this operation to modify a virtual paths


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[virtualpaths\_put\_success\_schema](#virtualpaths\_put\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* virtualpaths


<a name="virtualpaths-deletepathparam-delete"></a>
### DELETE operation for virtualpaths
```
DELETE /virtualpaths/{deletePathParam}
```


#### Description
Use this operation to delete a virtual paths


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[virtualpaths\_delete\_success\_schema](#virtualpaths\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* virtualpaths




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="local\_site"></a>
### local\_site
Virtual Path Local Site configuration

*Type* : < [local\_site](#local\_site-inline) > array

<a name="local\_site-inline"></a>
**local\_site**

|Name|Description|Schema|
|---|---|---|
|**default\_set**  <br>*optional*|Name of the Virtual Path Default Set that will be used to populate rules and classes for the Virtual Path on the Site|string|
|**route\_cost**  <br>*optional*|This Cost will be added to Routes learned via the Virtual Path|integer|
|**tracking\_ip\_address**  <br>*optional*|Tracking IP Address|string|


<a name="local\_site\_name"></a>
### local\_site\_name
Local Site name

*Type* : string


<a name="package\_name"></a>
### package\_name
Config package name using which the wan\_links API operation should be performed.

*Type* : string


<a name="paths"></a>
### paths
Path Configuration for Virtual Paths

*Type* : < [paths](#paths-inline) > array

<a name="paths-inline"></a>
**paths**

|Name|Description|Schema|
|---|---|---|
|**bad\_loss\_sensitive**  <br>*optional*|If Bad Loss Sensitive is set to Enable, Paths will be marked BAD due to loss and will incur a Path scoring penalty. Setting this option to Disable may be useful when the loss of bandwidth is intolerable. Custom settings allow you to specify the percentage of loss over time required to mark a Path BAD.  <br>**Default** : `"ENABLE"`|enum (ENABLE, DISABLE, CUSTOM)|
|**enable\_encryption**  <br>*optional*|If enabled, packets sent along this Path will be encrypted|boolean|
|**from\_site\_name**  <br>*optional*|Source site for the new path|string|
|**from\_wan\_link\_name**  <br>*optional*|Source WAN link for the new path|string|
|**instability\_sensitive**  <br>*optional*|If you enable Instability Sensitive, latency penalties due to the Path being in a BAD state and other latency spikes are considered in the Path scoring algorithm  <br>**Default** : `false`|boolean|
|**ip\_dscp\_tagging**  <br>*optional*|The DSCP Tag to set in the IP header for Path traffic  <br>**Default** : `"ANY"`|enum (ANY, DEFAULT, af11, af12, af13, af21, af22, af23, af31, af32, af33, af41, af42, af43, cs1, cs2, cs3, cs4, cs5, cs6, cs7, ef)|
|**reverse\_also**  <br>*optional*|Add reverse path configuration also|boolean|
|**reverse\_tracking\_ip\_address**  <br>*optional*|If Reverse Also is enabled, a virtual IP address on the Path that can be pinged to determine the state of the reverse Path|string|
|**silence\_period**  <br>*optional*|Specify silence duration before Path state transitions from GOOD to BAD. When not specified, the default is 150ms|integer|
|**static\_path**  <br>*optional*|Convert Path, and all other Paths associated by WAN Link, Generated by an Autopath Group, to a Static Path. This action cannot be undone|boolean|
|**to\_site\_name**  <br>*optional*|Destination site for the new path|string|
|**to\_wan\_link\_name**  <br>*optional*|Destination WAN Link for the new path|string|
|**tracking\_ip\_address**  <br>*optional*|A virtual IP address on the Path that can be pinged to determine the state of the Path|string|


<a name="remote\_site"></a>
### remote\_site
Virtual Path Remote Site configuration

*Type* : < [remote\_site](#remote\_site-inline) > array

<a name="remote\_site-inline"></a>
**remote\_site**

|Name|Description|Schema|
|---|---|---|
|**default\_set**  <br>*optional*|Name of the Virtual Path Default Set that will be used to populate rules and classes for the Virtual Path on the Site|string|
|**route\_cost**  <br>*optional*|This Cost will be added to Routes learned via the Virtual Path|integer|
|**tracking\_ip\_address**  <br>*optional*|Tracking IP Address|string|


<a name="remote\_site\_name"></a>
### remote\_site\_name
Remote Site name

*Type* : string


<a name="reverse"></a>
### reverse
It should create reverse virtual Path also

*Type* : boolean


<a name="virtualpaths"></a>
### virtualpaths

|Name|Schema|
|---|---|
|**local\_site**  <br>*optional*|[local\_site](#local\_site)|
|**local\_site\_name**  <br>*optional*|[local\_site\_name](#local\_site\_name)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**paths**  <br>*optional*|[paths](#paths)|
|**remote\_site**  <br>*optional*|[remote\_site](#remote\_site)|
|**remote\_site\_name**  <br>*optional*|[remote\_site\_name](#remote\_site\_name)|
|**reverse**  <br>*optional*|[reverse](#reverse)|


<a name="virtualpaths\_delete\_success\_schema"></a>
### virtualpaths\_delete\_success\_schema

|Name|Schema|
|---|---|
|**virtualpaths**  <br>*optional*|[virtualpaths](#virtualpaths\_delete\_success\_schema-virtualpaths)|

<a name="virtualpaths\_delete\_success\_schema-virtualpaths"></a>
**virtualpaths**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="virtualpaths\_post\_success\_schema"></a>
### virtualpaths\_post\_success\_schema

|Name|Schema|
|---|---|
|**virtualpaths**  <br>*optional*|[virtualpaths](#virtualpaths\_post\_success\_schema-virtualpaths)|

<a name="virtualpaths\_post\_success\_schema-virtualpaths"></a>
**virtualpaths**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="virtualpaths\_put\_success\_schema"></a>
### virtualpaths\_put\_success\_schema

|Name|Schema|
|---|---|
|**virtualpaths**  <br>*optional*|[virtualpaths](#virtualpaths\_put\_success\_schema-virtualpaths)|

<a name="virtualpaths\_put\_success\_schema-virtualpaths"></a>
**virtualpaths**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="virtualpaths\_request\_schema"></a>
### virtualpaths\_request\_schema

|Name|Schema|
|---|---|
|**virtualpaths**  <br>*optional*|[virtualpaths](#virtualpaths)|


<a name="virtualpaths\_response\_schema"></a>
### virtualpaths\_response\_schema
*Type* : < [virtualpaths\_response\_schema](#virtualpaths\_response\_schema-inline) > array

<a name="virtualpaths\_response\_schema-inline"></a>
**virtualpaths\_response\_schema**

|Name|Schema|
|---|---|
|**local\_site**  <br>*optional*|[local\_site](#local\_site)|
|**local\_site\_name**  <br>*optional*|[local\_site\_name](#local\_site\_name)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**paths**  <br>*optional*|[paths](#paths)|
|**remote\_site**  <br>*optional*|[remote\_site](#remote\_site)|
|**remote\_site\_name**  <br>*optional*|[remote\_site\_name](#remote\_site\_name)|
|**reverse**  <br>*optional*|[reverse](#reverse)|






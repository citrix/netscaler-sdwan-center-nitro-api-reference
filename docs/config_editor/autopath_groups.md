# autopath\_groups


<a name="overview"></a>
## Overview
API to add, delete, get, modify autopath groups


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* autopath\_groups : Operations related to autopath\_groups 




<a name="paths"></a>
## Paths

<a name="autopath\_groups-post"></a>
### POST operation for autopath\_groups
```
POST /autopath_groups
```


#### Description
Use this operation to add autopath groups


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[autopath\_groups\_post\_success\_schema](#autopath\_groups\_post\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* autopath\_groups


<a name="autopath\_groups-get"></a>
### Get operation for autopath\_groups
```
GET /autopath_groups
```


#### Description
Use this operation to get the autopath groups


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[autopath\_groups\_response\_schema](#autopath\_groups\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* autopath\_groups


<a name="autopath\_groups-put"></a>
### PUT operation for autopath\_groups
```
PUT /autopath_groups
```


#### Description
Use this operation to modify autopath groups


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[autopath\_groups\_request\_schema](#autopath\_groups\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[autopath\_groups\_put\_success\_schema](#autopath\_groups\_put\_success\_schema)|
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

* autopath\_groups


<a name="autopath\_groups-deletepathparam-delete"></a>
### DELETE operation for autopath\_groups
```
DELETE /autopath_groups/{deletePathParam}
```


#### Description
Use this operation to delete autopath groups


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[autopath\_groups\_delete\_success\_schema](#autopath\_groups\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* autopath\_groups




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="autopath\_groups"></a>
### autopath\_groups

|Name|Schema|
|---|---|
|**id**  <br>*optional*|[id](#id)|
|**name**  <br>*optional*|[name](#name)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**properties**  <br>*optional*|[properties](#properties)|


<a name="autopath\_groups\_delete\_success\_schema"></a>
### autopath\_groups\_delete\_success\_schema

|Name|Schema|
|---|---|
|**autopath\_groups**  <br>*optional*|[autopath\_groups](#autopath\_groups\_delete\_success\_schema-autopath\_groups)|

<a name="autopath\_groups\_delete\_success\_schema-autopath\_groups"></a>
**autopath\_groups**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="autopath\_groups\_post\_success\_schema"></a>
### autopath\_groups\_post\_success\_schema

|Name|Schema|
|---|---|
|**autopath\_groups**  <br>*optional*|[autopath\_groups](#autopath\_groups\_post\_success\_schema-autopath\_groups)|

<a name="autopath\_groups\_post\_success\_schema-autopath\_groups"></a>
**autopath\_groups**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="autopath\_groups\_put\_success\_schema"></a>
### autopath\_groups\_put\_success\_schema

|Name|Schema|
|---|---|
|**autopath\_groups**  <br>*optional*|[autopath\_groups](#autopath\_groups\_put\_success\_schema-autopath\_groups)|

<a name="autopath\_groups\_put\_success\_schema-autopath\_groups"></a>
**autopath\_groups**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="autopath\_groups\_request\_schema"></a>
### autopath\_groups\_request\_schema

|Name|Schema|
|---|---|
|**autopath\_groups**  <br>*optional*|[autopath\_groups](#autopath\_groups)|


<a name="autopath\_groups\_response\_schema"></a>
### autopath\_groups\_response\_schema
*Type* : < [autopath\_groups\_response\_schema](#autopath\_groups\_response\_schema-inline) > array

<a name="autopath\_groups\_response\_schema-inline"></a>
**autopath\_groups\_response\_schema**

|Name|Schema|
|---|---|
|**id**  <br>*optional*|[id](#id)|
|**name**  <br>*optional*|[name](#name)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**properties**  <br>*optional*|[properties](#properties)|


<a name="id"></a>
### id
Auto-generated ID to uniquely identify autopath group

*Type* : integer


<a name="name"></a>
### name
The name for the autopath group

*Type* : string


<a name="package\_name"></a>
### package\_name
Config package name using which the API operation should be performed.

*Type* : string


<a name="properties"></a>
### properties
Properties for the autopath group


|Name|Description|Schema|
|---|---|---|
|**bad\_loss\_sensitive**  <br>*optional*|If Bad Loss Sensitive is set to Enable, Paths will be marked BAD due to loss AND will incur a Path scoring penalty. Setting this option to Disable may be useful when the loss of bandwidth is intolerable. Custom settings allow you to specify the percentage of loss over time required to mark a Path BAD.|enum (enable, disable, custom)|
|**enable\_encryption**  <br>*optional*|If enabled, packets sent along this Path will be encrypted|boolean|
|**instability\_sensitive**  <br>*optional*|If you enable Instability Sensitive, latency penalties due to the Path being in a BAD state AND other latency spikes are considered in the Path scoring algorithm.|boolean|
|**ip\_dscp\_tagging**  <br>*optional*|The DSCP Tag to set in the IP header for Path traffic|enum (any, af11, af12, af13, af21, af22, af23, af31, af32, af33, af41, af42, af43, cs1, cs2, cs3, cs4, cs5, cs6, cs7, default, ef)|
|**over\_time\_ms**  <br>*optional*|Specify the time period, in milliseconds, over which Percent Loss is measured.|integer|
|**path\_probation\_period\_ms**  <br>*optional*|Specify the wait time, OR Path Probation Period, before a Path transitions from BAD to GOOD. The default is 10 seconds.|integer|
|**percent\_loss**  <br>*optional*|The Percent Loss is the percentage of packet loss observed before a Path is marked BAD which measured Over Time. By default, packet loss is based on the last 200 packets received. Use the drop-down menus to configure Percent Loss AND Over Time.|enum (default, 1, 2, 3, 4, 5, 10, 20, 30, 40, 50, 60, 70, 80, 90)|
|**set\_as\_default**  <br>*optional*|If enabled, this group will be used as the default Autopath Group for WAN Link Usages|boolean|
|**silence\_period\_ms**  <br>*optional*|Specify silence duration before Path state transitions from GOOD to BAD. When not specified, the default is 150ms.|string|






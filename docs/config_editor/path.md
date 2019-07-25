# path


<a name="overview"></a>
## Overview
Paths configuration for virtual paths


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* path : Operations related to path 




<a name="paths"></a>
## Paths

<a name="path-post"></a>
### POST operation for path
```
POST /path
```


#### Description
Use this operation to add paths


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[path\_post\_success\_schema](#path\_post\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* path


<a name="path-get"></a>
### Get operation for path
```
GET /path
```


#### Description
Use this operation to get the Path configuration for a particular virtual path


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[path\_response\_schema](#path\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* path


<a name="path-put"></a>
### PUT operation for path
```
PUT /path
```


#### Description
Use this operation to modify a path


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[path\_request\_schema](#path\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[path\_put\_success\_schema](#path\_put\_success\_schema)|
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

* path


<a name="path-deletepathparam-delete"></a>
### DELETE operation for path
```
DELETE /path/{deletePathParam}
```


#### Description
Use this operation to delete a path


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[path\_delete\_success\_schema](#path\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* path




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="bad\_loss\_sensitive"></a>
### bad\_loss\_sensitive
If Bad Loss Sensitive is set to Enable, Paths will be marked BAD due to loss and will incur a Path scoring penalty. Setting this option to Disable may be useful when the loss of bandwidth is intolerable. Custom settings allow you to specify the percentage of loss over time required to mark a Path BAD.

*Type* : enum (ENABLE, DISABLE, CUSTOM)


<a name="enable\_encryption"></a>
### enable\_encryption
If enabled, packets sent along this Path will be encrypted

*Type* : boolean


<a name="from\_site\_name"></a>
### from\_site\_name
Source site for the new path

*Type* : string


<a name="from\_wan\_link\_name"></a>
### from\_wan\_link\_name
Source WAN link for the new path

*Type* : string


<a name="instability\_sensitive"></a>
### instability\_sensitive
If you enable Instability Sensitive, latency penalties due to the Path being in a BAD state and other latency spikes are considered in the Path scoring algorithm

*Type* : boolean


<a name="ip\_dscp\_tagging"></a>
### ip\_dscp\_tagging
The DSCP Tag to set in the IP header for Path traffic

*Type* : enum (ANY, DEFAULT, af11, af12, af13, af21, af22, af23, af31, af32, af33, af41, af42, af43, cs1, cs2, cs3, cs4, cs5, cs6, cs7, ef)


<a name="package\_name"></a>
### package\_name
Package corresponding to the API operation

*Type* : string


<a name="path"></a>
### path

|Name|Schema|
|---|---|
|**bad\_loss\_sensitive**  <br>*optional*|[bad\_loss\_sensitive](#bad\_loss\_sensitive)|
|**enable\_encryption**  <br>*optional*|[enable\_encryption](#enable\_encryption)|
|**from\_site\_name**  <br>*optional*|[from\_site\_name](#from\_site\_name)|
|**from\_wan\_link\_name**  <br>*optional*|[from\_wan\_link\_name](#from\_wan\_link\_name)|
|**instability\_sensitive**  <br>*optional*|[instability\_sensitive](#instability\_sensitive)|
|**ip\_dscp\_tagging**  <br>*optional*|[ip\_dscp\_tagging](#ip\_dscp\_tagging)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**reverse\_also**  <br>*optional*|[reverse\_also](#reverse\_also)|
|**reverse\_tracking\_ip\_address**  <br>*optional*|[reverse\_tracking\_ip\_address](#reverse\_tracking\_ip\_address)|
|**silence\_period**  <br>*optional*|[silence\_period](#silence\_period)|
|**static\_path**  <br>*optional*|[static\_path](#static\_path)|
|**to\_site\_name**  <br>*optional*|[to\_site\_name](#to\_site\_name)|
|**to\_wan\_link\_name**  <br>*optional*|[to\_wan\_link\_name](#to\_wan\_link\_name)|
|**tracking\_ip\_address**  <br>*optional*|[tracking\_ip\_address](#tracking\_ip\_address)|
|**virtual\_path\_name**  <br>*optional*|[virtual\_path\_name](#virtual\_path\_name)|


<a name="path\_delete\_success\_schema"></a>
### path\_delete\_success\_schema

|Name|Schema|
|---|---|
|**path**  <br>*optional*|[path](#path\_delete\_success\_schema-path)|

<a name="path\_delete\_success\_schema-path"></a>
**path**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="path\_post\_success\_schema"></a>
### path\_post\_success\_schema

|Name|Schema|
|---|---|
|**path**  <br>*optional*|[path](#path\_post\_success\_schema-path)|

<a name="path\_post\_success\_schema-path"></a>
**path**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="path\_put\_success\_schema"></a>
### path\_put\_success\_schema

|Name|Schema|
|---|---|
|**path**  <br>*optional*|[path](#path\_put\_success\_schema-path)|

<a name="path\_put\_success\_schema-path"></a>
**path**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="path\_request\_schema"></a>
### path\_request\_schema

|Name|Schema|
|---|---|
|**path**  <br>*optional*|[path](#path)|


<a name="path\_response\_schema"></a>
### path\_response\_schema
*Type* : < [path\_response\_schema](#path\_response\_schema-inline) > array

<a name="path\_response\_schema-inline"></a>
**path\_response\_schema**

|Name|Schema|
|---|---|
|**bad\_loss\_sensitive**  <br>*optional*|[bad\_loss\_sensitive](#bad\_loss\_sensitive)|
|**enable\_encryption**  <br>*optional*|[enable\_encryption](#enable\_encryption)|
|**from\_site\_name**  <br>*optional*|[from\_site\_name](#from\_site\_name)|
|**from\_wan\_link\_name**  <br>*optional*|[from\_wan\_link\_name](#from\_wan\_link\_name)|
|**instability\_sensitive**  <br>*optional*|[instability\_sensitive](#instability\_sensitive)|
|**ip\_dscp\_tagging**  <br>*optional*|[ip\_dscp\_tagging](#ip\_dscp\_tagging)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**reverse\_also**  <br>*optional*|[reverse\_also](#reverse\_also)|
|**reverse\_tracking\_ip\_address**  <br>*optional*|[reverse\_tracking\_ip\_address](#reverse\_tracking\_ip\_address)|
|**silence\_period**  <br>*optional*|[silence\_period](#silence\_period)|
|**static\_path**  <br>*optional*|[static\_path](#static\_path)|
|**to\_site\_name**  <br>*optional*|[to\_site\_name](#to\_site\_name)|
|**to\_wan\_link\_name**  <br>*optional*|[to\_wan\_link\_name](#to\_wan\_link\_name)|
|**tracking\_ip\_address**  <br>*optional*|[tracking\_ip\_address](#tracking\_ip\_address)|
|**virtual\_path\_name**  <br>*optional*|[virtual\_path\_name](#virtual\_path\_name)|


<a name="reverse\_also"></a>
### reverse\_also
Add reverse path configuration also

*Type* : boolean


<a name="reverse\_tracking\_ip\_address"></a>
### reverse\_tracking\_ip\_address
If Reverse Also is enabled, a virtual IP address on the Path that can be pinged to determine the state of the reverse Path

*Type* : string


<a name="silence\_period"></a>
### silence\_period
Specify silence duration before Path state transitions from GOOD to BAD. When not specified, the default is 150ms

*Type* : enum (500, 750, 1000, 10000, 20000, 30000, 40000, 50000, 60000)


<a name="static\_path"></a>
### static\_path
Convert Path, and all other Paths associated by WAN Link, Generated by an Autopath Group, to a Static Path. This action cannot be undone

*Type* : boolean


<a name="to\_site\_name"></a>
### to\_site\_name
Destination site for the new path

*Type* : string


<a name="to\_wan\_link\_name"></a>
### to\_wan\_link\_name
Destination WAN Link for the new path

*Type* : string


<a name="tracking\_ip\_address"></a>
### tracking\_ip\_address
A virtual IP address on the Path that can be pinged to determine the state of the Path

*Type* : string


<a name="virtual\_path\_name"></a>
### virtual\_path\_name
Name of virtual path to which the path belongs

*Type* : string






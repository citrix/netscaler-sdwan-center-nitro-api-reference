# provisioning\_groups


<a name="overview"></a>
## Overview
API to get, modify, add and delete Provisioning Groups. A Provisioning Group is a container for an arbitrary collection of Services on any given WAN Link. They allow the user to allocate bandwidth at a high-level before drilling down to the individual Services within the Group for fine-tuning. They also provide a boundary for the automatic redistribution of bandwidth within the child Services of the Provisioning Group.


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* provisioning\_groups : Operations related to provisioning\_groups 




<a name="paths"></a>
## Paths

<a name="provisioning\_groups-post"></a>
### POST operation for provisioning\_groups
```
POST /provisioning_groups
```


#### Description
Use this operation to add a new provisioning group for a particular wan link.


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[provisioning\_groups\_request\_schema](#provisioning\_groups\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[provisioning\_groups\_post\_success\_schema](#provisioning\_groups\_post\_success\_schema)|
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

* provisioning\_groups


<a name="provisioning\_groups-get"></a>
### Get operation for provisioning\_groups
```
GET /provisioning_groups
```


#### Description
Use this operation to get the provisioning groups for each of the wan links.


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[provisioning\_groups\_response\_schema](#provisioning\_groups\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* provisioning\_groups


<a name="provisioning\_groups-put"></a>
### PUT operation for provisioning\_groups
```
PUT /provisioning_groups
```


#### Description
Use this operation to modify the fair shares of the provisioning group or rename the group.


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[provisioning\_groups\_put\_success\_schema](#provisioning\_groups\_put\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* provisioning\_groups


<a name="provisioning\_groups-deletepathparam-delete"></a>
### DELETE operation for provisioning\_groups
```
DELETE /provisioning_groups/{deletePathParam}
```


#### Description
Use this operation to delete a provisioning group. The 'Default' group may not be deleted.


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[provisioning\_groups\_delete\_success\_schema](#provisioning\_groups\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* provisioning\_groups




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
Auto-generated ID to uniquely identify the provisioning group.

*Type* : integer


<a name="lan\_to\_wan\_fair\_bitrate"></a>
### lan\_to\_wan\_fair\_bitrate
The fair bit rate available to Services assigned to the Group, based on its Fair Shares out of all Groups (LAN to WAN direction). Includes the Min rate.

*Type* : integer


<a name="lan\_to\_wan\_minimum\_bitrate"></a>
### lan\_to\_wan\_minimum\_bitrate
The sum of the Min rates of all Services assigned to the Group in LAN to WAN direction.

*Type* : integer


<a name="lan\_to\_wan\_rate\_fair\_share"></a>
### lan\_to\_wan\_rate\_fair\_share
The number of Fair Shares the Group should take out of the eligible bandwidth in LAN to WAN direction.

*Type* : integer


<a name="package\_name"></a>
### package\_name
Config package name using which the site API operation should be performed.

*Type* : string


<a name="provisioning\_group\_name"></a>
### provisioning\_group\_name
The name of the Group. The 'Default' group may not be renamed.

*Type* : string


<a name="provisioning\_groups"></a>
### provisioning\_groups

|Name|Schema|
|---|---|
|**id**  <br>*optional*|[id](#id)|
|**lan\_to\_wan\_rate\_fair\_share**  <br>*optional*|[lan\_to\_wan\_rate\_fair\_share](#lan\_to\_wan\_rate\_fair\_share)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**provisioning\_group\_name**  <br>*optional*|[provisioning\_group\_name](#provisioning\_group\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**wan\_link\_name**  <br>*optional*|[wan\_link\_name](#wan\_link\_name)|
|**wan\_to\_lan\_rate\_fair\_share**  <br>*optional*|[wan\_to\_lan\_rate\_fair\_share](#wan\_to\_lan\_rate\_fair\_share)|


<a name="provisioning\_groups\_delete\_success\_schema"></a>
### provisioning\_groups\_delete\_success\_schema

|Name|Schema|
|---|---|
|**provisioning\_groups**  <br>*optional*|[provisioning\_groups](#provisioning\_groups\_delete\_success\_schema-provisioning\_groups)|

<a name="provisioning\_groups\_delete\_success\_schema-provisioning\_groups"></a>
**provisioning\_groups**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="provisioning\_groups\_post\_success\_schema"></a>
### provisioning\_groups\_post\_success\_schema

|Name|Schema|
|---|---|
|**provisioning\_groups**  <br>*optional*|[provisioning\_groups](#provisioning\_groups\_post\_success\_schema-provisioning\_groups)|

<a name="provisioning\_groups\_post\_success\_schema-provisioning\_groups"></a>
**provisioning\_groups**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="provisioning\_groups\_put\_success\_schema"></a>
### provisioning\_groups\_put\_success\_schema

|Name|Schema|
|---|---|
|**provisioning\_groups**  <br>*optional*|[provisioning\_groups](#provisioning\_groups\_put\_success\_schema-provisioning\_groups)|

<a name="provisioning\_groups\_put\_success\_schema-provisioning\_groups"></a>
**provisioning\_groups**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="provisioning\_groups\_request\_schema"></a>
### provisioning\_groups\_request\_schema

|Name|Schema|
|---|---|
|**provisioning\_groups**  <br>*optional*|[provisioning\_groups](#provisioning\_groups)|


<a name="provisioning\_groups\_response\_schema"></a>
### provisioning\_groups\_response\_schema
*Type* : < [provisioning\_groups\_response\_schema](#provisioning\_groups\_response\_schema-inline) > array

<a name="provisioning\_groups\_response\_schema-inline"></a>
**provisioning\_groups\_response\_schema**

|Name|Schema|
|---|---|
|**id**  <br>*optional*|[id](#id)|
|**lan\_to\_wan\_fair\_bitrate**  <br>*optional*|[lan\_to\_wan\_fair\_bitrate](#lan\_to\_wan\_fair\_bitrate)|
|**lan\_to\_wan\_minimum\_bitrate**  <br>*optional*|[lan\_to\_wan\_minimum\_bitrate](#lan\_to\_wan\_minimum\_bitrate)|
|**lan\_to\_wan\_rate\_fair\_share**  <br>*optional*|[lan\_to\_wan\_rate\_fair\_share](#lan\_to\_wan\_rate\_fair\_share)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**provisioning\_group\_name**  <br>*optional*|[provisioning\_group\_name](#provisioning\_group\_name)|
|**service\_count**  <br>*optional*|[service\_count](#service\_count)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**wan\_link\_name**  <br>*optional*|[wan\_link\_name](#wan\_link\_name)|
|**wan\_to\_lan\_fair\_bitrate**  <br>*optional*|[wan\_to\_lan\_fair\_bitrate](#wan\_to\_lan\_fair\_bitrate)|
|**wan\_to\_lan\_minimum\_bitrate**  <br>*optional*|[wan\_to\_lan\_minimum\_bitrate](#wan\_to\_lan\_minimum\_bitrate)|
|**wan\_to\_lan\_rate\_fair\_share**  <br>*optional*|[wan\_to\_lan\_rate\_fair\_share](#wan\_to\_lan\_rate\_fair\_share)|


<a name="service\_count"></a>
### service\_count
The number of Services assigned to the group.

*Type* : integer


<a name="site\_name"></a>
### site\_name
Site Name

*Type* : string


<a name="wan\_link\_name"></a>
### wan\_link\_name
The WAN Link name

*Type* : string


<a name="wan\_to\_lan\_fair\_bitrate"></a>
### wan\_to\_lan\_fair\_bitrate
The fair bit rate available to Services assigned to the Group, based on its Fair Shares out of all Groups (WAN to LAN direction). Includes the Min rate.

*Type* : integer


<a name="wan\_to\_lan\_minimum\_bitrate"></a>
### wan\_to\_lan\_minimum\_bitrate
The sum of the Min rates of all Services assigned to the Group in WAN to LAN direction.

*Type* : integer


<a name="wan\_to\_lan\_rate\_fair\_share"></a>
### wan\_to\_lan\_rate\_fair\_share
The number of Fair Shares the Group should take out of the eligible bandwidth in WAN to LAN direction.

*Type* : integer






# virtual\_path\_wan\_links


<a name="overview"></a>
## Overview
API to get, modify wan links for Virtual Paths


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* virtual\_path\_wan\_links : Operations related to virtual\_path\_wan\_links 




<a name="paths"></a>
## Paths

<a name="virtual\_path\_wan\_links-post"></a>
### POST operation for virtual\_path\_wan\_links
```
POST /virtual_path_wan_links
```


#### Description
Use this operation to enable the Virtual Path service to use a particular wan link


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[virtual\_path\_wan\_links\_post\_success\_schema](#virtual\_path\_wan\_links\_post\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* virtual\_path\_wan\_links


<a name="virtual\_path\_wan\_links-get"></a>
### Get operation for virtual\_path\_wan\_links
```
GET /virtual_path_wan_links
```


#### Description
Use this operation to get the wan links for Virtual Paths. Only enabled wan links are listed


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[virtual\_path\_wan\_links\_response\_schema](#virtual\_path\_wan\_links\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* virtual\_path\_wan\_links


<a name="virtual\_path\_wan\_links-put"></a>
### PUT operation for virtual\_path\_wan\_links
```
PUT /virtual_path_wan_links
```


#### Description
Use this operation to modify wan links for a Virtual Path. This operation can only be used when the wan link is enabled for Virtual Path


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[virtual\_path\_wan\_links\_request\_schema](#virtual\_path\_wan\_links\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[virtual\_path\_wan\_links\_put\_success\_schema](#virtual\_path\_wan\_links\_put\_success\_schema)|
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

* virtual\_path\_wan\_links


<a name="virtual\_path\_wan\_links-deletepathparam-delete"></a>
### DELETE operation for virtual\_path\_wan\_links
```
DELETE /virtual_path_wan_links/{deletePathParam}
```


#### Description
Use this operation to disable the Virtual Path service to use a particular wan link


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[virtual\_path\_wan\_links\_delete\_success\_schema](#virtual\_path\_wan\_links\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* virtual\_path\_wan\_links




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="active\_mtu\_detect"></a>
### active\_mtu\_detect
If enabled, all LAN to WAN Paths for the Virtual Path Service will be actively probed for MTU

*Type* : boolean


<a name="autopath\_group"></a>
### autopath\_group
The group used to determine what paths may be automatically generated between this WAN Link and remote WAN Links and what default path settings to use. Use none for setting to None or Default for the Default value

*Type* : string


<a name="enable\_udp\_port\_switching"></a>
### enable\_udp\_port\_switching
If enabled, the WAN Link will alternate its UDP port at the specified interval

*Type* : boolean


<a name="id"></a>
### id
Auto-generated ID to uniquely identify the WAN Link

*Type* : integer


<a name="package\_name"></a>
### package\_name
Config package name using which the site API operation should be performed.

*Type* : string


<a name="site\_name"></a>
### site\_name
Site Name

*Type* : string


<a name="tunnel\_header\_size"></a>
### tunnel\_header\_size
The size, in bytes, of the tunnel header, if applicable

*Type* : integer


<a name="udp\_port"></a>
### udp\_port
The specified port will be used for LAN to WAN packets and required for WAN to LAN packets

*Type* : integer


<a name="udp\_port\_switching\_alt\_port"></a>
### udp\_port\_switching\_alt\_port
The alternate UDP port to be used when UDP Port Switching is enabled and active

*Type* : integer


<a name="udp\_port\_switching\_interval"></a>
### udp\_port\_switching\_interval
The interval, in minutes, that the WAN Link will alternate its UDP port

*Type* : integer


<a name="virtual\_path\_name"></a>
### virtual\_path\_name
Virtual Path name to which the rule belongs

*Type* : string


<a name="virtual\_path\_wan\_links"></a>
### virtual\_path\_wan\_links

|Name|Schema|
|---|---|
|**active\_mtu\_detect**  <br>*optional*|[active\_mtu\_detect](#active\_mtu\_detect)|
|**autopath\_group**  <br>*optional*|[autopath\_group](#autopath\_group)|
|**enable\_udp\_port\_switching**  <br>*optional*|[enable\_udp\_port\_switching](#enable\_udp\_port\_switching)|
|**id**  <br>*optional*|[id](#id)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**tunnel\_header\_size**  <br>*optional*|[tunnel\_header\_size](#tunnel\_header\_size)|
|**udp\_port**  <br>*optional*|[udp\_port](#udp\_port)|
|**udp\_port\_switching\_alt\_port**  <br>*optional*|[udp\_port\_switching\_alt\_port](#udp\_port\_switching\_alt\_port)|
|**udp\_port\_switching\_interval**  <br>*optional*|[udp\_port\_switching\_interval](#udp\_port\_switching\_interval)|
|**virtual\_path\_name**  <br>*optional*|[virtual\_path\_name](#virtual\_path\_name)|
|**wan\_link\_name**  <br>*optional*|[wan\_link\_name](#wan\_link\_name)|


<a name="virtual\_path\_wan\_links\_delete\_success\_schema"></a>
### virtual\_path\_wan\_links\_delete\_success\_schema

|Name|Schema|
|---|---|
|**virtual\_path\_wan\_links**  <br>*optional*|[virtual\_path\_wan\_links](#virtual\_path\_wan\_links\_delete\_success\_schema-virtual\_path\_wan\_links)|

<a name="virtual\_path\_wan\_links\_delete\_success\_schema-virtual\_path\_wan\_links"></a>
**virtual\_path\_wan\_links**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="virtual\_path\_wan\_links\_post\_success\_schema"></a>
### virtual\_path\_wan\_links\_post\_success\_schema

|Name|Schema|
|---|---|
|**virtual\_path\_wan\_links**  <br>*optional*|[virtual\_path\_wan\_links](#virtual\_path\_wan\_links\_post\_success\_schema-virtual\_path\_wan\_links)|

<a name="virtual\_path\_wan\_links\_post\_success\_schema-virtual\_path\_wan\_links"></a>
**virtual\_path\_wan\_links**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="virtual\_path\_wan\_links\_put\_success\_schema"></a>
### virtual\_path\_wan\_links\_put\_success\_schema

|Name|Schema|
|---|---|
|**virtual\_path\_wan\_links**  <br>*optional*|[virtual\_path\_wan\_links](#virtual\_path\_wan\_links\_put\_success\_schema-virtual\_path\_wan\_links)|

<a name="virtual\_path\_wan\_links\_put\_success\_schema-virtual\_path\_wan\_links"></a>
**virtual\_path\_wan\_links**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="virtual\_path\_wan\_links\_request\_schema"></a>
### virtual\_path\_wan\_links\_request\_schema

|Name|Schema|
|---|---|
|**virtual\_path\_wan\_links**  <br>*optional*|[virtual\_path\_wan\_links](#virtual\_path\_wan\_links)|


<a name="virtual\_path\_wan\_links\_response\_schema"></a>
### virtual\_path\_wan\_links\_response\_schema
*Type* : < [virtual\_path\_wan\_links\_response\_schema](#virtual\_path\_wan\_links\_response\_schema-inline) > array

<a name="virtual\_path\_wan\_links\_response\_schema-inline"></a>
**virtual\_path\_wan\_links\_response\_schema**

|Name|Schema|
|---|---|
|**active\_mtu\_detect**  <br>*optional*|[active\_mtu\_detect](#active\_mtu\_detect)|
|**autopath\_group**  <br>*optional*|[autopath\_group](#autopath\_group)|
|**enable\_udp\_port\_switching**  <br>*optional*|[enable\_udp\_port\_switching](#enable\_udp\_port\_switching)|
|**id**  <br>*optional*|[id](#id)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**tunnel\_header\_size**  <br>*optional*|[tunnel\_header\_size](#tunnel\_header\_size)|
|**udp\_port**  <br>*optional*|[udp\_port](#udp\_port)|
|**udp\_port\_switching\_alt\_port**  <br>*optional*|[udp\_port\_switching\_alt\_port](#udp\_port\_switching\_alt\_port)|
|**udp\_port\_switching\_interval**  <br>*optional*|[udp\_port\_switching\_interval](#udp\_port\_switching\_interval)|
|**virtual\_path\_name**  <br>*optional*|[virtual\_path\_name](#virtual\_path\_name)|
|**wan\_link\_name**  <br>*optional*|[wan\_link\_name](#wan\_link\_name)|


<a name="wan\_link\_name"></a>
### wan\_link\_name
The WAN Link name

*Type* : string






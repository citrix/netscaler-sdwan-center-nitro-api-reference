# wan\_to\_wan\_forwarding


<a name="overview"></a>
## Overview
API to get, modify WAN to WAN Forwarding Settings.


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* wan\_to\_wan\_forwarding : Operations related to wan\_to\_wan\_forwarding 




<a name="paths"></a>
## Paths

<a name="wan\_to\_wan\_forwarding-get"></a>
### Get operation for wan\_to\_wan\_forwarding
```
GET /wan_to_wan_forwarding
```


#### Description
Use this operation to get the current values WAN to WAN Forwarding settings


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[wan\_to\_wan\_forwarding\_response\_schema](#wan\_to\_wan\_forwarding\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* wan\_to\_wan\_forwarding


<a name="wan\_to\_wan\_forwarding-put"></a>
### PUT operation for wan\_to\_wan\_forwarding
```
PUT /wan_to_wan_forwarding
```


#### Description
Use this operation to modify the current values of WAN to WAN Forwarding settings


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[wan\_to\_wan\_forwarding\_request\_schema](#wan\_to\_wan\_forwarding\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[wan\_to\_wan\_forwarding\_put\_success\_schema](#wan\_to\_wan\_forwarding\_put\_success\_schema)|
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

* wan\_to\_wan\_forwarding




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="enable\_site\_as\_intermediate\_node"></a>
### enable\_site\_as\_intermediate\_node
Set to true to enable site as an intermediate node. If enabled, this Site may serve as a mediator for the creation and destruction of Dynamic Virtual Paths between two or more Sites connected to this Site.

*Type* : boolean


<a name="enable\_virtual\_path\_to\_internet\_or\_intranet\_forwarding"></a>
### enable\_virtual\_path\_to\_internet\_or\_intranet\_forwarding
Set to true to enable virtual path to Internet/Intranet forwarding. Allows this Site to serve as a proxy for multi-hop Internet or Intranet traffic between adjacent Sites. Unlike WAN-to-WAN forwarding, enabling this option will not export internet/intranet routes to other sites.

*Type* : boolean


<a name="enable\_virtual\_path\_to\_virtual\_path\_forwarding"></a>
### enable\_virtual\_path\_to\_virtual\_path\_forwarding
Set to true to enable virtual path to virtual path forwarding. Allows this Site to serve as a proxy for multi-hop Site-to-Site traffic between adjacent Sites. Unlike WAN-to-WAN forwarding, enabling this option will not export routes from site to site.

*Type* : boolean


<a name="enable\_wan\_to\_wan\_forwarding"></a>
### enable\_wan\_to\_wan\_forwarding
Set to true to enable wan to wan forwarding. Allows this Site to serve as a proxy for multi-hop Site-to-Site, Internet or Intranet traffic between adjacent Sites. Exports Local, Intranet, Internet and learned local routes to members of the WAN to WAN forwarding group.

*Type* : boolean


<a name="package\_name"></a>
### package\_name
Config package name using which the API operation should be performed.

*Type* : string


<a name="site\_name"></a>
### site\_name
Site Name

*Type* : string


<a name="wan\_to\_wan\_forwarding"></a>
### wan\_to\_wan\_forwarding

|Name|Schema|
|---|---|
|**enable\_site\_as\_intermediate\_node**  <br>*optional*|[enable\_site\_as\_intermediate\_node](#enable\_site\_as\_intermediate\_node)|
|**enable\_virtual\_path\_to\_internet\_or\_intranet\_forwarding**  <br>*optional*|[enable\_virtual\_path\_to\_internet\_or\_intranet\_forwarding](#enable\_virtual\_path\_to\_internet\_or\_intranet\_forwarding)|
|**enable\_virtual\_path\_to\_virtual\_path\_forwarding**  <br>*optional*|[enable\_virtual\_path\_to\_virtual\_path\_forwarding](#enable\_virtual\_path\_to\_virtual\_path\_forwarding)|
|**enable\_wan\_to\_wan\_forwarding**  <br>*optional*|[enable\_wan\_to\_wan\_forwarding](#enable\_wan\_to\_wan\_forwarding)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**wan\_to\_wan\_forwarding\_group**  <br>*optional*|[wan\_to\_wan\_forwarding\_group](#wan\_to\_wan\_forwarding\_group)|


<a name="wan\_to\_wan\_forwarding\_delete\_success\_schema"></a>
### wan\_to\_wan\_forwarding\_delete\_success\_schema

|Name|Schema|
|---|---|
|**wan\_to\_wan\_forwarding**  <br>*optional*|[wan\_to\_wan\_forwarding](#wan\_to\_wan\_forwarding\_delete\_success\_schema-wan\_to\_wan\_forwarding)|

<a name="wan\_to\_wan\_forwarding\_delete\_success\_schema-wan\_to\_wan\_forwarding"></a>
**wan\_to\_wan\_forwarding**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="wan\_to\_wan\_forwarding\_group"></a>
### wan\_to\_wan\_forwarding\_group
The WAN-to-WAN Forwarding Group used to determine which remote Sites can be used with this Site in WAN-to-WAN forwarding and Dynamic Virtual Paths

*Type* : string


<a name="wan\_to\_wan\_forwarding\_post\_success\_schema"></a>
### wan\_to\_wan\_forwarding\_post\_success\_schema

|Name|Schema|
|---|---|
|**wan\_to\_wan\_forwarding**  <br>*optional*|[wan\_to\_wan\_forwarding](#wan\_to\_wan\_forwarding\_post\_success\_schema-wan\_to\_wan\_forwarding)|

<a name="wan\_to\_wan\_forwarding\_post\_success\_schema-wan\_to\_wan\_forwarding"></a>
**wan\_to\_wan\_forwarding**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="wan\_to\_wan\_forwarding\_put\_success\_schema"></a>
### wan\_to\_wan\_forwarding\_put\_success\_schema

|Name|Schema|
|---|---|
|**wan\_to\_wan\_forwarding**  <br>*optional*|[wan\_to\_wan\_forwarding](#wan\_to\_wan\_forwarding\_put\_success\_schema-wan\_to\_wan\_forwarding)|

<a name="wan\_to\_wan\_forwarding\_put\_success\_schema-wan\_to\_wan\_forwarding"></a>
**wan\_to\_wan\_forwarding**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="wan\_to\_wan\_forwarding\_request\_schema"></a>
### wan\_to\_wan\_forwarding\_request\_schema

|Name|Schema|
|---|---|
|**wan\_to\_wan\_forwarding**  <br>*optional*|[wan\_to\_wan\_forwarding](#wan\_to\_wan\_forwarding)|


<a name="wan\_to\_wan\_forwarding\_response\_schema"></a>
### wan\_to\_wan\_forwarding\_response\_schema
*Type* : < [wan\_to\_wan\_forwarding\_response\_schema](#wan\_to\_wan\_forwarding\_response\_schema-inline) > array

<a name="wan\_to\_wan\_forwarding\_response\_schema-inline"></a>
**wan\_to\_wan\_forwarding\_response\_schema**

|Name|Schema|
|---|---|
|**enable\_site\_as\_intermediate\_node**  <br>*optional*|[enable\_site\_as\_intermediate\_node](#enable\_site\_as\_intermediate\_node)|
|**enable\_virtual\_path\_to\_internet\_or\_intranet\_forwarding**  <br>*optional*|[enable\_virtual\_path\_to\_internet\_or\_intranet\_forwarding](#enable\_virtual\_path\_to\_internet\_or\_intranet\_forwarding)|
|**enable\_virtual\_path\_to\_virtual\_path\_forwarding**  <br>*optional*|[enable\_virtual\_path\_to\_virtual\_path\_forwarding](#enable\_virtual\_path\_to\_virtual\_path\_forwarding)|
|**enable\_wan\_to\_wan\_forwarding**  <br>*optional*|[enable\_wan\_to\_wan\_forwarding](#enable\_wan\_to\_wan\_forwarding)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**wan\_to\_wan\_forwarding\_group**  <br>*optional*|[wan\_to\_wan\_forwarding\_group](#wan\_to\_wan\_forwarding\_group)|






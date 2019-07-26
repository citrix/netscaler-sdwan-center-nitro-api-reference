# saas\_gateway\_service


<a name="overview"></a>
## Overview
API to add, delete, get, modify saas gateway service objects


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* saas\_gateway\_service : Operations related to saas\_gateway\_service 




<a name="paths"></a>
## Paths

<a name="saas\_gateway\_service-post"></a>
### POST operation for saas\_gateway\_service
```
POST /saas_gateway_service
```


#### Description
Use this operation to add saas gateway service objects


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[saas\_gateway\_service\_request\_schema](#saas\_gateway\_service\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[saas\_gateway\_service\_post\_success\_schema](#saas\_gateway\_service\_post\_success\_schema)|
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

* saas\_gateway\_service


<a name="saas\_gateway\_service-get"></a>
### Get operation for saas\_gateway\_service
```
GET /saas_gateway_service
```


#### Description
Use this operation to get the saas gateway service objects


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[saas\_gateway\_service\_response\_schema](#saas\_gateway\_service\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* saas\_gateway\_service


<a name="saas\_gateway\_service-put"></a>
### PUT operation for saas\_gateway\_service
```
PUT /saas_gateway_service
```


#### Description
Use this operation to modify saas gateway service objects


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[saas\_gateway\_service\_put\_success\_schema](#saas\_gateway\_service\_put\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* saas\_gateway\_service


<a name="saas\_gateway\_service-deletepathparam-delete"></a>
### DELETE operation for saas\_gateway\_service
```
DELETE /saas_gateway_service/{deletePathParam}
```


#### Description
Use this operation to delete saas gateway service objects


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[saas\_gateway\_service\_delete\_success\_schema](#saas\_gateway\_service\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* saas\_gateway\_service




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="external\_nat"></a>
### external\_nat
If enabled, the nat rule is configured externally outside SD WAN appliance

*Type* : boolean


<a name="id"></a>
### id
Auto-generated ID to uniquely identify saas gateway service object

*Type* : integer


<a name="lan\_object\_ip"></a>
### lan\_object\_ip
LAN Object IP Address with a prefix

*Type* : string


<a name="package\_name"></a>
### package\_name
Config package name using which the API operation should be performed.

*Type* : string


<a name="primary\_pop"></a>
### primary\_pop
The code for the primary pop

*Type* : string


<a name="saas\_gateway\_application\_object"></a>
### saas\_gateway\_application\_object
Saas gateway application object

*Type* : < [saas\_gateway\_application\_object](#saas\_gateway\_application\_object-inline) > array

<a name="saas\_gateway\_application\_object-inline"></a>
**saas\_gateway\_application\_object**

|Name|Description|Schema|
|---|---|---|
|**application\_match\_name**  <br>*optional*|application Match Name. (A valid application object name or <All>)|string|
|**id**  <br>*optional*|Auto-generated ID to uniquely identify the saas gateway service application object|integer|


<a name="saas\_gateway\_service"></a>
### saas\_gateway\_service

|Name|Schema|
|---|---|
|**external\_nat**  <br>*optional*|[external\_nat](#external\_nat)|
|**id**  <br>*optional*|[id](#id)|
|**lan\_object\_ip**  <br>*optional*|[lan\_object\_ip](#lan\_object\_ip)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**primary\_pop**  <br>*optional*|[primary\_pop](#primary\_pop)|
|**saas\_gateway\_application\_object**  <br>*optional*|[saas\_gateway\_application\_object](#saas\_gateway\_application\_object)|
|**saas\_gateway\_wan\_link\_usage**  <br>*optional*|[saas\_gateway\_wan\_link\_usage](#saas\_gateway\_wan\_link\_usage)|
|**saas\_service\_id**  <br>*optional*|[saas\_service\_id](#saas\_service\_id)|
|**saas\_service\_state**  <br>*optional*|[saas\_service\_state](#saas\_service\_state)|
|**secondary\_pop**  <br>*optional*|[secondary\_pop](#secondary\_pop)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**subscription\_bandwidth**  <br>*optional*|[subscription\_bandwidth](#subscription\_bandwidth)|


<a name="saas\_gateway\_service\_delete\_success\_schema"></a>
### saas\_gateway\_service\_delete\_success\_schema

|Name|Schema|
|---|---|
|**saas\_gateway\_service**  <br>*optional*|[saas\_gateway\_service](#saas\_gateway\_service\_delete\_success\_schema-saas\_gateway\_service)|

<a name="saas\_gateway\_service\_delete\_success\_schema-saas\_gateway\_service"></a>
**saas\_gateway\_service**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="saas\_gateway\_service\_post\_success\_schema"></a>
### saas\_gateway\_service\_post\_success\_schema

|Name|Schema|
|---|---|
|**saas\_gateway\_service**  <br>*optional*|[saas\_gateway\_service](#saas\_gateway\_service\_post\_success\_schema-saas\_gateway\_service)|

<a name="saas\_gateway\_service\_post\_success\_schema-saas\_gateway\_service"></a>
**saas\_gateway\_service**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="saas\_gateway\_service\_put\_success\_schema"></a>
### saas\_gateway\_service\_put\_success\_schema

|Name|Schema|
|---|---|
|**saas\_gateway\_service**  <br>*optional*|[saas\_gateway\_service](#saas\_gateway\_service\_put\_success\_schema-saas\_gateway\_service)|

<a name="saas\_gateway\_service\_put\_success\_schema-saas\_gateway\_service"></a>
**saas\_gateway\_service**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="saas\_gateway\_service\_request\_schema"></a>
### saas\_gateway\_service\_request\_schema

|Name|Schema|
|---|---|
|**saas\_gateway\_service**  <br>*optional*|[saas\_gateway\_service](#saas\_gateway\_service)|


<a name="saas\_gateway\_service\_response\_schema"></a>
### saas\_gateway\_service\_response\_schema
*Type* : < [saas\_gateway\_service\_response\_schema](#saas\_gateway\_service\_response\_schema-inline) > array

<a name="saas\_gateway\_service\_response\_schema-inline"></a>
**saas\_gateway\_service\_response\_schema**

|Name|Schema|
|---|---|
|**external\_nat**  <br>*optional*|[external\_nat](#external\_nat)|
|**id**  <br>*optional*|[id](#id)|
|**lan\_object\_ip**  <br>*optional*|[lan\_object\_ip](#lan\_object\_ip)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**primary\_pop**  <br>*optional*|[primary\_pop](#primary\_pop)|
|**saas\_gateway\_application\_object**  <br>*optional*|[saas\_gateway\_application\_object](#saas\_gateway\_application\_object)|
|**saas\_gateway\_wan\_link\_usage**  <br>*optional*|[saas\_gateway\_wan\_link\_usage](#saas\_gateway\_wan\_link\_usage)|
|**saas\_service\_id**  <br>*optional*|[saas\_service\_id](#saas\_service\_id)|
|**saas\_service\_state**  <br>*optional*|[saas\_service\_state](#saas\_service\_state)|
|**secondary\_pop**  <br>*optional*|[secondary\_pop](#secondary\_pop)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**subscription\_bandwidth**  <br>*optional*|[subscription\_bandwidth](#subscription\_bandwidth)|


<a name="saas\_gateway\_wan\_link\_usage"></a>
### saas\_gateway\_wan\_link\_usage
Saas Gateway Servic WAN Link usage

*Type* : < [saas\_gateway\_wan\_link\_usage](#saas\_gateway\_wan\_link\_usage-inline) > array

<a name="saas\_gateway\_wan\_link\_usage-inline"></a>
**saas\_gateway\_wan\_link\_usage**

|Name|Description|Schema|
|---|---|---|
|**id**  <br>*optional*|Auto-generated ID to uniquely identify the saas wan link usage|integer|
|**lan\_to\_wan\_reserved\_bandwidth\_kbps**  <br>*optional*|Reserved Bandwidth in the LAN to WAN direction|integer|
|**wan\_link\_index**  <br>*optional*|WAN link index used for WAN Link Saas Tap interface mapping|integer|
|**wan\_link\_name**  <br>*optional*|WAN Link Name|string|
|**wan\_link\_type**  <br>*optional*|WAN Link Type|string|
|**wan\_to\_lan\_reserved\_bandwidth\_kbps**  <br>*optional*|Reserved Bandwidth in the WAN to LAN direction|integer|


<a name="saas\_service\_id"></a>
### saas\_service\_id
Saas Service Side id.

*Type* : integer


<a name="saas\_service\_state"></a>
### saas\_service\_state
Saas Service State.

*Type* : string


<a name="secondary\_pop"></a>
### secondary\_pop
The code for the secondary pop

*Type* : string


<a name="site\_name"></a>
### site\_name
Site Name

*Type* : string


<a name="subscription\_bandwidth"></a>
### subscription\_bandwidth
The subscribed service bandwidth for the site

*Type* : integer






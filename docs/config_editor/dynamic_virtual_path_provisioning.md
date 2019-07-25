# dynamic\_virtual\_path\_provisioning


<a name="overview"></a>
## Overview
API to get and modify the provisioning parameters of an individual dynamic virtual path enabled on a particular wan link.


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* dynamic\_virtual\_path\_provisioning : Operations related to dynamic\_virtual\_path\_provisioning 




<a name="paths"></a>
## Paths

<a name="dynamic\_virtual\_path\_provisioning-get"></a>
### Get operation for dynamic\_virtual\_path\_provisioning
```
GET /dynamic_virtual_path_provisioning
```


#### Description
Use this operation to get the provisioning parameters of an individual dynamic virtual path enabled on a particular wan link.


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[dynamic\_virtual\_path\_provisioning\_response\_schema](#dynamic\_virtual\_path\_provisioning\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* dynamic\_virtual\_path\_provisioning


<a name="dynamic\_virtual\_path\_provisioning-put"></a>
### PUT operation for dynamic\_virtual\_path\_provisioning
```
PUT /dynamic_virtual_path_provisioning
```


#### Description
Use this operation to modify the the provisioning parameters of an individual dynamic virtual path enabled on a particular wan link.


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[dynamic\_virtual\_path\_provisioning\_request\_schema](#dynamic\_virtual\_path\_provisioning\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[dynamic\_virtual\_path\_provisioning\_put\_success\_schema](#dynamic\_virtual\_path\_provisioning\_put\_success\_schema)|
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

* dynamic\_virtual\_path\_provisioning




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="dynamic\_virtual\_path\_provisioning"></a>
### dynamic\_virtual\_path\_provisioning

|Name|Schema|
|---|---|
|**id**  <br>*optional*|[id](#id)|
|**lan\_to\_wan\_maximum\_allowed\_bitrate**  <br>*optional*|[lan\_to\_wan\_maximum\_allowed\_bitrate](#lan\_to\_wan\_maximum\_allowed\_bitrate)|
|**lan\_to\_wan\_minimum\_reserved\_bitrate**  <br>*optional*|[lan\_to\_wan\_minimum\_reserved\_bitrate](#lan\_to\_wan\_minimum\_reserved\_bitrate)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**wan\_to\_lan\_maximum\_allowed\_bitrate**  <br>*optional*|[wan\_to\_lan\_maximum\_allowed\_bitrate](#wan\_to\_lan\_maximum\_allowed\_bitrate)|
|**wan\_to\_lan\_minimum\_reserved\_bitrate**  <br>*optional*|[wan\_to\_lan\_minimum\_reserved\_bitrate](#wan\_to\_lan\_minimum\_reserved\_bitrate)|


<a name="dynamic\_virtual\_path\_provisioning\_delete\_success\_schema"></a>
### dynamic\_virtual\_path\_provisioning\_delete\_success\_schema

|Name|Schema|
|---|---|
|**dynamic\_virtual\_path\_provisioning**  <br>*optional*|[dynamic\_virtual\_path\_provisioning](#dynamic\_virtual\_path\_provisioning\_delete\_success\_schema-dynamic\_virtual\_path\_provisioning)|

<a name="dynamic\_virtual\_path\_provisioning\_delete\_success\_schema-dynamic\_virtual\_path\_provisioning"></a>
**dynamic\_virtual\_path\_provisioning**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="dynamic\_virtual\_path\_provisioning\_post\_success\_schema"></a>
### dynamic\_virtual\_path\_provisioning\_post\_success\_schema

|Name|Schema|
|---|---|
|**dynamic\_virtual\_path\_provisioning**  <br>*optional*|[dynamic\_virtual\_path\_provisioning](#dynamic\_virtual\_path\_provisioning\_post\_success\_schema-dynamic\_virtual\_path\_provisioning)|

<a name="dynamic\_virtual\_path\_provisioning\_post\_success\_schema-dynamic\_virtual\_path\_provisioning"></a>
**dynamic\_virtual\_path\_provisioning**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="dynamic\_virtual\_path\_provisioning\_put\_success\_schema"></a>
### dynamic\_virtual\_path\_provisioning\_put\_success\_schema

|Name|Schema|
|---|---|
|**dynamic\_virtual\_path\_provisioning**  <br>*optional*|[dynamic\_virtual\_path\_provisioning](#dynamic\_virtual\_path\_provisioning\_put\_success\_schema-dynamic\_virtual\_path\_provisioning)|

<a name="dynamic\_virtual\_path\_provisioning\_put\_success\_schema-dynamic\_virtual\_path\_provisioning"></a>
**dynamic\_virtual\_path\_provisioning**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="dynamic\_virtual\_path\_provisioning\_request\_schema"></a>
### dynamic\_virtual\_path\_provisioning\_request\_schema

|Name|Schema|
|---|---|
|**dynamic\_virtual\_path\_provisioning**  <br>*optional*|[dynamic\_virtual\_path\_provisioning](#dynamic\_virtual\_path\_provisioning)|


<a name="dynamic\_virtual\_path\_provisioning\_response\_schema"></a>
### dynamic\_virtual\_path\_provisioning\_response\_schema
*Type* : < [dynamic\_virtual\_path\_provisioning\_response\_schema](#dynamic\_virtual\_path\_provisioning\_response\_schema-inline) > array

<a name="dynamic\_virtual\_path\_provisioning\_response\_schema-inline"></a>
**dynamic\_virtual\_path\_provisioning\_response\_schema**

|Name|Schema|
|---|---|
|**id**  <br>*optional*|[id](#id)|
|**lan\_to\_wan\_fair\_bitrate**  <br>*optional*|[lan\_to\_wan\_fair\_bitrate](#lan\_to\_wan\_fair\_bitrate)|
|**lan\_to\_wan\_maximum\_allowed\_bitrate**  <br>*optional*|[lan\_to\_wan\_maximum\_allowed\_bitrate](#lan\_to\_wan\_maximum\_allowed\_bitrate)|
|**lan\_to\_wan\_maximum\_allowed\_bitrate\_for\_all**  <br>*optional*|[lan\_to\_wan\_maximum\_allowed\_bitrate\_for\_all](#lan\_to\_wan\_maximum\_allowed\_bitrate\_for\_all)|
|**lan\_to\_wan\_minimum\_reserved\_bitrate**  <br>*optional*|[lan\_to\_wan\_minimum\_reserved\_bitrate](#lan\_to\_wan\_minimum\_reserved\_bitrate)|
|**lan\_to\_wan\_minimum\_reserved\_bitrate\_for\_all**  <br>*optional*|[lan\_to\_wan\_minimum\_reserved\_bitrate\_for\_all](#lan\_to\_wan\_minimum\_reserved\_bitrate\_for\_all)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**possible\_dynamic\_virtual\_paths**  <br>*optional*|[possible\_dynamic\_virtual\_paths](#possible\_dynamic\_virtual\_paths)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**wan\_link\_name**  <br>*optional*|[wan\_link\_name](#wan\_link\_name)|
|**wan\_to\_lan\_fair\_bitrate**  <br>*optional*|[wan\_to\_lan\_fair\_bitrate](#wan\_to\_lan\_fair\_bitrate)|
|**wan\_to\_lan\_maximum\_allowed\_bitrate**  <br>*optional*|[wan\_to\_lan\_maximum\_allowed\_bitrate](#wan\_to\_lan\_maximum\_allowed\_bitrate)|
|**wan\_to\_lan\_maximum\_allowed\_bitrate\_for\_all**  <br>*optional*|[wan\_to\_lan\_maximum\_allowed\_bitrate\_for\_all](#wan\_to\_lan\_maximum\_allowed\_bitrate\_for\_all)|
|**wan\_to\_lan\_minimum\_reserved\_bitrate**  <br>*optional*|[wan\_to\_lan\_minimum\_reserved\_bitrate](#wan\_to\_lan\_minimum\_reserved\_bitrate)|
|**wan\_to\_lan\_minimum\_reserved\_bitrate\_for\_all**  <br>*optional*|[wan\_to\_lan\_minimum\_reserved\_bitrate\_for\_all](#wan\_to\_lan\_minimum\_reserved\_bitrate\_for\_all)|


<a name="id"></a>
### id
Auto-generated ID to uniquely identify the service provisioning.

*Type* : integer


<a name="lan\_to\_wan\_fair\_bitrate"></a>
### lan\_to\_wan\_fair\_bitrate
The fair bit rate for an individual dynamic virtual path in LAN to WAN direction, based on its shares of group set in the service provisioning. Includes the Min rate, and will not exceed the Max rate.

*Type* : integer


<a name="lan\_to\_wan\_maximum\_allowed\_bitrate"></a>
### lan\_to\_wan\_maximum\_allowed\_bitrate
The maximum bandwidth an individual dynamic virtual path is allowed to utilize in LAN to WAN direction. (A value of 0 implies no limit.)

*Type* : integer


<a name="lan\_to\_wan\_maximum\_allowed\_bitrate\_for\_all"></a>
### lan\_to\_wan\_maximum\_allowed\_bitrate\_for\_all
The total maximum bandwidth for all dynamic virtual paths in LAN to WAN direction (Max rate multiplied by possible dynamic virtual paths).

*Type* : integer


<a name="lan\_to\_wan\_minimum\_reserved\_bitrate"></a>
### lan\_to\_wan\_minimum\_reserved\_bitrate
The minimum bandwidth for an individual dynamic visrtual path in LAN to WAN direction.

*Type* : integer


<a name="lan\_to\_wan\_minimum\_reserved\_bitrate\_for\_all"></a>
### lan\_to\_wan\_minimum\_reserved\_bitrate\_for\_all
The total minimum bandwidth for all dynamic virtual paths in LAN to WAN direction (Min rate multiplied by possible dynamic virtual paths).

*Type* : integer


<a name="package\_name"></a>
### package\_name
Config package name using which the site API operation should be performed.

*Type* : string


<a name="possible\_dynamic\_virtual\_paths"></a>
### possible\_dynamic\_virtual\_paths
The number of dynamic conduits that could exist simultaneously, based on the current configuration.

*Type* : string


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
The fair bit rate for an individual dynamic virtual path in WAN to LAN direction, based on its shares of group set in the service provisioning. Includes the Min rate, and will not exceed the Max rate.

*Type* : integer


<a name="wan\_to\_lan\_maximum\_allowed\_bitrate"></a>
### wan\_to\_lan\_maximum\_allowed\_bitrate
The maximum bandwidth an individual dynamic virtual path is allowed to utilize in WAN to LAN direction. (A value of 0 implies no limit.)

*Type* : integer


<a name="wan\_to\_lan\_maximum\_allowed\_bitrate\_for\_all"></a>
### wan\_to\_lan\_maximum\_allowed\_bitrate\_for\_all
The total maximum bandwidth for all dynamic virtual paths in WAN to LAN direction (Max rate multiplied by possible dynamic virtual paths).

*Type* : integer


<a name="wan\_to\_lan\_minimum\_reserved\_bitrate"></a>
### wan\_to\_lan\_minimum\_reserved\_bitrate
The minimum bandwidth for an individual dynamic visrtual path in WAN to LAN direction.

*Type* : integer


<a name="wan\_to\_lan\_minimum\_reserved\_bitrate\_for\_all"></a>
### wan\_to\_lan\_minimum\_reserved\_bitrate\_for\_all
The total minimum bandwidth for all dynamic virtual paths in WAN to LAN direction (Min rate multiplied by possible dynamic virtual paths).

*Type* : integer






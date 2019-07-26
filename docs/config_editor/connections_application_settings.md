# connections\_application\_settings


<a name="overview"></a>
## Overview
API to add, delete, get, modify connections application settings


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* connections\_application\_settings : Operations related to connections\_application\_settings 




<a name="paths"></a>
## Paths

<a name="connections\_application\_settings-get"></a>
### Get operation for connections\_application\_settings
```
GET /connections_application_settings
```


#### Description
Use this operation to get the connections application settings


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[connections\_application\_settings\_response\_schema](#connections\_application\_settings\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* connections\_application\_settings


<a name="connections\_application\_settings-put"></a>
### PUT operation for connections\_application\_settings
```
PUT /connections_application_settings
```


#### Description
Use this operation to modify connections application settings


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[connections\_application\_settings\_request\_schema](#connections\_application\_settings\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[connections\_application\_settings\_put\_success\_schema](#connections\_application\_settings\_put\_success\_schema)|
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

* connections\_application\_settings




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="connections\_application\_settings"></a>
### connections\_application\_settings

|Name|Schema|
|---|---|
|**dpi\_ica\_ip1**  <br>*optional*|[dpi\_ica\_ip1](#dpi\_ica\_ip1)|
|**dpi\_ica\_ip2**  <br>*optional*|[dpi\_ica\_ip2](#dpi\_ica\_ip2)|
|**dpi\_ica\_ip3**  <br>*optional*|[dpi\_ica\_ip3](#dpi\_ica\_ip3)|
|**dpi\_ica\_ip4**  <br>*optional*|[dpi\_ica\_ip4](#dpi\_ica\_ip4)|
|**dpi\_ica\_ip5**  <br>*optional*|[dpi\_ica\_ip5](#dpi\_ica\_ip5)|
|**dpi\_ica\_port1**  <br>*optional*|[dpi\_ica\_port1](#dpi\_ica\_port1)|
|**dpi\_ica\_port2**  <br>*optional*|[dpi\_ica\_port2](#dpi\_ica\_port2)|
|**dpi\_ica\_port3**  <br>*optional*|[dpi\_ica\_port3](#dpi\_ica\_port3)|
|**dpi\_ica\_port4**  <br>*optional*|[dpi\_ica\_port4](#dpi\_ica\_port4)|
|**dpi\_ica\_port5**  <br>*optional*|[dpi\_ica\_port5](#dpi\_ica\_port5)|
|**enable\_deep\_packet\_inspection**  <br>*optional*|[enable\_deep\_packet\_inspection](#enable\_deep\_packet\_inspection)|
|**enable\_deep\_packet\_inspection\_ica**  <br>*optional*|[enable\_deep\_packet\_inspection\_ica](#enable\_deep\_packet\_inspection\_ica)|
|**enable\_multistream\_ica**  <br>*optional*|[enable\_multistream\_ica](#enable\_multistream\_ica)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**use\_global\_application\_settings**  <br>*optional*|[use\_global\_application\_settings](#use\_global\_application\_settings)|


<a name="connections\_application\_settings\_delete\_success\_schema"></a>
### connections\_application\_settings\_delete\_success\_schema

|Name|Schema|
|---|---|
|**connections\_application\_settings**  <br>*optional*|[connections\_application\_settings](#connections\_application\_settings\_delete\_success\_schema-connections\_application\_settings)|

<a name="connections\_application\_settings\_delete\_success\_schema-connections\_application\_settings"></a>
**connections\_application\_settings**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="connections\_application\_settings\_post\_success\_schema"></a>
### connections\_application\_settings\_post\_success\_schema

|Name|Schema|
|---|---|
|**connections\_application\_settings**  <br>*optional*|[connections\_application\_settings](#connections\_application\_settings\_post\_success\_schema-connections\_application\_settings)|

<a name="connections\_application\_settings\_post\_success\_schema-connections\_application\_settings"></a>
**connections\_application\_settings**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="connections\_application\_settings\_put\_success\_schema"></a>
### connections\_application\_settings\_put\_success\_schema

|Name|Schema|
|---|---|
|**connections\_application\_settings**  <br>*optional*|[connections\_application\_settings](#connections\_application\_settings\_put\_success\_schema-connections\_application\_settings)|

<a name="connections\_application\_settings\_put\_success\_schema-connections\_application\_settings"></a>
**connections\_application\_settings**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="connections\_application\_settings\_request\_schema"></a>
### connections\_application\_settings\_request\_schema

|Name|Schema|
|---|---|
|**connections\_application\_settings**  <br>*optional*|[connections\_application\_settings](#connections\_application\_settings)|


<a name="connections\_application\_settings\_response\_schema"></a>
### connections\_application\_settings\_response\_schema
*Type* : < [connections\_application\_settings\_response\_schema](#connections\_application\_settings\_response\_schema-inline) > array

<a name="connections\_application\_settings\_response\_schema-inline"></a>
**connections\_application\_settings\_response\_schema**

|Name|Schema|
|---|---|
|**dpi\_ica\_ip1**  <br>*optional*|[dpi\_ica\_ip1](#dpi\_ica\_ip1)|
|**dpi\_ica\_ip2**  <br>*optional*|[dpi\_ica\_ip2](#dpi\_ica\_ip2)|
|**dpi\_ica\_ip3**  <br>*optional*|[dpi\_ica\_ip3](#dpi\_ica\_ip3)|
|**dpi\_ica\_ip4**  <br>*optional*|[dpi\_ica\_ip4](#dpi\_ica\_ip4)|
|**dpi\_ica\_ip5**  <br>*optional*|[dpi\_ica\_ip5](#dpi\_ica\_ip5)|
|**dpi\_ica\_port1**  <br>*optional*|[dpi\_ica\_port1](#dpi\_ica\_port1)|
|**dpi\_ica\_port2**  <br>*optional*|[dpi\_ica\_port2](#dpi\_ica\_port2)|
|**dpi\_ica\_port3**  <br>*optional*|[dpi\_ica\_port3](#dpi\_ica\_port3)|
|**dpi\_ica\_port4**  <br>*optional*|[dpi\_ica\_port4](#dpi\_ica\_port4)|
|**dpi\_ica\_port5**  <br>*optional*|[dpi\_ica\_port5](#dpi\_ica\_port5)|
|**enable\_deep\_packet\_inspection**  <br>*optional*|[enable\_deep\_packet\_inspection](#enable\_deep\_packet\_inspection)|
|**enable\_deep\_packet\_inspection\_ica**  <br>*optional*|[enable\_deep\_packet\_inspection\_ica](#enable\_deep\_packet\_inspection\_ica)|
|**enable\_multistream\_ica**  <br>*optional*|[enable\_multistream\_ica](#enable\_multistream\_ica)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**use\_global\_application\_settings**  <br>*optional*|[use\_global\_application\_settings](#use\_global\_application\_settings)|


<a name="dpi\_ica\_ip1"></a>
### dpi\_ica\_ip1
IP Address 1 for DPI ICA

*Type* : string


<a name="dpi\_ica\_ip2"></a>
### dpi\_ica\_ip2
IP Address 2 for DPI ICA

*Type* : string


<a name="dpi\_ica\_ip3"></a>
### dpi\_ica\_ip3
IP Address 3 for DPI ICA

*Type* : string


<a name="dpi\_ica\_ip4"></a>
### dpi\_ica\_ip4
IP Address 4 for DPI ICA

*Type* : string


<a name="dpi\_ica\_ip5"></a>
### dpi\_ica\_ip5
IP Address 5 for DPI ICA

*Type* : string


<a name="dpi\_ica\_port1"></a>
### dpi\_ica\_port1
Port 1 for DPI ICA

*Type* : string


<a name="dpi\_ica\_port2"></a>
### dpi\_ica\_port2
Port 2 for DPI ICA

*Type* : string


<a name="dpi\_ica\_port3"></a>
### dpi\_ica\_port3
Port 3 for DPI ICA

*Type* : string


<a name="dpi\_ica\_port4"></a>
### dpi\_ica\_port4
Port 4 for DPI ICA

*Type* : string


<a name="dpi\_ica\_port5"></a>
### dpi\_ica\_port5
Port 5 for DPI ICA

*Type* : string


<a name="enable\_deep\_packet\_inspection"></a>
### enable\_deep\_packet\_inspection
Set to true to Enable Deep Packet Inspection

*Type* : boolean


<a name="enable\_deep\_packet\_inspection\_ica"></a>
### enable\_deep\_packet\_inspection\_ica
Set to true to Enable Deep Packet Inspection for Citrix ICA Applications

*Type* : boolean


<a name="enable\_multistream\_ica"></a>
### enable\_multistream\_ica
Set to true to Enable Multi-stream ICA

*Type* : boolean


<a name="package\_name"></a>
### package\_name
Config package name using which the API operation should be performed.

*Type* : string


<a name="site\_name"></a>
### site\_name
Site Name

*Type* : string


<a name="use\_global\_application\_settings"></a>
### use\_global\_application\_settings
Set to true to use global application settings

*Type* : boolean






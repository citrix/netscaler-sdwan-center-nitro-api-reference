# wan\_optimization\_features


<a name="overview"></a>
## Overview
API to get, modify global WAN Optimization Features.


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* wan\_optimization\_features : Operations related to wan\_optimization\_features 




<a name="paths"></a>
## Paths

<a name="wan\_optimization\_features-get"></a>
### Get operation for wan\_optimization\_features
```
GET /wan_optimization_features
```


#### Description
Use this operation to get the current values of WAN Optimization features


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[wan\_optimization\_features\_response\_schema](#wan\_optimization\_features\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* wan\_optimization\_features


<a name="wan\_optimization\_features-put"></a>
### PUT operation for wan\_optimization\_features
```
PUT /wan_optimization_features
```


#### Description
Use this operation to modify the current values of WAN Optimization features


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[wan\_optimization\_features\_request\_schema](#wan\_optimization\_features\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[wan\_optimization\_features\_put\_success\_schema](#wan\_optimization\_features\_put\_success\_schema)|
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

* wan\_optimization\_features




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="enable\_hdx\_qos\_priorities"></a>
### enable\_hdx\_qos\_priorities
Set to true to enable HDX QoS priorities.

*Type* : boolean


<a name="enable\_mapi\_cross\_protocol\_optimization"></a>
### enable\_mapi\_cross\_protocol\_optimization
Set to true to enable MAPI cross protocol optimization.

*Type* : boolean


<a name="enable\_native\_mapi"></a>
### enable\_native\_mapi
Set to true to enable native MAPI.

*Type* : boolean


<a name="enable\_rpc\_over\_http"></a>
### enable\_rpc\_over\_http
Set to true to enable rpc over http.

*Type* : boolean


<a name="enable\_scps"></a>
### enable\_scps
Set to true to enable scps.

*Type* : boolean


<a name="enable\_smb1"></a>
### enable\_smb1
Set to true to enable SMB1 as part of CIFS Optimization.

*Type* : boolean


<a name="enable\_smb2"></a>
### enable\_smb2
Set to true to enable SMB2.

*Type* : boolean


<a name="enable\_smb3"></a>
### enable\_smb3
Set to true to enable SMB3. SMB3 can be selected only if SMB2 is selected.

*Type* : boolean


<a name="enable\_ssl\_optimization"></a>
### enable\_ssl\_optimization
Set to true to enable ssl optimization.

*Type* : boolean


<a name="enable\_user\_data\_store\_encryption"></a>
### enable\_user\_data\_store\_encryption
Set to true to enable user data store encryption.

*Type* : boolean


<a name="enable\_wan\_optimization"></a>
### enable\_wan\_optimization
Set to true to enable wan optimization.

*Type* : boolean


<a name="package\_name"></a>
### package\_name
Config package name using which the API operation should be performed.

*Type* : string


<a name="wan\_optimization\_features"></a>
### wan\_optimization\_features

|Name|Schema|
|---|---|
|**enable\_hdx\_qos\_priorities**  <br>*optional*|[enable\_hdx\_qos\_priorities](#enable\_hdx\_qos\_priorities)|
|**enable\_mapi\_cross\_protocol\_optimization**  <br>*optional*|[enable\_mapi\_cross\_protocol\_optimization](#enable\_mapi\_cross\_protocol\_optimization)|
|**enable\_native\_mapi**  <br>*optional*|[enable\_native\_mapi](#enable\_native\_mapi)|
|**enable\_rpc\_over\_http**  <br>*optional*|[enable\_rpc\_over\_http](#enable\_rpc\_over\_http)|
|**enable\_scps**  <br>*optional*|[enable\_scps](#enable\_scps)|
|**enable\_smb1**  <br>*optional*|[enable\_smb1](#enable\_smb1)|
|**enable\_smb2**  <br>*optional*|[enable\_smb2](#enable\_smb2)|
|**enable\_smb3**  <br>*optional*|[enable\_smb3](#enable\_smb3)|
|**enable\_ssl\_optimization**  <br>*optional*|[enable\_ssl\_optimization](#enable\_ssl\_optimization)|
|**enable\_user\_data\_store\_encryption**  <br>*optional*|[enable\_user\_data\_store\_encryption](#enable\_user\_data\_store\_encryption)|
|**enable\_wan\_optimization**  <br>*optional*|[enable\_wan\_optimization](#enable\_wan\_optimization)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|


<a name="wan\_optimization\_features\_delete\_success\_schema"></a>
### wan\_optimization\_features\_delete\_success\_schema

|Name|Schema|
|---|---|
|**wan\_optimization\_features**  <br>*optional*|[wan\_optimization\_features](#wan\_optimization\_features\_delete\_success\_schema-wan\_optimization\_features)|

<a name="wan\_optimization\_features\_delete\_success\_schema-wan\_optimization\_features"></a>
**wan\_optimization\_features**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="wan\_optimization\_features\_post\_success\_schema"></a>
### wan\_optimization\_features\_post\_success\_schema

|Name|Schema|
|---|---|
|**wan\_optimization\_features**  <br>*optional*|[wan\_optimization\_features](#wan\_optimization\_features\_post\_success\_schema-wan\_optimization\_features)|

<a name="wan\_optimization\_features\_post\_success\_schema-wan\_optimization\_features"></a>
**wan\_optimization\_features**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="wan\_optimization\_features\_put\_success\_schema"></a>
### wan\_optimization\_features\_put\_success\_schema

|Name|Schema|
|---|---|
|**wan\_optimization\_features**  <br>*optional*|[wan\_optimization\_features](#wan\_optimization\_features\_put\_success\_schema-wan\_optimization\_features)|

<a name="wan\_optimization\_features\_put\_success\_schema-wan\_optimization\_features"></a>
**wan\_optimization\_features**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="wan\_optimization\_features\_request\_schema"></a>
### wan\_optimization\_features\_request\_schema

|Name|Schema|
|---|---|
|**wan\_optimization\_features**  <br>*optional*|[wan\_optimization\_features](#wan\_optimization\_features)|


<a name="wan\_optimization\_features\_response\_schema"></a>
### wan\_optimization\_features\_response\_schema
*Type* : < [wan\_optimization\_features\_response\_schema](#wan\_optimization\_features\_response\_schema-inline) > array

<a name="wan\_optimization\_features\_response\_schema-inline"></a>
**wan\_optimization\_features\_response\_schema**

|Name|Schema|
|---|---|
|**enable\_hdx\_qos\_priorities**  <br>*optional*|[enable\_hdx\_qos\_priorities](#enable\_hdx\_qos\_priorities)|
|**enable\_mapi\_cross\_protocol\_optimization**  <br>*optional*|[enable\_mapi\_cross\_protocol\_optimization](#enable\_mapi\_cross\_protocol\_optimization)|
|**enable\_native\_mapi**  <br>*optional*|[enable\_native\_mapi](#enable\_native\_mapi)|
|**enable\_rpc\_over\_http**  <br>*optional*|[enable\_rpc\_over\_http](#enable\_rpc\_over\_http)|
|**enable\_scps**  <br>*optional*|[enable\_scps](#enable\_scps)|
|**enable\_smb1**  <br>*optional*|[enable\_smb1](#enable\_smb1)|
|**enable\_smb2**  <br>*optional*|[enable\_smb2](#enable\_smb2)|
|**enable\_smb3**  <br>*optional*|[enable\_smb3](#enable\_smb3)|
|**enable\_ssl\_optimization**  <br>*optional*|[enable\_ssl\_optimization](#enable\_ssl\_optimization)|
|**enable\_user\_data\_store\_encryption**  <br>*optional*|[enable\_user\_data\_store\_encryption](#enable\_user\_data\_store\_encryption)|
|**enable\_wan\_optimization**  <br>*optional*|[enable\_wan\_optimization](#enable\_wan\_optimization)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|






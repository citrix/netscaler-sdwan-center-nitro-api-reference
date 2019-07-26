# app\_qoe\_profile


<a name="overview"></a>
## Overview
API to add , delete, get, modify global application qoe profile


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* app\_qoe\_profile : Operations related to app\_qoe\_profile 




<a name="paths"></a>
## Paths

<a name="app\_qoe\_profile-post"></a>
### POST operation for app\_qoe\_profile
```
POST /app_qoe_profile
```


#### Description
This operation is to add new application QoE profiles


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[app\_qoe\_profile\_request\_schema](#app\_qoe\_profile\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[app\_qoe\_profile\_post\_success\_schema](#app\_qoe\_profile\_post\_success\_schema)|
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

* app\_qoe\_profile


<a name="app\_qoe\_profile-get"></a>
### Get operation for app\_qoe\_profile
```
GET /app_qoe_profile
```


#### Description
This opertaion is to get the application QoE Profiles


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[app\_qoe\_profile\_response\_schema](#app\_qoe\_profile\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* app\_qoe\_profile


<a name="app\_qoe\_profile-put"></a>
### PUT operation for app\_qoe\_profile
```
PUT /app_qoe_profile
```


#### Description
This operation is to modify existing application QoE profiles


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[app\_qoe\_profile\_put\_success\_schema](#app\_qoe\_profile\_put\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* app\_qoe\_profile


<a name="app\_qoe\_profile-deletepathparam-delete"></a>
### DELETE operation for app\_qoe\_profile
```
DELETE /app_qoe_profile/{deletePathParam}
```


#### Description
This operation is to delete application QoE profiles except for the default profile which is auto created


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[app\_qoe\_profile\_delete\_success\_schema](#app\_qoe\_profile\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* app\_qoe\_profile




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="app\_qoe\_profile"></a>
### app\_qoe\_profile

|Name|Schema|
|---|---|
|**burst\_rate**  <br>*optional*|[burst\_rate](#burst\_rate)|
|**id**  <br>*optional*|[id](#id)|
|**jitter**  <br>*optional*|[jitter](#jitter)|
|**latency**  <br>*optional*|[latency](#latency)|
|**name**  <br>*optional*|[name](#name)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**packet\_loss**  <br>*optional*|[packet\_loss](#packet\_loss)|
|**packet\_loss\_per\_flow**  <br>*optional*|[packet\_loss\_per\_flow](#packet\_loss\_per\_flow)|


<a name="app\_qoe\_profile\_delete\_success\_schema"></a>
### app\_qoe\_profile\_delete\_success\_schema

|Name|Schema|
|---|---|
|**app\_qoe\_profile**  <br>*optional*|[app\_qoe\_profile](#app\_qoe\_profile\_delete\_success\_schema-app\_qoe\_profile)|

<a name="app\_qoe\_profile\_delete\_success\_schema-app\_qoe\_profile"></a>
**app\_qoe\_profile**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="app\_qoe\_profile\_post\_success\_schema"></a>
### app\_qoe\_profile\_post\_success\_schema

|Name|Schema|
|---|---|
|**app\_qoe\_profile**  <br>*optional*|[app\_qoe\_profile](#app\_qoe\_profile\_post\_success\_schema-app\_qoe\_profile)|

<a name="app\_qoe\_profile\_post\_success\_schema-app\_qoe\_profile"></a>
**app\_qoe\_profile**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="app\_qoe\_profile\_put\_success\_schema"></a>
### app\_qoe\_profile\_put\_success\_schema

|Name|Schema|
|---|---|
|**app\_qoe\_profile**  <br>*optional*|[app\_qoe\_profile](#app\_qoe\_profile\_put\_success\_schema-app\_qoe\_profile)|

<a name="app\_qoe\_profile\_put\_success\_schema-app\_qoe\_profile"></a>
**app\_qoe\_profile**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="app\_qoe\_profile\_request\_schema"></a>
### app\_qoe\_profile\_request\_schema

|Name|Schema|
|---|---|
|**app\_qoe\_profile**  <br>*optional*|[app\_qoe\_profile](#app\_qoe\_profile)|


<a name="app\_qoe\_profile\_response\_schema"></a>
### app\_qoe\_profile\_response\_schema
*Type* : < [app\_qoe\_profile\_response\_schema](#app\_qoe\_profile\_response\_schema-inline) > array

<a name="app\_qoe\_profile\_response\_schema-inline"></a>
**app\_qoe\_profile\_response\_schema**

|Name|Schema|
|---|---|
|**burst\_rate**  <br>*optional*|[burst\_rate](#burst\_rate)|
|**id**  <br>*optional*|[id](#id)|
|**jitter**  <br>*optional*|[jitter](#jitter)|
|**latency**  <br>*optional*|[latency](#latency)|
|**name**  <br>*optional*|[name](#name)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**packet\_loss**  <br>*optional*|[packet\_loss](#packet\_loss)|
|**packet\_loss\_per\_flow**  <br>*optional*|[packet\_loss\_per\_flow](#packet\_loss\_per\_flow)|


<a name="burst\_rate"></a>
### burst\_rate
Burst rate

*Type* : number


<a name="id"></a>
### id
Auto-generated ID to uniquely identify application qoe profile

*Type* : integer


<a name="jitter"></a>
### jitter
Jitter in ms

*Type* : integer


<a name="latency"></a>
### latency
Latency in ms

*Type* : integer


<a name="name"></a>
### name
Name of the application qoe profile

*Type* : string


<a name="package\_name"></a>
### package\_name
Config package name using which the API operation should be performed.

*Type* : string


<a name="packet\_loss"></a>
### packet\_loss
Packet loss(%)

*Type* : number


<a name="packet\_loss\_per\_flow"></a>
### packet\_loss\_per\_flow
Packet loss per flow for interactive traffic(%)

*Type* : number






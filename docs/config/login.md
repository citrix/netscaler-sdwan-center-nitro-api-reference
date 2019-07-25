# login


<a name="overview"></a>
## Overview
This resource can be used to login and logout of SD-WAN Center


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config/  
*Schemes* : HTTP


### Tags

* login : Operations related to login 




<a name="paths"></a>
## Paths

<a name="login-post"></a>
### POST operation for login
```
POST /login
```


#### Description
Use this operation to Login To SD-WAN Center


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[login\_request\_schema](#login\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[login\_post\_success\_schema](#login\_post\_success\_schema)|
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

* login


<a name="login-deletepathparam-delete"></a>
### DELETE operation for login
```
DELETE /login/{deletePathParam}
```


#### Description
Use this operation to Logout From SD-WAN Center


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[login\_delete\_success\_schema](#login\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* login




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="login"></a>
### login

|Name|Schema|
|---|---|
|**password**  <br>*optional*|[password](#password)|
|**secondaryPassword**  <br>*optional*|[secondaryPassword](#secondarypassword)|
|**username**  <br>*optional*|[username](#username)|


<a name="login\_delete\_success\_schema"></a>
### login\_delete\_success\_schema

|Name|Schema|
|---|---|
|**login**  <br>*optional*|[login](#login\_delete\_success\_schema-login)|

<a name="login\_delete\_success\_schema-login"></a>
**login**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="login\_post\_success\_schema"></a>
### login\_post\_success\_schema

|Name|Schema|
|---|---|
|**login**  <br>*optional*|[login](#login\_post\_success\_schema-login)|

<a name="login\_post\_success\_schema-login"></a>
**login**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="login\_put\_success\_schema"></a>
### login\_put\_success\_schema

|Name|Schema|
|---|---|
|**login**  <br>*optional*|[login](#login\_put\_success\_schema-login)|

<a name="login\_put\_success\_schema-login"></a>
**login**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="login\_request\_schema"></a>
### login\_request\_schema

|Name|Schema|
|---|---|
|**login**  <br>*optional*|[login](#login)|


<a name="login\_response\_schema"></a>
### login\_response\_schema
*Type* : < [login\_response\_schema](#login\_response\_schema-inline) > array

<a name="login\_response\_schema-inline"></a>
**login\_response\_schema**

|Name|Schema|
|---|---|
|**password**  <br>*optional*|[password](#password)|
|**secondaryPassword**  <br>*optional*|[secondaryPassword](#secondarypassword)|
|**username**  <br>*optional*|[username](#username)|


<a name="password"></a>
### password
Authentication Password

*Type* : string


<a name="secondarypassword"></a>
### secondaryPassword
Optional Parameter for secondary password of a user with two-factor enabled.

*Type* : string


<a name="username"></a>
### username
User Name

*Type* : string






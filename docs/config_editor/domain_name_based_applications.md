# domain\_name\_based\_applications


<a name="overview"></a>
## Overview
API to add, delete, get, modify custom domain details


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* domain\_name\_based\_applications : Operations related to domain\_name\_based\_applications 




<a name="paths"></a>
## Paths

<a name="domain\_name\_based\_applications-post"></a>
### POST operation for domain\_name\_based\_applications
```
POST /domain_name_based_applications
```


#### Description
Use this operation to add Domain Based Application globally


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[domain\_name\_based\_applications\_post\_success\_schema](#domain\_name\_based\_applications\_post\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* domain\_name\_based\_applications


<a name="domain\_name\_based\_applications-get"></a>
### Get operation for domain\_name\_based\_applications
```
GET /domain_name_based_applications
```


#### Description
Use this operation to get the global Domain Based Application configured


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[domain\_name\_based\_applications\_response\_schema](#domain\_name\_based\_applications\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* domain\_name\_based\_applications


<a name="domain\_name\_based\_applications-put"></a>
### PUT operation for domain\_name\_based\_applications
```
PUT /domain_name_based_applications
```


#### Description
Use this operation to modify Domain Based Application


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[domain\_name\_based\_applications\_request\_schema](#domain\_name\_based\_applications\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[domain\_name\_based\_applications\_put\_success\_schema](#domain\_name\_based\_applications\_put\_success\_schema)|
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

* domain\_name\_based\_applications


<a name="domain\_name\_based\_applications-deletepathparam-delete"></a>
### DELETE operation for domain\_name\_based\_applications
```
DELETE /domain_name_based_applications/{deletePathParam}
```


#### Description
Use this operation to delete Domain Based Application configured


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[domain\_name\_based\_applications\_delete\_success\_schema](#domain\_name\_based\_applications\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* domain\_name\_based\_applications




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="application\_domain\_details"></a>
### application\_domain\_details
domain name

*Type* : < [application\_domain\_details](#application\_domain\_details-inline) > array

<a name="application\_domain\_details-inline"></a>
**application\_domain\_details**

|Name|Description|Schema|
|---|---|---|
|**domain\_name**  <br>*optional*|The name of the domain|string|
|**id**  <br>*optional*|Auto-generated ID to uniquely identify domain name|integer|


<a name="domain\_name\_based\_applications"></a>
### domain\_name\_based\_applications

|Name|Schema|
|---|---|
|**application\_domain\_details**  <br>*optional*|[application\_domain\_details](#application\_domain\_details)|
|**id**  <br>*optional*|[id](#id)|
|**name**  <br>*optional*|[name](#name)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|


<a name="domain\_name\_based\_applications\_delete\_success\_schema"></a>
### domain\_name\_based\_applications\_delete\_success\_schema

|Name|Schema|
|---|---|
|**domain\_name\_based\_applications**  <br>*optional*|[domain\_name\_based\_applications](#domain\_name\_based\_applications\_delete\_success\_schema-domain\_name\_based\_applications)|

<a name="domain\_name\_based\_applications\_delete\_success\_schema-domain\_name\_based\_applications"></a>
**domain\_name\_based\_applications**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="domain\_name\_based\_applications\_post\_success\_schema"></a>
### domain\_name\_based\_applications\_post\_success\_schema

|Name|Schema|
|---|---|
|**domain\_name\_based\_applications**  <br>*optional*|[domain\_name\_based\_applications](#domain\_name\_based\_applications\_post\_success\_schema-domain\_name\_based\_applications)|

<a name="domain\_name\_based\_applications\_post\_success\_schema-domain\_name\_based\_applications"></a>
**domain\_name\_based\_applications**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="domain\_name\_based\_applications\_put\_success\_schema"></a>
### domain\_name\_based\_applications\_put\_success\_schema

|Name|Schema|
|---|---|
|**domain\_name\_based\_applications**  <br>*optional*|[domain\_name\_based\_applications](#domain\_name\_based\_applications\_put\_success\_schema-domain\_name\_based\_applications)|

<a name="domain\_name\_based\_applications\_put\_success\_schema-domain\_name\_based\_applications"></a>
**domain\_name\_based\_applications**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="domain\_name\_based\_applications\_request\_schema"></a>
### domain\_name\_based\_applications\_request\_schema

|Name|Schema|
|---|---|
|**domain\_name\_based\_applications**  <br>*optional*|[domain\_name\_based\_applications](#domain\_name\_based\_applications)|


<a name="domain\_name\_based\_applications\_response\_schema"></a>
### domain\_name\_based\_applications\_response\_schema
*Type* : < [domain\_name\_based\_applications\_response\_schema](#domain\_name\_based\_applications\_response\_schema-inline) > array

<a name="domain\_name\_based\_applications\_response\_schema-inline"></a>
**domain\_name\_based\_applications\_response\_schema**

|Name|Schema|
|---|---|
|**application\_domain\_details**  <br>*optional*|[application\_domain\_details](#application\_domain\_details)|
|**id**  <br>*optional*|[id](#id)|
|**name**  <br>*optional*|[name](#name)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|


<a name="id"></a>
### id
Auto-generated ID to uniquely identify Domain Based Application

*Type* : integer


<a name="name"></a>
### name
The name of the Domain Based Application

*Type* : string


<a name="package\_name"></a>
### package\_name
Config package name using which the API operation should be performed.

*Type* : string






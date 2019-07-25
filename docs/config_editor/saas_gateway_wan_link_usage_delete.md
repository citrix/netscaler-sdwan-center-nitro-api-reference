# saas\_gateway\_wan\_link\_usage\_delete


<a name="overview"></a>
## Overview
API to delete saas gateway service wan link usage configuration object


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* saas\_gateway\_wan\_link\_usage\_delete : Operations related to saas\_gateway\_wan\_link\_usage\_delete 




<a name="paths"></a>
## Paths

<a name="saas\_gateway\_wan\_link\_usage\_delete-deletepathparam-delete"></a>
### DELETE operation for saas\_gateway\_wan\_link\_usage\_delete
```
DELETE /saas_gateway_wan_link_usage_delete/{deletePathParam}
```


#### Description
Use this operation to delete the saas gateway service wan link usage object


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[saas\_gateway\_wan\_link\_usage\_delete\_delete\_success\_schema](#saas\_gateway\_wan\_link\_usage\_delete\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* saas\_gateway\_wan\_link\_usage\_delete




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
saas gateway service wan link usage id

*Type* : integer


<a name="package\_name"></a>
### package\_name
Config package name using which the API operation should be performed.

*Type* : string


<a name="saas\_gateway\_wan\_link\_usage\_delete"></a>
### saas\_gateway\_wan\_link\_usage\_delete

|Name|Schema|
|---|---|
|**id**  <br>*optional*|[id](#id)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|


<a name="saas\_gateway\_wan\_link\_usage\_delete\_delete\_success\_schema"></a>
### saas\_gateway\_wan\_link\_usage\_delete\_delete\_success\_schema

|Name|Schema|
|---|---|
|**saas\_gateway\_wan\_link\_usage\_delete**  <br>*optional*|[saas\_gateway\_wan\_link\_usage\_delete](#saas\_gateway\_wan\_link\_usage\_delete\_delete\_success\_schema-saas\_gateway\_wan\_link\_usage\_delete)|

<a name="saas\_gateway\_wan\_link\_usage\_delete\_delete\_success\_schema-saas\_gateway\_wan\_link\_usage\_delete"></a>
**saas\_gateway\_wan\_link\_usage\_delete**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="saas\_gateway\_wan\_link\_usage\_delete\_post\_success\_schema"></a>
### saas\_gateway\_wan\_link\_usage\_delete\_post\_success\_schema

|Name|Schema|
|---|---|
|**saas\_gateway\_wan\_link\_usage\_delete**  <br>*optional*|[saas\_gateway\_wan\_link\_usage\_delete](#saas\_gateway\_wan\_link\_usage\_delete\_post\_success\_schema-saas\_gateway\_wan\_link\_usage\_delete)|

<a name="saas\_gateway\_wan\_link\_usage\_delete\_post\_success\_schema-saas\_gateway\_wan\_link\_usage\_delete"></a>
**saas\_gateway\_wan\_link\_usage\_delete**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="saas\_gateway\_wan\_link\_usage\_delete\_put\_success\_schema"></a>
### saas\_gateway\_wan\_link\_usage\_delete\_put\_success\_schema

|Name|Schema|
|---|---|
|**saas\_gateway\_wan\_link\_usage\_delete**  <br>*optional*|[saas\_gateway\_wan\_link\_usage\_delete](#saas\_gateway\_wan\_link\_usage\_delete\_put\_success\_schema-saas\_gateway\_wan\_link\_usage\_delete)|

<a name="saas\_gateway\_wan\_link\_usage\_delete\_put\_success\_schema-saas\_gateway\_wan\_link\_usage\_delete"></a>
**saas\_gateway\_wan\_link\_usage\_delete**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="saas\_gateway\_wan\_link\_usage\_delete\_request\_schema"></a>
### saas\_gateway\_wan\_link\_usage\_delete\_request\_schema

|Name|Schema|
|---|---|
|**saas\_gateway\_wan\_link\_usage\_delete**  <br>*optional*|[saas\_gateway\_wan\_link\_usage\_delete](#saas\_gateway\_wan\_link\_usage\_delete)|


<a name="saas\_gateway\_wan\_link\_usage\_delete\_response\_schema"></a>
### saas\_gateway\_wan\_link\_usage\_delete\_response\_schema
*Type* : < [saas\_gateway\_wan\_link\_usage\_delete\_response\_schema](#saas\_gateway\_wan\_link\_usage\_delete\_response\_schema-inline) > array

<a name="saas\_gateway\_wan\_link\_usage\_delete\_response\_schema-inline"></a>
**saas\_gateway\_wan\_link\_usage\_delete\_response\_schema**

|Name|Schema|
|---|---|
|**id**  <br>*optional*|[id](#id)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|


<a name="site\_name"></a>
### site\_name
The Site Name

*Type* : string






# virtual\_path\_wan\_link\_mpls\_usage\_delete


<a name="overview"></a>
## Overview
API to delete MPLS Usage for a particular virtual path service


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* virtual\_path\_wan\_link\_mpls\_usage\_delete : Operations related to virtual\_path\_wan\_link\_mpls\_usage\_delete 




<a name="paths"></a>
## Paths

<a name="virtual\_path\_wan\_link\_mpls\_usage\_delete-deletepathparam-delete"></a>
### DELETE operation for virtual\_path\_wan\_link\_mpls\_usage\_delete
```
DELETE /virtual_path_wan_link_mpls_usage_delete/{deletePathParam}
```


#### Description
Use this operation to delete the mpls queue usage for a virtual path service


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[virtual\_path\_wan\_link\_mpls\_usage\_delete\_delete\_success\_schema](#virtual\_path\_wan\_link\_mpls\_usage\_delete\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* virtual\_path\_wan\_link\_mpls\_usage\_delete




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
MPLS Queue Usage auto generated id

*Type* : integer


<a name="package\_name"></a>
### package\_name
Config package name using which the API operation should be performed.

*Type* : string


<a name="site\_name"></a>
### site\_name
Site Name

*Type* : string


<a name="virtual\_path\_wan\_link\_mpls\_usage\_delete"></a>
### virtual\_path\_wan\_link\_mpls\_usage\_delete

|Name|Schema|
|---|---|
|**id**  <br>*optional*|[id](#id)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|


<a name="virtual\_path\_wan\_link\_mpls\_usage\_delete\_delete\_success\_schema"></a>
### virtual\_path\_wan\_link\_mpls\_usage\_delete\_delete\_success\_schema

|Name|Schema|
|---|---|
|**virtual\_path\_wan\_link\_mpls\_usage\_delete**  <br>*optional*|[virtual\_path\_wan\_link\_mpls\_usage\_delete](#virtual\_path\_wan\_link\_mpls\_usage\_delete\_delete\_success\_schema-virtual\_path\_wan\_link\_mpls\_usage\_delete)|

<a name="virtual\_path\_wan\_link\_mpls\_usage\_delete\_delete\_success\_schema-virtual\_path\_wan\_link\_mpls\_usage\_delete"></a>
**virtual\_path\_wan\_link\_mpls\_usage\_delete**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="virtual\_path\_wan\_link\_mpls\_usage\_delete\_post\_success\_schema"></a>
### virtual\_path\_wan\_link\_mpls\_usage\_delete\_post\_success\_schema

|Name|Schema|
|---|---|
|**virtual\_path\_wan\_link\_mpls\_usage\_delete**  <br>*optional*|[virtual\_path\_wan\_link\_mpls\_usage\_delete](#virtual\_path\_wan\_link\_mpls\_usage\_delete\_post\_success\_schema-virtual\_path\_wan\_link\_mpls\_usage\_delete)|

<a name="virtual\_path\_wan\_link\_mpls\_usage\_delete\_post\_success\_schema-virtual\_path\_wan\_link\_mpls\_usage\_delete"></a>
**virtual\_path\_wan\_link\_mpls\_usage\_delete**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="virtual\_path\_wan\_link\_mpls\_usage\_delete\_put\_success\_schema"></a>
### virtual\_path\_wan\_link\_mpls\_usage\_delete\_put\_success\_schema

|Name|Schema|
|---|---|
|**virtual\_path\_wan\_link\_mpls\_usage\_delete**  <br>*optional*|[virtual\_path\_wan\_link\_mpls\_usage\_delete](#virtual\_path\_wan\_link\_mpls\_usage\_delete\_put\_success\_schema-virtual\_path\_wan\_link\_mpls\_usage\_delete)|

<a name="virtual\_path\_wan\_link\_mpls\_usage\_delete\_put\_success\_schema-virtual\_path\_wan\_link\_mpls\_usage\_delete"></a>
**virtual\_path\_wan\_link\_mpls\_usage\_delete**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="virtual\_path\_wan\_link\_mpls\_usage\_delete\_request\_schema"></a>
### virtual\_path\_wan\_link\_mpls\_usage\_delete\_request\_schema

|Name|Schema|
|---|---|
|**virtual\_path\_wan\_link\_mpls\_usage\_delete**  <br>*optional*|[virtual\_path\_wan\_link\_mpls\_usage\_delete](#virtual\_path\_wan\_link\_mpls\_usage\_delete)|


<a name="virtual\_path\_wan\_link\_mpls\_usage\_delete\_response\_schema"></a>
### virtual\_path\_wan\_link\_mpls\_usage\_delete\_response\_schema
*Type* : < [virtual\_path\_wan\_link\_mpls\_usage\_delete\_response\_schema](#virtual\_path\_wan\_link\_mpls\_usage\_delete\_response\_schema-inline) > array

<a name="virtual\_path\_wan\_link\_mpls\_usage\_delete\_response\_schema-inline"></a>
**virtual\_path\_wan\_link\_mpls\_usage\_delete\_response\_schema**

|Name|Schema|
|---|---|
|**id**  <br>*optional*|[id](#id)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|






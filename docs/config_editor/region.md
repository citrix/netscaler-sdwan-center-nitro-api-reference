# region


<a name="overview"></a>
## Overview
API to add, modify, delete, and get regions


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* region : Operations related to region 




<a name="paths"></a>
## Paths

<a name="region-post"></a>
### POST operation for region
```
POST /region
```


#### Description
Use this operation to add a region


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[region\_post\_success\_schema](#region\_post\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* region


<a name="region-get"></a>
### Get operation for region
```
GET /region
```


#### Description
Use this operation to get the regions


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[region\_response\_schema](#region\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* region


<a name="region-put"></a>
### PUT operation for region
```
PUT /region
```


#### Description
Use this operation to modify a region


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[region\_request\_schema](#region\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[region\_put\_success\_schema](#region\_put\_success\_schema)|
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

* region


<a name="region-deletepathparam-delete"></a>
### DELETE operation for region
```
DELETE /region/{deletePathParam}
```


#### Description
Use this operation to delete a region. This operation also deletes all the sites in the region


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[region\_delete\_success\_schema](#region\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* region




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="allow\_external\_vip\_matching"></a>
### allow\_external\_vip\_matching
When enabled, non-private Virtual IP Addresses from other regions will be allowed to match the configured subnets

*Type* : boolean


<a name="force\_internal\_vip\_matching"></a>
### force\_internal\_vip\_matching
When enabled, all non-private Virtual IP Addressess in the Region will be forced to match the configured subnets

*Type* : boolean


<a name="id"></a>
### id
Config package name using which the region API operation should be performed.

*Type* : string


<a name="is\_default"></a>
### is\_default
If enabled, the Region will be used as the default Region for the network

*Type* : boolean


<a name="package\_name"></a>
### package\_name
Config package name using which the region API operation should be performed.

*Type* : string


<a name="region"></a>
### region

|Name|Schema|
|---|---|
|**allow\_external\_vip\_matching**  <br>*optional*|[allow\_external\_vip\_matching](#allow\_external\_vip\_matching)|
|**force\_internal\_vip\_matching**  <br>*optional*|[force\_internal\_vip\_matching](#force\_internal\_vip\_matching)|
|**id**  <br>*optional*|[id](#id)|
|**is\_default**  <br>*optional*|[is\_default](#is\_default)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**region\_description**  <br>*optional*|[region\_description](#region\_description)|
|**region\_name**  <br>*optional*|[region\_name](#region\_name)|
|**subnets**  <br>*optional*|[subnets](#subnets)|


<a name="region\_delete\_success\_schema"></a>
### region\_delete\_success\_schema

|Name|Schema|
|---|---|
|**region**  <br>*optional*|[region](#region\_delete\_success\_schema-region)|

<a name="region\_delete\_success\_schema-region"></a>
**region**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="region\_description"></a>
### region\_description
Region description

*Type* : string


<a name="region\_name"></a>
### region\_name
Region Name

*Type* : string


<a name="region\_post\_success\_schema"></a>
### region\_post\_success\_schema

|Name|Schema|
|---|---|
|**region**  <br>*optional*|[region](#region\_post\_success\_schema-region)|

<a name="region\_post\_success\_schema-region"></a>
**region**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="region\_put\_success\_schema"></a>
### region\_put\_success\_schema

|Name|Schema|
|---|---|
|**region**  <br>*optional*|[region](#region\_put\_success\_schema-region)|

<a name="region\_put\_success\_schema-region"></a>
**region**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="region\_request\_schema"></a>
### region\_request\_schema

|Name|Schema|
|---|---|
|**region**  <br>*optional*|[region](#region)|


<a name="region\_response\_schema"></a>
### region\_response\_schema
*Type* : < [region\_response\_schema](#region\_response\_schema-inline) > array

<a name="region\_response\_schema-inline"></a>
**region\_response\_schema**

|Name|Schema|
|---|---|
|**allow\_external\_vip\_matching**  <br>*optional*|[allow\_external\_vip\_matching](#allow\_external\_vip\_matching)|
|**force\_internal\_vip\_matching**  <br>*optional*|[force\_internal\_vip\_matching](#force\_internal\_vip\_matching)|
|**id**  <br>*optional*|[id](#id)|
|**is\_default**  <br>*optional*|[is\_default](#is\_default)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**region\_description**  <br>*optional*|[region\_description](#region\_description)|
|**region\_name**  <br>*optional*|[region\_name](#region\_name)|
|**subnets**  <br>*optional*|[subnets](#subnets)|


<a name="subnets"></a>
### subnets
Subnets for this region

*Type* : < [subnets](#subnets-inline) > array

<a name="subnets-inline"></a>
**subnets**

|Name|Description|Schema|
|---|---|---|
|**network**  <br>*optional*|The IP address and mask for the subnet|string|
|**routing\_domain**  <br>*optional*|The routing domain|string|






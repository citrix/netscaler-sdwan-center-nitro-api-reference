# firewall\_local\_policy\_delete


<a name="overview"></a>
## Overview
API delete configuration for Firewall Local Policy


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* firewall\_local\_policy\_delete : Operations related to firewall\_local\_policy\_delete 




<a name="paths"></a>
## Paths

<a name="firewall\_local\_policy\_delete-deletepathparam-delete"></a>
### DELETE operation for firewall\_local\_policy\_delete
```
DELETE /firewall_local_policy_delete/{deletePathParam}
```


#### Description
Use this operation to delete the basic and advanced Firewall Local Policy


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[firewall\_local\_policy\_delete\_delete\_success\_schema](#firewall\_local\_policy\_delete\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* firewall\_local\_policy\_delete




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="firewall\_local\_policy\_delete"></a>
### firewall\_local\_policy\_delete

|Name|Schema|
|---|---|
|**id**  <br>*optional*|[id](#id)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|


<a name="firewall\_local\_policy\_delete\_delete\_success\_schema"></a>
### firewall\_local\_policy\_delete\_delete\_success\_schema

|Name|Schema|
|---|---|
|**firewall\_local\_policy\_delete**  <br>*optional*|[firewall\_local\_policy\_delete](#firewall\_local\_policy\_delete\_delete\_success\_schema-firewall\_local\_policy\_delete)|

<a name="firewall\_local\_policy\_delete\_delete\_success\_schema-firewall\_local\_policy\_delete"></a>
**firewall\_local\_policy\_delete**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="firewall\_local\_policy\_delete\_post\_success\_schema"></a>
### firewall\_local\_policy\_delete\_post\_success\_schema

|Name|Schema|
|---|---|
|**firewall\_local\_policy\_delete**  <br>*optional*|[firewall\_local\_policy\_delete](#firewall\_local\_policy\_delete\_post\_success\_schema-firewall\_local\_policy\_delete)|

<a name="firewall\_local\_policy\_delete\_post\_success\_schema-firewall\_local\_policy\_delete"></a>
**firewall\_local\_policy\_delete**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="firewall\_local\_policy\_delete\_put\_success\_schema"></a>
### firewall\_local\_policy\_delete\_put\_success\_schema

|Name|Schema|
|---|---|
|**firewall\_local\_policy\_delete**  <br>*optional*|[firewall\_local\_policy\_delete](#firewall\_local\_policy\_delete\_put\_success\_schema-firewall\_local\_policy\_delete)|

<a name="firewall\_local\_policy\_delete\_put\_success\_schema-firewall\_local\_policy\_delete"></a>
**firewall\_local\_policy\_delete**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="firewall\_local\_policy\_delete\_request\_schema"></a>
### firewall\_local\_policy\_delete\_request\_schema

|Name|Schema|
|---|---|
|**firewall\_local\_policy\_delete**  <br>*optional*|[firewall\_local\_policy\_delete](#firewall\_local\_policy\_delete)|


<a name="firewall\_local\_policy\_delete\_response\_schema"></a>
### firewall\_local\_policy\_delete\_response\_schema
*Type* : < [firewall\_local\_policy\_delete\_response\_schema](#firewall\_local\_policy\_delete\_response\_schema-inline) > array

<a name="firewall\_local\_policy\_delete\_response\_schema-inline"></a>
**firewall\_local\_policy\_delete\_response\_schema**

|Name|Schema|
|---|---|
|**id**  <br>*optional*|[id](#id)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|


<a name="id"></a>
### id
Firewall local policy id

*Type* : integer


<a name="package\_name"></a>
### package\_name
Config package name using which the API operation should be performed.

*Type* : string


<a name="site\_name"></a>
### site\_name
Site Name

*Type* : string






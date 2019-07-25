# firewall\_policy\_template\_delete


<a name="overview"></a>
## Overview
API to delete a firewall template for a site


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* firewall\_policy\_template\_delete : Operations related to firewall\_policy\_template\_delete 




<a name="paths"></a>
## Paths

<a name="firewall\_policy\_template\_delete-deletepathparam-delete"></a>
### DELETE operation for firewall\_policy\_template\_delete
```
DELETE /firewall_policy_template_delete/{deletePathParam}
```


#### Description
Use this operation to delete the firewall related policy templates


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[firewall\_policy\_template\_delete\_delete\_success\_schema](#firewall\_policy\_template\_delete\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* firewall\_policy\_template\_delete




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="firewall\_policy\_template\_delete"></a>
### firewall\_policy\_template\_delete

|Name|Schema|
|---|---|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**template\_name**  <br>*optional*|[template\_name](#template\_name)|


<a name="firewall\_policy\_template\_delete\_delete\_success\_schema"></a>
### firewall\_policy\_template\_delete\_delete\_success\_schema

|Name|Schema|
|---|---|
|**firewall\_policy\_template\_delete**  <br>*optional*|[firewall\_policy\_template\_delete](#firewall\_policy\_template\_delete\_delete\_success\_schema-firewall\_policy\_template\_delete)|

<a name="firewall\_policy\_template\_delete\_delete\_success\_schema-firewall\_policy\_template\_delete"></a>
**firewall\_policy\_template\_delete**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="firewall\_policy\_template\_delete\_post\_success\_schema"></a>
### firewall\_policy\_template\_delete\_post\_success\_schema

|Name|Schema|
|---|---|
|**firewall\_policy\_template\_delete**  <br>*optional*|[firewall\_policy\_template\_delete](#firewall\_policy\_template\_delete\_post\_success\_schema-firewall\_policy\_template\_delete)|

<a name="firewall\_policy\_template\_delete\_post\_success\_schema-firewall\_policy\_template\_delete"></a>
**firewall\_policy\_template\_delete**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="firewall\_policy\_template\_delete\_put\_success\_schema"></a>
### firewall\_policy\_template\_delete\_put\_success\_schema

|Name|Schema|
|---|---|
|**firewall\_policy\_template\_delete**  <br>*optional*|[firewall\_policy\_template\_delete](#firewall\_policy\_template\_delete\_put\_success\_schema-firewall\_policy\_template\_delete)|

<a name="firewall\_policy\_template\_delete\_put\_success\_schema-firewall\_policy\_template\_delete"></a>
**firewall\_policy\_template\_delete**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="firewall\_policy\_template\_delete\_request\_schema"></a>
### firewall\_policy\_template\_delete\_request\_schema

|Name|Schema|
|---|---|
|**firewall\_policy\_template\_delete**  <br>*optional*|[firewall\_policy\_template\_delete](#firewall\_policy\_template\_delete)|


<a name="firewall\_policy\_template\_delete\_response\_schema"></a>
### firewall\_policy\_template\_delete\_response\_schema
*Type* : < [firewall\_policy\_template\_delete\_response\_schema](#firewall\_policy\_template\_delete\_response\_schema-inline) > array

<a name="firewall\_policy\_template\_delete\_response\_schema-inline"></a>
**firewall\_policy\_template\_delete\_response\_schema**

|Name|Schema|
|---|---|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**template\_name**  <br>*optional*|[template\_name](#template\_name)|


<a name="package\_name"></a>
### package\_name
Config package name using which the API operation should be performed.

*Type* : string


<a name="site\_name"></a>
### site\_name
Site Name

*Type* : string


<a name="template\_name"></a>
### template\_name
firewall policy template name

*Type* : string






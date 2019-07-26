# license\_server\_host\_id


<a name="overview"></a>
## Overview
This resource can be used to get the License server Host ID Details.


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/license/  
*Schemes* : HTTP


### Tags

* license\_server\_host\_id : Operations related to license\_server\_host\_id 




<a name="paths"></a>
## Paths

<a name="license\_server\_host\_id-get"></a>
### Get operation for license\_server\_host\_id
```
GET /license_server_host_id
```


#### Description
Use this operation to get the License Server Host ID Details.


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[license\_server\_host\_id\_response\_schema](#license\_server\_host\_id\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* license\_server\_host\_id




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="host\_id"></a>
### host\_id
The Host Id of the license server

*Type* : string


<a name="license\_server\_host\_id\_delete\_success\_schema"></a>
### license\_server\_host\_id\_delete\_success\_schema

|Name|Schema|
|---|---|
|**license\_server\_host\_id**  <br>*optional*|[license\_server\_host\_id](#license\_server\_host\_id\_delete\_success\_schema-license\_server\_host\_id)|

<a name="license\_server\_host\_id\_delete\_success\_schema-license\_server\_host\_id"></a>
**license\_server\_host\_id**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="license\_server\_host\_id\_post\_success\_schema"></a>
### license\_server\_host\_id\_post\_success\_schema

|Name|Schema|
|---|---|
|**license\_server\_host\_id**  <br>*optional*|[license\_server\_host\_id](#license\_server\_host\_id\_post\_success\_schema-license\_server\_host\_id)|

<a name="license\_server\_host\_id\_post\_success\_schema-license\_server\_host\_id"></a>
**license\_server\_host\_id**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="license\_server\_host\_id\_put\_success\_schema"></a>
### license\_server\_host\_id\_put\_success\_schema

|Name|Schema|
|---|---|
|**license\_server\_host\_id**  <br>*optional*|[license\_server\_host\_id](#license\_server\_host\_id\_put\_success\_schema-license\_server\_host\_id)|

<a name="license\_server\_host\_id\_put\_success\_schema-license\_server\_host\_id"></a>
**license\_server\_host\_id**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="license\_server\_host\_id\_response\_schema"></a>
### license\_server\_host\_id\_response\_schema
*Type* : < [license\_server\_host\_id\_response\_schema](#license\_server\_host\_id\_response\_schema-inline) > array

<a name="license\_server\_host\_id\_response\_schema-inline"></a>
**license\_server\_host\_id\_response\_schema**

|Name|Schema|
|---|---|
|**host\_id**  <br>*optional*|[host\_id](#host\_id)|






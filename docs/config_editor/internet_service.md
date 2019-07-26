# internet\_service


<a name="overview"></a>
## Overview
API to add, delete, get, modify Internet Services


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* internet\_service : Operations related to internet\_service 




<a name="paths"></a>
## Paths

<a name="internet\_service-post"></a>
### POST operation for internet\_service
```
POST /internet_service
```


#### Description
Use this operation to add Intranet services


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[internet\_service\_post\_success\_schema](#internet\_service\_post\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* internet\_service


<a name="internet\_service-get"></a>
### Get operation for internet\_service
```
GET /internet_service
```


#### Description
Use this operation to get the list of Intranet Services with basic settings


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[internet\_service\_response\_schema](#internet\_service\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* internet\_service


<a name="internet\_service-put"></a>
### PUT operation for internet\_service
```
PUT /internet_service
```


#### Description
Use this operation to modify Intranet services


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[internet\_service\_request\_schema](#internet\_service\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[internet\_service\_put\_success\_schema](#internet\_service\_put\_success\_schema)|
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

* internet\_service


<a name="internet\_service-deletepathparam-delete"></a>
### DELETE operation for internet\_service
```
DELETE /internet_service/{deletePathParam}
```


#### Description
Use this operation to delete Intranet services


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[internet\_service\_delete\_success\_schema](#internet\_service\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* internet\_service




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
Auto-generated ID to uniquely identify internet service

*Type* : integer


<a name="internet\_service"></a>
### internet\_service

|Name|Schema|
|---|---|
|**id**  <br>*optional*|[id](#id)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**properties**  <br>*optional*|[properties](#properties)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|


<a name="internet\_service\_delete\_success\_schema"></a>
### internet\_service\_delete\_success\_schema

|Name|Schema|
|---|---|
|**internet\_service**  <br>*optional*|[internet\_service](#internet\_service\_delete\_success\_schema-internet\_service)|

<a name="internet\_service\_delete\_success\_schema-internet\_service"></a>
**internet\_service**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="internet\_service\_post\_success\_schema"></a>
### internet\_service\_post\_success\_schema

|Name|Schema|
|---|---|
|**internet\_service**  <br>*optional*|[internet\_service](#internet\_service\_post\_success\_schema-internet\_service)|

<a name="internet\_service\_post\_success\_schema-internet\_service"></a>
**internet\_service**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="internet\_service\_put\_success\_schema"></a>
### internet\_service\_put\_success\_schema

|Name|Schema|
|---|---|
|**internet\_service**  <br>*optional*|[internet\_service](#internet\_service\_put\_success\_schema-internet\_service)|

<a name="internet\_service\_put\_success\_schema-internet\_service"></a>
**internet\_service**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="internet\_service\_request\_schema"></a>
### internet\_service\_request\_schema

|Name|Schema|
|---|---|
|**internet\_service**  <br>*optional*|[internet\_service](#internet\_service)|


<a name="internet\_service\_response\_schema"></a>
### internet\_service\_response\_schema
*Type* : < [internet\_service\_response\_schema](#internet\_service\_response\_schema-inline) > array

<a name="internet\_service\_response\_schema-inline"></a>
**internet\_service\_response\_schema**

|Name|Schema|
|---|---|
|**id**  <br>*optional*|[id](#id)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**properties**  <br>*optional*|[properties](#properties)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|


<a name="package\_name"></a>
### package\_name
Config package name using which the site API operation should be performed.

*Type* : string


<a name="properties"></a>
### properties
Internet Service Properties


|Name|Description|Schema|
|---|---|---|
|**default\_route\_cost**  <br>*optional*|The route cost, 1-65534, that will be used for the default internet route added to this appliance|integer|
|**default\_set**  <br>*optional*|The name of the Default Set that will be used to populate rules for the Service on the Site. Pass <none> to set <none> as the value|string|
|**enable\_primary\_reclaim**  <br>*optional*|If enabled, the (use=primary) Usage associated with this service on a WAN Link will forcefully reclaim status as the active service on that WAN Link|boolean|
|**export\_default\_routes**  <br>*optional*|If enabled, the default route for the Internet Service, 0.0.0.0/0, will be exported to other Sites if WAN-to-WAN Forwarding has been enabled|boolean|
|**ignore\_wanlink\_status**  <br>*optional*|If enabled, packets destined for this service will still choose this service even if all WAN Links for this service are unavailable|boolean|


<a name="site\_name"></a>
### site\_name
Site Name

*Type* : string






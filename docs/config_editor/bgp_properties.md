# bgp\_properties


<a name="overview"></a>
## Overview
API to edit basic properties for BGP


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* bgp\_properties : Operations related to bgp\_properties 




<a name="paths"></a>
## Paths

<a name="bgp\_properties-get"></a>
### Get operation for bgp\_properties
```
GET /bgp_properties
```


#### Description
Use this operation to get the basic BGP properties


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[bgp\_properties\_response\_schema](#bgp\_properties\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* bgp\_properties


<a name="bgp\_properties-put"></a>
### PUT operation for bgp\_properties
```
PUT /bgp_properties
```


#### Description
Use this operation to modify the basic BGP properties


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[bgp\_properties\_request\_schema](#bgp\_properties\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[bgp\_properties\_put\_success\_schema](#bgp\_properties\_put\_success\_schema)|
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

* bgp\_properties




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="advertise\_ospf\_routes"></a>
### advertise\_ospf\_routes
Set to true to allow routes learnt from OSPF peers to be advertised via BGP.

*Type* : boolean


<a name="advertise\_sdwan\_routes"></a>
### advertise\_sdwan\_routes
Set to true to allow SD-WAN routes to be advertised via BGP.

*Type* : boolean


<a name="bgp\_properties"></a>
### bgp\_properties

|Name|Schema|
|---|---|
|**advertise\_ospf\_routes**  <br>*optional*|[advertise\_ospf\_routes](#advertise\_ospf\_routes)|
|**advertise\_sdwan\_routes**  <br>*optional*|[advertise\_sdwan\_routes](#advertise\_sdwan\_routes)|
|**enable**  <br>*optional*|[enable](#enable)|
|**local\_autonomous\_system**  <br>*optional*|[local\_autonomous\_system](#local\_autonomous\_system)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**router\_id**  <br>*optional*|[router\_id](#router\_id)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|


<a name="bgp\_properties\_delete\_success\_schema"></a>
### bgp\_properties\_delete\_success\_schema

|Name|Schema|
|---|---|
|**bgp\_properties**  <br>*optional*|[bgp\_properties](#bgp\_properties\_delete\_success\_schema-bgp\_properties)|

<a name="bgp\_properties\_delete\_success\_schema-bgp\_properties"></a>
**bgp\_properties**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="bgp\_properties\_post\_success\_schema"></a>
### bgp\_properties\_post\_success\_schema

|Name|Schema|
|---|---|
|**bgp\_properties**  <br>*optional*|[bgp\_properties](#bgp\_properties\_post\_success\_schema-bgp\_properties)|

<a name="bgp\_properties\_post\_success\_schema-bgp\_properties"></a>
**bgp\_properties**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="bgp\_properties\_put\_success\_schema"></a>
### bgp\_properties\_put\_success\_schema

|Name|Schema|
|---|---|
|**bgp\_properties**  <br>*optional*|[bgp\_properties](#bgp\_properties\_put\_success\_schema-bgp\_properties)|

<a name="bgp\_properties\_put\_success\_schema-bgp\_properties"></a>
**bgp\_properties**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="bgp\_properties\_request\_schema"></a>
### bgp\_properties\_request\_schema

|Name|Schema|
|---|---|
|**bgp\_properties**  <br>*optional*|[bgp\_properties](#bgp\_properties)|


<a name="bgp\_properties\_response\_schema"></a>
### bgp\_properties\_response\_schema
*Type* : < [bgp\_properties\_response\_schema](#bgp\_properties\_response\_schema-inline) > array

<a name="bgp\_properties\_response\_schema-inline"></a>
**bgp\_properties\_response\_schema**

|Name|Schema|
|---|---|
|**advertise\_ospf\_routes**  <br>*optional*|[advertise\_ospf\_routes](#advertise\_ospf\_routes)|
|**advertise\_sdwan\_routes**  <br>*optional*|[advertise\_sdwan\_routes](#advertise\_sdwan\_routes)|
|**enable**  <br>*optional*|[enable](#enable)|
|**local\_autonomous\_system**  <br>*optional*|[local\_autonomous\_system](#local\_autonomous\_system)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**router\_id**  <br>*optional*|[router\_id](#router\_id)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|


<a name="enable"></a>
### enable
Set to true to enable BGP.

*Type* : boolean


<a name="local\_autonomous\_system"></a>
### local\_autonomous\_system
Enter the Local Autonomous System number to learn routes from and advertise routes to. This must match what is configured on the neighboring routers.

*Type* : integer


<a name="package\_name"></a>
### package\_name
Config package name using which the site API operation should be performed.

*Type* : string


<a name="router\_id"></a>
### router\_id
A unique identifier, in IPv4 format, used for BGP advertisements

*Type* : string


<a name="site\_name"></a>
### site\_name
Site Name

*Type* : string






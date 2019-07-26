# ospf\_properties


<a name="overview"></a>
## Overview
API to edit basic properties for OSPF


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* ospf\_properties : Operations related to ospf\_properties 




<a name="paths"></a>
## Paths

<a name="ospf\_properties-get"></a>
### Get operation for ospf\_properties
```
GET /ospf_properties
```


#### Description
Use this operation to get the basic OSPF properties


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[ospf\_properties\_response\_schema](#ospf\_properties\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* ospf\_properties


<a name="ospf\_properties-put"></a>
### PUT operation for ospf\_properties
```
PUT /ospf_properties
```


#### Description
Use this operation to modify the basic OSPF properties


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[ospf\_properties\_request\_schema](#ospf\_properties\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[ospf\_properties\_put\_success\_schema](#ospf\_properties\_put\_success\_schema)|
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

* ospf\_properties




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="advertise\_bgp\_routes"></a>
### advertise\_bgp\_routes
Set to true to advertise the routes learnt from BGP peers to the OSPF peers.

*Type* : boolean


<a name="advertise\_sdwan\_routes"></a>
### advertise\_sdwan\_routes
Set to true to allow SD-WAN routes to be advertised via OSPF.

*Type* : boolean


<a name="enabled"></a>
### enabled
Set to true to enable OSPF.

*Type* : boolean


<a name="export\_ospf\_route\_type"></a>
### export\_ospf\_route\_type
Advertise the SD-WAN route to OSPF neighbors as type-1 Intra-area route or type-5 External route. Default route is always advertised as type-5 External route to normal areas and type-1 summary route to stub areas.

*Type* : enum (type\_1, type\_5)


<a name="export\_ospf\_route\_weight"></a>
### export\_ospf\_route\_weight
When export SD-WAN routes to OSPF, add the weight to each route's SD-WAN cost as total cost

*Type* : integer


<a name="ospf\_properties"></a>
### ospf\_properties

|Name|Schema|
|---|---|
|**advertise\_bgp\_routes**  <br>*optional*|[advertise\_bgp\_routes](#advertise\_bgp\_routes)|
|**advertise\_sdwan\_routes**  <br>*optional*|[advertise\_sdwan\_routes](#advertise\_sdwan\_routes)|
|**enabled**  <br>*optional*|[enabled](#enabled)|
|**export\_ospf\_route\_type**  <br>*optional*|[export\_ospf\_route\_type](#export\_ospf\_route\_type)|
|**export\_ospf\_route\_weight**  <br>*optional*|[export\_ospf\_route\_weight](#export\_ospf\_route\_weight)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**router\_id**  <br>*optional*|[router\_id](#router\_id)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|


<a name="ospf\_properties\_delete\_success\_schema"></a>
### ospf\_properties\_delete\_success\_schema

|Name|Schema|
|---|---|
|**ospf\_properties**  <br>*optional*|[ospf\_properties](#ospf\_properties\_delete\_success\_schema-ospf\_properties)|

<a name="ospf\_properties\_delete\_success\_schema-ospf\_properties"></a>
**ospf\_properties**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="ospf\_properties\_post\_success\_schema"></a>
### ospf\_properties\_post\_success\_schema

|Name|Schema|
|---|---|
|**ospf\_properties**  <br>*optional*|[ospf\_properties](#ospf\_properties\_post\_success\_schema-ospf\_properties)|

<a name="ospf\_properties\_post\_success\_schema-ospf\_properties"></a>
**ospf\_properties**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="ospf\_properties\_put\_success\_schema"></a>
### ospf\_properties\_put\_success\_schema

|Name|Schema|
|---|---|
|**ospf\_properties**  <br>*optional*|[ospf\_properties](#ospf\_properties\_put\_success\_schema-ospf\_properties)|

<a name="ospf\_properties\_put\_success\_schema-ospf\_properties"></a>
**ospf\_properties**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="ospf\_properties\_request\_schema"></a>
### ospf\_properties\_request\_schema

|Name|Schema|
|---|---|
|**ospf\_properties**  <br>*optional*|[ospf\_properties](#ospf\_properties)|


<a name="ospf\_properties\_response\_schema"></a>
### ospf\_properties\_response\_schema
*Type* : < [ospf\_properties\_response\_schema](#ospf\_properties\_response\_schema-inline) > array

<a name="ospf\_properties\_response\_schema-inline"></a>
**ospf\_properties\_response\_schema**

|Name|Schema|
|---|---|
|**advertise\_bgp\_routes**  <br>*optional*|[advertise\_bgp\_routes](#advertise\_bgp\_routes)|
|**advertise\_sdwan\_routes**  <br>*optional*|[advertise\_sdwan\_routes](#advertise\_sdwan\_routes)|
|**enabled**  <br>*optional*|[enabled](#enabled)|
|**export\_ospf\_route\_type**  <br>*optional*|[export\_ospf\_route\_type](#export\_ospf\_route\_type)|
|**export\_ospf\_route\_weight**  <br>*optional*|[export\_ospf\_route\_weight](#export\_ospf\_route\_weight)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**router\_id**  <br>*optional*|[router\_id](#router\_id)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|


<a name="package\_name"></a>
### package\_name
Config package name using which the site API operation should be performed.

*Type* : string


<a name="router\_id"></a>
### router\_id
A unique identifier in IPv4 format, used for OSPF advertisements.

*Type* : string


<a name="site\_name"></a>
### site\_name
Site Name

*Type* : string






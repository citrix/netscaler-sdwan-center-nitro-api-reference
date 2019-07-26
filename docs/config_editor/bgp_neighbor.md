# bgp\_neighbor


<a name="overview"></a>
## Overview
API to add, delete, get, modify BGP neighbours - All of the configured BGP peer routers that are scrutinized to find the shortest paths for data. All of the neighbors must be part of the same Autonomous System.


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* bgp\_neighbor : Operations related to bgp\_neighbor 




<a name="paths"></a>
## Paths

<a name="bgp\_neighbor-post"></a>
### POST operation for bgp\_neighbor
```
POST /bgp_neighbor
```


#### Description
Use this operation to add BGP neighbours


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[bgp\_neighbor\_post\_success\_schema](#bgp\_neighbor\_post\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* bgp\_neighbor


<a name="bgp\_neighbor-get"></a>
### Get operation for bgp\_neighbor
```
GET /bgp_neighbor
```


#### Description
Use this operation to get BGP neighbours


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[bgp\_neighbor\_response\_schema](#bgp\_neighbor\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* bgp\_neighbor


<a name="bgp\_neighbor-put"></a>
### PUT operation for bgp\_neighbor
```
PUT /bgp_neighbor
```


#### Description
Use this operation to modify BGP neighbours


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[bgp\_neighbor\_request\_schema](#bgp\_neighbor\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[bgp\_neighbor\_put\_success\_schema](#bgp\_neighbor\_put\_success\_schema)|
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

* bgp\_neighbor


<a name="bgp\_neighbor-deletepathparam-delete"></a>
### DELETE operation for bgp\_neighbor
```
DELETE /bgp_neighbor/{deletePathParam}
```


#### Description
Use this operation to delete BGP neighbours


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[bgp\_neighbor\_delete\_success\_schema](#bgp\_neighbor\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* bgp\_neighbor




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="bgp\_neighbor"></a>
### bgp\_neighbor

|Name|Schema|
|---|---|
|**bgp\_neighbor\_policy**  <br>*optional*|[bgp\_neighbor\_policy](#bgp\_neighbor\_policy)|
|**bgp\_neighbor\_properties**  <br>*optional*|[bgp\_neighbor\_properties](#bgp\_neighbor\_properties)|
|**id**  <br>*optional*|[id](#id)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|


<a name="bgp\_neighbor\_delete\_success\_schema"></a>
### bgp\_neighbor\_delete\_success\_schema

|Name|Schema|
|---|---|
|**bgp\_neighbor**  <br>*optional*|[bgp\_neighbor](#bgp\_neighbor\_delete\_success\_schema-bgp\_neighbor)|

<a name="bgp\_neighbor\_delete\_success\_schema-bgp\_neighbor"></a>
**bgp\_neighbor**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="bgp\_neighbor\_policy"></a>
### bgp\_neighbor\_policy
BGP neighbour policies

*Type* : < [bgp\_neighbor\_policy](#bgp\_neighbor\_policy-inline) > array

<a name="bgp\_neighbor\_policy-inline"></a>
**bgp\_neighbor\_policy**

|Name|Description|Schema|
|---|---|---|
|**as\_path**  <br>*optional*|The AS Path of the BGP Route|string|
|**bgp\_policy**  <br>*optional*|Choose a configured BGP policy to apply against the matching routes or select default </b>Accept</b> or </Reject> policies to either accept or reject all matching routes.|string|
|**community\_string\_asn**  <br>*optional*|The ASN for which the BGP Community was configured.|integer|
|**community\_string\_list\_name**  <br>*optional*|BGP community string list|string|
|**community\_string\_value**  <br>*optional*|The Value of the BGP Community that we are using for matching route(s)|integer|
|**direction**  <br>*optional*|Choose the direction in which the BGP policy is applied|enum (in, out)|
|**id**  <br>*optional*|Auto-generated ID to uniquely identify the policy|integer|
|**network\_ip\_address**  <br>*optional*|IP address with subnet|string|
|**network\_object\_name**  <br>*optional*|The Network Object that describes the route's destination for matching|string|
|**order**  <br>*optional*|The Order in which policies are prioritized. Once policies are applied, they are automatically sorted by Order.|integer|


<a name="bgp\_neighbor\_post\_success\_schema"></a>
### bgp\_neighbor\_post\_success\_schema

|Name|Schema|
|---|---|
|**bgp\_neighbor**  <br>*optional*|[bgp\_neighbor](#bgp\_neighbor\_post\_success\_schema-bgp\_neighbor)|

<a name="bgp\_neighbor\_post\_success\_schema-bgp\_neighbor"></a>
**bgp\_neighbor**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="bgp\_neighbor\_properties"></a>
### bgp\_neighbor\_properties
BGP neighbour properties


|Name|Description|Schema|
|---|---|---|
|**hold\_time**  <br>*optional*|Enter the Hold Time, in seconds, to wait before declaring a neighbor down (the default is 180).|integer|
|**id**  <br>*optional*|Auto-generated ID to uniquely identify the property|integer|
|**igp\_metric**  <br>*optional*|To enable the comparison of internal distances to calculate the best route.|boolean|
|**local\_preference**  <br>*optional*|Enter the Local Preference value which is used for selecting from multiple BGP routes (the default is 100).|integer|
|**multihop**  <br>*optional*|Set to true if the neighbour is a few hops away. The default multihop count is 255. This is by default selected, but if the neighbour is directly connected, it can be set to false|boolean|
|**neighbor\_as**  <br>*optional*|Enter the Local Autonomous System number to learn routes from and advertise routes to. This must match what is configured on the neighboring routers.|integer|
|**neighbor\_ip\_address**  <br>*optional*|IP address of the BGP neighbour router|string|
|**password**  <br>*optional*|Enter a password for MD5 authentication of BGP sessions (authentication is not required).|string|
|**routing\_domain**  <br>*optional*  <br>*read-only*|Routing domain|string|
|**virtual\_interface\_name**  <br>*optional*|The Virtual Interface|string|


<a name="bgp\_neighbor\_put\_success\_schema"></a>
### bgp\_neighbor\_put\_success\_schema

|Name|Schema|
|---|---|
|**bgp\_neighbor**  <br>*optional*|[bgp\_neighbor](#bgp\_neighbor\_put\_success\_schema-bgp\_neighbor)|

<a name="bgp\_neighbor\_put\_success\_schema-bgp\_neighbor"></a>
**bgp\_neighbor**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="bgp\_neighbor\_request\_schema"></a>
### bgp\_neighbor\_request\_schema

|Name|Schema|
|---|---|
|**bgp\_neighbor**  <br>*optional*|[bgp\_neighbor](#bgp\_neighbor)|


<a name="bgp\_neighbor\_response\_schema"></a>
### bgp\_neighbor\_response\_schema
*Type* : < [bgp\_neighbor\_response\_schema](#bgp\_neighbor\_response\_schema-inline) > array

<a name="bgp\_neighbor\_response\_schema-inline"></a>
**bgp\_neighbor\_response\_schema**

|Name|Schema|
|---|---|
|**bgp\_neighbor\_policy**  <br>*optional*|[bgp\_neighbor\_policy](#bgp\_neighbor\_policy)|
|**bgp\_neighbor\_properties**  <br>*optional*|[bgp\_neighbor\_properties](#bgp\_neighbor\_properties)|
|**id**  <br>*optional*|[id](#id)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|


<a name="id"></a>
### id
Auto-generated ID to uniquely identify BGP Neighbour

*Type* : integer


<a name="package\_name"></a>
### package\_name
Config package name using which the site API operation should be performed.

*Type* : string


<a name="site\_name"></a>
### site\_name
Site Name

*Type* : string






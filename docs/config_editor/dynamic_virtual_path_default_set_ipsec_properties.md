# dynamic\_virtual\_path\_default\_set\_ipsec\_properties


<a name="overview"></a>
## Overview
API to modify, get Dynamic Virtual Path Default Set IPsec settings


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* dynamic\_virtual\_path\_default\_set\_ipsec\_properties : Operations related to dynamic\_virtual\_path\_default\_set\_ipsec\_properties 




<a name="paths"></a>
## Paths

<a name="dynamic\_virtual\_path\_default\_set\_ipsec\_properties-get"></a>
### Get operation for dynamic\_virtual\_path\_default\_set\_ipsec\_properties
```
GET /dynamic_virtual_path_default_set_ipsec_properties
```


#### Description
Use this operation to get the Dynamic Virtual Path Default Set IPsec settings


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[dynamic\_virtual\_path\_default\_set\_ipsec\_properties\_response\_schema](#dynamic\_virtual\_path\_default\_set\_ipsec\_properties\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* dynamic\_virtual\_path\_default\_set\_ipsec\_properties


<a name="dynamic\_virtual\_path\_default\_set\_ipsec\_properties-put"></a>
### PUT operation for dynamic\_virtual\_path\_default\_set\_ipsec\_properties
```
PUT /dynamic_virtual_path_default_set_ipsec_properties
```


#### Description
Use this operation to modify Dynamic Virtual Path Default Set IPsec settings


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[dynamic\_virtual\_path\_default\_set\_ipsec\_properties\_request\_schema](#dynamic\_virtual\_path\_default\_set\_ipsec\_properties\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[dynamic\_virtual\_path\_default\_set\_ipsec\_properties\_put\_success\_schema](#dynamic\_virtual\_path\_default\_set\_ipsec\_properties\_put\_success\_schema)|
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

* dynamic\_virtual\_path\_default\_set\_ipsec\_properties




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="dynamic\_virtual\_path\_default\_set\_ipsec\_properties"></a>
### dynamic\_virtual\_path\_default\_set\_ipsec\_properties

|Name|Schema|
|---|---|
|**encapsulation\_type**  <br>*optional*|[encapsulation\_type](#encapsulation\_type)|
|**encryption\_mode**  <br>*optional*|[encryption\_mode](#encryption\_mode)|
|**hash\_algorithm**  <br>*optional*|[hash\_algorithm](#hash\_algorithm)|
|**id**  <br>*optional*|[id](#id)|
|**lifetime**  <br>*optional*|[lifetime](#lifetime)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**secure\_virtual\_path\_user\_data\_with\_ipsec**  <br>*optional*|[secure\_virtual\_path\_user\_data\_with\_ipsec](#secure\_virtual\_path\_user\_data\_with\_ipsec)|


<a name="dynamic\_virtual\_path\_default\_set\_ipsec\_properties\_delete\_success\_schema"></a>
### dynamic\_virtual\_path\_default\_set\_ipsec\_properties\_delete\_success\_schema

|Name|Schema|
|---|---|
|**dynamic\_virtual\_path\_default\_set\_ipsec\_properties**  <br>*optional*|[dynamic\_virtual\_path\_default\_set\_ipsec\_properties](#dynamic\_virtual\_path\_default\_set\_ipsec\_properties\_delete\_success\_schema-dynamic\_virtual\_path\_default\_set\_ipsec\_properties)|

<a name="dynamic\_virtual\_path\_default\_set\_ipsec\_properties\_delete\_success\_schema-dynamic\_virtual\_path\_default\_set\_ipsec\_properties"></a>
**dynamic\_virtual\_path\_default\_set\_ipsec\_properties**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="dynamic\_virtual\_path\_default\_set\_ipsec\_properties\_post\_success\_schema"></a>
### dynamic\_virtual\_path\_default\_set\_ipsec\_properties\_post\_success\_schema

|Name|Schema|
|---|---|
|**dynamic\_virtual\_path\_default\_set\_ipsec\_properties**  <br>*optional*|[dynamic\_virtual\_path\_default\_set\_ipsec\_properties](#dynamic\_virtual\_path\_default\_set\_ipsec\_properties\_post\_success\_schema-dynamic\_virtual\_path\_default\_set\_ipsec\_properties)|

<a name="dynamic\_virtual\_path\_default\_set\_ipsec\_properties\_post\_success\_schema-dynamic\_virtual\_path\_default\_set\_ipsec\_properties"></a>
**dynamic\_virtual\_path\_default\_set\_ipsec\_properties**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="dynamic\_virtual\_path\_default\_set\_ipsec\_properties\_put\_success\_schema"></a>
### dynamic\_virtual\_path\_default\_set\_ipsec\_properties\_put\_success\_schema

|Name|Schema|
|---|---|
|**dynamic\_virtual\_path\_default\_set\_ipsec\_properties**  <br>*optional*|[dynamic\_virtual\_path\_default\_set\_ipsec\_properties](#dynamic\_virtual\_path\_default\_set\_ipsec\_properties\_put\_success\_schema-dynamic\_virtual\_path\_default\_set\_ipsec\_properties)|

<a name="dynamic\_virtual\_path\_default\_set\_ipsec\_properties\_put\_success\_schema-dynamic\_virtual\_path\_default\_set\_ipsec\_properties"></a>
**dynamic\_virtual\_path\_default\_set\_ipsec\_properties**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="dynamic\_virtual\_path\_default\_set\_ipsec\_properties\_request\_schema"></a>
### dynamic\_virtual\_path\_default\_set\_ipsec\_properties\_request\_schema

|Name|Schema|
|---|---|
|**dynamic\_virtual\_path\_default\_set\_ipsec\_properties**  <br>*optional*|[dynamic\_virtual\_path\_default\_set\_ipsec\_properties](#dynamic\_virtual\_path\_default\_set\_ipsec\_properties)|


<a name="dynamic\_virtual\_path\_default\_set\_ipsec\_properties\_response\_schema"></a>
### dynamic\_virtual\_path\_default\_set\_ipsec\_properties\_response\_schema
*Type* : < [dynamic\_virtual\_path\_default\_set\_ipsec\_properties\_response\_schema](#dynamic\_virtual\_path\_default\_set\_ipsec\_properties\_response\_schema-inline) > array

<a name="dynamic\_virtual\_path\_default\_set\_ipsec\_properties\_response\_schema-inline"></a>
**dynamic\_virtual\_path\_default\_set\_ipsec\_properties\_response\_schema**

|Name|Schema|
|---|---|
|**dynamic\_virtual\_path\_default\_set\_name**  <br>*optional*|[dynamic\_virtual\_path\_default\_set\_name](#dynamic\_virtual\_path\_default\_set\_name)|
|**encapsulation\_type**  <br>*optional*|[encapsulation\_type](#encapsulation\_type)|
|**encryption\_mode**  <br>*optional*|[encryption\_mode](#encryption\_mode)|
|**hash\_algorithm**  <br>*optional*|[hash\_algorithm](#hash\_algorithm)|
|**id**  <br>*optional*|[id](#id)|
|**lifetime**  <br>*optional*|[lifetime](#lifetime)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**secure\_virtual\_path\_user\_data\_with\_ipsec**  <br>*optional*|[secure\_virtual\_path\_user\_data\_with\_ipsec](#secure\_virtual\_path\_user\_data\_with\_ipsec)|


<a name="dynamic\_virtual\_path\_default\_set\_name"></a>
### dynamic\_virtual\_path\_default\_set\_name
Dynamic Virtual path default set name using which the API operation should be performed.

*Type* : string


<a name="encapsulation\_type"></a>
### encapsulation\_type
Choose an IPsec protocol

*Type* : enum (esp, esp\_auth, ah)


<a name="encryption\_mode"></a>
### encryption\_mode
If you chose ESP as the Tunnel Mode for this Virtual Path, choose an Encryption Algorithm.

*Type* : enum (aes128, aes256)


<a name="hash\_algorithm"></a>
### hash\_algorithm
If you chose AH or ESP+Auth as the Tunnel Mode for this Virtual Path, choose a Hash Algorithm.

*Type* : enum (sha, sha256)


<a name="id"></a>
### id
Auto-generated ID to uniquely identify Virtual Path Default Set IPsec settings

*Type* : integer


<a name="lifetime"></a>
### lifetime
Enter the amount of time, in seconds, for an IPsec security association to exist.

*Type* : integer


<a name="package\_name"></a>
### package\_name
Config package name using which the API operation should be performed.

*Type* : string


<a name="secure\_virtual\_path\_user\_data\_with\_ipsec"></a>
### secure\_virtual\_path\_user\_data\_with\_ipsec
Enable Secure Virtual Path User Data with IPsec to secure all user data in the Virtual Path using an IPsec tunnel.

*Type* : boolean






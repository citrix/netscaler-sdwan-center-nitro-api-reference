# ssl\_certificate


<a name="overview"></a>
## Overview
This resource can be used to edit SSL Certificate.


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config/  
*Schemes* : HTTP


### Tags

* ssl\_certificate : Operations related to ssl\_certificate 




<a name="paths"></a>
## Paths

<a name="ssl\_certificate-post"></a>
### POST operation for ssl\_certificate
```
POST /ssl_certificate
```


#### Description
Use this operation to download ssl certificate.


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Query**|**action**  <br>*required*|Select if action is other that ADD|enum (download\_certificate, regenerate\_certificate)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[ssl\_certificate\_post\_success\_schema](#ssl\_certificate\_post\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* ssl\_certificate


<a name="ssl\_certificate-get"></a>
### Get operation for ssl\_certificate
```
GET /ssl_certificate
```


#### Description
Use this operation to get the Certificate Details.


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[ssl\_certificate\_response\_schema](#ssl\_certificate\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* ssl\_certificate




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="expiry\_date"></a>
### expiry\_date
The expiry date of the Certificate

*Type* : string


<a name="fingerprint"></a>
### fingerprint
The FingerPrint of the Certificate

*Type* : string


<a name="ssl\_certificate\_delete\_success\_schema"></a>
### ssl\_certificate\_delete\_success\_schema

|Name|Schema|
|---|---|
|**ssl\_certificate**  <br>*optional*|[ssl\_certificate](#ssl\_certificate\_delete\_success\_schema-ssl\_certificate)|

<a name="ssl\_certificate\_delete\_success\_schema-ssl\_certificate"></a>
**ssl\_certificate**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="ssl\_certificate\_post\_success\_schema"></a>
### ssl\_certificate\_post\_success\_schema

|Name|Schema|
|---|---|
|**ssl\_certificate**  <br>*optional*|[ssl\_certificate](#ssl\_certificate\_post\_success\_schema-ssl\_certificate)|

<a name="ssl\_certificate\_post\_success\_schema-ssl\_certificate"></a>
**ssl\_certificate**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="ssl\_certificate\_put\_success\_schema"></a>
### ssl\_certificate\_put\_success\_schema

|Name|Schema|
|---|---|
|**ssl\_certificate**  <br>*optional*|[ssl\_certificate](#ssl\_certificate\_put\_success\_schema-ssl\_certificate)|

<a name="ssl\_certificate\_put\_success\_schema-ssl\_certificate"></a>
**ssl\_certificate**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="ssl\_certificate\_response\_schema"></a>
### ssl\_certificate\_response\_schema
*Type* : < [ssl\_certificate\_response\_schema](#ssl\_certificate\_response\_schema-inline) > array

<a name="ssl\_certificate\_response\_schema-inline"></a>
**ssl\_certificate\_response\_schema**

|Name|Schema|
|---|---|
|**expiry\_date**  <br>*optional*|[expiry\_date](#expiry\_date)|
|**fingerprint**  <br>*optional*|[fingerprint](#fingerprint)|
|**start\_date**  <br>*optional*|[start\_date](#start\_date)|


<a name="start\_date"></a>
### start\_date
The Start Date of the Certificate.

*Type* : string






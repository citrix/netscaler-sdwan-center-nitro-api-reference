# license\_details


<a name="overview"></a>
## Overview
This resource can be used to get the License Details.


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/license/  
*Schemes* : HTTP


### Tags

* license\_details : Operations related to license\_details 




<a name="paths"></a>
## Paths

<a name="license\_details-get"></a>
### Get operation for license\_details
```
GET /license_details
```


#### Description
Use this operation to get the License Details.


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[license\_details\_response\_schema](#license\_details\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* license\_details




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
The Expiry Date of the license.

*Type* : string


<a name="in\_use\_count"></a>
### in\_use\_count
Use count of the license

*Type* : string


<a name="license\_details\_delete\_success\_schema"></a>
### license\_details\_delete\_success\_schema

|Name|Schema|
|---|---|
|**license\_details**  <br>*optional*|[license\_details](#license\_details\_delete\_success\_schema-license\_details)|

<a name="license\_details\_delete\_success\_schema-license\_details"></a>
**license\_details**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="license\_details\_post\_success\_schema"></a>
### license\_details\_post\_success\_schema

|Name|Schema|
|---|---|
|**license\_details**  <br>*optional*|[license\_details](#license\_details\_post\_success\_schema-license\_details)|

<a name="license\_details\_post\_success\_schema-license\_details"></a>
**license\_details**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="license\_details\_put\_success\_schema"></a>
### license\_details\_put\_success\_schema

|Name|Schema|
|---|---|
|**license\_details**  <br>*optional*|[license\_details](#license\_details\_put\_success\_schema-license\_details)|

<a name="license\_details\_put\_success\_schema-license\_details"></a>
**license\_details**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="license\_details\_response\_schema"></a>
### license\_details\_response\_schema
*Type* : < [license\_details\_response\_schema](#license\_details\_response\_schema-inline) > array

<a name="license\_details\_response\_schema-inline"></a>
**license\_details\_response\_schema**

|Name|Schema|
|---|---|
|**expiry\_date**  <br>*optional*|[expiry\_date](#expiry\_date)|
|**in\_use\_count**  <br>*optional*|[in\_use\_count](#in\_use\_count)|
|**license\_type**  <br>*optional*|[license\_type](#license\_type)|
|**maintenance\_expiry**  <br>*optional*|[maintenance\_expiry](#maintenance\_expiry)|
|**model**  <br>*optional*|[model](#model)|
|**total\_count**  <br>*optional*|[total\_count](#total\_count)|


<a name="license\_type"></a>
### license\_type
The type of License

*Type* : string


<a name="maintenance\_expiry"></a>
### maintenance\_expiry
The maintenance expiry date of the License

*Type* : string


<a name="model"></a>
### model
The License Model

*Type* : string


<a name="total\_count"></a>
### total\_count
Total Count of the License

*Type* : string






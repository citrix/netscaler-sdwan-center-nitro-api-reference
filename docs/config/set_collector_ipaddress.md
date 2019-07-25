# set\_collector\_ipaddress


<a name="overview"></a>
## Overview
This resource can be used to set the collector ip.


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config/  
*Schemes* : HTTP


### Tags

* set\_collector\_ipaddress : Operations related to set\_collector\_ipaddress 




<a name="paths"></a>
## Paths

<a name="set\_collector\_ipaddress-post"></a>
### POST operation for set\_collector\_ipaddress
```
POST /set_collector_ipaddress
```


#### Description
Use this operation to set the Collector IPs.


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[set\_collector\_ipaddress\_request\_schema](#set\_collector\_ipaddress\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[set\_collector\_ipaddress\_post\_success\_schema](#set\_collector\_ipaddress\_post\_success\_schema)|
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

* set\_collector\_ipaddress




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="certificate\_password"></a>
### certificate\_password
The certificate password

*Type* : string


<a name="certificate\_username"></a>
### certificate\_username
The certificate username

*Type* : string


<a name="collector\_ip"></a>
### collector\_ip
The IP of the collector

*Type* : string


<a name="rcn\_name"></a>
### rcn\_name
The name of the corresponding rcn

*Type* : string


<a name="set\_collector\_ipaddress"></a>
### set\_collector\_ipaddress

|Name|Schema|
|---|---|
|**certificate\_password**  <br>*optional*|[certificate\_password](#certificate\_password)|
|**certificate\_username**  <br>*optional*|[certificate\_username](#certificate\_username)|
|**collector\_ip**  <br>*optional*|[collector\_ip](#collector\_ip)|
|**rcn\_name**  <br>*optional*|[rcn\_name](#rcn\_name)|


<a name="set\_collector\_ipaddress\_delete\_success\_schema"></a>
### set\_collector\_ipaddress\_delete\_success\_schema

|Name|Schema|
|---|---|
|**set\_collector\_ipaddress**  <br>*optional*|[set\_collector\_ipaddress](#set\_collector\_ipaddress\_delete\_success\_schema-set\_collector\_ipaddress)|

<a name="set\_collector\_ipaddress\_delete\_success\_schema-set\_collector\_ipaddress"></a>
**set\_collector\_ipaddress**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="set\_collector\_ipaddress\_post\_success\_schema"></a>
### set\_collector\_ipaddress\_post\_success\_schema

|Name|Schema|
|---|---|
|**set\_collector\_ipaddress**  <br>*optional*|[set\_collector\_ipaddress](#set\_collector\_ipaddress\_post\_success\_schema-set\_collector\_ipaddress)|

<a name="set\_collector\_ipaddress\_post\_success\_schema-set\_collector\_ipaddress"></a>
**set\_collector\_ipaddress**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="set\_collector\_ipaddress\_put\_success\_schema"></a>
### set\_collector\_ipaddress\_put\_success\_schema

|Name|Schema|
|---|---|
|**set\_collector\_ipaddress**  <br>*optional*|[set\_collector\_ipaddress](#set\_collector\_ipaddress\_put\_success\_schema-set\_collector\_ipaddress)|

<a name="set\_collector\_ipaddress\_put\_success\_schema-set\_collector\_ipaddress"></a>
**set\_collector\_ipaddress**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="set\_collector\_ipaddress\_request\_schema"></a>
### set\_collector\_ipaddress\_request\_schema

|Name|Schema|
|---|---|
|**set\_collector\_ipaddress**  <br>*optional*|[set\_collector\_ipaddress](#set\_collector\_ipaddress)|


<a name="set\_collector\_ipaddress\_response\_schema"></a>
### set\_collector\_ipaddress\_response\_schema
*Type* : < [set\_collector\_ipaddress\_response\_schema](#set\_collector\_ipaddress\_response\_schema-inline) > array

<a name="set\_collector\_ipaddress\_response\_schema-inline"></a>
**set\_collector\_ipaddress\_response\_schema**

|Name|Schema|
|---|---|
|**certificate\_password**  <br>*optional*|[certificate\_password](#certificate\_password)|
|**certificate\_username**  <br>*optional*|[certificate\_username](#certificate\_username)|
|**collector\_ip**  <br>*optional*|[collector\_ip](#collector\_ip)|
|**rcn\_name**  <br>*optional*|[rcn\_name](#rcn\_name)|






# hdx\_summary


<a name="overview"></a>
## Overview
API to get reports for HDX Summary(bandwidth is in Kbps and data is in KB)


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/reports/  
*Schemes* : HTTP


### Tags

* hdx\_summary : Operations related to hdx\_summary 




<a name="paths"></a>
## Paths

<a name="hdx\_summary-get"></a>
### Get operation for hdx\_summary
```
GET /hdx_summary
```


#### Description
Use this operation to get a report for HDX Summary. The response payload also contains the meta\_data block.


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[hdx\_summary\_response\_schema](#hdx\_summary\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* hdx\_summary




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="bytes\_from\_client"></a>
### bytes\_from\_client
Bytes from client

*Type* : integer


<a name="bytes\_from\_server"></a>
### bytes\_from\_server
Bytes from Server

*Type* : integer


<a name="client\_ip"></a>
### client\_ip
Client IP Address of the user

*Type* : string


<a name="hdx\_channel\_available"></a>
### hdx\_channel\_available
HDX channel availability

*Type* : enum (Yes, No)


<a name="hdx\_summary\_delete\_success\_schema"></a>
### hdx\_summary\_delete\_success\_schema

|Name|Schema|
|---|---|
|**hdx\_summary**  <br>*optional*|[hdx\_summary](#hdx\_summary\_delete\_success\_schema-hdx\_summary)|

<a name="hdx\_summary\_delete\_success\_schema-hdx\_summary"></a>
**hdx\_summary**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="hdx\_summary\_post\_success\_schema"></a>
### hdx\_summary\_post\_success\_schema

|Name|Schema|
|---|---|
|**hdx\_summary**  <br>*optional*|[hdx\_summary](#hdx\_summary\_post\_success\_schema-hdx\_summary)|

<a name="hdx\_summary\_post\_success\_schema-hdx\_summary"></a>
**hdx\_summary**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="hdx\_summary\_put\_success\_schema"></a>
### hdx\_summary\_put\_success\_schema

|Name|Schema|
|---|---|
|**hdx\_summary**  <br>*optional*|[hdx\_summary](#hdx\_summary\_put\_success\_schema-hdx\_summary)|

<a name="hdx\_summary\_put\_success\_schema-hdx\_summary"></a>
**hdx\_summary**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="hdx\_summary\_response\_schema"></a>
### hdx\_summary\_response\_schema
*Type* : < [hdx\_summary\_response\_schema](#hdx\_summary\_response\_schema-inline) > array

<a name="hdx\_summary\_response\_schema-inline"></a>
**hdx\_summary\_response\_schema**

|Name|Schema|
|---|---|
|**bytes\_from\_client**  <br>*optional*|[bytes\_from\_client](#bytes\_from\_client)|
|**bytes\_from\_server**  <br>*optional*|[bytes\_from\_server](#bytes\_from\_server)|
|**client\_ip**  <br>*optional*|[client\_ip](#client\_ip)|
|**hdx\_channel\_available**  <br>*optional*|[hdx\_channel\_available](#hdx\_channel\_available)|
|**msi\_count**  <br>*optional*|[msi\_count](#msi\_count)|
|**region\_name**  <br>*optional*|[region\_name](#region\_name)|
|**ssi\_count**  <br>*optional*|[ssi\_count](#ssi\_count)|
|**user\_name**  <br>*optional*|[user\_name](#user\_name)|


<a name="msi\_count"></a>
### msi\_count
Multi Stream ICA session count

*Type* : integer


<a name="region\_name"></a>
### region\_name
The region name

*Type* : string


<a name="ssi\_count"></a>
### ssi\_count
Single Stream ICA session count

*Type* : integer


<a name="user\_name"></a>
### user\_name
Name of the user who initiated HDX sessions

*Type* : string






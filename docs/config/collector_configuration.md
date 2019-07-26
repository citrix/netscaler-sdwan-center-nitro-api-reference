# collector\_configuration


<a name="overview"></a>
## Overview
This resource can be used for getting collector configuration


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config/  
*Schemes* : HTTP


### Tags

* collector\_configuration : Operations related to collector\_configuration 




<a name="paths"></a>
## Paths

<a name="collector\_configuration-get"></a>
### Get operation for collector\_configuration
```
GET /collector_configuration
```


#### Description
Use this operation to get the collector configuration settings


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[collector\_configuration\_response\_schema](#collector\_configuration\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* collector\_configuration




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="collector\_configuration\_delete\_success\_schema"></a>
### collector\_configuration\_delete\_success\_schema

|Name|Schema|
|---|---|
|**collector\_configuration**  <br>*optional*|[collector\_configuration](#collector\_configuration\_delete\_success\_schema-collector\_configuration)|

<a name="collector\_configuration\_delete\_success\_schema-collector\_configuration"></a>
**collector\_configuration**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="collector\_configuration\_post\_success\_schema"></a>
### collector\_configuration\_post\_success\_schema

|Name|Schema|
|---|---|
|**collector\_configuration**  <br>*optional*|[collector\_configuration](#collector\_configuration\_post\_success\_schema-collector\_configuration)|

<a name="collector\_configuration\_post\_success\_schema-collector\_configuration"></a>
**collector\_configuration**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="collector\_configuration\_put\_success\_schema"></a>
### collector\_configuration\_put\_success\_schema

|Name|Schema|
|---|---|
|**collector\_configuration**  <br>*optional*|[collector\_configuration](#collector\_configuration\_put\_success\_schema-collector\_configuration)|

<a name="collector\_configuration\_put\_success\_schema-collector\_configuration"></a>
**collector\_configuration**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="collector\_configuration\_response\_schema"></a>
### collector\_configuration\_response\_schema
*Type* : < [collector\_configuration\_response\_schema](#collector\_configuration\_response\_schema-inline) > array

<a name="collector\_configuration\_response\_schema-inline"></a>
**collector\_configuration\_response\_schema**

|Name|Schema|
|---|---|
|**collector\_ip**  <br>*optional*|[collector\_ip](#collector\_ip)|
|**discovery\_status**  <br>*optional*|[discovery\_status](#discovery\_status)|
|**rcn\_ip**  <br>*optional*|[rcn\_ip](#rcn\_ip)|
|**region\_name**  <br>*optional*|[region\_name](#region\_name)|


<a name="collector\_ip"></a>
### collector\_ip
The IP Address of the collector

*Type* : string


<a name="discovery\_status"></a>
### discovery\_status
The discovery status of region appliances

*Type* : string


<a name="rcn\_ip"></a>
### rcn\_ip
The IP Address of the corresponding RCN

*Type* : string


<a name="region\_name"></a>
### region\_name
The region whose appliances are polled by the collector

*Type* : string






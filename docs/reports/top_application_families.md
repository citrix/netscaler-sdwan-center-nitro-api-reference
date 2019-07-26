# top\_application\_families


<a name="overview"></a>
## Overview
API to get reports for Top Application Families (bandwidth is in Kbps and data is in KB)


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/reports/  
*Schemes* : HTTP


### Tags

* top\_application\_families : Operations related to top\_application\_families 




<a name="paths"></a>
## Paths

<a name="top\_application\_families-get"></a>
### Get operation for top\_application\_families
```
GET /top_application_families
```


#### Description
Use this operation to get a report for top application families. The response payload also contains the meta\_data block.


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[top\_application\_families\_response\_schema](#top\_application\_families\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* top\_application\_families




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="application\_family"></a>
### application\_family
The application family

*Type* : string


<a name="incoming\_traffic"></a>
### incoming\_traffic
Incoming traffic

*Type* : number


<a name="outgoing\_traffic"></a>
### outgoing\_traffic
Outgoing traffic

*Type* : number


<a name="region\_name"></a>
### region\_name
The region name

*Type* : string


<a name="top\_application\_families\_delete\_success\_schema"></a>
### top\_application\_families\_delete\_success\_schema

|Name|Schema|
|---|---|
|**top\_application\_families**  <br>*optional*|[top\_application\_families](#top\_application\_families\_delete\_success\_schema-top\_application\_families)|

<a name="top\_application\_families\_delete\_success\_schema-top\_application\_families"></a>
**top\_application\_families**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="top\_application\_families\_post\_success\_schema"></a>
### top\_application\_families\_post\_success\_schema

|Name|Schema|
|---|---|
|**top\_application\_families**  <br>*optional*|[top\_application\_families](#top\_application\_families\_post\_success\_schema-top\_application\_families)|

<a name="top\_application\_families\_post\_success\_schema-top\_application\_families"></a>
**top\_application\_families**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="top\_application\_families\_put\_success\_schema"></a>
### top\_application\_families\_put\_success\_schema

|Name|Schema|
|---|---|
|**top\_application\_families**  <br>*optional*|[top\_application\_families](#top\_application\_families\_put\_success\_schema-top\_application\_families)|

<a name="top\_application\_families\_put\_success\_schema-top\_application\_families"></a>
**top\_application\_families**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="top\_application\_families\_response\_schema"></a>
### top\_application\_families\_response\_schema
*Type* : < [top\_application\_families\_response\_schema](#top\_application\_families\_response\_schema-inline) > array

<a name="top\_application\_families\_response\_schema-inline"></a>
**top\_application\_families\_response\_schema**

|Name|Schema|
|---|---|
|**application\_family**  <br>*optional*|[application\_family](#application\_family)|
|**incoming\_traffic**  <br>*optional*|[incoming\_traffic](#incoming\_traffic)|
|**outgoing\_traffic**  <br>*optional*|[outgoing\_traffic](#outgoing\_traffic)|
|**region\_name**  <br>*optional*|[region\_name](#region\_name)|
|**total\_traffic**  <br>*optional*|[total\_traffic](#total\_traffic)|


<a name="total\_traffic"></a>
### total\_traffic
Total traffic

*Type* : number






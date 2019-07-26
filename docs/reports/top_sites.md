# top\_sites


<a name="overview"></a>
## Overview
API to get reports for Top Sites (bandwidth is in Kbps and data is in KB)


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/reports/  
*Schemes* : HTTP


### Tags

* top\_sites : Operations related to top\_sites 




<a name="paths"></a>
## Paths

<a name="top\_sites-get"></a>
### Get operation for top\_sites
```
GET /top_sites
```


#### Description
Use this operation to get a report for Top sites. The response payload also contains the meta\_data block.


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[top\_sites\_response\_schema](#top\_sites\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* top\_sites




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


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


<a name="site\_name"></a>
### site\_name
The site name

*Type* : string


<a name="top\_sites\_delete\_success\_schema"></a>
### top\_sites\_delete\_success\_schema

|Name|Schema|
|---|---|
|**top\_sites**  <br>*optional*|[top\_sites](#top\_sites\_delete\_success\_schema-top\_sites)|

<a name="top\_sites\_delete\_success\_schema-top\_sites"></a>
**top\_sites**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="top\_sites\_post\_success\_schema"></a>
### top\_sites\_post\_success\_schema

|Name|Schema|
|---|---|
|**top\_sites**  <br>*optional*|[top\_sites](#top\_sites\_post\_success\_schema-top\_sites)|

<a name="top\_sites\_post\_success\_schema-top\_sites"></a>
**top\_sites**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="top\_sites\_put\_success\_schema"></a>
### top\_sites\_put\_success\_schema

|Name|Schema|
|---|---|
|**top\_sites**  <br>*optional*|[top\_sites](#top\_sites\_put\_success\_schema-top\_sites)|

<a name="top\_sites\_put\_success\_schema-top\_sites"></a>
**top\_sites**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="top\_sites\_response\_schema"></a>
### top\_sites\_response\_schema
*Type* : < [top\_sites\_response\_schema](#top\_sites\_response\_schema-inline) > array

<a name="top\_sites\_response\_schema-inline"></a>
**top\_sites\_response\_schema**

|Name|Schema|
|---|---|
|**incoming\_traffic**  <br>*optional*|[incoming\_traffic](#incoming\_traffic)|
|**outgoing\_traffic**  <br>*optional*|[outgoing\_traffic](#outgoing\_traffic)|
|**region\_name**  <br>*optional*|[region\_name](#region\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**total\_traffic**  <br>*optional*|[total\_traffic](#total\_traffic)|


<a name="total\_traffic"></a>
### total\_traffic
Total traffic

*Type* : number






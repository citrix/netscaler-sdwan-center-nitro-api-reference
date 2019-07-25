# mos\_scores


<a name="overview"></a>
## Overview
API to get reports for MOS Scores (bandwidth is in Kbps and data is in KB)


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/reports/  
*Schemes* : HTTP


### Tags

* mos\_scores : Operations related to mos\_scores 




<a name="paths"></a>
## Paths

<a name="mos\_scores-get"></a>
### Get operation for mos\_scores
```
GET /mos_scores
```


#### Description
Use this operation to get a report for MOS Scores. The response payload also contains the meta\_data block.


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[mos\_scores\_response\_schema](#mos\_scores\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* mos\_scores




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="average\_virtual\_wan\_mos"></a>
### average\_virtual\_wan\_mos
The worst average quality score for an application during the time period measured using a scale of 1-5

*Type* : integer


<a name="lowest\_virtual\_wan\_mos"></a>
### lowest\_virtual\_wan\_mos
The worst quality score for an application during the time period measured using a scale of 1-5

*Type* : integer


<a name="mos\_scores\_delete\_success\_schema"></a>
### mos\_scores\_delete\_success\_schema

|Name|Schema|
|---|---|
|**mos\_scores**  <br>*optional*|[mos\_scores](#mos\_scores\_delete\_success\_schema-mos\_scores)|

<a name="mos\_scores\_delete\_success\_schema-mos\_scores"></a>
**mos\_scores**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="mos\_scores\_post\_success\_schema"></a>
### mos\_scores\_post\_success\_schema

|Name|Schema|
|---|---|
|**mos\_scores**  <br>*optional*|[mos\_scores](#mos\_scores\_post\_success\_schema-mos\_scores)|

<a name="mos\_scores\_post\_success\_schema-mos\_scores"></a>
**mos\_scores**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="mos\_scores\_put\_success\_schema"></a>
### mos\_scores\_put\_success\_schema

|Name|Schema|
|---|---|
|**mos\_scores**  <br>*optional*|[mos\_scores](#mos\_scores\_put\_success\_schema-mos\_scores)|

<a name="mos\_scores\_put\_success\_schema-mos\_scores"></a>
**mos\_scores**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="mos\_scores\_response\_schema"></a>
### mos\_scores\_response\_schema
*Type* : < [mos\_scores\_response\_schema](#mos\_scores\_response\_schema-inline) > array

<a name="mos\_scores\_response\_schema-inline"></a>
**mos\_scores\_response\_schema**

|Name|Schema|
|---|---|
|**average\_virtual\_wan\_mos**  <br>*optional*|[average\_virtual\_wan\_mos](#average\_virtual\_wan\_mos)|
|**lowest\_virtual\_wan\_mos**  <br>*optional*|[lowest\_virtual\_wan\_mos](#lowest\_virtual\_wan\_mos)|
|**name**  <br>*optional*|[name](#name)|
|**region\_name**  <br>*optional*|[region\_name](#region\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**virtual\_service**  <br>*optional*|[virtual\_service](#virtual\_service)|


<a name="name"></a>
### name
The MOS Score name

*Type* : string


<a name="region\_name"></a>
### region\_name
The region name

*Type* : string


<a name="site\_name"></a>
### site\_name
The site name

*Type* : string


<a name="virtual\_service"></a>
### virtual\_service
The Virtual Path name

*Type* : string






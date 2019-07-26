# applications


<a name="overview"></a>
## Overview
API to get reports for Top Applications (bandwidth is in Kbps and data is in KB)


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/reports/  
*Schemes* : HTTP


### Tags

* applications : Operations related to applications 




<a name="paths"></a>
## Paths

<a name="applications-get"></a>
### Get operation for applications
```
GET /applications
```


#### Description
Use this operation to get a report for applications. The response payload also contains the meta\_data block.


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[applications\_response\_schema](#applications\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* applications




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="aggregate\_data"></a>
### aggregate\_data
Aggregate data for application traffic

*Type* : number


<a name="aggregate\_incoming\_data"></a>
### aggregate\_incoming\_data
Aggregate Data for Incoming application traffi

*Type* : number


<a name="aggregate\_outgoing\_data"></a>
### aggregate\_outgoing\_data
Aggregate Data for Outgoing application traffic

*Type* : number


<a name="application\_name"></a>
### application\_name
The application name

*Type* : string


<a name="applications"></a>
### applications

|Name|Schema|
|---|---|
|**operations**  <br>*optional*|[operations](#operations)|


<a name="applications\_delete\_success\_schema"></a>
### applications\_delete\_success\_schema

|Name|Schema|
|---|---|
|**applications**  <br>*optional*|[applications](#applications\_delete\_success\_schema-applications)|

<a name="applications\_delete\_success\_schema-applications"></a>
**applications**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="applications\_post\_success\_schema"></a>
### applications\_post\_success\_schema

|Name|Schema|
|---|---|
|**applications**  <br>*optional*|[applications](#applications\_post\_success\_schema-applications)|

<a name="applications\_post\_success\_schema-applications"></a>
**applications**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="applications\_put\_success\_schema"></a>
### applications\_put\_success\_schema

|Name|Schema|
|---|---|
|**applications**  <br>*optional*|[applications](#applications\_put\_success\_schema-applications)|

<a name="applications\_put\_success\_schema-applications"></a>
**applications**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="applications\_request\_schema"></a>
### applications\_request\_schema

|Name|Schema|
|---|---|
|**applications**  <br>*optional*|[applications](#applications)|


<a name="applications\_response\_schema"></a>
### applications\_response\_schema
*Type* : < [applications\_response\_schema](#applications\_response\_schema-inline) > array

<a name="applications\_response\_schema-inline"></a>
**applications\_response\_schema**

|Name|Schema|
|---|---|
|**aggregate\_data**  <br>*optional*|[aggregate\_data](#aggregate\_data)|
|**aggregate\_incoming\_data**  <br>*optional*|[aggregate\_incoming\_data](#aggregate\_incoming\_data)|
|**aggregate\_outgoing\_data**  <br>*optional*|[aggregate\_outgoing\_data](#aggregate\_outgoing\_data)|
|**application\_name**  <br>*optional*|[application\_name](#application\_name)|
|**average\_bandwidth**  <br>*optional*|[average\_bandwidth](#average\_bandwidth)|
|**average\_incoming\_bandwidth**  <br>*optional*|[average\_incoming\_bandwidth](#average\_incoming\_bandwidth)|
|**average\_outgoing\_bandwidth**  <br>*optional*|[average\_outgoing\_bandwidth](#average\_outgoing\_bandwidth)|
|**operations**  <br>*optional*|[operations](#operations)|
|**region\_name**  <br>*optional*|[region\_name](#region\_name)|


<a name="average\_bandwidth"></a>
### average\_bandwidth
Average bandwidth when the application is active

*Type* : string


<a name="average\_incoming\_bandwidth"></a>
### average\_incoming\_bandwidth
Average bandwidth of incoming traffic when application is active

*Type* : string


<a name="average\_outgoing\_bandwidth"></a>
### average\_outgoing\_bandwidth
Average bandwidth of outgoing traffic when application is active

*Type* : string


<a name="operations"></a>
### operations
*Type* : string


<a name="region\_name"></a>
### region\_name
*Type* : string






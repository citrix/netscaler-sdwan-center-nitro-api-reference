# classes


<a name="overview"></a>
## Overview
API to get reports for classes (bandwidth is in Kbps and data is in KB)


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/reports/  
*Schemes* : HTTP


### Tags

* classes : Operations related to classes 




<a name="paths"></a>
## Paths

<a name="classes-get"></a>
### Get operation for classes
```
GET /classes
```


#### Description
Use this operation to get a report for classes.  The response payload also contains the meta\_data block.


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[classes\_response\_schema](#classes\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* classes




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="class\_name"></a>
### class\_name
The class name

*Type* : string


<a name="class\_type"></a>
### class\_type
Class type (control, real-time, interact or bulk)

*Type* : string


<a name="classes\_delete\_success\_schema"></a>
### classes\_delete\_success\_schema

|Name|Schema|
|---|---|
|**classes**  <br>*optional*|[classes](#classes\_delete\_success\_schema-classes)|

<a name="classes\_delete\_success\_schema-classes"></a>
**classes**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="classes\_post\_success\_schema"></a>
### classes\_post\_success\_schema

|Name|Schema|
|---|---|
|**classes**  <br>*optional*|[classes](#classes\_post\_success\_schema-classes)|

<a name="classes\_post\_success\_schema-classes"></a>
**classes**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="classes\_put\_success\_schema"></a>
### classes\_put\_success\_schema

|Name|Schema|
|---|---|
|**classes**  <br>*optional*|[classes](#classes\_put\_success\_schema-classes)|

<a name="classes\_put\_success\_schema-classes"></a>
**classes**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="classes\_response\_schema"></a>
### classes\_response\_schema
*Type* : < [classes\_response\_schema](#classes\_response\_schema-inline) > array

<a name="classes\_response\_schema-inline"></a>
**classes\_response\_schema**

|Name|Schema|
|---|---|
|**class\_name**  <br>*optional*|[class\_name](#class\_name)|
|**class\_type**  <br>*optional*|[class\_type](#class\_type)|
|**data\_coverage**  <br>*optional*|[data\_coverage](#data\_coverage)|
|**data\_dropped**  <br>*optional*|[data\_dropped](#data\_dropped)|
|**data\_pending**  <br>*optional*|[data\_pending](#data\_pending)|
|**incoming\_traffic**  <br>*optional*|[incoming\_traffic](#incoming\_traffic)|
|**packets\_dropped**  <br>*optional*|[packets\_dropped](#packets\_dropped)|
|**packets\_pending**  <br>*optional*|[packets\_pending](#packets\_pending)|
|**packets\_sent**  <br>*optional*|[packets\_sent](#packets\_sent)|
|**percent\_drop**  <br>*optional*|[percent\_drop](#percent\_drop)|
|**region\_name**  <br>*optional*|[region\_name](#region\_name)|
|**sent\_bandwidth**  <br>*optional*|[sent\_bandwidth](#sent\_bandwidth)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**virtual\_service**  <br>*optional*|[virtual\_service](#virtual\_service)|
|**wait\_time**  <br>*optional*|[wait\_time](#wait\_time)|


<a name="data\_coverage"></a>
### data\_coverage
The amount, in percent of the selected time period for which there is data

*Type* : number


<a name="data\_dropped"></a>
### data\_dropped
Data dropped

*Type* : number


<a name="data\_pending"></a>
### data\_pending
Data pending

*Type* : number


<a name="incoming\_traffic"></a>
### incoming\_traffic
Incoming traffic

*Type* : number


<a name="packets\_dropped"></a>
### packets\_dropped
Packets dropped

*Type* : integer


<a name="packets\_pending"></a>
### packets\_pending
Packets pending

*Type* : integer


<a name="packets\_sent"></a>
### packets\_sent
Packets sent

*Type* : integer


<a name="percent\_drop"></a>
### percent\_drop
Drop, in percent

*Type* : number


<a name="region\_name"></a>
### region\_name
The region name

*Type* : string


<a name="sent\_bandwidth"></a>
### sent\_bandwidth
Sent bandwidth

*Type* : number


<a name="site\_name"></a>
### site\_name
The site name

*Type* : string


<a name="virtual\_service"></a>
### virtual\_service
The Virtual Path name

*Type* : string


<a name="wait\_time"></a>
### wait\_time
Wait time, in milliseconds

*Type* : integer






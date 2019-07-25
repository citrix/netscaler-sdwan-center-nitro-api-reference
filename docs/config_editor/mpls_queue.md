# mpls\_queue


<a name="overview"></a>
## Overview
MPLS queue objects


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* mpls\_queue : Operations related to mpls\_queue 




<a name="paths"></a>
## Paths

<a name="mpls\_queue-post"></a>
### POST operation for mpls\_queue
```
POST /mpls_queue
```


#### Description
Use this operation to add mpls queues


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[mpls\_queue\_post\_success\_schema](#mpls\_queue\_post\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* mpls\_queue


<a name="mpls\_queue-get"></a>
### Get operation for mpls\_queue
```
GET /mpls_queue
```


#### Description
Use this operation to get the list of mpls queues


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[mpls\_queue\_response\_schema](#mpls\_queue\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* mpls\_queue


<a name="mpls\_queue-put"></a>
### PUT operation for mpls\_queue
```
PUT /mpls_queue
```


#### Description
Use this operation to modify a mpls queue


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[mpls\_queue\_request\_schema](#mpls\_queue\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[mpls\_queue\_put\_success\_schema](#mpls\_queue\_put\_success\_schema)|
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

* mpls\_queue


<a name="mpls\_queue-deletepathparam-delete"></a>
### DELETE operation for mpls\_queue
```
DELETE /mpls_queue/{deletePathParam}
```


#### Description
Use this operation to delete a mpls queue


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[mpls\_queue\_delete\_success\_schema](#mpls\_queue\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* mpls\_queue




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="congestion\_threshold"></a>
### congestion\_threshold
The amount of congestion (in microseconds) after which the MPLS Queue will throttle packet transmission to avoid further congestion

*Type* : integer


<a name="dscp\_tag"></a>
### dscp\_tag
The DSCP tag for the MPLS queue

*Type* : enum (DEFAULT, af11, af12, af13, af21, af22, af23, af31, af32, af33, af41, af42, af43, cs1, cs2, cs3, cs4, cs5, cs6, cs7, ef)


<a name="lan\_to\_wan\_bulk\_eligibility"></a>
### lan\_to\_wan\_bulk\_eligibility
Allows paths from this WAN Link to transmit bulk traffic. If disabled, these paths will still be considered eligible if no other paths are available

*Type* : boolean


<a name="lan\_to\_wan\_interactive\_eligibility"></a>
### lan\_to\_wan\_interactive\_eligibility
Allows paths from this WAN Link to transmit interactive traffic. If disabled, these paths will still be considered eligible if no other paths are available

*Type* : boolean


<a name="lan\_to\_wan\_permitted\_rate\_kbps"></a>
### lan\_to\_wan\_permitted\_rate\_kbps
The available or allowed rate for LAN to WAN traffic

*Type* : integer


<a name="lan\_to\_wan\_realtime\_eligibility"></a>
### lan\_to\_wan\_realtime\_eligibility
Allows paths from this WAN Link to transmit realtime traffic. If disabled, these paths will still be considered eligible if no other paths are available

*Type* : boolean


<a name="mpls\_queue"></a>
### mpls\_queue

|Name|Schema|
|---|---|
|**congestion\_threshold**  <br>*optional*|[congestion\_threshold](#congestion\_threshold)|
|**dscp\_tag**  <br>*optional*|[dscp\_tag](#dscp\_tag)|
|**lan\_to\_wan\_bulk\_eligibility**  <br>*optional*|[lan\_to\_wan\_bulk\_eligibility](#lan\_to\_wan\_bulk\_eligibility)|
|**lan\_to\_wan\_interactive\_eligibility**  <br>*optional*|[lan\_to\_wan\_interactive\_eligibility](#lan\_to\_wan\_interactive\_eligibility)|
|**lan\_to\_wan\_permitted\_rate\_kbps**  <br>*optional*|[lan\_to\_wan\_permitted\_rate\_kbps](#lan\_to\_wan\_permitted\_rate\_kbps)|
|**lan\_to\_wan\_realtime\_eligibility**  <br>*optional*|[lan\_to\_wan\_realtime\_eligibility](#lan\_to\_wan\_realtime\_eligibility)|
|**mpls\_queue\_name**  <br>*optional*|[mpls\_queue\_name](#mpls\_queue\_name)|
|**no\_retag**  <br>*optional*|[no\_retag](#no\_retag)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**tracking\_ip\_address**  <br>*optional*|[tracking\_ip\_address](#tracking\_ip\_address)|
|**unmatched**  <br>*optional*|[unmatched](#unmatched)|
|**wan\_link\_name**  <br>*optional*|[wan\_link\_name](#wan\_link\_name)|
|**wan\_to\_lan\_bulk\_eligibility**  <br>*optional*|[wan\_to\_lan\_bulk\_eligibility](#wan\_to\_lan\_bulk\_eligibility)|
|**wan\_to\_lan\_interactive\_eligibility**  <br>*optional*|[wan\_to\_lan\_interactive\_eligibility](#wan\_to\_lan\_interactive\_eligibility)|
|**wan\_to\_lan\_permitted\_rate\_kbps**  <br>*optional*|[wan\_to\_lan\_permitted\_rate\_kbps](#wan\_to\_lan\_permitted\_rate\_kbps)|
|**wan\_to\_lan\_realtime\_eligibility**  <br>*optional*|[wan\_to\_lan\_realtime\_eligibility](#wan\_to\_lan\_realtime\_eligibility)|


<a name="mpls\_queue\_delete\_success\_schema"></a>
### mpls\_queue\_delete\_success\_schema

|Name|Schema|
|---|---|
|**mpls\_queue**  <br>*optional*|[mpls\_queue](#mpls\_queue\_delete\_success\_schema-mpls\_queue)|

<a name="mpls\_queue\_delete\_success\_schema-mpls\_queue"></a>
**mpls\_queue**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="mpls\_queue\_name"></a>
### mpls\_queue\_name
The name of the MPLS Queue

*Type* : string


<a name="mpls\_queue\_post\_success\_schema"></a>
### mpls\_queue\_post\_success\_schema

|Name|Schema|
|---|---|
|**mpls\_queue**  <br>*optional*|[mpls\_queue](#mpls\_queue\_post\_success\_schema-mpls\_queue)|

<a name="mpls\_queue\_post\_success\_schema-mpls\_queue"></a>
**mpls\_queue**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="mpls\_queue\_put\_success\_schema"></a>
### mpls\_queue\_put\_success\_schema

|Name|Schema|
|---|---|
|**mpls\_queue**  <br>*optional*|[mpls\_queue](#mpls\_queue\_put\_success\_schema-mpls\_queue)|

<a name="mpls\_queue\_put\_success\_schema-mpls\_queue"></a>
**mpls\_queue**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="mpls\_queue\_request\_schema"></a>
### mpls\_queue\_request\_schema

|Name|Schema|
|---|---|
|**mpls\_queue**  <br>*optional*|[mpls\_queue](#mpls\_queue)|


<a name="mpls\_queue\_response\_schema"></a>
### mpls\_queue\_response\_schema
*Type* : < [mpls\_queue\_response\_schema](#mpls\_queue\_response\_schema-inline) > array

<a name="mpls\_queue\_response\_schema-inline"></a>
**mpls\_queue\_response\_schema**

|Name|Schema|
|---|---|
|**congestion\_threshold**  <br>*optional*|[congestion\_threshold](#congestion\_threshold)|
|**dscp\_tag**  <br>*optional*|[dscp\_tag](#dscp\_tag)|
|**lan\_to\_wan\_bulk\_eligibility**  <br>*optional*|[lan\_to\_wan\_bulk\_eligibility](#lan\_to\_wan\_bulk\_eligibility)|
|**lan\_to\_wan\_interactive\_eligibility**  <br>*optional*|[lan\_to\_wan\_interactive\_eligibility](#lan\_to\_wan\_interactive\_eligibility)|
|**lan\_to\_wan\_permitted\_rate\_kbps**  <br>*optional*|[lan\_to\_wan\_permitted\_rate\_kbps](#lan\_to\_wan\_permitted\_rate\_kbps)|
|**lan\_to\_wan\_realtime\_eligibility**  <br>*optional*|[lan\_to\_wan\_realtime\_eligibility](#lan\_to\_wan\_realtime\_eligibility)|
|**mpls\_queue\_name**  <br>*optional*|[mpls\_queue\_name](#mpls\_queue\_name)|
|**no\_retag**  <br>*optional*|[no\_retag](#no\_retag)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**tracking\_ip\_address**  <br>*optional*|[tracking\_ip\_address](#tracking\_ip\_address)|
|**unmatched**  <br>*optional*|[unmatched](#unmatched)|
|**wan\_link\_name**  <br>*optional*|[wan\_link\_name](#wan\_link\_name)|
|**wan\_to\_lan\_bulk\_eligibility**  <br>*optional*|[wan\_to\_lan\_bulk\_eligibility](#wan\_to\_lan\_bulk\_eligibility)|
|**wan\_to\_lan\_interactive\_eligibility**  <br>*optional*|[wan\_to\_lan\_interactive\_eligibility](#wan\_to\_lan\_interactive\_eligibility)|
|**wan\_to\_lan\_permitted\_rate\_kbps**  <br>*optional*|[wan\_to\_lan\_permitted\_rate\_kbps](#wan\_to\_lan\_permitted\_rate\_kbps)|
|**wan\_to\_lan\_realtime\_eligibility**  <br>*optional*|[wan\_to\_lan\_realtime\_eligibility](#wan\_to\_lan\_realtime\_eligibility)|


<a name="no\_retag"></a>
### no\_retag
If enabled, DCSP tags using unmatched Queue will not get retagged to the unmatched Queue tag for LAN to WAN intranet traffic

*Type* : boolean


<a name="package\_name"></a>
### package\_name
Config package name using which the wan\_links API operation should be performed.

*Type* : string


<a name="site\_name"></a>
### site\_name
Site Name

*Type* : string


<a name="tracking\_ip\_address"></a>
### tracking\_ip\_address
A virtual IP address that can be pinged to determine the state of the MPLS Queue

*Type* : string


<a name="unmatched"></a>
### unmatched
If enabled, DSCP tags not matched by other MPLS Queues will use this queue

*Type* : boolean


<a name="wan\_link\_name"></a>
### wan\_link\_name
The WAN Link Name

*Type* : string


<a name="wan\_to\_lan\_bulk\_eligibility"></a>
### wan\_to\_lan\_bulk\_eligibility
Allows paths to this WAN Link to transmit bulk traffic. If disabled, these paths will still be considered eligible if no other paths are available

*Type* : boolean


<a name="wan\_to\_lan\_interactive\_eligibility"></a>
### wan\_to\_lan\_interactive\_eligibility
Allows paths to this WAN Link to transmit interactive traffic. If disabled, these paths will still be considered eligible if no other paths are available.

*Type* : boolean


<a name="wan\_to\_lan\_permitted\_rate\_kbps"></a>
### wan\_to\_lan\_permitted\_rate\_kbps
The available or allowed rate for WAN to LAN traffic

*Type* : integer


<a name="wan\_to\_lan\_realtime\_eligibility"></a>
### wan\_to\_lan\_realtime\_eligibility
Allows paths to this WAN Link to transmit realtime traffic. If disabled, these paths will still be considered eligible if no other paths are available.

*Type* : boolean






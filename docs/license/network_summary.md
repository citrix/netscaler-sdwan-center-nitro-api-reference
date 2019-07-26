# network\_summary


<a name="overview"></a>
## Overview
This resource can be used to get the License summary of the network.


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/license/  
*Schemes* : HTTP


### Tags

* network\_summary : Operations related to network\_summary 




<a name="paths"></a>
## Paths

<a name="network\_summary-get"></a>
### Get operation for network\_summary
```
GET /network_summary
```


#### Description
Use this operation to get the license network summary. Region can be filtered by using query parameter(?region=REGION\_NAME)


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[network\_summary\_response\_schema](#network\_summary\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* network\_summary




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="feature"></a>
### feature
License Feature(SE/EE)

*Type* : string


<a name="license\_expiry"></a>
### license\_expiry
Expiry date of license

*Type* : string


<a name="license\_server"></a>
### license\_server
Local or Centralized License server used

*Type* : string


<a name="license\_type"></a>
### license\_type
License Type

*Type* : string


<a name="maintenance\_expiry"></a>
### maintenance\_expiry
Maintenance Expiry date of license

*Type* : string


<a name="maximum\_bandwidth"></a>
### maximum\_bandwidth
Max BW of the license in MB

*Type* : string


<a name="model"></a>
### model
The License Model

*Type* : string


<a name="network\_summary\_delete\_success\_schema"></a>
### network\_summary\_delete\_success\_schema

|Name|Schema|
|---|---|
|**network\_summary**  <br>*optional*|[network\_summary](#network\_summary\_delete\_success\_schema-network\_summary)|

<a name="network\_summary\_delete\_success\_schema-network\_summary"></a>
**network\_summary**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="network\_summary\_post\_success\_schema"></a>
### network\_summary\_post\_success\_schema

|Name|Schema|
|---|---|
|**network\_summary**  <br>*optional*|[network\_summary](#network\_summary\_post\_success\_schema-network\_summary)|

<a name="network\_summary\_post\_success\_schema-network\_summary"></a>
**network\_summary**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="network\_summary\_put\_success\_schema"></a>
### network\_summary\_put\_success\_schema

|Name|Schema|
|---|---|
|**network\_summary**  <br>*optional*|[network\_summary](#network\_summary\_put\_success\_schema-network\_summary)|

<a name="network\_summary\_put\_success\_schema-network\_summary"></a>
**network\_summary**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="network\_summary\_response\_schema"></a>
### network\_summary\_response\_schema
*Type* : < [network\_summary\_response\_schema](#network\_summary\_response\_schema-inline) > array

<a name="network\_summary\_response\_schema-inline"></a>
**network\_summary\_response\_schema**

|Name|Schema|
|---|---|
|**feature**  <br>*optional*|[feature](#feature)|
|**license\_expiry**  <br>*optional*|[license\_expiry](#license\_expiry)|
|**license\_server**  <br>*optional*|[license\_server](#license\_server)|
|**license\_type**  <br>*optional*|[license\_type](#license\_type)|
|**maintenance\_expiry**  <br>*optional*|[maintenance\_expiry](#maintenance\_expiry)|
|**maximum\_bandwidth**  <br>*optional*|[maximum\_bandwidth](#maximum\_bandwidth)|
|**model**  <br>*optional*|[model](#model)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**state**  <br>*optional*|[state](#state)|


<a name="site\_name"></a>
### site\_name
Site Name

*Type* : string


<a name="state"></a>
### state
License State

*Type* : string






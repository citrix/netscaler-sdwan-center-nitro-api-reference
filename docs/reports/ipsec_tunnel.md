# ipsec\_tunnel


<a name="overview"></a>
## Overview
API to add, modify, delete, and get configuration for ipsec tunnels


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/reports/  
*Schemes* : HTTP


### Tags

* ipsec\_tunnel : Operations related to ipsec\_tunnel 




<a name="paths"></a>
## Paths

<a name="ipsec\_tunnel-post"></a>
### POST operation for ipsec\_tunnel
```
POST /ipsec_tunnel
```


#### Description
Use this operation to add ipsec tunnel


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[ipsec\_tunnel\_post\_success\_schema](#ipsec\_tunnel\_post\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* ipsec\_tunnel


<a name="ipsec\_tunnel-get"></a>
### Get operation for ipsec\_tunnel
```
GET /ipsec_tunnel
```


#### Description
Use this operation to get the list of ipsec tunnels


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[ipsec\_tunnel\_response\_schema](#ipsec\_tunnel\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* ipsec\_tunnel


<a name="ipsec\_tunnel-put"></a>
### PUT operation for ipsec\_tunnel
```
PUT /ipsec_tunnel
```


#### Description
Use this operation to modify a ipsec tunnel


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[ipsec\_tunnel\_request\_schema](#ipsec\_tunnel\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[ipsec\_tunnel\_put\_success\_schema](#ipsec\_tunnel\_put\_success\_schema)|
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

* ipsec\_tunnel


<a name="ipsec\_tunnel-deletepathparam-delete"></a>
### DELETE operation for ipsec\_tunnel
```
DELETE /ipsec_tunnel/{deletePathParam}
```


#### Description
Use this operation to delete a ipsec tunnel


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[ipsec\_tunnel\_delete\_success\_schema](#ipsec\_tunnel\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* ipsec\_tunnel




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="id"></a>
### id
Auto-generated ID. Use this ID to modify or delete a IPSec Tunnel

*Type* : integer


<a name="ike\_authentication"></a>
### ike\_authentication
Type of authentication

*Type* : enum (PSK, Certificate)


<a name="ike\_dh\_group"></a>
### ike\_dh\_group
DH group to use for IKE Key Generation

*Type* : enum (Group1, Group2, Group5, Group14, Group15, Group16, Group19, Group20, Group21)


<a name="ike\_dpd\_timeout\_s"></a>
### ike\_dpd\_timeout\_s
Time, in seconds, after receiving no packets or DPD replies to consider an IKE peer DEAD

*Type* : integer


<a name="ike\_encryption"></a>
### ike\_encryption
Encryption Mode for IKE messages

*Type* : enum (AES128, AES192, AES256)


<a name="ike\_hash\_algo"></a>
### ike\_hash\_algo
HASH algorithm used to authenticate IKE Messages

*Type* : enum (MD5, SHA1, SHA256)


<a name="ike\_identity"></a>
### ike\_identity
Method by which to identify the peer

*Type* : enum (Auto, IP Address, User\_fqdn)


<a name="ike\_identity\_data"></a>
### ike\_identity\_data
Ike identity data for Manual-ipaddress and user\_fqdn

*Type* : string


<a name="ike\_integ\_algo"></a>
### ike\_integ\_algo
HASH algorithm used to authenticate IKE Messages

*Type* : enum (MD5, SHA1, SHA256)


<a name="ike\_lifetime\_s"></a>
### ike\_lifetime\_s
Preferred duration in seconds, for an IKE association to exist

*Type* : integer


<a name="ike\_lifetime\_s\_max"></a>
### ike\_lifetime\_s\_max
Maximum preferred duration in seconds, to allow for an IKE association to exist

*Type* : integer


<a name="ike\_mode"></a>
### ike\_mode
Mode of IKE negotiation to use

*Type* : enum (Main, Aggressive)


<a name="ike\_peer\_authentication"></a>
### ike\_peer\_authentication
Type of authentication

*Type* : enum (Mirrored, PSK, Certificate)


<a name="ike\_peer\_preshared\_key"></a>
### ike\_peer\_preshared\_key
Peer's Pre-Shared Key to use for IKE Authentication

*Type* : string


<a name="ike\_preshared\_key"></a>
### ike\_preshared\_key
Pre-Shared Key to use for IKE Authentication

*Type* : string


<a name="ike\_version"></a>
### ike\_version
Version of the IKE protocol to use

*Type* : enum (IKEv1, IKEv2)


<a name="intranet\_service\_type"></a>
### intranet\_service\_type
Choose the service type to associate with the intranet service type

*Type* : enum (0, 1, 2, 3)


<a name="ipsec\_dest\_protected\_network"></a>
### ipsec\_dest\_protected\_network
Destination network IP and prefix of traffic to be protected by the Tunnel

*Type* : string


<a name="ipsec\_encryption"></a>
### ipsec\_encryption
Encryption type for IPsec messages

*Type* : enum (AES128, AES192, AES256, AES128GCM64, AES192GCM64, AES256GCM64, AES128GCM64, AES192GCM96, AES256GCM96, AES128GCM128, AES192GCM128, AES256GCM128)


<a name="ipsec\_hash\_algo"></a>
### ipsec\_hash\_algo
HASH algorithm used to authenticate IKE Messages

*Type* : enum (MD5, SHA1, SHA256)


<a name="ipsec\_lifetime\_kb"></a>
### ipsec\_lifetime\_kb
Amount of data in kb, for an IPsec association to exist

*Type* : integer


<a name="ipsec\_lifetime\_kb\_max"></a>
### ipsec\_lifetime\_kb\_max
Maximum amount of data in kb, to allow for an IPsec association to exist

*Type* : integer


<a name="ipsec\_lifetime\_s"></a>
### ipsec\_lifetime\_s
Preferred duration in seconds, for an IPsec association to exist

*Type* : integer


<a name="ipsec\_lifetime\_s\_max"></a>
### ipsec\_lifetime\_s\_max
Maximum preferred duration in seconds, to allow for an IPsec association to exist

*Type* : integer


<a name="ipsec\_mismatch\_behaviour"></a>
### ipsec\_mismatch\_behaviour
Action to take if a packet does not match the IPsec tunnels protected network

*Type* : enum (Drop, Send UnEncrypted, Use Non IPsec route)


<a name="ipsec\_pfs\_group"></a>
### ipsec\_pfs\_group
PFS group to use for perfect forward secrecy Key Generation

*Type* : enum (None, Group1, Group2, Group5, Group14, Group15, Group16, Group19, Group20, Group21)


<a name="ipsec\_service\_type"></a>
### ipsec\_service\_type
Choose the service type to associate with the ipsec tunnel

*Type* : enum (Intranet, LAN)


<a name="ipsec\_source\_protected\_network"></a>
### ipsec\_source\_protected\_network
Source network IP and prefix of traffic to be protected by the Tunnel

*Type* : string


<a name="ipsec\_tunnel"></a>
### ipsec\_tunnel

|Name|Schema|
|---|---|
|**id**  <br>*optional*|[id](#id)|
|**ike\_authentication**  <br>*optional*|[ike\_authentication](#ike\_authentication)|
|**ike\_dh\_group**  <br>*optional*|[ike\_dh\_group](#ike\_dh\_group)|
|**ike\_dpd\_timeout\_s**  <br>*optional*|[ike\_dpd\_timeout\_s](#ike\_dpd\_timeout\_s)|
|**ike\_encryption**  <br>*optional*|[ike\_encryption](#ike\_encryption)|
|**ike\_hash\_algo**  <br>*optional*|[ike\_hash\_algo](#ike\_hash\_algo)|
|**ike\_identity**  <br>*optional*|[ike\_identity](#ike\_identity)|
|**ike\_identity\_data**  <br>*optional*|[ike\_identity\_data](#ike\_identity\_data)|
|**ike\_integ\_algo**  <br>*optional*|[ike\_integ\_algo](#ike\_integ\_algo)|
|**ike\_lifetime\_s**  <br>*optional*|[ike\_lifetime\_s](#ike\_lifetime\_s)|
|**ike\_lifetime\_s\_max**  <br>*optional*|[ike\_lifetime\_s\_max](#ike\_lifetime\_s\_max)|
|**ike\_mode**  <br>*optional*|[ike\_mode](#ike\_mode)|
|**ike\_peer\_authentication**  <br>*optional*|[ike\_peer\_authentication](#ike\_peer\_authentication)|
|**ike\_peer\_preshared\_key**  <br>*optional*|[ike\_peer\_preshared\_key](#ike\_peer\_preshared\_key)|
|**ike\_preshared\_key**  <br>*optional*|[ike\_preshared\_key](#ike\_preshared\_key)|
|**ike\_version**  <br>*optional*|[ike\_version](#ike\_version)|
|**intranet\_service\_type**  <br>*optional*|[intranet\_service\_type](#intranet\_service\_type)|
|**ipsec\_dest\_protected\_network**  <br>*optional*|[ipsec\_dest\_protected\_network](#ipsec\_dest\_protected\_network)|
|**ipsec\_encryption**  <br>*optional*|[ipsec\_encryption](#ipsec\_encryption)|
|**ipsec\_hash\_algo**  <br>*optional*|[ipsec\_hash\_algo](#ipsec\_hash\_algo)|
|**ipsec\_lifetime\_kb**  <br>*optional*|[ipsec\_lifetime\_kb](#ipsec\_lifetime\_kb)|
|**ipsec\_lifetime\_kb\_max**  <br>*optional*|[ipsec\_lifetime\_kb\_max](#ipsec\_lifetime\_kb\_max)|
|**ipsec\_lifetime\_s**  <br>*optional*|[ipsec\_lifetime\_s](#ipsec\_lifetime\_s)|
|**ipsec\_lifetime\_s\_max**  <br>*optional*|[ipsec\_lifetime\_s\_max](#ipsec\_lifetime\_s\_max)|
|**ipsec\_mismatch\_behaviour**  <br>*optional*|[ipsec\_mismatch\_behaviour](#ipsec\_mismatch\_behaviour)|
|**ipsec\_pfs\_group**  <br>*optional*|[ipsec\_pfs\_group](#ipsec\_pfs\_group)|
|**ipsec\_service\_type**  <br>*optional*|[ipsec\_service\_type](#ipsec\_service\_type)|
|**ipsec\_source\_protected\_network**  <br>*optional*|[ipsec\_source\_protected\_network](#ipsec\_source\_protected\_network)|
|**ipsec\_tunnel\_additional\_protected\_network**  <br>*optional*|[ipsec\_tunnel\_additional\_protected\_network](#ipsec\_tunnel\_additional\_protected\_network)|
|**ipsec\_tunnel\_firewall\_zone**  <br>*optional*|[ipsec\_tunnel\_firewall\_zone](#ipsec\_tunnel\_firewall\_zone)|
|**ipsec\_tunnel\_type**  <br>*optional*|[ipsec\_tunnel\_type](#ipsec\_tunnel\_type)|
|**ipsec\_tunnel\_via\_api**  <br>*optional*|[ipsec\_tunnel\_via\_api](#ipsec\_tunnel\_via\_api)|
|**keepalive**  <br>*optional*|[keepalive](#keepalive)|
|**local\_ip**  <br>*optional*|[local\_ip](#local\_ip)|
|**mtu**  <br>*optional*|[mtu](#mtu)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**peer\_ip**  <br>*optional*|[peer\_ip](#peer\_ip)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**tunnel\_name**  <br>*optional*|[tunnel\_name](#tunnel\_name)|
|**validate\_peer\_identity**  <br>*optional*|[validate\_peer\_identity](#validate\_peer\_identity)|


<a name="ipsec\_tunnel\_additional\_protected\_network"></a>
### ipsec\_tunnel\_additional\_protected\_network
Flag to indicate if tunnel created via API

*Type* : boolean


<a name="ipsec\_tunnel\_delete\_success\_schema"></a>
### ipsec\_tunnel\_delete\_success\_schema

|Name|Schema|
|---|---|
|**ipsec\_tunnel**  <br>*optional*|[ipsec\_tunnel](#ipsec\_tunnel\_delete\_success\_schema-ipsec\_tunnel)|

<a name="ipsec\_tunnel\_delete\_success\_schema-ipsec\_tunnel"></a>
**ipsec\_tunnel**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="ipsec\_tunnel\_firewall\_zone"></a>
### ipsec\_tunnel\_firewall\_zone
ipsec tunnel firewall zone

*Type* : string


<a name="ipsec\_tunnel\_post\_success\_schema"></a>
### ipsec\_tunnel\_post\_success\_schema

|Name|Schema|
|---|---|
|**ipsec\_tunnel**  <br>*optional*|[ipsec\_tunnel](#ipsec\_tunnel\_post\_success\_schema-ipsec\_tunnel)|

<a name="ipsec\_tunnel\_post\_success\_schema-ipsec\_tunnel"></a>
**ipsec\_tunnel**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="ipsec\_tunnel\_put\_success\_schema"></a>
### ipsec\_tunnel\_put\_success\_schema

|Name|Schema|
|---|---|
|**ipsec\_tunnel**  <br>*optional*|[ipsec\_tunnel](#ipsec\_tunnel\_put\_success\_schema-ipsec\_tunnel)|

<a name="ipsec\_tunnel\_put\_success\_schema-ipsec\_tunnel"></a>
**ipsec\_tunnel**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="ipsec\_tunnel\_request\_schema"></a>
### ipsec\_tunnel\_request\_schema

|Name|Schema|
|---|---|
|**ipsec\_tunnel**  <br>*optional*|[ipsec\_tunnel](#ipsec\_tunnel)|


<a name="ipsec\_tunnel\_response\_schema"></a>
### ipsec\_tunnel\_response\_schema
*Type* : < [ipsec\_tunnel\_response\_schema](#ipsec\_tunnel\_response\_schema-inline) > array

<a name="ipsec\_tunnel\_response\_schema-inline"></a>
**ipsec\_tunnel\_response\_schema**

|Name|Schema|
|---|---|
|**id**  <br>*optional*|[id](#id)|
|**ike\_authentication**  <br>*optional*|[ike\_authentication](#ike\_authentication)|
|**ike\_dh\_group**  <br>*optional*|[ike\_dh\_group](#ike\_dh\_group)|
|**ike\_dpd\_timeout\_s**  <br>*optional*|[ike\_dpd\_timeout\_s](#ike\_dpd\_timeout\_s)|
|**ike\_encryption**  <br>*optional*|[ike\_encryption](#ike\_encryption)|
|**ike\_hash\_algo**  <br>*optional*|[ike\_hash\_algo](#ike\_hash\_algo)|
|**ike\_identity**  <br>*optional*|[ike\_identity](#ike\_identity)|
|**ike\_identity\_data**  <br>*optional*|[ike\_identity\_data](#ike\_identity\_data)|
|**ike\_integ\_algo**  <br>*optional*|[ike\_integ\_algo](#ike\_integ\_algo)|
|**ike\_lifetime\_s**  <br>*optional*|[ike\_lifetime\_s](#ike\_lifetime\_s)|
|**ike\_lifetime\_s\_max**  <br>*optional*|[ike\_lifetime\_s\_max](#ike\_lifetime\_s\_max)|
|**ike\_mode**  <br>*optional*|[ike\_mode](#ike\_mode)|
|**ike\_peer\_authentication**  <br>*optional*|[ike\_peer\_authentication](#ike\_peer\_authentication)|
|**ike\_peer\_preshared\_key**  <br>*optional*|[ike\_peer\_preshared\_key](#ike\_peer\_preshared\_key)|
|**ike\_preshared\_key**  <br>*optional*|[ike\_preshared\_key](#ike\_preshared\_key)|
|**ike\_version**  <br>*optional*|[ike\_version](#ike\_version)|
|**intranet\_service\_type**  <br>*optional*|[intranet\_service\_type](#intranet\_service\_type)|
|**ipsec\_dest\_protected\_network**  <br>*optional*|[ipsec\_dest\_protected\_network](#ipsec\_dest\_protected\_network)|
|**ipsec\_encryption**  <br>*optional*|[ipsec\_encryption](#ipsec\_encryption)|
|**ipsec\_hash\_algo**  <br>*optional*|[ipsec\_hash\_algo](#ipsec\_hash\_algo)|
|**ipsec\_lifetime\_kb**  <br>*optional*|[ipsec\_lifetime\_kb](#ipsec\_lifetime\_kb)|
|**ipsec\_lifetime\_kb\_max**  <br>*optional*|[ipsec\_lifetime\_kb\_max](#ipsec\_lifetime\_kb\_max)|
|**ipsec\_lifetime\_s**  <br>*optional*|[ipsec\_lifetime\_s](#ipsec\_lifetime\_s)|
|**ipsec\_lifetime\_s\_max**  <br>*optional*|[ipsec\_lifetime\_s\_max](#ipsec\_lifetime\_s\_max)|
|**ipsec\_mismatch\_behaviour**  <br>*optional*|[ipsec\_mismatch\_behaviour](#ipsec\_mismatch\_behaviour)|
|**ipsec\_pfs\_group**  <br>*optional*|[ipsec\_pfs\_group](#ipsec\_pfs\_group)|
|**ipsec\_service\_type**  <br>*optional*|[ipsec\_service\_type](#ipsec\_service\_type)|
|**ipsec\_source\_protected\_network**  <br>*optional*|[ipsec\_source\_protected\_network](#ipsec\_source\_protected\_network)|
|**ipsec\_tunnel\_additional\_protected\_network**  <br>*optional*|[ipsec\_tunnel\_additional\_protected\_network](#ipsec\_tunnel\_additional\_protected\_network)|
|**ipsec\_tunnel\_firewall\_zone**  <br>*optional*|[ipsec\_tunnel\_firewall\_zone](#ipsec\_tunnel\_firewall\_zone)|
|**ipsec\_tunnel\_type**  <br>*optional*|[ipsec\_tunnel\_type](#ipsec\_tunnel\_type)|
|**ipsec\_tunnel\_via\_api**  <br>*optional*|[ipsec\_tunnel\_via\_api](#ipsec\_tunnel\_via\_api)|
|**keepalive**  <br>*optional*|[keepalive](#keepalive)|
|**local\_ip**  <br>*optional*|[local\_ip](#local\_ip)|
|**mtu**  <br>*optional*|[mtu](#mtu)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**peer\_ip**  <br>*optional*|[peer\_ip](#peer\_ip)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**tunnel\_name**  <br>*optional*|[tunnel\_name](#tunnel\_name)|
|**validate\_peer\_identity**  <br>*optional*|[validate\_peer\_identity](#validate\_peer\_identity)|


<a name="ipsec\_tunnel\_type"></a>
### ipsec\_tunnel\_type
IPsec Tunnel Encapsulation Type

*Type* : enum (ESP, ESP\_NULL, ESP\_Auth, AH)


<a name="ipsec\_tunnel\_via\_api"></a>
### ipsec\_tunnel\_via\_api
Flag to indicate if tunnel created via API

*Type* : boolean


<a name="keepalive"></a>
### keepalive
Enable to keep the tunnel active and enable route eligiblity

*Type* : boolean


<a name="local\_ip"></a>
### local\_ip
Choose the local IP Address of the IPsec Tunnel

*Type* : string


<a name="mtu"></a>
### mtu
Enter the MTU for fragmenting IKE and IPsec packets

*Type* : integer


<a name="package\_name"></a>
### package\_name
Config package name using which the ipsec\_tunnel API operation should be performed.

*Type* : string


<a name="peer\_ip"></a>
### peer\_ip
Enter the peer IP Address of the IPsec Tunnel

*Type* : string


<a name="site\_name"></a>
### site\_name
Site Name

*Type* : string


<a name="tunnel\_name"></a>
### tunnel\_name
IPsec tunnel name or the intranet service name

*Type* : string


<a name="validate\_peer\_identity"></a>
### validate\_peer\_identity
Validate the IKE's peer Identity

*Type* : boolean






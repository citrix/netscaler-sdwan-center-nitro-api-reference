# login

This resource can be used to login and logout of SD-WAN Center

## Read/write properties

**password&lt;String>**

Authentication Password.

**username&lt;String>**

User Name.
Minimum length = 1
Maximum length = 32

## Read only properties

## Operations

* [add](#add) 
* [delete](#delete)

### <a name="add">add</a>

**URL**: http://&lt;MGMT-IP>/sdwan\_center/nitro/v1/config/login?action=add

**Description**: Use this operation to Login To SD-WAN Center

**HTTP Method**: POST

**Request Payload**: JSON

```json
{"login": {
      "password":<String_value>,
      "username":<String_value>}}
```

**Response Payload**: JSON

```json
{ "login":{
      "password":<String_value>,
      "username":<String_value>}]}
```

### <a name="delete">delete</a>

**URL**: http:/&lt;MGMT-IP>/sdwan\_center/nitro/v1/config/login/

**Description**: Use this operation to Logout From SD-WAN Center

**HTTP Method**: DELETE

**Response Payload**: JSON

```json
{ "errorcode": 0, "message": "Done", "severity": <String_value> }
```
#regions

This resource can be used to get the region discovery configuration.

## Read/write properties

## Read only properties

**region\_control\_node\_ip&lt;String>**

The primary region control node ip address.

**region\_name&lt;String>**

The region name.

**collector\_ip&lt;String>**

The IP address of the collector configured to work with the region.

**region\_discovery\_status&lt;String>**

The status of discovery by Collector for the region appliances.

## Operations

### get (all)

**URL**: http://&lt;MGMT-IP&gt;/sdwan\_center/nitro/v1/config/regions

**Description**: Use this operation to get the regions discovery configuration.

**HTTP Method**: GET

**Response Payload**: JSON

```json
{"regions":[{
      "region_control_node_ip":<String_value>,
      "region_name":<String_value>,
      "collector_ip":<String_value>,
      "region_discovery_status":<String_value>}]}
```
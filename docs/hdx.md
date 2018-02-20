# hdx

API to get reports for HDX (bandwidth is in Kbps and data is in KB)

## Read/write properties

## Read only properties

**sessions&lt;Integer&gt;**

Sessions.

**udp\_flows&lt;Integer&gt;**

UDP Flows.

**region\_name&lt;String&gt;**

The region name.

**tcp\_flows&lt;Integer&gt;**

TCP Flows.

**qoe\_index&lt;Integer&gt;**

Quality of experience index.

**users&lt;Integer&gt;**

Users.

**site\_name&lt;String&gt;**

The site name.

## Operations

### get (all)

**URL**: http://&lt;MGMT-IP>/sdwan\_center/nitro/v1/reports/hdx

**Description**: Use this operation to get a report for HDX. The response payload also contains the meta\_data block.

**HTTP Method**: GET

**Response Payload**: JSON

```json
{"hdx":[{
      "sessions":<Integer_value>,
      "udp_flows":<Integer_value>,
      "region_name":<String_value>,
      "tcp_flows":<Integer_value>,
      "qoe_index":<Integer_value>,
      "users":<Integer_value>,
      "site_name":<String_value>}]}
```
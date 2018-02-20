# events

API to get reports for Events (bandwidth is in Kbps and data is in KB)

## Read/write properties

## Read only properties

**debug\_events&lt;String&gt;**

The number of debugging events that have occured.

**region\_name&lt;String&gt;**

The region name.

**alert\_events&lt;Integer&gt;**

The number of alert events that have occured.

**info\_events&lt;String&gt;**

The number of informational events that have occured.

**notice\_events&lt;String&gt;**

The number of notice events that have occured.

**critical\_events&lt;Integer&gt;**

The number of critical events that have occured.

**warning\_events&lt;Integer&gt;**

The number of warning events that have occured.

**error\_events&lt;Integer&gt;**

The number of error events that have occured.

**emergency\_events&lt;Integer&gt;**

The number of emergency events that have occured.

## Operations

### get (all)

**URL**: http://&lt;MGMT-IP&gt;/sdwan\_center/nitro/v1/reports/events

**Description**: Use this operation to get a report for Events. The response payload also contains the meta\_data block.

**HTTP Method**: GET

**Response Payload**: JSON

```json
{"events":[{
      "debug_events":<String_value>,
      "region_name":<String_value>,
      "alert_events":<Integer_value>,
      "info_events":<String_value>,
      "notice_events":<String_value>,
      "critical_events":<Integer_value>,
      "warning_events":<Integer_value>,
      "error_events":<Integer_value>,
      "emergency_events":<Integer_value>}]}
```
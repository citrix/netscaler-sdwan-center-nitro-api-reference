# applications

API to get reports for Top Applications (bandwidth is in Kbps and data is in KB)

## Read/write properties

## Read only properties

**incoming\_traffic&lt;Double&gt;**

Incoming traffic.

**region\_name&lt;String&gt;**

The region name.

**application\_name&lt;String&gt;**

The application name.

**outgoing\_traffic&lt;Double&gt;**

Outgoing traffic.

**total\_traffic&lt;Double&gt;**

Total traffic.

## Operations

## get (all)

**URL**: http://&lt;MGMT-IP>/sdwan\_center/nitro/v1/reports/applications

**Description**: Use this operation to get a report for Top applications. The response payload also contains the meta\_data block.

**HTTP Method**: GET

**Response Payload**: JSON

```json
{"applications":[{
      "incoming_traffic":<Double_value>,
      "region_name":<String_value>,
      "application_name":<String_value>,
      "outgoing_traffic":<Double_value>,
      "total_traffic":<Double_value>}]}
```
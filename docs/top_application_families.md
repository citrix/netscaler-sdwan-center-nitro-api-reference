# top\_application\_families

API to get reports for Top Application Families (bandwidth is in Kbps and data is in KB)

## Read/write properties

## Read only properties

**incoming\_traffic&lt;Double&gt;**

Incoming traffic.

**application\_family&lt;String&gt;**

The application family.

**region\_name&lt;String&gt;**

The region name.

**outgoing\_traffic&lt;Double&gt;**

Outgoing traffic.

**total\_traffic&lt;Double&gt;**

Total traffic.

## Operations

### get (all)

**URL**: http://&lt;MGMT-IP>/sdwan\_center/nitro/v1/reports/top\_application\_families

**Description**: Use this operation to get a report for top application families. The response payload also contains the meta\_data block.

**HTTP Method**: GET

**Response Payload**: JSON

```json
{"top_application_families":[{
      "incoming_traffic":<Double_value>,
      "application_family":<String_value>,
      "region_name":<String_value>,
      "outgoing_traffic":<Double_value>,
      "total_traffic":<Double_value>}]}
```
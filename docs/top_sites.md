# top\_sites

API to get reports for Top Sites (bandwidth is in Kbps and data is in KB)

## Read/write properties

## Read only properties

incoming\_traffic&lt;Double>

Incoming traffic.

region\_name&lt;String>

The region name.

outgoing\_traffic&lt;Double>

Outgoing traffic.

site\_name&lt;String>

The site name.

total\_traffic&lt;Double>

Total traffic.

## Operations

### get (all)

**URL**: http://&lt;MGMT-IP>/sdwan\_center/nitro/v1/reports/top\_sites

**Description**: Use this operation to get a report for Top sites. The response payload also contains the meta_data block.

**HTTP Method**: GET

**Response Payload**: JSON

```json
{"top_sites":[{
      "incoming_traffic":<Double_value>,
      "region_name":<String_value>,
      "outgoing_traffic":<Double_value>,
      "site_name":<String_value>,
      "total_traffic":<Double_value>}]}
```
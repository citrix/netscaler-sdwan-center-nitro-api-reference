# mos\_scores

API to get reports for MOS Scores (bandwidth is in Kbps and data is in KB)

## Read/write properties

## Read only properties

**lowest\_virtual\_wan\_mos&lt;Integer&gt;**

The worst quality score for an application during the time period measured using a scale of 1-5.

**region\_name&lt;String&gt;**

The region name.

**virtual\_service&lt;String&gt;**

The Virtual Path name.

**name&lt;String&gt;**

The MOS Score name.

**site\_name&lt;String&gt;**

The site name.

**average\_virtual\_wan\_mos&lt;Integer&gt;**

The worst average quality score for an application during the time period measured using a scale of 1-5.

## Operations

### get (all)

**URL**: http://&lt;MGMT-IP>/sdwan\_center/nitro/v1/reports/mos\_scores

**Description**: Use this operation to get a report for MOS Scores. The response payload also contains the meta\_data block.

**HTTP Method**: GET

**Response Payload**: JSON

```json
{"mos_scores":[{
      "lowest_virtual_wan_mos":<Integer_value>,
      "region_name":<String_value>,
      "virtual_service":<String_value>,
      "name":<String_value>,
      "site_name":<String_value>,
      "average_virtual_wan_mos":<Integer_value>}]}
```
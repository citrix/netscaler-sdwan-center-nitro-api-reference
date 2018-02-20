# services

API to get reports for services (bandwidth is in Kbps and data is in KB)

## Read/write properties

## Read only properties

**wan\_2\_lan\_percent\_drop&lt;Double&gt;**

The WAN to LAN packets dropped.

**lan\_2\_wan\_bandwidth&lt;Double&gt;**

The LAN to WAN Bandwidth for all packet types.

**service\_type&lt;String&gt;**

The Service Type (Virtual Path, Internet, Intranet or Passthrough).

**region\_name&lt;String&gt;**

The region name.

**wan\_2\_lan\_packets&lt;Integer&gt;**

The WAN to LAN packets for all packet types.

**name&lt;String&gt;**

The site name.

**lan\_2\_wan\_percent\_drop&lt;Double&gt;**

The LAN to WAN drop, in percent.

**wan\_2\_lan\_bandwidth&lt;Double&gt;**

The WAN to LAN bandwidth for all packet types.

**wan\_2\_lan\_packets\_dropped&lt;Integer&gt;**

The WAN to LAN packets dropped.

**data\_coverage&lt;Double&gt;**

The amount in percent, of the selected time period for which there is data.

**lan\_2\_wan\_packets\_dropped&lt;Integer&gt;**

The LAN to WAN packets dropped.

**lan\_2\_wan\_packets&lt;Integer&gt;**

The LAN to WAN packets for all packet types.

## Operations

### get (all)

**URL**: http://&lt;MGMT-IP>/sdwan\_center/nitro/v1/reports/services

**Description**: Use this operation to get a report for services. The response payload also contains the meta\_data block.

**HTTP Method**: GET

**Response Payload**: JSON

```json
{"services":[{
      "wan_2_lan_percent_drop":<Double_value>,
      "lan_2_wan_bandwidth":<Double_value>,
      "service_type":<String_value>,
      "region_name":<String_value>,
      "wan_2_lan_packets":<Integer_value>,
      "name":<String_value>,
      "lan_2_wan_percent_drop":<Double_value>,
      "wan_2_lan_bandwidth":<Double_value>,
      "wan_2_lan_packets_dropped":<Integer_value>,
      "data_coverage":<Double_value>,
      "lan_2_wan_packets_dropped":<Integer_value>,
      "lan_2_wan_packets":<Integer_value>}]}
```
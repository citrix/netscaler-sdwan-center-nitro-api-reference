# sites

API to get reports for sites (bandwidth is in Kbps and data is in KB)

## Read/write properties

## Read only properties

**wan\_2\_lan\_data&lt;Double&gt;**

The WAN to LAN data received.

**lan\_2\_wan\_data&lt;Double&gt;**

The LAN to WAN data sent.

**wan\_2\_lan\_packets&lt;Integer&gt;**

The WAN to LAN packets for all packet types.

**lan\_2\_wan\_control\_packets&lt;Integer&gt;**

The LAN to WAN control packets.

**lan\_2\_wan\_realtime\_packets&lt;Integer&gt;**

The LAN to WAN real-time packets.

**lan\_2\_wan\_available\_bandwidth&lt;Double&gt;**

The LAN to WAN available Bandwidth.

**wan\_2\_lan\_permitted\_bandwidth&lt;Double&gt;**

The WAN to LAN Permitted Bandwidth.

**wan\_2\_lan\_bandwidth&lt;Double&gt;**

The WAN to LAN Bandwidth for all packet types.

**lan\_2\_wan\_bulk\_bandwidth\_packets&lt;Integer&gt;**

The LAN to WAN bulk Bandwidth packets.

**lan\_2\_wan\_realtime\_bandwidth&lt;Double&gt;**

The LAN to WAN real-time Bandwidth.

**lan\_2\_wan\_interactive\_packets&lt;Integer&gt;**

The LAN to WAN interactive packets.

**site\_name&lt;String&gt;**

The site name.

**lan\_2\_wan\_control\_bandwidth&lt;Double&gt;**

The LAN to WAN control Bandwidth.

**lan\_2\_wan\_bandwidth&lt;Double&gt;**

The LAN to WAN Bandwidth for all packet types.

**wan\_2\_lan\_available\_bandwidth&lt;Double&gt;**

The WAN to LAN available Bandwidth.

**total\_permitted\_bandwidth&lt;Double&gt;**

The total permitted bandwidth.

**region\_name&lt;String&gt;**

The region name.

**lan\_2\_wan\_permitted\_bandwidth&lt;Double&gt;**

The LAN to WAN permitted Bandwidth.

**total\_available\_bandwidth&lt;Double&gt;**

The total available bandwidth.

**total\_data&lt;Double&gt;**

The total data.

**total\_bandwidth&lt;Double&gt;**

The total bandwidth.

**lan\_2\_wan\_interactive\_bandwidth&lt;Double&gt;**

The LAN to WAN interactive Bandwidth.

**lan\_2\_wan\_bulk\_packets&lt;Integer&gt;**

The LAN to WAN bulk packets.

**data\_coverage&lt;Double&gt;**

The amount in percent of the selected time for which there is data.

**lan\_2\_wan\_packets&lt;Integer&gt;**

The LAN to WAN packets for all packet types.

## Operations

### get (all)

**URL**: http://&lt;MGMT-IP>/sdwan\_center/nitro/v1/reports/sites

**Description**: Use this operation to get a report for sites. The response payload also contains the meta\_data block.

**HTTP Method**: GET

**Response Payload**: JSON

```json
{"sites":[{
      "wan_2_lan_data":<Double_value>,
      "lan_2_wan_data":<Double_value>,
      "wan_2_lan_packets":<Integer_value>,
      "lan_2_wan_control_packets":<Integer_value>,
      "lan_2_wan_realtime_packets":<Integer_value>,
      "lan_2_wan_available_bandwidth":<Double_value>,
      "wan_2_lan_permitted_bandwidth":<Double_value>,
      "wan_2_lan_bandwidth":<Double_value>,
      "lan_2_wan_bulk_bandwidth_packets":<Integer_value>,
      "lan_2_wan_realtime_bandwidth":<Double_value>,
      "lan_2_wan_interactive_packets":<Integer_value>,
      "site_name":<String_value>,
      "lan_2_wan_control_bandwidth":<Double_value>,
      "lan_2_wan_bandwidth":<Double_value>,
      "wan_2_lan_available_bandwidth":<Double_value>,
      "total_permitted_bandwidth":<Double_value>,
      "region_name":<String_value>,
      "lan_2_wan_permitted_bandwidth":<Double_value>,
      "total_available_bandwidth":<Double_value>,
      "total_data":<Double_value>,
      "total_bandwidth":<Double_value>,
      "lan_2_wan_interactive_bandwidth":<Double_value>,
      "lan_2_wan_bulk_packets":<Integer_value>,
      "data_coverage":<Double_value>,
      "lan_2_wan_packets":<Integer_value>}]}
```
# wan\_links

API to get reports for WAN links (bandwidth is in Kbps and data is in KB)

## Read/write properties

## Read only properties

**wan\_2\_lan\_packets&lt;Integer&gt;**

The WAN to LAN packets for all packet types.

**wan\_2\_lan\_mismatched\_packets&lt;Integer&gt;**

The WAN to LAN packets not matching an MPLS Queue.

**wan\_2\_lan\_permitted\_bandwidth&lt;Double&gt;**

The WAN to LAN permitted bandwidth.

**lan\_2\_wan\_interactive\_packets&lt;Integer&gt;**

The LAN to WAN interactive packets.

**lan\_2\_wan\_control\_bandwidth&lt;Double&gt;**

The LAN to WAN control bandwidth.

**wan\_2\_lan\_available\_bandwidth&lt;Double&gt;**

The WAN to LAN available bandwidth.

**lan\_2\_wan\_bandwidth&lt;Double&gt;**

The LAN to WAN bandwidth for all packet types.

**total\_permitted\_bandwidth&lt;Double&gt;**

Total permitted bandwidth.

**region\_name&lt;String&gt;**

The region name.

**wan\_2\_lan\_loss\_percent&lt;Double&gt;**

The WAN to LAN loss, in percent.

**lan\_2\_wan\_mismatched\_bandwidth&lt;Double&gt;**

The LAN to WAN Bandwidth not matching an MPLS Queue.

**total\_bandwidth&lt;Double&gt;**

Total bandwidth.

**wan\_2\_lan\_best\_one\_way\_time\_latency&lt;Integer&gt;**

The WAN to LAN best one way time latency, in milliseconds.

**lan\_2\_wan\_bulk\_packets&lt;Integer&gt;**

The LAN to WAN bulk packets.

**wan\_2\_lan\_jitter&lt;Integer&gt;**

Maximum WAN to LAN jitter, in milliseconds.

**wan\_2\_lan\_mismatched\_bandwidth&lt;Double&gt;**

The WAN to LAN bandwidth not matching an MPLS Queue.

**lan\_2\_wan\_control\_packets&lt;Integer&gt;**

The LAN to WAN control packets.

**lan\_2\_wan\_mismatched\_packets&lt;Integer&gt;**

The LAN to WAN packets not matching an MPLS Queue.

**wan\_2\_lan\_packets\_lost&lt;Integer&gt;**

The WAN to LAN packet loss.

**lan\_2\_wan\_realtime\_packets&lt;Integer&gt;**

The LAN to WAN real-time packets.

**lan\_2\_wan\_available\_bandwidth&lt;Double&gt;**

The LAN to WAN available Bandwidth.

**wan\_2\_lan\_congestion&lt;String&gt;**

Congestion detected due to increased, unexpected packet flow in the WAN.

**wan\_2\_lan\_bandwidth&lt;Double&gt;**

The WAN to LAN bandwidth for all packet types.

**lan\_2\_wan\_realtime\_bandwidth&lt;Double&gt;**

The LAN to WAN real-time bandwidth.

**site\_name&lt;String&gt;**

The site name.

**lan\_2\_wan\_bulk\_bandwidth&lt;Double&gt;**

The LAN to WAN bulk bandwidth.

**wan\_2\_lan\_packets\_ooo&lt;Integer&gt;**

The WAN to LAN packets out-of-order.

**lan\_2\_wan\_permitted\_bandwidth&lt;Double&gt;**

The LAN to WAN permitted Bandwidth.

**total\_available\_bandwidth&lt;Double&gt;**

Total available bandwidth.

**total\_data&lt;Double&gt;**

Total data.

**lan\_2\_wan\_interactive\_bandwidth&lt;Double&gt;**

The LAN to WAN interactive bandwidth.

**wan\_link\_name&lt;String&gt;**

The WAN link name.

**wan\_2\_lan\_ooo\_percent&lt;Double&gt;**

The WAN to LAN out-of-order, in percent.

**data\_coverage&lt;Double&gt;**

The amount, in percent of the selected time period for which there is data.

**lan\_2\_wan\_packets&lt;Integer&gt;**

The LAN to WAN packets for all packet types.

## Operations

### get (all)

**URL**: http://&lt;MGMT-IP>/sdwan\_center/nitro/v1/reports/wan\_links

**Description**: Use this operation to get a report for WAN Links. The response payload also contains the meta\_data block.

**HTTP Method**: GET

**Response Payload**: JSON

```json
{"wan_links":[{
      "wan_2_lan_packets":<Integer_value>,
      "wan_2_lan_mismatched_packets":<Integer_value>,
      "wan_2_lan_permitted_bandwidth":<Double_value>,
      "lan_2_wan_interactive_packets":<Integer_value>,
      "lan_2_wan_control_bandwidth":<Double_value>,
      "wan_2_lan_available_bandwidth":<Double_value>,
      "lan_2_wan_bandwidth":<Double_value>,
      "total_permitted_bandwidth":<Double_value>,
      "region_name":<String_value>,
      "wan_2_lan_loss_percent":<Double_value>,
      "lan_2_wan_mismatched_bandwidth":<Double_value>,
      "total_bandwidth":<Double_value>,
      "wan_2_lan_best_one_way_time_latency":<Integer_value>,
      "lan_2_wan_bulk_packets":<Integer_value>,
      "wan_2_lan_jitter":<Integer_value>,
      "wan_2_lan_mismatched_bandwidth":<Double_value>,
      "lan_2_wan_control_packets":<Integer_value>,
      "lan_2_wan_mismatched_packets":<Integer_value>,
      "wan_2_lan_packets_lost":<Integer_value>,
      "lan_2_wan_realtime_packets":<Integer_value>,
      "lan_2_wan_available_bandwidth":<Double_value>,
      "wan_2_lan_congestion":<String_value>,
      "wan_2_lan_bandwidth":<Double_value>,
      "lan_2_wan_realtime_bandwidth":<Double_value>,
      "site_name":<String_value>,
      "lan_2_wan_bulk_bandwidth":<Double_value>,
      "wan_2_lan_packets_ooo":<Integer_value>,
      "lan_2_wan_permitted_bandwidth":<Double_value>,
      "total_available_bandwidth":<Double_value>,
      "total_data":<Double_value>,
      "lan_2_wan_interactive_bandwidth":<Double_value>,
      "wan_link_name":<String_value>,
      "wan_2_lan_ooo_percent":<Double_value>,
      "data_coverage":<Double_value>,
      "lan_2_wan_packets":<Integer_value>}]}
```
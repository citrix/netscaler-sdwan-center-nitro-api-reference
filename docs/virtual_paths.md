# virtual\_paths

API to get reports for virtual paths (bandwidth is in Kbps and data is in KB)

## Read/write properties

## Read only properties

**wan\_2\_lan\_packets\_loss&lt;Integer&gt;**

The WAN to LAN packets lost.

**wan\_2\_lan\_packets&lt;Integer&gt;**

The WAN to LAN packets for all packet types.

**good\_time&lt;String&gt;**

The time that the service was good, in seconds.

**wan\_2\_lan\_permitted\_bandwidth&lt;Double&gt;**

The WAN to LAN permitted bandwidth.

**lan\_2\_wan\_interactive\_packets&lt;Integer&gt;**

The LAN to WAN interactive packets.

**lan\_2\_wan\_control\_bandwidth&lt;Double&gt;**

The LAN to WAN Control Bandwidth.

**wan\_2\_lan\_mismtached\_packets&lt;Integer&gt;**

The WAN to LAN packets not matching an MPLS Queue.

**lan\_2\_wan\_bandwidth&lt;Double&gt;**

The LAN to WAN Bandwidth for all packet types.

**region\_name&lt;String&gt;**

The region name.

**lan\_2\_wan\_bulk\_packets&lt;Integer&gt;**

The LAN to WAN bulk packets.

**wan\_2\_lan\_percent\_ooo&lt;Double&gt;**

The WAN to LAN out-of-order in percent.

**wan\_2\_lan\_mismatched\_bandwidth&lt;Double&gt;**

The WAN to LAN bandwidth not matching an MPLS Queue.

**wan\_2\_lan\_percent\_loss&lt;Double&gt;**

The WAN to LAN loss, in percent.

**lan\_2\_wan\_control\_packets&lt;Integer&gt;**

The LAN to WAN control packets.

**lan\_2\_wan\_realtime\_packets&lt;Integer&gt;**

The LAN to WAN real-time packets.

**virtual\_path\_name&lt;String&gt;**

The virtual path name.

**ipsec\_worst\_state&lt;String&gt;**

The IPsec tunnel worst state observed during the time period.

**down\_time&lt;String&gt;**

The time that the service was unusable, in seconds.

**wan\_2\_lan\_bandwidth&lt;Double&gt;**

The WAN to LAN bandwidth for all packet types.

**good\_time\_percent&lt;Double&gt;**

The time, in percent that the service was good.

**lan\_2\_wan\_realtime\_bandwidth&lt;Double&gt;**

The LAN to WAN Realtime Bandwidth.

**site\_name&lt;String&gt;**

The site name.

**down\_time\_percent&lt;Double&gt;**

The time, in percent that the service was unusable.

**bad\_time\_percent&lt;Double&gt;**

The time, in percent that the service was bad.

**up\_time&lt;String&gt;**

The time that the service was usable, in seconds.

**worst\_state&lt;String&gt;**

The worst state observed during the time period.

**lan\_2\_wan\_bulk\_bandwidth&lt;Double&gt;**

The LAN to WAN bulk bandwidth.

**wan\_2\_lan\_packets\_ooo&lt;Integer&gt;**

The WAN to LAN packets out-of-order.

**bad\_time&lt;String&gt;**

The time that the service was bad, in seconds.

**lan\_2\_wan\_permitted bandwidth&lt;Double&gt;**

The LAN to WAN permitted bandwidth.

**percent\_up\_time&lt;Double&gt;**

The time, in percent that the service was usable.

**lan\_2\_wan\_interactive\_bandwidth&lt;Double&gt;**

The LAN to WAN interactive bandwidth.

**virtual\_path\_type&lt;String&gt;**

Virtual path type ( static or dynamic).

**wan\_2\_lan\_best\_one\_way\_time\_latency\_ms&lt;Integer&gt;**

The WAN to LAN best one way time latency in milliseconds.

**wan\_2\_lan\_congestion\_count&lt;String&gt;**

Congestion detected due to increased, unexpected delay in packet flow in the WAN.

**data\_coverage&lt;Double&gt;**

The amount, in percent of the selected time period for which there is data.

**lan\_2\_wan\_packets&lt;Integer&gt;**

The LAN to WAN packets for all packet types.

**wan\_2\_lan\_max\_jitter\_ms&lt;Integer&gt;**

The maximum WAN to LAN jitter in milliseconds.

## Operations

### get (all)

**URL**: http://&lt;MGMT-IP>/sdwan\_center/nitro/v1/reports/virtual\_paths

**Description**: Use this operation to get a report for virtual paths. The response payload also contains the meta\_data block.

**HTTP Method**: GET

**Response Payload**: JSON

```json
{"virtual_paths":[{
      "wan_2_lan_packets_loss":<Integer_value>,
      "wan_2_lan_packets":<Integer_value>,
      "good_time":<String_value>,
      "wan_2_lan_permitted_bandwidth":<Double_value>,
      "lan_2_wan_interactive_packets":<Integer_value>,
      "lan_2_wan_control_bandwidth":<Double_value>,
      "wan_2_lan_mismtached_packets":<Integer_value>,
      "lan_2_wan_bandwidth":<Double_value>,
      "region_name":<String_value>,
      "lan_2_wan_bulk_packets":<Integer_value>,
      "wan_2_lan_percent_ooo":<Double_value>,
      "wan_2_lan_mismatched_bandwidth":<Double_value>,
      "wan_2_lan_percent_loss":<Double_value>,
      "lan_2_wan_control_packets":<Integer_value>,
      "lan_2_wan_realtime_packets":<Integer_value>,
      "virtual_path_name":<String_value>,
      "ipsec_worst_state":<String_value>,
      "down_time":<String_value>,
      "wan_2_lan_bandwidth":<Double_value>,
      "good_time_percent":<Double_value>,
      "lan_2_wan_realtime_bandwidth":<Double_value>,
      "site_name":<String_value>,
      "down_time_percent":<Double_value>,
      "bad_time_percent":<Double_value>,
      "up_time":<String_value>,
      "worst_state":<String_value>,
      "lan_2_wan_bulk_bandwidth":<Double_value>,
      "wan_2_lan_packets_ooo":<Integer_value>,
      "bad_time":<String_value>,
      "lan_2_wan_permitted bandwidth":<Double_value>,
      "percent_up_time":<Double_value>,
      "lan_2_wan_interactive_bandwidth":<Double_value>,
      "virtual_path_type":<String_value>,
      "wan_2_lan_best_one_way_time_latency_ms":<Integer_value>,
      "wan_2_lan_congestion_count":<String_value>,
      "data_coverage":<Double_value>,
      "lan_2_wan_packets":<Integer_value>,
      "wan_2_lan_max_jitter_ms":<Integer_value>}]}
```
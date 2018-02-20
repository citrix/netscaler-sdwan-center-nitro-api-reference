# gre\_tunnels

API to get reports for GRE Tunnels (bandwidth is in Kbps and data is in KB)

## Read/write properties

## Read only properties

**packets\_dropped&lt;Integer&gt;**

Packets dropped.

**region\_name&lt;String&gt;**

The region name.

**packets\_received&lt;Integer&gt;**

Packets received.

**gre\_tunnel\_name&lt;String&gt;**

The GRE Tunnel name.

**bandwidth\_transmitted&lt;Double&gt;**

Transmit bandwidth.

**packets\_transmitted&lt;Integer&gt;**

Packets transmitted.

**data\_coverage&lt;Double&gt;**

The amount, in percent of the selected time period for which there is data.

**packets\_fragmented&lt;String&gt;**

Packets fragmented.

**link\_state&lt;String&gt;**

The worst state observed during the time period.

**site\_name&lt;String&gt;**

The site name.

**mtu&lt;String&gt;**

The maximum transmission unit.

**bandwidth\_received&lt;Double&gt;**

Receive bandwidth.

## Operations

### get (all)

**URL**: http://&lt;MGMT-IP>/sdwan\_center/nitro/v1/reports/gre\_tunnels

**Description**: Use this operation to get a report for GRE Tunnels. The response payload also contains the meta\_data block.

**HTTP Method**: GET

**Response Payload**: JSON

```json
{"gre_tunnels":[{
      "packets_dropped":<Integer_value>,
      "region_name":<String_value>,
      "packets_received":<Integer_value>,
      "gre_tunnel_name":<String_value>,
      "bandwidth_transmitted":<Double_value>,
      "packets_transmitted":<Integer_value>,
      "data_coverage":<Double_value>,
      "packets_fragmented":<String_value>,
      "link_state":<String_value>,
      "site_name":<String_value>,
      "mtu":<String_value>,
      "bandwidth_received":<Double_value>}]}
```
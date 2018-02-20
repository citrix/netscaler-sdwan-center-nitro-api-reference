# ipsec\_tunnels

API to get reports for IPsec Tunnels (bandwidth is in Kbps and data is in KB)

## Read/write properties

## Read only properties

**packets\_dropped&lt;Integer&gt;**

Packets dropped.

**data\_dropped&lt;Integer&gt;**

Data dropped.

**service\_type&lt;String&gt;**

The type of service associated with the IPsec tunnel.

**region\_name&lt;String&gt;**

The region name.

**ipsec\_tunnel\_worst\_state&lt;String&gt;**

The IPsec tunnel worst state observed during the time period.

**packets\_received&lt;Integer&gt;**

Packets received.

**ipsec\_tunnel\_name&lt;String&gt;**

The IPsec Tunnel name.

**bandwidth\_transmitted&lt;Double&gt;**

Transmit bandwidth.

**packets\_transmitted&lt;Integer&gt;**

Packets transmitted.

**site\_name&lt;String&gt;**

The site name.

**mtu&lt;Integer&gt;**

The maximum transmission unit, in bytes.

**bandwidth\_received&lt;Double&gt;**

Receive bandwidth.

## Operations

### get (all)

**URL**: http://&lt;MGMT-IP>/sdwan\_center/nitro/v1/reports/ipsec\_tunnels

**Description**: Use this operation to get a report for IPsec Tunnels. The response payload also contains the meta\_data block.

**HTTP Method**: GET

**Response Payload**: JSON

```json
{"ipsec_tunnels":[{
      "packets_dropped":<Integer_value>,
      "data_dropped":<Integer_value>,
      "service_type":<String_value>,
      "region_name":<String_value>,
      "ipsec_tunnel_worst_state":<String_value>,
      "packets_received":<Integer_value>,
      "ipsec_tunnel_name":<String_value>,
      "bandwidth_transmitted":<Double_value>,
      "packets_transmitted":<Integer_value>,
      "site_name":<String_value>,
      "mtu":<Integer_value>,
      "bandwidth_received":<Double_value>}]}
```
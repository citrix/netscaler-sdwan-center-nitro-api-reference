# ethernet\_interfaces

API to get reports for Ethernet Interfaces (bandwidth is in Kbps and data is in KB)

## Read/write properties

## Read only properties

**errors&lt;Integer&gt;**

Errors.

**region\_name&lt;String&gt;**

The region name.

**packets\_received&lt;Integer&gt;**

Packets received.

**ethernet\_interface\_name&lt;String&gt;**

The name.

**bandwidth\_transmitted&lt;Double&gt;**

Transmit bandwidth.

**packets\_transmitted&lt;Integer&gt;**

Packets transmitted.

**data\_coverage&lt;Double&gt;**

The amount, in percent of the selected time period for which there is data.

**link\_state&lt;String&gt;**

The worst state observed during the time period.

**site\_name&lt;String&gt;**

The site name.

**bandwidth\_received&lt;Double&gt;**

Receive bandwidth.

## Operations

### get (all)

**URL**: http://&lt;MGMT-IP&gt;/sdwan\_center/nitro/v1/reports/ethernet\_interfaces

**Description**: Use this operation to get a report for Ethernet interfaces. The response payload also contains the meta\_data block.

**HTTP Method**: GET

**Response Payload**: JSON

```json
{"ethernet_interfaces":[{
      "errors":<Integer_value>,
      "region_name":<String_value>,
      "packets_received":<Integer_value>,
      "ethernet_interface_name":<String_value>,
      "bandwidth_transmitted":<Double_value>,
      "packets_transmitted":<Integer_value>,
      "data_coverage":<Double_value>,
      "link_state":<String_value>,
      "site_name":<String_value>,
      "bandwidth_received":<Double_value>}]}
```
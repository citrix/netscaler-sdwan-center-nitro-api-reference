# classes

API to get reports for classes (bandwidth is in Kbps and data is in KB)

## Read/write properties

## Read only properties

**packets\_dropped&lt;Integer&gt;**

Packets dropped.

**data\_dropped&lt;Double&gt;**

Data dropped.

**data\_pending&lt;Double&gt;**

Data pending.

**wait\_time&lt;Integer&gt;**

Wait time, in milliseconds.

**class\_name&lt;String&gt;**

The class name.

**percent\_drop&lt;Double&gt;**

Drop, in percent.

**region\_name&lt;String&gt;**

The region name.

**virtual\_service&lt;String&gt;**

The Virtual Path name.

**packets\_pending&lt;Integer&gt;**

Packets pending.

**sent\_bandwidth&lt;Double&gt;**

Sent bandwidth.

**incoming\_traffic&lt;Double&gt;**

Incoming traffic.

**data\_coverage&lt;Double&gt;**

The amount, in percent of the selected time period for which there is data.

**class\_type&lt;String&gt;**

Class type (control, real-time, interact or bulk).

**site\_name&lt;String&gt;**

The site name.

**packets\_sent&lt;Integer&gt;**

Packets sent.

## Operations

### get (all)

**URL**: http://&lt;MGMT-IP>/sdwan\_center/nitro/v1/reports/classes

**Description**: Use this operation to get a report for classes. The response payload also contains the meta\_data block.

**HTTP Method**: GET

**Response Payload**: JSON

```json
{"classes":[{
      "packets_dropped":<Integer_value>,
      "data_dropped":<Double_value>,
      "data_pending":<Double_value>,
      "wait_time":<Integer_value>,
      "class_name":<String_value>,
      "percent_drop":<Double_value>,
      "region_name":<String_value>,
      "virtual_service":<String_value>,
      "packets_pending":<Integer_value>,
      "sent_bandwidth":<Double_value>,
      "incoming_traffic":<Double_value>,
      "data_coverage":<Double_value>,
      "class_type":<String_value>,
      "site_name":<String_value>,
      "packets_sent":<Integer_value>}]}
```
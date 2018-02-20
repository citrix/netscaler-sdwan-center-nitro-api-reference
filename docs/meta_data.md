# meta\_data

Displays the Meta Data. It is part of the JSON response payload for all APIs for reports

## Read/write properties

**total\_pages&lt;Integer>**

The total number of pages.

**page\_size&lt;Integer>**

The page size.

**end\_time&lt;String>**

The end time.

**current\_page&lt;Integer>**

The current page number.

**total\_records&lt;Integer>**

The total number of records.

**start\_time&lt;String>**

The start time.

## Read only properties

## Operations

### get (all)

**URL**: http://&lt;MGMT-IP>/sdwan\_center/nitro/v1/custom\_objects/meta\_data

**Description**: Use this operation to get meta data

**HTTP Method**: GET

**Response Payload**: JSON

```json
{"meta_data":[{
      "total_pages":<Integer_value>,
      "page_size":<Integer_value>,
      "end_time":<String_value>,
      "current_page":<Integer_value>,
      "total_records":<Integer_value>,
      "start_time":<String_value>}]}
```
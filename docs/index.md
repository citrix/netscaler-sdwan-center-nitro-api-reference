# Citrix NetScaler SD-WAN Center 10.0 NITRO REST API Getting Started Guide

## NITRO API

The NetScaler SD-WAN Center NITRO API allows you to configure and monitor the SD-WAN Center VM
programmatically. NITRO provides its functionality through Representational State Transfer (REST)
interfaces. Therefore, NITRO applications can be developed in any programming language.

**Note:** You must have a basic understanding of the NetScaler SD-WAN Center before using the NITRO API.

To use the NITRO API, the client application needs only the following:

- Access to a NetScaler SD-WAN Center system, version 10. 0 or later.
- Have a system to generate HTTPS requests (payload in JSON format) to the NetScaler SD-WAN Center system. You can use any programming language or tool.

The detailed description of all NITRO resources is provided in the tar.gz file that is available for download using NetScaler SD-WAN Center Graphical User Interface. To download, navigate to the NITRO API tab and click **Download Nitro API Doc** button.

## How NITRO Works

The NITRO infrastructure consists of a client application and the NITRO Web service running on a NetScaler SD-WAN Center system. The communication between the client application and the NITRO web service is based on REST architecture using HTTPS.

As shown in the above figure, a NITRO request is executed as follows:

1. The client application sends REST request message to the NITRO web service.
2. The web service processes the REST request message.
3. The NITRO web service returns the corresponding REST response message to the client application.

NITRO APIs are synchronous in nature. This means that the client application waits for a response from the NITRO web service before executing another NITRO API.

## General API Usage

REST (Representational State Transfer) is an architectural style based on simple HTTPS requests and responses between the client and the server. REST is used to query or change the state of objects on the server side. In REST, the server side is modelled as a set of entities where each entity is identified by a unique URL.

Each resource also has a state on which the following operations can be performed:

- **Create.** Clients can create new server-side resources on a "container" resource. You can think of container resources as folders, and child resources as files or subfolders. The calling client provides the state for the resource to be created. The state can be specified in the request by using JSON format. The HTTPS method used for create requests is POST.
- **Read.** Clients can retrieve the state of a resource by specifying its URL with the HTTPS GET method. The response message contains the resource state, expressed in JSON format.
- **Update.** You can update the state of an existing resource by specifying the URL that identifies that object and its new state in JSON, using the PUT HTTPS method.
- **Delete.** You can destroy a resource that exists on the server-side by using the DELETE HTTPS method and the URL identifying the resource to be removed.

In addition to the above four operations, resources can support other operations or actions. These operations use the HTTPS POST method, with the request body (if applicable) in JSON specifying the details of the operation.

## Authenticating NITRO APIs

NetScaler SD-WAN Center NITRO APIs work on session based session cookie based authentication. Use login NITRO API with HTTPS POST operation to create session cookie. This session cookie should be used in follow on NITRO requests. After execution of all required NITROs, logout of the system using HTTPS DELETE operation on login NITRO resource.

## Reporting NITRO APIs

Statistics tables stored in the NetScaler SD-WAN Center can be retrieved using REST APIs where each report corresponds to a resource. Following section explains the general usage aspects of the NetScaler SD WAN Center reports REST API.

### Request

Use the HTTP GET Method with the following URL:

`https://<sd wan center device ip>/sdwan_center/nitro/v1/reports/<resource>?filter=<filter type>:<value>;<filter type>:<value>&page=number:<page no>;size:<page size>&attrs=<attr 1>,<attr 2>`	

### Query
Following optional query parameters are supported.

###filter 

To retrieve data based on specific interval use the 'start_at' and 'end_at' filter types.

```
start_at:< Date time in ISO 8601 format (eg:2012-04-23T18:25:43.511Z) > 
end_at:< Date time in ISO 8601 format >
```

To retrieve reports since last hour, day, week or month use the 'last_by' filter type. 

```
last_by:< Possible values = hour, day, week, month >
```
To retrieve reports by site name, use the ‘site_name’ filter type.

To retrieve reports filtered on the basis of routing domain, use the ‘routing_domain’ filter. This filter is only applicable for the Sites API.

To retrieve reports by region name, use the ‘region_name’ filter type.

### page

The result reports data is divided into pages and are retrieved page by page (paginated). For example, if you are retrieving all the 53 sites data, instead of retrieving all 53 in one response, you can configure the results to be divided into 6 pages each having 10 results using the page query as `&page=number:1;size:10`

### attrs
To retrieve only specific attributes of a particular resource, use the attrs query. The complete set of attributes that correspond to each resource shall be specified in the respective API reference. eg to retrieve only the name, LAN to WAN Bandwidth and WAN to LAN Bandwidth use: 

```
attrs=name,lan_2_wan_bandwidth,wan_2_lan_bandwidth
```	
### Response

The response shall be JSON with the resource collection and a "_meta" block containing meta data, viz.: 'start_time', 'end_time', 'current_page', 'page_size', 'total_pages', 'total_records'

eg:

```
{
"<resource>": [
	{
		"attr1": "val1", 
		"attr2": "val2", 
		.....
	}, 
	..... 
	{
		"attr1": "val1", 
		"attr2": "val2", 
		.....
	},
  ],
"_meta": {
	"start_time": "Sat, 05 Aug 2017 18:30:00 +0000", 
	"end_time": "Mon, 04 Sep 2017 18:31:00 +0000", 
	"current_page": "1",
	"page_size": "10",
	"total_pages": 2,
	"total_records": 18
	} 
}

```

## API Request Content type

NetScaler SD-WAN Center NITRO APIs which accept input payload as part of the request need the input to be in JSON format with HTTPS request Content-Type application/json.

### Example Usage of NITRO APIs

Following examples are demonstrated using curl as the NITRO API client.

**1. Login**

```
curl -X POST -c /tmp/admincookies.txt -H "Content-Type: application/json" -- insecure https:// <sd_wan_center_device_ip>/sdwan_center/nitro/v1/config/login --data
'{"login":{"username":"admin","password":"password"}}''
```
**2. Reporting - Sites (without any query parameters)**

```    
curl	-X	GET	-b	/tmp/admincookies.txt	--insecure "https://<sd_wan_center_device_ip>/sdwan_center/nitro/v1/reports/sites"
```
**3. Reporting - Sites (with filter, page and attrs query parameters)** 

```
 curl -X GET -b /tmp/admincookies.txt --insecure "https://<sd_wan_center_device_ip>/sdwan_center/nitro/v1/reports/sites?filter=last_by:week &page=size:10;number:1&attrs=lan_2_wan_bandwidth,wan_2_lan_bandwidth"
```

**4. Reporting – Services (with filter, page and attrs query parameters)**
   
    curl	-X	GET	-b	/tmp/admincookies.txt	--insecure	
    "https://<sd_wan_center_device_ip>/sdwan_center/nitro/v1/reports/services?page=size:10;nu
    mber:1&attrs=wan_2_lan_percent_drop&filter=start_at:2017- 01 - 03T10:00Z;end_at:2017- 09 -
    05T15:00Z"
**5. Reporting	– Paths (without	any	query parameters)**
    
    curl	-X	GET	-b	/tmp/admincookies.txt	--insecure	
    "https://<sd_wan_center_device_ip>/sdwan_center/nitro/v1/reports/paths”
**6. Reporting	– Virtual	Paths (without any query parameters)**
   
    curl	-X	GET	-b	/tmp/admincookies.txt	--insecure	
    "https://<sd_wan_center_device_ip>/sdwan_center/nitro/v1/reports/virtual_paths”



# OpenAPI\Client\SalesPersonV2Api



All URIs are relative to https://api.finance.visma.net, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**salesPersonV2GetSalespersonBysalespersonCd()**](SalesPersonV2Api.md#salesPersonV2GetSalespersonBysalespersonCd) | **GET** /v2/salesperson/{salespersonCd} | Get a specific Salesperson - screen ID: AR205000 |
| [**salesPersonV2GetSalespersons()**](SalesPersonV2Api.md#salesPersonV2GetSalespersons) | **GET** /v2/salesperson | Get all or a range of Salespersons - screen ID: AR205000  Please use a page size lower or equal to the allowed max page size which is returned under metadata.   If pagesize is greater than the max page size, it will be limited to max page size. |


## `salesPersonV2GetSalespersonBysalespersonCd()`

```php
salesPersonV2GetSalespersonBysalespersonCd($salesperson_cd, $erp_api_background): \OpenAPI\Client\Model\SalesPersonDto
```

Get a specific Salesperson - screen ID: AR205000

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SalesPersonV2Api(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$salesperson_cd = 'salesperson_cd_example'; // string | Identifies the Salesperson
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->salesPersonV2GetSalespersonBysalespersonCd($salesperson_cd, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SalesPersonV2Api->salesPersonV2GetSalespersonBysalespersonCd: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **salesperson_cd** | **string**| Identifies the Salesperson | |
| **erp_api_background** | **string**| Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \&quot;none\&quot; (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \&quot;subscription[:&lt;name_1&gt;&#x3D;&lt;value_1&gt;,..,&lt;name_n&gt;&#x3D;&lt;value_n&gt;]\&quot; (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription&#39;s url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content | [optional] |

### Return type

[**\OpenAPI\Client\Model\SalesPersonDto**](../Model/SalesPersonDto.md)

### Authorization

[serviceapi](../../README.md#serviceapi)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `salesPersonV2GetSalespersons()`

```php
salesPersonV2GetSalespersons($salesperson_cd, $name, $is_active, $commission_pct, $sales_sub, $greater_than_value, $number_to_read, $skip_records, $last_modified_date_time, $last_modified_date_time_condition, $created_date_time, $created_date_time_condition, $page_number, $page_size, $erp_api_background): \OpenAPI\Client\Model\SalesPersonDto[]
```

Get all or a range of Salespersons - screen ID: AR205000  Please use a page size lower or equal to the allowed max page size which is returned under metadata.   If pagesize is greater than the max page size, it will be limited to max page size.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SalesPersonV2Api(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$salesperson_cd = 'salesperson_cd_example'; // string
$name = 'name_example'; // string
$is_active = True; // bool
$commission_pct = 3.4; // float
$sales_sub = 'sales_sub_example'; // string
$greater_than_value = 'greater_than_value_example'; // string | Greater than value. The item which is the object for this, varies from API to API.
$number_to_read = 56; // int | This field has been deprecated and will be removed in future versions. Use pagenumber and pagesize for pagination purposes. Pagenumber and pagesize does not work with NumberToRead and SkipRecords.
$skip_records = 56; // int | This field has been deprecated and will be removed in future versions. Use pagenumber and pagesize for pagination purposes. Pagenumber and pagesize does not work with NumberToRead and SkipRecords.
$last_modified_date_time = 'last_modified_date_time_example'; // string | This value, generated by the system, indicates the last time the record was modified. Use it to retrieve all records that have been modified since that time, up to the present.    Accepted format:  * ```yyyy-MM-dd```  * ```yyyy-MM-dd HH:mm:ss```  * ```yyyy-MM-dd HH:mm:ss.FFF```  * ```yyyy-MM-ddTHH:mm:ss```  * ```yyyy-MM-ddTHH:mm:ss.FFF```    _Note:_ __LastModifiedDateTime__ and __LastModifiedDateTimeCondition__ are __mutually inclusive__.
$last_modified_date_time_condition = 'last_modified_date_time_condition_example'; // string | This value represents the condition to be applied when retrieving records.    Accepted values (without the single quotes):  * '&gt;' for greater than  * '&lt;' for less than  * '&gt;=' for greater than or equal  * '&lt;=' for less than or equal    _Note:_ __LastModifiedDateTime__ and __LastModifiedDateTimeCondition__ are __mutually inclusive__.
$created_date_time = 'created_date_time_example'; // string | Creation date and time.
$created_date_time_condition = 'created_date_time_condition_example'; // string | System-retrieved information for state/condition
$page_number = 56; // int | Pagination parameter. Page number.
$page_size = 56; // int | Pagination parameter. Number of items to be collected.  Please use a page size lower or equal to the allowed max page size which is returned as part of the metadata information.  If requested page size is greater than allowed max page size, request will be limited to max page size.
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->salesPersonV2GetSalespersons($salesperson_cd, $name, $is_active, $commission_pct, $sales_sub, $greater_than_value, $number_to_read, $skip_records, $last_modified_date_time, $last_modified_date_time_condition, $created_date_time, $created_date_time_condition, $page_number, $page_size, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SalesPersonV2Api->salesPersonV2GetSalespersons: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **salesperson_cd** | **string**|  | [optional] |
| **name** | **string**|  | [optional] |
| **is_active** | **bool**|  | [optional] |
| **commission_pct** | **float**|  | [optional] |
| **sales_sub** | **string**|  | [optional] |
| **greater_than_value** | **string**| Greater than value. The item which is the object for this, varies from API to API. | [optional] |
| **number_to_read** | **int**| This field has been deprecated and will be removed in future versions. Use pagenumber and pagesize for pagination purposes. Pagenumber and pagesize does not work with NumberToRead and SkipRecords. | [optional] |
| **skip_records** | **int**| This field has been deprecated and will be removed in future versions. Use pagenumber and pagesize for pagination purposes. Pagenumber and pagesize does not work with NumberToRead and SkipRecords. | [optional] |
| **last_modified_date_time** | **string**| This value, generated by the system, indicates the last time the record was modified. Use it to retrieve all records that have been modified since that time, up to the present.    Accepted format:  * &#x60;&#x60;&#x60;yyyy-MM-dd&#x60;&#x60;&#x60;  * &#x60;&#x60;&#x60;yyyy-MM-dd HH:mm:ss&#x60;&#x60;&#x60;  * &#x60;&#x60;&#x60;yyyy-MM-dd HH:mm:ss.FFF&#x60;&#x60;&#x60;  * &#x60;&#x60;&#x60;yyyy-MM-ddTHH:mm:ss&#x60;&#x60;&#x60;  * &#x60;&#x60;&#x60;yyyy-MM-ddTHH:mm:ss.FFF&#x60;&#x60;&#x60;    _Note:_ __LastModifiedDateTime__ and __LastModifiedDateTimeCondition__ are __mutually inclusive__. | [optional] |
| **last_modified_date_time_condition** | **string**| This value represents the condition to be applied when retrieving records.    Accepted values (without the single quotes):  * &#39;&amp;gt;&#39; for greater than  * &#39;&amp;lt;&#39; for less than  * &#39;&amp;gt;&#x3D;&#39; for greater than or equal  * &#39;&amp;lt;&#x3D;&#39; for less than or equal    _Note:_ __LastModifiedDateTime__ and __LastModifiedDateTimeCondition__ are __mutually inclusive__. | [optional] |
| **created_date_time** | **string**| Creation date and time. | [optional] |
| **created_date_time_condition** | **string**| System-retrieved information for state/condition | [optional] |
| **page_number** | **int**| Pagination parameter. Page number. | [optional] |
| **page_size** | **int**| Pagination parameter. Number of items to be collected.  Please use a page size lower or equal to the allowed max page size which is returned as part of the metadata information.  If requested page size is greater than allowed max page size, request will be limited to max page size. | [optional] |
| **erp_api_background** | **string**| Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \&quot;none\&quot; (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \&quot;subscription[:&lt;name_1&gt;&#x3D;&lt;value_1&gt;,..,&lt;name_n&gt;&#x3D;&lt;value_n&gt;]\&quot; (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription&#39;s url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content | [optional] |

### Return type

[**\OpenAPI\Client\Model\SalesPersonDto[]**](../Model/SalesPersonDto.md)

### Authorization

[serviceapi](../../README.md#serviceapi)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

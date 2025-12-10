# OpenAPI\Client\CustomerSalesPriceApi



All URIs are relative to https://api.finance.visma.net, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**customerSalesPriceGetCustomerSalesPriceByrecordId()**](CustomerSalesPriceApi.md#customerSalesPriceGetCustomerSalesPriceByrecordId) | **GET** /v1/customerSalesPrice/{recordId} | Get a specific Customer Sales Price by recordId |
| [**customerSalesPriceGetCustomerSalesPrices()**](CustomerSalesPriceApi.md#customerSalesPriceGetCustomerSalesPrices) | **GET** /v1/customerSalesPrice | Get a range of Customer Sales Prices - ScreenId&#x3D;AR202000  Request page size must be lower or equal to the allowed max page size which is returned as part of the metadata information.  If requested page size is greater than allowed max page size, request will be limited to max page size |
| [**customerSalesPricePostCustomerSalesPrice()**](CustomerSalesPriceApi.md#customerSalesPricePostCustomerSalesPrice) | **POST** /v1/customerSalesPrice | Create a new Customer Sales Price |
| [**customerSalesPricePutCustomerSalesPriceByrecordId()**](CustomerSalesPriceApi.md#customerSalesPricePutCustomerSalesPriceByrecordId) | **PUT** /v1/customerSalesPrice/{recordId} | Update an existing Customer Sales Price |


## `customerSalesPriceGetCustomerSalesPriceByrecordId()`

```php
customerSalesPriceGetCustomerSalesPriceByrecordId($record_id, $erp_api_background): \OpenAPI\Client\Model\CustomerSalesPriceDto
```

Get a specific Customer Sales Price by recordId

The response headers include an ETag after a successful GET operation.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CustomerSalesPriceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$record_id = 56; // int | The recordId of the Customer Sales Price
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->customerSalesPriceGetCustomerSalesPriceByrecordId($record_id, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomerSalesPriceApi->customerSalesPriceGetCustomerSalesPriceByrecordId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **record_id** | **int**| The recordId of the Customer Sales Price | |
| **erp_api_background** | **string**| Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \&quot;none\&quot; (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \&quot;subscription[:&lt;name_1&gt;&#x3D;&lt;value_1&gt;,..,&lt;name_n&gt;&#x3D;&lt;value_n&gt;]\&quot; (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription&#39;s url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content | [optional] |

### Return type

[**\OpenAPI\Client\Model\CustomerSalesPriceDto**](../Model/CustomerSalesPriceDto.md)

### Authorization

[serviceapi](../../README.md#serviceapi)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `customerSalesPriceGetCustomerSalesPrices()`

```php
customerSalesPriceGetCustomerSalesPrices($greater_than_value, $number_to_read, $skip_records, $price_type, $price_code, $inventory_id, $effective_as_of, $last_modified_date_time, $last_modified_date_time_condition, $page_number, $page_size, $erp_api_background): \OpenAPI\Client\Model\CustomerSalesPriceDto[]
```

Get a range of Customer Sales Prices - ScreenId=AR202000  Request page size must be lower or equal to the allowed max page size which is returned as part of the metadata information.  If requested page size is greater than allowed max page size, request will be limited to max page size

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CustomerSalesPriceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$greater_than_value = 'greater_than_value_example'; // string
$number_to_read = 56; // int | This field has been deprecated and will be removed in future versions. Use pagenumber and pagesize for pagination purposes. Pagenumber and pagesize does not work with NumberToRead and SkipRecords.
$skip_records = 56; // int | This field has been deprecated and will be removed in future versions. Use pagenumber and pagesize for pagination purposes. Pagenumber and pagesize does not work with NumberToRead and SkipRecords.
$price_type = 'price_type_example'; // string
$price_code = 'price_code_example'; // string
$inventory_id = 'inventory_id_example'; // string
$effective_as_of = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime
$last_modified_date_time = 'last_modified_date_time_example'; // string
$last_modified_date_time_condition = 'last_modified_date_time_condition_example'; // string
$page_number = 56; // int | Pagination parameter. Page number.
$page_size = 56; // int | Pagination parameter. Number of items to be collected.  Please use a page size lower or equal to the allowed max page size which is returned as part of the metadata information.  If requested page size is greater than allowed max page size, request will be limited to max page size.
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->customerSalesPriceGetCustomerSalesPrices($greater_than_value, $number_to_read, $skip_records, $price_type, $price_code, $inventory_id, $effective_as_of, $last_modified_date_time, $last_modified_date_time_condition, $page_number, $page_size, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomerSalesPriceApi->customerSalesPriceGetCustomerSalesPrices: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **greater_than_value** | **string**|  | [optional] |
| **number_to_read** | **int**| This field has been deprecated and will be removed in future versions. Use pagenumber and pagesize for pagination purposes. Pagenumber and pagesize does not work with NumberToRead and SkipRecords. | [optional] |
| **skip_records** | **int**| This field has been deprecated and will be removed in future versions. Use pagenumber and pagesize for pagination purposes. Pagenumber and pagesize does not work with NumberToRead and SkipRecords. | [optional] |
| **price_type** | **string**|  | [optional] |
| **price_code** | **string**|  | [optional] |
| **inventory_id** | **string**|  | [optional] |
| **effective_as_of** | **\DateTime**|  | [optional] |
| **last_modified_date_time** | **string**|  | [optional] |
| **last_modified_date_time_condition** | **string**|  | [optional] |
| **page_number** | **int**| Pagination parameter. Page number. | [optional] |
| **page_size** | **int**| Pagination parameter. Number of items to be collected.  Please use a page size lower or equal to the allowed max page size which is returned as part of the metadata information.  If requested page size is greater than allowed max page size, request will be limited to max page size. | [optional] |
| **erp_api_background** | **string**| Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \&quot;none\&quot; (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \&quot;subscription[:&lt;name_1&gt;&#x3D;&lt;value_1&gt;,..,&lt;name_n&gt;&#x3D;&lt;value_n&gt;]\&quot; (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription&#39;s url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content | [optional] |

### Return type

[**\OpenAPI\Client\Model\CustomerSalesPriceDto[]**](../Model/CustomerSalesPriceDto.md)

### Authorization

[serviceapi](../../README.md#serviceapi)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `customerSalesPricePostCustomerSalesPrice()`

```php
customerSalesPricePostCustomerSalesPrice($customer_sales_price_update_dto, $erp_api_background): object
```

Create a new Customer Sales Price

Response Message has StatusCode Created if POST operation succeed <br></br>  Response Message has StatusCode BadRequest or InternalServerError if POST operation failed <br></br>  The response headers include an ETag after a successful POST operation.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CustomerSalesPriceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$customer_sales_price_update_dto = new \OpenAPI\Client\Model\CustomerSalesPriceUpdateDto(); // \OpenAPI\Client\Model\CustomerSalesPriceUpdateDto | The CustomerSalesPriceUpdateDto to create
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->customerSalesPricePostCustomerSalesPrice($customer_sales_price_update_dto, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomerSalesPriceApi->customerSalesPricePostCustomerSalesPrice: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **customer_sales_price_update_dto** | [**\OpenAPI\Client\Model\CustomerSalesPriceUpdateDto**](../Model/CustomerSalesPriceUpdateDto.md)| The CustomerSalesPriceUpdateDto to create | |
| **erp_api_background** | **string**| Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \&quot;none\&quot; (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \&quot;subscription[:&lt;name_1&gt;&#x3D;&lt;value_1&gt;,..,&lt;name_n&gt;&#x3D;&lt;value_n&gt;]\&quot; (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription&#39;s url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content | [optional] |

### Return type

**object**

### Authorization

[serviceapi](../../README.md#serviceapi)

### HTTP request headers

- **Content-Type**: `application/json`, `text/json`, `application/xml`, `text/xml`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `customerSalesPricePutCustomerSalesPriceByrecordId()`

```php
customerSalesPricePutCustomerSalesPriceByrecordId($record_id, $customer_sales_price_update_dto, $erp_api_background, $if_match): \OpenAPI\Client\Model\BackgroundApiAcceptedDto
```

Update an existing Customer Sales Price

Response Message has StatusCode NoContent if PUT operation succeed <br></br>  Response Message has StatusCode BadRequest if PUT operation failed <br></br>  In this endpoint, If-Match can be checked against resource current version when calling with 'erp-api-background' HTTP header.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CustomerSalesPriceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$record_id = 56; // int | 
$customer_sales_price_update_dto = new \OpenAPI\Client\Model\CustomerSalesPriceUpdateDto(); // \OpenAPI\Client\Model\CustomerSalesPriceUpdateDto | The CustomerSalesPriceUpdateDto to update
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content
$if_match = 'if_match_example'; // string | The If-Match HTTP header allows clients to update a resource only if its current version matches a specific ETag. This mechanism helps prevent conflicts when multiple clients attempt to modify the same resource simultaneously. The If-Match header should be included in the request headers using the following syntax: If-Match: \"etag_value\" * If the update is successful, the server responds with 204 No Content and includes the new ETag value in the response headers. * If the ETag on the server does not match the value provided in the If-Match header, the server responds with 412 Precondition Failed.

try {
    $result = $apiInstance->customerSalesPricePutCustomerSalesPriceByrecordId($record_id, $customer_sales_price_update_dto, $erp_api_background, $if_match);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomerSalesPriceApi->customerSalesPricePutCustomerSalesPriceByrecordId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **record_id** | **int**|  | |
| **customer_sales_price_update_dto** | [**\OpenAPI\Client\Model\CustomerSalesPriceUpdateDto**](../Model/CustomerSalesPriceUpdateDto.md)| The CustomerSalesPriceUpdateDto to update | |
| **erp_api_background** | **string**| Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \&quot;none\&quot; (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \&quot;subscription[:&lt;name_1&gt;&#x3D;&lt;value_1&gt;,..,&lt;name_n&gt;&#x3D;&lt;value_n&gt;]\&quot; (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription&#39;s url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content | [optional] |
| **if_match** | **string**| The If-Match HTTP header allows clients to update a resource only if its current version matches a specific ETag. This mechanism helps prevent conflicts when multiple clients attempt to modify the same resource simultaneously. The If-Match header should be included in the request headers using the following syntax: If-Match: \&quot;etag_value\&quot; * If the update is successful, the server responds with 204 No Content and includes the new ETag value in the response headers. * If the ETag on the server does not match the value provided in the If-Match header, the server responds with 412 Precondition Failed. | [optional] |

### Return type

[**\OpenAPI\Client\Model\BackgroundApiAcceptedDto**](../Model/BackgroundApiAcceptedDto.md)

### Authorization

[serviceapi](../../README.md#serviceapi)

### HTTP request headers

- **Content-Type**: `application/json`, `text/json`, `application/xml`, `text/xml`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

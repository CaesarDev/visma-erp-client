# OpenAPI\Client\StocktakeV2Api



All URIs are relative to https://api.finance.visma.net, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**stocktakeV2GetAllStocktakes()**](StocktakeV2Api.md#stocktakeV2GetAllStocktakes) | **GET** /v2/stocktake | Get a range of stocktakes - ScreenId&#x3D;IN305000  Request page size must be lower or equal to the allowed max page size which is returned as part of the metadata information. If requested page size is greater than allowed max page size, request will be limited to max page size. |
| [**stocktakeV2GetByreferenceNumber()**](StocktakeV2Api.md#stocktakeV2GetByreferenceNumber) | **GET** /v2/stocktake/{referenceNumber} | Get a specific |
| [**stocktakeV2PutByreferenceNumber()**](StocktakeV2Api.md#stocktakeV2PutByreferenceNumber) | **PUT** /v2/stocktake/{referenceNumber} | Update a specific stocktake |


## `stocktakeV2GetAllStocktakes()`

```php
stocktakeV2GetAllStocktakes($warehouse, $location, $inventory, $lot_serial_number, $summary_status, $start_with_line, $end_with_line, $freeze_date_time, $freeze_date_time_condition, $last_modified_date_time, $last_modified_date_time_condition, $expiration_date_time, $expiration_date_time_condition, $status, $page_number, $page_size, $erp_api_background): \OpenAPI\Client\Model\StocktakeV2Dto[]
```

Get a range of stocktakes - ScreenId=IN305000  Request page size must be lower or equal to the allowed max page size which is returned as part of the metadata information. If requested page size is greater than allowed max page size, request will be limited to max page size.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\StocktakeV2Api(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$warehouse = 'warehouse_example'; // string | Filter by Warehouse.
$location = 'location_example'; // string | Filter by Location.
$inventory = 'inventory_example'; // string | Filter by Inventory.
$lot_serial_number = 'lot_serial_number_example'; // string | Filter by LotSerialNumber.
$summary_status = 'summary_status_example'; // string | Filter by SummaryStatus.
$start_with_line = 56; // int | Filter by LineNumber GreaterEqual StartWithLine.
$end_with_line = 56; // int | Filter by by LineNumber LessEqual EndWithLine.
$freeze_date_time = 'freeze_date_time_example'; // string | Filter by FreezeDateTime.
$freeze_date_time_condition = 'freeze_date_time_condition_example'; // string | Filter by FreezeDateTimeCondition.
$last_modified_date_time = 'last_modified_date_time_example'; // string | System generated value for last modification of transaction/record. Use format: YYYY-MM-DD HH:MM (date and time) to filter from date to present..
$last_modified_date_time_condition = 'last_modified_date_time_condition_example'; // string | System retrieved information for state/condition.
$expiration_date_time = 'expiration_date_time_example'; // string | Filter by ExpirationDateTime.
$expiration_date_time_condition = 'expiration_date_time_condition_example'; // string | Filter by ExpirationDateTimeCondition.
$status = 'status_example'; // string | Filter by StocktakeLineStatus.
$page_number = 56; // int | Pagination parameter. Page number.
$page_size = 56; // int | Pagination parameter. Number of items to be collected.  Please use a page size lower or equal to the allowed max page size which is returned as part of the metadata information.  If requested page size is greater than allowed max page size, request will be limited to max page size.
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->stocktakeV2GetAllStocktakes($warehouse, $location, $inventory, $lot_serial_number, $summary_status, $start_with_line, $end_with_line, $freeze_date_time, $freeze_date_time_condition, $last_modified_date_time, $last_modified_date_time_condition, $expiration_date_time, $expiration_date_time_condition, $status, $page_number, $page_size, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StocktakeV2Api->stocktakeV2GetAllStocktakes: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **warehouse** | **string**| Filter by Warehouse. | [optional] |
| **location** | **string**| Filter by Location. | [optional] |
| **inventory** | **string**| Filter by Inventory. | [optional] |
| **lot_serial_number** | **string**| Filter by LotSerialNumber. | [optional] |
| **summary_status** | **string**| Filter by SummaryStatus. | [optional] |
| **start_with_line** | **int**| Filter by LineNumber GreaterEqual StartWithLine. | [optional] |
| **end_with_line** | **int**| Filter by by LineNumber LessEqual EndWithLine. | [optional] |
| **freeze_date_time** | **string**| Filter by FreezeDateTime. | [optional] |
| **freeze_date_time_condition** | **string**| Filter by FreezeDateTimeCondition. | [optional] |
| **last_modified_date_time** | **string**| System generated value for last modification of transaction/record. Use format: YYYY-MM-DD HH:MM (date and time) to filter from date to present.. | [optional] |
| **last_modified_date_time_condition** | **string**| System retrieved information for state/condition. | [optional] |
| **expiration_date_time** | **string**| Filter by ExpirationDateTime. | [optional] |
| **expiration_date_time_condition** | **string**| Filter by ExpirationDateTimeCondition. | [optional] |
| **status** | **string**| Filter by StocktakeLineStatus. | [optional] |
| **page_number** | **int**| Pagination parameter. Page number. | [optional] |
| **page_size** | **int**| Pagination parameter. Number of items to be collected.  Please use a page size lower or equal to the allowed max page size which is returned as part of the metadata information.  If requested page size is greater than allowed max page size, request will be limited to max page size. | [optional] |
| **erp_api_background** | **string**| Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \&quot;none\&quot; (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \&quot;subscription[:&lt;name_1&gt;&#x3D;&lt;value_1&gt;,..,&lt;name_n&gt;&#x3D;&lt;value_n&gt;]\&quot; (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription&#39;s url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content | [optional] |

### Return type

[**\OpenAPI\Client\Model\StocktakeV2Dto[]**](../Model/StocktakeV2Dto.md)

### Authorization

[serviceapi](../../README.md#serviceapi)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `stocktakeV2GetByreferenceNumber()`

```php
stocktakeV2GetByreferenceNumber($reference_number, $erp_api_background): \OpenAPI\Client\Model\StocktakeV2Dto
```

Get a specific

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\StocktakeV2Api(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$reference_number = 'reference_number_example'; // string | Identifies the Stocktake
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->stocktakeV2GetByreferenceNumber($reference_number, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StocktakeV2Api->stocktakeV2GetByreferenceNumber: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **reference_number** | **string**| Identifies the Stocktake | |
| **erp_api_background** | **string**| Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \&quot;none\&quot; (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \&quot;subscription[:&lt;name_1&gt;&#x3D;&lt;value_1&gt;,..,&lt;name_n&gt;&#x3D;&lt;value_n&gt;]\&quot; (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription&#39;s url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content | [optional] |

### Return type

[**\OpenAPI\Client\Model\StocktakeV2Dto**](../Model/StocktakeV2Dto.md)

### Authorization

[serviceapi](../../README.md#serviceapi)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `stocktakeV2PutByreferenceNumber()`

```php
stocktakeV2PutByreferenceNumber($reference_number, $stocktake_update_dto, $erp_api_background): \OpenAPI\Client\Model\BackgroundApiAcceptedDto
```

Update a specific stocktake

Response Message has StatusCode NoContent if PUT operation succeed    Response Message has StatusCode BadRequest if PUT operation failed     If PUT operation failed, Response body contains all stocktake line details (the ones that have values), the error message and also an error code (The first member of StocktakeExceptionErrorCode will be 0, and the value of each successive enum member is increased by 1)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\StocktakeV2Api(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$reference_number = 'reference_number_example'; // string | Identifies the stocktake to update
$stocktake_update_dto = new \OpenAPI\Client\Model\StocktakeUpdateDto(); // \OpenAPI\Client\Model\StocktakeUpdateDto | The data to update for stocktake
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->stocktakeV2PutByreferenceNumber($reference_number, $stocktake_update_dto, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StocktakeV2Api->stocktakeV2PutByreferenceNumber: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **reference_number** | **string**| Identifies the stocktake to update | |
| **stocktake_update_dto** | [**\OpenAPI\Client\Model\StocktakeUpdateDto**](../Model/StocktakeUpdateDto.md)| The data to update for stocktake | |
| **erp_api_background** | **string**| Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \&quot;none\&quot; (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \&quot;subscription[:&lt;name_1&gt;&#x3D;&lt;value_1&gt;,..,&lt;name_n&gt;&#x3D;&lt;value_n&gt;]\&quot; (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription&#39;s url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content | [optional] |

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

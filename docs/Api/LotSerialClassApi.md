# OpenAPI\Client\LotSerialClassApi



All URIs are relative to https://api.finance.visma.net, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**lotSerialClassGetAllLotSerialClass()**](LotSerialClassApi.md#lotSerialClassGetAllLotSerialClass) | **GET** /v1/lotserialclass | Get a range of lot serial classes - ScreenId&#x3D;IN207000  Request page size must be lower or equal to the allowed max page size which is returned as part of the metadata information. If requested page size is greater than allowed max page size, request will be limited to max page size. |
| [**lotSerialClassGetByid()**](LotSerialClassApi.md#lotSerialClassGetByid) | **GET** /v1/lotserialclass/{id} | Get a specific |


## `lotSerialClassGetAllLotSerialClass()`

```php
lotSerialClassGetAllLotSerialClass($description, $tracking_method, $track_expiration_date, $required_for_drop_ship, $assignment_method, $issue_method, $auto_incremental_value_between_classes, $auto_incremental_value, $auto_generate_next_number, $last_modified_date_time, $last_modified_date_time_condition, $page_number, $page_size, $erp_api_background): \OpenAPI\Client\Model\LotSerialClassDto[]
```

Get a range of lot serial classes - ScreenId=IN207000  Request page size must be lower or equal to the allowed max page size which is returned as part of the metadata information. If requested page size is greater than allowed max page size, request will be limited to max page size.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\LotSerialClassApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$description = 'description_example'; // string
$tracking_method = 'tracking_method_example'; // string
$track_expiration_date = True; // bool
$required_for_drop_ship = True; // bool
$assignment_method = 'assignment_method_example'; // string
$issue_method = 'issue_method_example'; // string
$auto_incremental_value_between_classes = True; // bool
$auto_incremental_value = 'auto_incremental_value_example'; // string
$auto_generate_next_number = True; // bool
$last_modified_date_time = 'last_modified_date_time_example'; // string
$last_modified_date_time_condition = 'last_modified_date_time_condition_example'; // string
$page_number = 56; // int | Pagination parameter. Page number.
$page_size = 56; // int | Pagination parameter. Number of items to be collected.  Please use a page size lower or equal to the allowed max page size which is returned as part of the metadata information.  If requested page size is greater than allowed max page size, request will be limited to max page size.
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->lotSerialClassGetAllLotSerialClass($description, $tracking_method, $track_expiration_date, $required_for_drop_ship, $assignment_method, $issue_method, $auto_incremental_value_between_classes, $auto_incremental_value, $auto_generate_next_number, $last_modified_date_time, $last_modified_date_time_condition, $page_number, $page_size, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LotSerialClassApi->lotSerialClassGetAllLotSerialClass: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **description** | **string**|  | [optional] |
| **tracking_method** | **string**|  | [optional] |
| **track_expiration_date** | **bool**|  | [optional] |
| **required_for_drop_ship** | **bool**|  | [optional] |
| **assignment_method** | **string**|  | [optional] |
| **issue_method** | **string**|  | [optional] |
| **auto_incremental_value_between_classes** | **bool**|  | [optional] |
| **auto_incremental_value** | **string**|  | [optional] |
| **auto_generate_next_number** | **bool**|  | [optional] |
| **last_modified_date_time** | **string**|  | [optional] |
| **last_modified_date_time_condition** | **string**|  | [optional] |
| **page_number** | **int**| Pagination parameter. Page number. | [optional] |
| **page_size** | **int**| Pagination parameter. Number of items to be collected.  Please use a page size lower or equal to the allowed max page size which is returned as part of the metadata information.  If requested page size is greater than allowed max page size, request will be limited to max page size. | [optional] |
| **erp_api_background** | **string**| Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \&quot;none\&quot; (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \&quot;subscription[:&lt;name_1&gt;&#x3D;&lt;value_1&gt;,..,&lt;name_n&gt;&#x3D;&lt;value_n&gt;]\&quot; (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription&#39;s url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content | [optional] |

### Return type

[**\OpenAPI\Client\Model\LotSerialClassDto[]**](../Model/LotSerialClassDto.md)

### Authorization

[serviceapi](../../README.md#serviceapi)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `lotSerialClassGetByid()`

```php
lotSerialClassGetByid($id, $erp_api_background): \OpenAPI\Client\Model\LotSerialClassDto
```

Get a specific

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\LotSerialClassApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | Identifies the LotSerialClass
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->lotSerialClassGetByid($id, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LotSerialClassApi->lotSerialClassGetByid: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Identifies the LotSerialClass | |
| **erp_api_background** | **string**| Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \&quot;none\&quot; (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \&quot;subscription[:&lt;name_1&gt;&#x3D;&lt;value_1&gt;,..,&lt;name_n&gt;&#x3D;&lt;value_n&gt;]\&quot; (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription&#39;s url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content | [optional] |

### Return type

[**\OpenAPI\Client\Model\LotSerialClassDto**](../Model/LotSerialClassDto.md)

### Authorization

[serviceapi](../../README.md#serviceapi)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

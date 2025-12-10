# OpenAPI\Client\FixedAssetPropertyTaxGroupApi



All URIs are relative to https://api.finance.visma.net, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**fixedAssetPropertyTaxGroupGetAll()**](FixedAssetPropertyTaxGroupApi.md#fixedAssetPropertyTaxGroupGetAll) | **GET** /v1/fixedAssetPropertyTaxGroup | Get a range of Fixed Asset Property Tax Groups - Screen ID: FA209000 |
| [**fixedAssetPropertyTaxGroupGetByPropertyTaxID()**](FixedAssetPropertyTaxGroupApi.md#fixedAssetPropertyTaxGroupGetByPropertyTaxID) | **GET** /v1/fixedAssetPropertyTaxGroup/{PropertyTaxID} | Get a specific Fixed Asset Property Tax Group - Screen ID: FA209000 |


## `fixedAssetPropertyTaxGroupGetAll()`

```php
fixedAssetPropertyTaxGroupGetAll($property_tax_id, $active, $page_number, $page_size, $erp_api_background): \OpenAPI\Client\Model\FixedAssetPropertyTaxDto[]
```

Get a range of Fixed Asset Property Tax Groups - Screen ID: FA209000

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\FixedAssetPropertyTaxGroupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$property_tax_id = 'property_tax_id_example'; // string | Property Tax ID that identifies the property tax group.
$active = True; // bool | Set to True to select active fixed asset property tax groups.
$page_number = 56; // int | Pagination parameter. Page number.
$page_size = 56; // int | Pagination parameter. Number of items to be collected.  Please use a page size lower or equal to the allowed max page size which is returned as part of the metadata information.  If requested page size is greater than allowed max page size, request will be limited to max page size.
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->fixedAssetPropertyTaxGroupGetAll($property_tax_id, $active, $page_number, $page_size, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FixedAssetPropertyTaxGroupApi->fixedAssetPropertyTaxGroupGetAll: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **property_tax_id** | **string**| Property Tax ID that identifies the property tax group. | [optional] |
| **active** | **bool**| Set to True to select active fixed asset property tax groups. | [optional] |
| **page_number** | **int**| Pagination parameter. Page number. | [optional] |
| **page_size** | **int**| Pagination parameter. Number of items to be collected.  Please use a page size lower or equal to the allowed max page size which is returned as part of the metadata information.  If requested page size is greater than allowed max page size, request will be limited to max page size. | [optional] |
| **erp_api_background** | **string**| Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \&quot;none\&quot; (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \&quot;subscription[:&lt;name_1&gt;&#x3D;&lt;value_1&gt;,..,&lt;name_n&gt;&#x3D;&lt;value_n&gt;]\&quot; (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription&#39;s url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content | [optional] |

### Return type

[**\OpenAPI\Client\Model\FixedAssetPropertyTaxDto[]**](../Model/FixedAssetPropertyTaxDto.md)

### Authorization

[serviceapi](../../README.md#serviceapi)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `fixedAssetPropertyTaxGroupGetByPropertyTaxID()`

```php
fixedAssetPropertyTaxGroupGetByPropertyTaxID($property_tax_id, $erp_api_background): \OpenAPI\Client\Model\FixedAssetPropertyTaxDto
```

Get a specific Fixed Asset Property Tax Group - Screen ID: FA209000

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\FixedAssetPropertyTaxGroupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$property_tax_id = 'property_tax_id_example'; // string | 
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->fixedAssetPropertyTaxGroupGetByPropertyTaxID($property_tax_id, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FixedAssetPropertyTaxGroupApi->fixedAssetPropertyTaxGroupGetByPropertyTaxID: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **property_tax_id** | **string**|  | |
| **erp_api_background** | **string**| Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \&quot;none\&quot; (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \&quot;subscription[:&lt;name_1&gt;&#x3D;&lt;value_1&gt;,..,&lt;name_n&gt;&#x3D;&lt;value_n&gt;]\&quot; (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription&#39;s url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content | [optional] |

### Return type

[**\OpenAPI\Client\Model\FixedAssetPropertyTaxDto**](../Model/FixedAssetPropertyTaxDto.md)

### Authorization

[serviceapi](../../README.md#serviceapi)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

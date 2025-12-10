# OpenAPI\Client\BackgroundApi



All URIs are relative to https://api.finance.visma.net, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**backgroundGetBackgroundApiOperationByrequestId()**](BackgroundApi.md#backgroundGetBackgroundApiOperationByrequestId) | **GET** /v1/background/{requestId} | Gets the state of a previously started background API operation |
| [**backgroundGetBackgroundApiOperationContentByrequestId()**](BackgroundApi.md#backgroundGetBackgroundApiOperationContentByrequestId) | **GET** /v1/background/{requestId}/content | Gets the response content, if any, of a previously started background API operation that has finished |


## `backgroundGetBackgroundApiOperationByrequestId()`

```php
backgroundGetBackgroundApiOperationByrequestId($request_id): \OpenAPI\Client\Model\BackgroundRequestStateDto
```

Gets the state of a previously started background API operation

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BackgroundApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$request_id = 'request_id_example'; // string | 

try {
    $result = $apiInstance->backgroundGetBackgroundApiOperationByrequestId($request_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BackgroundApi->backgroundGetBackgroundApiOperationByrequestId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **request_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\BackgroundRequestStateDto**](../Model/BackgroundRequestStateDto.md)

### Authorization

[serviceapi](../../README.md#serviceapi)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `backgroundGetBackgroundApiOperationContentByrequestId()`

```php
backgroundGetBackgroundApiOperationContentByrequestId($request_id): object
```

Gets the response content, if any, of a previously started background API operation that has finished

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BackgroundApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$request_id = 'request_id_example'; // string | 

try {
    $result = $apiInstance->backgroundGetBackgroundApiOperationContentByrequestId($request_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BackgroundApi->backgroundGetBackgroundApiOperationContentByrequestId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **request_id** | **string**|  | |

### Return type

**object**

### Authorization

[serviceapi](../../README.md#serviceapi)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

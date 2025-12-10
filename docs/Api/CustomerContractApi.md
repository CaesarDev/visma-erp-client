# OpenAPI\Client\CustomerContractApi



All URIs are relative to https://api.finance.visma.net, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**customerContractActivateContractBycontractId()**](CustomerContractApi.md#customerContractActivateContractBycontractId) | **POST** /v1/customerContract/{contractId}/action/activateContract | Activate contract operation |
| [**customerContractActivateUpgradeBycontractId()**](CustomerContractApi.md#customerContractActivateUpgradeBycontractId) | **POST** /v1/customerContract/{contractId}/action/activateUpgrade | Activate upgrade contract operation |
| [**customerContractCreateCustomerContract()**](CustomerContractApi.md#customerContractCreateCustomerContract) | **POST** /v1/customerContract | Create a CustomerContract |
| [**customerContractGetAll()**](CustomerContractApi.md#customerContractGetAll) | **GET** /v1/customerContract | Get a range of Customer Contracts, a filter needs to be specified - ScreenId&#x3D;CT301000 |
| [**customerContractGetCustomerContractBycontractId()**](CustomerContractApi.md#customerContractGetCustomerContractBycontractId) | **GET** /v1/customerContract/{contractId} | Get a specific Customer Contract |
| [**customerContractGetCustomerContractDetailsBycontractId()**](CustomerContractApi.md#customerContractGetCustomerContractDetailsBycontractId) | **GET** /v1/customerContract/{contractId}/details | Get a specific Customer Contract Details |
| [**customerContractGetCustomerContractRecurringSummaryBycontractId()**](CustomerContractApi.md#customerContractGetCustomerContractRecurringSummaryBycontractId) | **GET** /v1/customerContract/{contractId}/recurringSummary | Get a specific Customer Contract Recurring Summary |
| [**customerContractGetCustomerContractSummaryBycontractId()**](CustomerContractApi.md#customerContractGetCustomerContractSummaryBycontractId) | **GET** /v1/customerContract/{contractId}/summary | Get a specific Customer Contract Summary |
| [**customerContractPutBycontractId()**](CustomerContractApi.md#customerContractPutBycontractId) | **PUT** /v1/customerContract/{contractId} | Update a specific CustomerContract |
| [**customerContractSetupAndActivateContractBycontractId()**](CustomerContractApi.md#customerContractSetupAndActivateContractBycontractId) | **POST** /v1/customerContract/{contractId}/action/setupAndActivateContract | Setup and Activate contract operation |
| [**customerContractSetupContractBycontractId()**](CustomerContractApi.md#customerContractSetupContractBycontractId) | **POST** /v1/customerContract/{contractId}/action/setupContract | Setup contract operation |
| [**customerContractTerminateContractBycontractId()**](CustomerContractApi.md#customerContractTerminateContractBycontractId) | **POST** /v1/customerContract/{contractId}/action/terminateContract | Terminate contract operation |
| [**customerContractUpgradeContractBycontractId()**](CustomerContractApi.md#customerContractUpgradeContractBycontractId) | **POST** /v1/customerContract/{contractId}/action/upgradeContract | Upgrade contract operation |


## `customerContractActivateContractBycontractId()`

```php
customerContractActivateContractBycontractId($contract_id, $activation_date, $erp_api_background): object
```

Activate contract operation

Response Message has StatusCode BadRequest or InternalServerError if POST operation failed

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CustomerContractApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$contract_id = 'contract_id_example'; // string | Reference number of the customer contract to be activated
$activation_date = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime | Optional Activation Date
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->customerContractActivateContractBycontractId($contract_id, $activation_date, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomerContractApi->customerContractActivateContractBycontractId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **contract_id** | **string**| Reference number of the customer contract to be activated | |
| **activation_date** | **\DateTime**| Optional Activation Date | [optional] |
| **erp_api_background** | **string**| Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \&quot;none\&quot; (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \&quot;subscription[:&lt;name_1&gt;&#x3D;&lt;value_1&gt;,..,&lt;name_n&gt;&#x3D;&lt;value_n&gt;]\&quot; (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription&#39;s url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content | [optional] |

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

## `customerContractActivateUpgradeBycontractId()`

```php
customerContractActivateUpgradeBycontractId($contract_id, $activation_date, $erp_api_background): object
```

Activate upgrade contract operation

Response Message has StatusCode BadRequest or InternalServerError if POST operation failed

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CustomerContractApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$contract_id = 'contract_id_example'; // string | Reference number of the customer contract to be activated
$activation_date = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime | Optional Activation Date
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->customerContractActivateUpgradeBycontractId($contract_id, $activation_date, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomerContractApi->customerContractActivateUpgradeBycontractId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **contract_id** | **string**| Reference number of the customer contract to be activated | |
| **activation_date** | **\DateTime**| Optional Activation Date | [optional] |
| **erp_api_background** | **string**| Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \&quot;none\&quot; (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \&quot;subscription[:&lt;name_1&gt;&#x3D;&lt;value_1&gt;,..,&lt;name_n&gt;&#x3D;&lt;value_n&gt;]\&quot; (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription&#39;s url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content | [optional] |

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

## `customerContractCreateCustomerContract()`

```php
customerContractCreateCustomerContract($customer_contract_update_dto, $erp_api_background): object
```

Create a CustomerContract

Response Message has StatusCode Created if POST operation succeed

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CustomerContractApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$customer_contract_update_dto = new \OpenAPI\Client\Model\CustomerContractUpdateDto(); // \OpenAPI\Client\Model\CustomerContractUpdateDto | Defines the data for the CustomerContract to create
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->customerContractCreateCustomerContract($customer_contract_update_dto, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomerContractApi->customerContractCreateCustomerContract: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **customer_contract_update_dto** | [**\OpenAPI\Client\Model\CustomerContractUpdateDto**](../Model/CustomerContractUpdateDto.md)| Defines the data for the CustomerContract to create | |
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

## `customerContractGetAll()`

```php
customerContractGetAll($greater_than_value, $number_to_read, $skip_records, $order_by, $last_modified_date_time, $last_modified_date_time_condition, $contract_template, $status, $customer, $expand_summary, $expand_details, $attributes, $expand_attributes, $erp_api_background): \OpenAPI\Client\Model\CustomerContractDto[]
```

Get a range of Customer Contracts, a filter needs to be specified - ScreenId=CT301000

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CustomerContractApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$greater_than_value = 'greater_than_value_example'; // string
$number_to_read = 56; // int
$skip_records = 56; // int
$order_by = 'order_by_example'; // string
$last_modified_date_time = 'last_modified_date_time_example'; // string
$last_modified_date_time_condition = 'last_modified_date_time_condition_example'; // string
$contract_template = 'contract_template_example'; // string
$status = 'status_example'; // string
$customer = 'customer_example'; // string
$expand_summary = True; // bool
$expand_details = True; // bool
$attributes = 'attributes_example'; // string | Attributes (additional information) connected to the entity.   Examples:  {{base}}/customerContract?attributes={\"AttributeID\":\"ValueID\",\"AttributeID\":\"ValueID\"}  {{base}}/customerContract?attributes={\"AttributeID\":\"ValueID1,ValueID2\"}
$expand_attributes = True; // bool
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->customerContractGetAll($greater_than_value, $number_to_read, $skip_records, $order_by, $last_modified_date_time, $last_modified_date_time_condition, $contract_template, $status, $customer, $expand_summary, $expand_details, $attributes, $expand_attributes, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomerContractApi->customerContractGetAll: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **greater_than_value** | **string**|  | [optional] |
| **number_to_read** | **int**|  | [optional] |
| **skip_records** | **int**|  | [optional] |
| **order_by** | **string**|  | [optional] |
| **last_modified_date_time** | **string**|  | [optional] |
| **last_modified_date_time_condition** | **string**|  | [optional] |
| **contract_template** | **string**|  | [optional] |
| **status** | **string**|  | [optional] |
| **customer** | **string**|  | [optional] |
| **expand_summary** | **bool**|  | [optional] |
| **expand_details** | **bool**|  | [optional] |
| **attributes** | **string**| Attributes (additional information) connected to the entity.   Examples:  {{base}}/customerContract?attributes&#x3D;{\&quot;AttributeID\&quot;:\&quot;ValueID\&quot;,\&quot;AttributeID\&quot;:\&quot;ValueID\&quot;}  {{base}}/customerContract?attributes&#x3D;{\&quot;AttributeID\&quot;:\&quot;ValueID1,ValueID2\&quot;} | [optional] |
| **expand_attributes** | **bool**|  | [optional] |
| **erp_api_background** | **string**| Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \&quot;none\&quot; (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \&quot;subscription[:&lt;name_1&gt;&#x3D;&lt;value_1&gt;,..,&lt;name_n&gt;&#x3D;&lt;value_n&gt;]\&quot; (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription&#39;s url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content | [optional] |

### Return type

[**\OpenAPI\Client\Model\CustomerContractDto[]**](../Model/CustomerContractDto.md)

### Authorization

[serviceapi](../../README.md#serviceapi)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `customerContractGetCustomerContractBycontractId()`

```php
customerContractGetCustomerContractBycontractId($contract_id, $erp_api_background): \OpenAPI\Client\Model\CustomerContractDto
```

Get a specific Customer Contract

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CustomerContractApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$contract_id = 'contract_id_example'; // string | Identifies the customer contract
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->customerContractGetCustomerContractBycontractId($contract_id, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomerContractApi->customerContractGetCustomerContractBycontractId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **contract_id** | **string**| Identifies the customer contract | |
| **erp_api_background** | **string**| Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \&quot;none\&quot; (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \&quot;subscription[:&lt;name_1&gt;&#x3D;&lt;value_1&gt;,..,&lt;name_n&gt;&#x3D;&lt;value_n&gt;]\&quot; (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription&#39;s url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content | [optional] |

### Return type

[**\OpenAPI\Client\Model\CustomerContractDto**](../Model/CustomerContractDto.md)

### Authorization

[serviceapi](../../README.md#serviceapi)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `customerContractGetCustomerContractDetailsBycontractId()`

```php
customerContractGetCustomerContractDetailsBycontractId($contract_id, $erp_api_background): \OpenAPI\Client\Model\CustomerContractDetailsDto
```

Get a specific Customer Contract Details

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CustomerContractApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$contract_id = 'contract_id_example'; // string | Identifies the customer contract
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->customerContractGetCustomerContractDetailsBycontractId($contract_id, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomerContractApi->customerContractGetCustomerContractDetailsBycontractId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **contract_id** | **string**| Identifies the customer contract | |
| **erp_api_background** | **string**| Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \&quot;none\&quot; (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \&quot;subscription[:&lt;name_1&gt;&#x3D;&lt;value_1&gt;,..,&lt;name_n&gt;&#x3D;&lt;value_n&gt;]\&quot; (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription&#39;s url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content | [optional] |

### Return type

[**\OpenAPI\Client\Model\CustomerContractDetailsDto**](../Model/CustomerContractDetailsDto.md)

### Authorization

[serviceapi](../../README.md#serviceapi)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `text/json`, `application/xml`, `text/xml`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `customerContractGetCustomerContractRecurringSummaryBycontractId()`

```php
customerContractGetCustomerContractRecurringSummaryBycontractId($contract_id, $erp_api_background): \OpenAPI\Client\Model\CustomerContractRecurringSummaryDto
```

Get a specific Customer Contract Recurring Summary

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CustomerContractApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$contract_id = 'contract_id_example'; // string | Identifies the customer contract
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->customerContractGetCustomerContractRecurringSummaryBycontractId($contract_id, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomerContractApi->customerContractGetCustomerContractRecurringSummaryBycontractId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **contract_id** | **string**| Identifies the customer contract | |
| **erp_api_background** | **string**| Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \&quot;none\&quot; (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \&quot;subscription[:&lt;name_1&gt;&#x3D;&lt;value_1&gt;,..,&lt;name_n&gt;&#x3D;&lt;value_n&gt;]\&quot; (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription&#39;s url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content | [optional] |

### Return type

[**\OpenAPI\Client\Model\CustomerContractRecurringSummaryDto**](../Model/CustomerContractRecurringSummaryDto.md)

### Authorization

[serviceapi](../../README.md#serviceapi)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `text/json`, `application/xml`, `text/xml`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `customerContractGetCustomerContractSummaryBycontractId()`

```php
customerContractGetCustomerContractSummaryBycontractId($contract_id, $erp_api_background): \OpenAPI\Client\Model\CustomerContractSummaryDto
```

Get a specific Customer Contract Summary

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CustomerContractApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$contract_id = 'contract_id_example'; // string | Identifies the customer contract
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->customerContractGetCustomerContractSummaryBycontractId($contract_id, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomerContractApi->customerContractGetCustomerContractSummaryBycontractId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **contract_id** | **string**| Identifies the customer contract | |
| **erp_api_background** | **string**| Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \&quot;none\&quot; (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \&quot;subscription[:&lt;name_1&gt;&#x3D;&lt;value_1&gt;,..,&lt;name_n&gt;&#x3D;&lt;value_n&gt;]\&quot; (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription&#39;s url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content | [optional] |

### Return type

[**\OpenAPI\Client\Model\CustomerContractSummaryDto**](../Model/CustomerContractSummaryDto.md)

### Authorization

[serviceapi](../../README.md#serviceapi)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `text/json`, `application/xml`, `text/xml`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `customerContractPutBycontractId()`

```php
customerContractPutBycontractId($contract_id, $customer_contract_update_dto, $erp_api_background): \OpenAPI\Client\Model\BackgroundApiAcceptedDto
```

Update a specific CustomerContract

Response Message has StatusCode NoContent if PUT operation succeed

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CustomerContractApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$contract_id = 'contract_id_example'; // string | Identifies the CustomerContract to update
$customer_contract_update_dto = new \OpenAPI\Client\Model\CustomerContractUpdateDto(); // \OpenAPI\Client\Model\CustomerContractUpdateDto | Defines the data for the CustomerContract to update
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->customerContractPutBycontractId($contract_id, $customer_contract_update_dto, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomerContractApi->customerContractPutBycontractId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **contract_id** | **string**| Identifies the CustomerContract to update | |
| **customer_contract_update_dto** | [**\OpenAPI\Client\Model\CustomerContractUpdateDto**](../Model/CustomerContractUpdateDto.md)| Defines the data for the CustomerContract to update | |
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

## `customerContractSetupAndActivateContractBycontractId()`

```php
customerContractSetupAndActivateContractBycontractId($contract_id, $activation_date, $erp_api_background): object
```

Setup and Activate contract operation

Response Message has StatusCode BadRequest or InternalServerError if POST operation failed

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CustomerContractApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$contract_id = 'contract_id_example'; // string | Reference number of the customer contract to be setup and activated
$activation_date = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime | Optional Activation Date
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->customerContractSetupAndActivateContractBycontractId($contract_id, $activation_date, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomerContractApi->customerContractSetupAndActivateContractBycontractId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **contract_id** | **string**| Reference number of the customer contract to be setup and activated | |
| **activation_date** | **\DateTime**| Optional Activation Date | [optional] |
| **erp_api_background** | **string**| Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \&quot;none\&quot; (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \&quot;subscription[:&lt;name_1&gt;&#x3D;&lt;value_1&gt;,..,&lt;name_n&gt;&#x3D;&lt;value_n&gt;]\&quot; (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription&#39;s url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content | [optional] |

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

## `customerContractSetupContractBycontractId()`

```php
customerContractSetupContractBycontractId($contract_id, $setup_date, $erp_api_background): object
```

Setup contract operation

Response Message has StatusCode BadRequest or InternalServerError if POST operation failed

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CustomerContractApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$contract_id = 'contract_id_example'; // string | Reference number of the customer contract to be set up
$setup_date = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime | Optional Setup Date
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->customerContractSetupContractBycontractId($contract_id, $setup_date, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomerContractApi->customerContractSetupContractBycontractId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **contract_id** | **string**| Reference number of the customer contract to be set up | |
| **setup_date** | **\DateTime**| Optional Setup Date | [optional] |
| **erp_api_background** | **string**| Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \&quot;none\&quot; (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \&quot;subscription[:&lt;name_1&gt;&#x3D;&lt;value_1&gt;,..,&lt;name_n&gt;&#x3D;&lt;value_n&gt;]\&quot; (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription&#39;s url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content | [optional] |

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

## `customerContractTerminateContractBycontractId()`

```php
customerContractTerminateContractBycontractId($contract_id, $termination_date, $erp_api_background): object
```

Terminate contract operation

Response Message has StatusCode BadRequest or InternalServerError if POST operation failed

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CustomerContractApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$contract_id = 'contract_id_example'; // string | Reference number of the customer contract to be terminated
$termination_date = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime | Optional Termination Date
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->customerContractTerminateContractBycontractId($contract_id, $termination_date, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomerContractApi->customerContractTerminateContractBycontractId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **contract_id** | **string**| Reference number of the customer contract to be terminated | |
| **termination_date** | **\DateTime**| Optional Termination Date | [optional] |
| **erp_api_background** | **string**| Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \&quot;none\&quot; (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \&quot;subscription[:&lt;name_1&gt;&#x3D;&lt;value_1&gt;,..,&lt;name_n&gt;&#x3D;&lt;value_n&gt;]\&quot; (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription&#39;s url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content | [optional] |

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

## `customerContractUpgradeContractBycontractId()`

```php
customerContractUpgradeContractBycontractId($contract_id, $erp_api_background): object
```

Upgrade contract operation

Response Message has StatusCode BadRequest or InternalServerError if POST operation failed

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CustomerContractApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$contract_id = 'contract_id_example'; // string | Reference number of the customer contract to be upgraded
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->customerContractUpgradeContractBycontractId($contract_id, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomerContractApi->customerContractUpgradeContractBycontractId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **contract_id** | **string**| Reference number of the customer contract to be upgraded | |
| **erp_api_background** | **string**| Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \&quot;none\&quot; (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \&quot;subscription[:&lt;name_1&gt;&#x3D;&lt;value_1&gt;,..,&lt;name_n&gt;&#x3D;&lt;value_n&gt;]\&quot; (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription&#39;s url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content | [optional] |

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

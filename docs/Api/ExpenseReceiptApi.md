# OpenAPI\Client\ExpenseReceiptApi



All URIs are relative to https://api.finance.visma.net, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**expenseReceiptCreateAttachmentByreceiptNumber()**](ExpenseReceiptApi.md#expenseReceiptCreateAttachmentByreceiptNumber) | **POST** /v1/expenseReceipt/{receiptNumber}/attachment | Creates an attachment and associates it with an expense receipt. If the file already exists, a new revision is created. |
| [**expenseReceiptDeleteByreceiptNumber()**](ExpenseReceiptApi.md#expenseReceiptDeleteByreceiptNumber) | **DELETE** /v1/expenseReceipt/{receiptNumber} | Deletes a specific Expense Receipt |
| [**expenseReceiptGetAll()**](ExpenseReceiptApi.md#expenseReceiptGetAll) | **GET** /v1/expenseReceipt | Get a range of Expense Receipts, a filter needs to be specified. ScreenId&#x3D;EP301020 |
| [**expenseReceiptGetByreceiptNumber()**](ExpenseReceiptApi.md#expenseReceiptGetByreceiptNumber) | **GET** /v1/expenseReceipt/{receiptNumber} | Get a specific ExpenseReceipt |
| [**expenseReceiptPost()**](ExpenseReceiptApi.md#expenseReceiptPost) | **POST** /v1/expenseReceipt | Create a Expense Receipt |
| [**expenseReceiptPutByreceiptNumber()**](ExpenseReceiptApi.md#expenseReceiptPutByreceiptNumber) | **PUT** /v1/expenseReceipt/{receiptNumber} | Update a Expense Receipt |


## `expenseReceiptCreateAttachmentByreceiptNumber()`

```php
expenseReceiptCreateAttachmentByreceiptNumber($receipt_number, $erp_api_background, $if_match): \OpenAPI\Client\Model\BackgroundApiAcceptedDto
```

Creates an attachment and associates it with an expense receipt. If the file already exists, a new revision is created.

The action result dto contains information about the result of running the action. <br></br>  Response Message has StatusCode BadRequest or InternalServerError if POST operation failed. <br></br>  In this endpoint, If-Match can be checked against resource current version when calling with 'erp-api-background' HTTP header.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ExpenseReceiptApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$receipt_number = 'receipt_number_example'; // string | Identifies the credit note
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content
$if_match = 'if_match_example'; // string | The If-Match HTTP header allows clients to update a resource only if its current version matches a specific ETag. This mechanism helps prevent conflicts when multiple clients attempt to modify the same resource simultaneously. The If-Match header should be included in the request headers using the following syntax: If-Match: \"etag_value\" * If the POST operation is successful, the server responds with 200 OK and includes the new ETag value in the response headers. * If the ETag on the server does not match the value provided in the If-Match header, the server responds with 412 Precondition Failed.

try {
    $result = $apiInstance->expenseReceiptCreateAttachmentByreceiptNumber($receipt_number, $erp_api_background, $if_match);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ExpenseReceiptApi->expenseReceiptCreateAttachmentByreceiptNumber: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **receipt_number** | **string**| Identifies the credit note | |
| **erp_api_background** | **string**| Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \&quot;none\&quot; (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \&quot;subscription[:&lt;name_1&gt;&#x3D;&lt;value_1&gt;,..,&lt;name_n&gt;&#x3D;&lt;value_n&gt;]\&quot; (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription&#39;s url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content | [optional] |
| **if_match** | **string**| The If-Match HTTP header allows clients to update a resource only if its current version matches a specific ETag. This mechanism helps prevent conflicts when multiple clients attempt to modify the same resource simultaneously. The If-Match header should be included in the request headers using the following syntax: If-Match: \&quot;etag_value\&quot; * If the POST operation is successful, the server responds with 200 OK and includes the new ETag value in the response headers. * If the ETag on the server does not match the value provided in the If-Match header, the server responds with 412 Precondition Failed. | [optional] |

### Return type

[**\OpenAPI\Client\Model\BackgroundApiAcceptedDto**](../Model/BackgroundApiAcceptedDto.md)

### Authorization

[serviceapi](../../README.md#serviceapi)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `expenseReceiptDeleteByreceiptNumber()`

```php
expenseReceiptDeleteByreceiptNumber($receipt_number, $erp_api_background): \OpenAPI\Client\Model\BackgroundApiAcceptedDto
```

Deletes a specific Expense Receipt

Response Message has StatusCode NoContent if DELETE operation succeed

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ExpenseReceiptApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$receipt_number = 'receipt_number_example'; // string | Identifies the Expense Receipt to delete
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->expenseReceiptDeleteByreceiptNumber($receipt_number, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ExpenseReceiptApi->expenseReceiptDeleteByreceiptNumber: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **receipt_number** | **string**| Identifies the Expense Receipt to delete | |
| **erp_api_background** | **string**| Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \&quot;none\&quot; (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \&quot;subscription[:&lt;name_1&gt;&#x3D;&lt;value_1&gt;,..,&lt;name_n&gt;&#x3D;&lt;value_n&gt;]\&quot; (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription&#39;s url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content | [optional] |

### Return type

[**\OpenAPI\Client\Model\BackgroundApiAcceptedDto**](../Model/BackgroundApiAcceptedDto.md)

### Authorization

[serviceapi](../../README.md#serviceapi)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `expenseReceiptGetAll()`

```php
expenseReceiptGetAll($date, $date_condition, $inventory, $project, $claimed_by, $project_task, $invoiceable, $status, $customer, $erp_api_background): \OpenAPI\Client\Model\ExpenseReceiptDto[]
```

Get a range of Expense Receipts, a filter needs to be specified. ScreenId=EP301020

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ExpenseReceiptApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$date = 'date_example'; // string | The date of the document
$date_condition = 'date_condition_example'; // string
$inventory = 'inventory_example'; // string | Identifies the inventory item from the document
$project = 'project_example'; // string | Identifies the project from the document
$claimed_by = 'claimed_by_example'; // string | Identifies the employee from the document
$project_task = 'project_task_example'; // string | Filter on Task ID.
$invoiceable = True; // bool | If the document is invoiceable
$status = 'status_example'; // string | The status of the document.
$customer = 'customer_example'; // string | Identifies the customer from the document
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->expenseReceiptGetAll($date, $date_condition, $inventory, $project, $claimed_by, $project_task, $invoiceable, $status, $customer, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ExpenseReceiptApi->expenseReceiptGetAll: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **date** | **string**| The date of the document | [optional] |
| **date_condition** | **string**|  | [optional] |
| **inventory** | **string**| Identifies the inventory item from the document | [optional] |
| **project** | **string**| Identifies the project from the document | [optional] |
| **claimed_by** | **string**| Identifies the employee from the document | [optional] |
| **project_task** | **string**| Filter on Task ID. | [optional] |
| **invoiceable** | **bool**| If the document is invoiceable | [optional] |
| **status** | **string**| The status of the document. | [optional] |
| **customer** | **string**| Identifies the customer from the document | [optional] |
| **erp_api_background** | **string**| Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \&quot;none\&quot; (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \&quot;subscription[:&lt;name_1&gt;&#x3D;&lt;value_1&gt;,..,&lt;name_n&gt;&#x3D;&lt;value_n&gt;]\&quot; (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription&#39;s url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content | [optional] |

### Return type

[**\OpenAPI\Client\Model\ExpenseReceiptDto[]**](../Model/ExpenseReceiptDto.md)

### Authorization

[serviceapi](../../README.md#serviceapi)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `expenseReceiptGetByreceiptNumber()`

```php
expenseReceiptGetByreceiptNumber($receipt_number, $erp_api_background): \OpenAPI\Client\Model\ExpenseReceiptDto
```

Get a specific ExpenseReceipt

Data for a single expense receipt <br></br>  The response headers include an ETag after a successful GET operation.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ExpenseReceiptApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$receipt_number = 'receipt_number_example'; // string | Identifies the ExpenseReceipt
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->expenseReceiptGetByreceiptNumber($receipt_number, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ExpenseReceiptApi->expenseReceiptGetByreceiptNumber: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **receipt_number** | **string**| Identifies the ExpenseReceipt | |
| **erp_api_background** | **string**| Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \&quot;none\&quot; (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \&quot;subscription[:&lt;name_1&gt;&#x3D;&lt;value_1&gt;,..,&lt;name_n&gt;&#x3D;&lt;value_n&gt;]\&quot; (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription&#39;s url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content | [optional] |

### Return type

[**\OpenAPI\Client\Model\ExpenseReceiptDto**](../Model/ExpenseReceiptDto.md)

### Authorization

[serviceapi](../../README.md#serviceapi)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `expenseReceiptPost()`

```php
expenseReceiptPost($expense_receipt_update_dto, $erp_api_background): object
```

Create a Expense Receipt

Response Message has StatusCode Created if POST operation succeed. <br></br>              Response Message has StatusCode BadRequest or InternalServerError if POST operation failed. <br></br>              The response headers include an ETag after a successful POST operation.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ExpenseReceiptApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$expense_receipt_update_dto = new \OpenAPI\Client\Model\ExpenseReceiptUpdateDto(); // \OpenAPI\Client\Model\ExpenseReceiptUpdateDto | Defines the data for the Expense Receipt to create
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->expenseReceiptPost($expense_receipt_update_dto, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ExpenseReceiptApi->expenseReceiptPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **expense_receipt_update_dto** | [**\OpenAPI\Client\Model\ExpenseReceiptUpdateDto**](../Model/ExpenseReceiptUpdateDto.md)| Defines the data for the Expense Receipt to create | |
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

## `expenseReceiptPutByreceiptNumber()`

```php
expenseReceiptPutByreceiptNumber($receipt_number, $expense_receipt_update_dto, $erp_api_background, $if_match): \OpenAPI\Client\Model\BackgroundApiAcceptedDto
```

Update a Expense Receipt

Response Message has StatusCode NoContent if PUT operation succeed. <br></br>              Response Message has StatusCode BadRequest if PUT operation failed. <br></br>              The response headers include an ETag after a successful PUT operation.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ExpenseReceiptApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$receipt_number = 'receipt_number_example'; // string | Identifies the ExpenseReceipt
$expense_receipt_update_dto = new \OpenAPI\Client\Model\ExpenseReceiptUpdateDto(); // \OpenAPI\Client\Model\ExpenseReceiptUpdateDto | Defines the data for the Expense Receipt to create
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content
$if_match = 'if_match_example'; // string | The If-Match HTTP header allows clients to update a resource only if its current version matches a specific ETag. This mechanism helps prevent conflicts when multiple clients attempt to modify the same resource simultaneously. The If-Match header should be included in the request headers using the following syntax: If-Match: \"etag_value\" * If the update is successful, the server responds with 204 No Content and includes the new ETag value in the response headers. * If the ETag on the server does not match the value provided in the If-Match header, the server responds with 412 Precondition Failed.

try {
    $result = $apiInstance->expenseReceiptPutByreceiptNumber($receipt_number, $expense_receipt_update_dto, $erp_api_background, $if_match);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ExpenseReceiptApi->expenseReceiptPutByreceiptNumber: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **receipt_number** | **string**| Identifies the ExpenseReceipt | |
| **expense_receipt_update_dto** | [**\OpenAPI\Client\Model\ExpenseReceiptUpdateDto**](../Model/ExpenseReceiptUpdateDto.md)| Defines the data for the Expense Receipt to create | |
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

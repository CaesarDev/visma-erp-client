# OpenAPI\Client\SupplierInvoiceApi



All URIs are relative to https://api.finance.visma.net, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**supplierInvoiceCorrectInvoiceByinvoiceNumber()**](SupplierInvoiceApi.md#supplierInvoiceCorrectInvoiceByinvoiceNumber) | **POST** /v1/supplierInvoice/{invoiceNumber}/action/correct | Correct invoice operation |
| [**supplierInvoiceCreateHeaderAttachmentByTypeBydocumentTypeinvoiceNumber()**](SupplierInvoiceApi.md#supplierInvoiceCreateHeaderAttachmentByTypeBydocumentTypeinvoiceNumber) | **POST** /v1/supplierInvoice/documentType/{documentType}/{invoiceNumber}/attachment | Creates an attachment and associates it with a supplier invoice. If the file already exists, a new revision is created. |
| [**supplierInvoiceCreateHeaderAttachmentByinvoiceNumber()**](SupplierInvoiceApi.md#supplierInvoiceCreateHeaderAttachmentByinvoiceNumber) | **POST** /v1/supplierInvoice/{invoiceNumber}/attachment | Creates an attachment and associates it with a supplier invoice. If the file already exists, a new revision is created. |
| [**supplierInvoiceCreateLineAttachmentByTypeBydocumentTypeinvoiceNumberlineNumber()**](SupplierInvoiceApi.md#supplierInvoiceCreateLineAttachmentByTypeBydocumentTypeinvoiceNumberlineNumber) | **POST** /v1/supplierInvoice/documentType/{documentType}/{invoiceNumber}/{lineNumber}/attachment | Creates an attachment and associates it with a certain supplier invoice line. If the file already exists, a new revision is created. |
| [**supplierInvoiceCreateLineAttachmentByinvoiceNumberlineNumber()**](SupplierInvoiceApi.md#supplierInvoiceCreateLineAttachmentByinvoiceNumberlineNumber) | **POST** /v1/supplierInvoice/{invoiceNumber}/{lineNumber}/attachment | Creates an attachment and associates it with a certain supplier invoice line. If the file already exists, a new revision is created. |
| [**supplierInvoiceDeleteBydocumentTypeinvoiceNumber()**](SupplierInvoiceApi.md#supplierInvoiceDeleteBydocumentTypeinvoiceNumber) | **DELETE** /v1/supplierInvoice/{documentType}/{invoiceNumber} | Deletes a specific Supplier Invoice |
| [**supplierInvoiceDeleteByinvoiceNumber()**](SupplierInvoiceApi.md#supplierInvoiceDeleteByinvoiceNumber) | **DELETE** /v1/supplierInvoice/{invoiceNumber} | Deletes a specific Supplier Invoice |
| [**supplierInvoiceGetAllInvoices()**](SupplierInvoiceApi.md#supplierInvoiceGetAllInvoices) | **GET** /v1/supplierInvoice | Get a range of Invoices - ScreenId&#x3D;AP301000.   Request page size must be lower or equal to the allowed max page size which is returned as part of the metadata information.  If requested page size is greater than allowed max page size, request will be limited to max page size |
| [**supplierInvoiceGetByApprovalDocumentId()**](SupplierInvoiceApi.md#supplierInvoiceGetByApprovalDocumentId) | **GET** /v1/supplierInvoice/approval | Get an invoice based on the systemId. SystemID is used for approving supplier invoices |
| [**supplierInvoiceGetByTypeBydocumentTypeinvoiceNumber()**](SupplierInvoiceApi.md#supplierInvoiceGetByTypeBydocumentTypeinvoiceNumber) | **GET** /v1/supplierInvoice/{documentType}/{invoiceNumber} | Get a specific Invoice, DebitAdj, CreditAdj or Prepayment |
| [**supplierInvoiceGetByinvoiceNumber()**](SupplierInvoiceApi.md#supplierInvoiceGetByinvoiceNumber) | **GET** /v1/supplierInvoice/{invoiceNumber} | GET a specific invoice. Only standard invoices are supported. Credit adjustments, credit notes or Prepayments are excluded. |
| [**supplierInvoicePost()**](SupplierInvoiceApi.md#supplierInvoicePost) | **POST** /v1/supplierInvoice | Create an SupplierInvoice |
| [**supplierInvoicePrebookInvoiceBydocumentTypeinvoiceNumber()**](SupplierInvoiceApi.md#supplierInvoicePrebookInvoiceBydocumentTypeinvoiceNumber) | **POST** /v1/supplierInvoice/{documentType}/{invoiceNumber}/action/prebook | Pre-Book invoice operation |
| [**supplierInvoicePutByTypeBydocumentTypeinvoiceNumber()**](SupplierInvoiceApi.md#supplierInvoicePutByTypeBydocumentTypeinvoiceNumber) | **PUT** /v1/supplierInvoice/{documentType}/{invoiceNumber} | Update a specific SupplierInvoice |
| [**supplierInvoicePutByinvoiceNumber()**](SupplierInvoiceApi.md#supplierInvoicePutByinvoiceNumber) | **PUT** /v1/supplierInvoice/{invoiceNumber} | Update a specific SupplierInvoice |
| [**supplierInvoiceReleaseInvoiceByTypeBydocumentTypeinvoiceNumber()**](SupplierInvoiceApi.md#supplierInvoiceReleaseInvoiceByTypeBydocumentTypeinvoiceNumber) | **POST** /v1/supplierInvoice/{documentType}/{invoiceNumber}/action/release | Release invoice operation |
| [**supplierInvoiceReleaseInvoiceByinvoiceNumber()**](SupplierInvoiceApi.md#supplierInvoiceReleaseInvoiceByinvoiceNumber) | **POST** /v1/supplierInvoice/{invoiceNumber}/action/release | Release invoice operation |
| [**supplierInvoiceReverseInvoiceBydocumentTypeinvoiceNumber()**](SupplierInvoiceApi.md#supplierInvoiceReverseInvoiceBydocumentTypeinvoiceNumber) | **POST** /v1/supplierInvoice/{documentType}/{invoiceNumber}/action/reverse | Provides an action for reversing a supplier invoice/adjustment |
| [**supplierInvoiceSendToApprovalBydocumentTypeinvoiceNumber()**](SupplierInvoiceApi.md#supplierInvoiceSendToApprovalBydocumentTypeinvoiceNumber) | **POST** /v1/supplierInvoice/{documentType}/{invoiceNumber}/action/sendtoapproval | Send invoice to approval |
| [**supplierInvoiceVoidInvoiceBydocumentTypeinvoiceNumber()**](SupplierInvoiceApi.md#supplierInvoiceVoidInvoiceBydocumentTypeinvoiceNumber) | **POST** /v1/supplierInvoice/{documentType}/{invoiceNumber}/action/voidinvoice | Void invoice operation |
| [**supplierInvoiceWriteoffInvoiceBydocumentTypeinvoiceNumber()**](SupplierInvoiceApi.md#supplierInvoiceWriteoffInvoiceBydocumentTypeinvoiceNumber) | **POST** /v1/supplierInvoice/{documentType}/{invoiceNumber}/action/writeoff | Write-off invoice operation |


## `supplierInvoiceCorrectInvoiceByinvoiceNumber()`

```php
supplierInvoiceCorrectInvoiceByinvoiceNumber($invoice_number, $erp_api_background, $if_match): \OpenAPI\Client\Model\BackgroundApiAcceptedDto
```

Correct invoice operation

The response headers include an ETag after a successful POST operation.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SupplierInvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$invoice_number = 'invoice_number_example'; // string | Reference number of the document to be corrected
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content
$if_match = 'if_match_example'; // string | The If-Match HTTP header allows clients to update a resource only if its current version matches a specific ETag. This mechanism helps prevent conflicts when multiple clients attempt to modify the same resource simultaneously. The If-Match header should be included in the request headers using the following syntax: If-Match: \"etag_value\" * If the POST operation is successful, the server responds with 200 OK and includes the new ETag value in the response headers. * If the ETag on the server does not match the value provided in the If-Match header, the server responds with 412 Precondition Failed.

try {
    $result = $apiInstance->supplierInvoiceCorrectInvoiceByinvoiceNumber($invoice_number, $erp_api_background, $if_match);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SupplierInvoiceApi->supplierInvoiceCorrectInvoiceByinvoiceNumber: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invoice_number** | **string**| Reference number of the document to be corrected | |
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

## `supplierInvoiceCreateHeaderAttachmentByTypeBydocumentTypeinvoiceNumber()`

```php
supplierInvoiceCreateHeaderAttachmentByTypeBydocumentTypeinvoiceNumber($document_type, $invoice_number, $erp_api_background, $if_match): object
```

Creates an attachment and associates it with a supplier invoice. If the file already exists, a new revision is created.

Response Message has StatusCode Created if POST operation succeed. <br></br>  Response Message has StatusCode BadRequest if POST operation failed. <br></br>  The response headers include an ETag after a successful POST operation.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SupplierInvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$document_type = 'document_type_example'; // string | 
$invoice_number = 'invoice_number_example'; // string | Identifies the supplier invoice
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content
$if_match = 'if_match_example'; // string | The If-Match HTTP header allows clients to update a resource only if its current version matches a specific ETag. This mechanism helps prevent conflicts when multiple clients attempt to modify the same resource simultaneously. The If-Match header should be included in the request headers using the following syntax: If-Match: \"etag_value\" * If the POST operation is successful, the server responds with 200 OK and includes the new ETag value in the response headers. * If the ETag on the server does not match the value provided in the If-Match header, the server responds with 412 Precondition Failed.

try {
    $result = $apiInstance->supplierInvoiceCreateHeaderAttachmentByTypeBydocumentTypeinvoiceNumber($document_type, $invoice_number, $erp_api_background, $if_match);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SupplierInvoiceApi->supplierInvoiceCreateHeaderAttachmentByTypeBydocumentTypeinvoiceNumber: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **document_type** | **string**|  | |
| **invoice_number** | **string**| Identifies the supplier invoice | |
| **erp_api_background** | **string**| Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \&quot;none\&quot; (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \&quot;subscription[:&lt;name_1&gt;&#x3D;&lt;value_1&gt;,..,&lt;name_n&gt;&#x3D;&lt;value_n&gt;]\&quot; (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription&#39;s url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content | [optional] |
| **if_match** | **string**| The If-Match HTTP header allows clients to update a resource only if its current version matches a specific ETag. This mechanism helps prevent conflicts when multiple clients attempt to modify the same resource simultaneously. The If-Match header should be included in the request headers using the following syntax: If-Match: \&quot;etag_value\&quot; * If the POST operation is successful, the server responds with 200 OK and includes the new ETag value in the response headers. * If the ETag on the server does not match the value provided in the If-Match header, the server responds with 412 Precondition Failed. | [optional] |

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

## `supplierInvoiceCreateHeaderAttachmentByinvoiceNumber()`

```php
supplierInvoiceCreateHeaderAttachmentByinvoiceNumber($invoice_number, $erp_api_background, $if_match): object
```

Creates an attachment and associates it with a supplier invoice. If the file already exists, a new revision is created.

Response Message has StatusCode Created if POST operation succeed. <br></br>  Response Message has StatusCode BadRequest if POST operation failed. <br></br>  The response headers include an ETag after a successful POST operation.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SupplierInvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$invoice_number = 'invoice_number_example'; // string | Identifies the supplier invoice
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content
$if_match = 'if_match_example'; // string | The If-Match HTTP header allows clients to update a resource only if its current version matches a specific ETag. This mechanism helps prevent conflicts when multiple clients attempt to modify the same resource simultaneously. The If-Match header should be included in the request headers using the following syntax: If-Match: \"etag_value\" * If the POST operation is successful, the server responds with 200 OK and includes the new ETag value in the response headers. * If the ETag on the server does not match the value provided in the If-Match header, the server responds with 412 Precondition Failed.

try {
    $result = $apiInstance->supplierInvoiceCreateHeaderAttachmentByinvoiceNumber($invoice_number, $erp_api_background, $if_match);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SupplierInvoiceApi->supplierInvoiceCreateHeaderAttachmentByinvoiceNumber: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invoice_number** | **string**| Identifies the supplier invoice | |
| **erp_api_background** | **string**| Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \&quot;none\&quot; (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \&quot;subscription[:&lt;name_1&gt;&#x3D;&lt;value_1&gt;,..,&lt;name_n&gt;&#x3D;&lt;value_n&gt;]\&quot; (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription&#39;s url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content | [optional] |
| **if_match** | **string**| The If-Match HTTP header allows clients to update a resource only if its current version matches a specific ETag. This mechanism helps prevent conflicts when multiple clients attempt to modify the same resource simultaneously. The If-Match header should be included in the request headers using the following syntax: If-Match: \&quot;etag_value\&quot; * If the POST operation is successful, the server responds with 200 OK and includes the new ETag value in the response headers. * If the ETag on the server does not match the value provided in the If-Match header, the server responds with 412 Precondition Failed. | [optional] |

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

## `supplierInvoiceCreateLineAttachmentByTypeBydocumentTypeinvoiceNumberlineNumber()`

```php
supplierInvoiceCreateLineAttachmentByTypeBydocumentTypeinvoiceNumberlineNumber($document_type, $invoice_number, $line_number, $erp_api_background, $if_match): object
```

Creates an attachment and associates it with a certain supplier invoice line. If the file already exists, a new revision is created.

Response Message has StatusCode Created if POST operation succeed. <br></br>  Response Message has StatusCode BadRequest if POST operation failed. <br></br>  The response headers include an ETag after a successful POST operation.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SupplierInvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$document_type = 'document_type_example'; // string | 
$invoice_number = 'invoice_number_example'; // string | Identifies the supplier invoice
$line_number = 56; // int | Identifies the supplier invoice line
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content
$if_match = 'if_match_example'; // string | The If-Match HTTP header allows clients to update a resource only if its current version matches a specific ETag. This mechanism helps prevent conflicts when multiple clients attempt to modify the same resource simultaneously. The If-Match header should be included in the request headers using the following syntax: If-Match: \"etag_value\" * If the POST operation is successful, the server responds with 200 OK and includes the new ETag value in the response headers. * If the ETag on the server does not match the value provided in the If-Match header, the server responds with 412 Precondition Failed.

try {
    $result = $apiInstance->supplierInvoiceCreateLineAttachmentByTypeBydocumentTypeinvoiceNumberlineNumber($document_type, $invoice_number, $line_number, $erp_api_background, $if_match);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SupplierInvoiceApi->supplierInvoiceCreateLineAttachmentByTypeBydocumentTypeinvoiceNumberlineNumber: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **document_type** | **string**|  | |
| **invoice_number** | **string**| Identifies the supplier invoice | |
| **line_number** | **int**| Identifies the supplier invoice line | |
| **erp_api_background** | **string**| Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \&quot;none\&quot; (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \&quot;subscription[:&lt;name_1&gt;&#x3D;&lt;value_1&gt;,..,&lt;name_n&gt;&#x3D;&lt;value_n&gt;]\&quot; (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription&#39;s url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content | [optional] |
| **if_match** | **string**| The If-Match HTTP header allows clients to update a resource only if its current version matches a specific ETag. This mechanism helps prevent conflicts when multiple clients attempt to modify the same resource simultaneously. The If-Match header should be included in the request headers using the following syntax: If-Match: \&quot;etag_value\&quot; * If the POST operation is successful, the server responds with 200 OK and includes the new ETag value in the response headers. * If the ETag on the server does not match the value provided in the If-Match header, the server responds with 412 Precondition Failed. | [optional] |

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

## `supplierInvoiceCreateLineAttachmentByinvoiceNumberlineNumber()`

```php
supplierInvoiceCreateLineAttachmentByinvoiceNumberlineNumber($invoice_number, $line_number, $erp_api_background, $if_match): object
```

Creates an attachment and associates it with a certain supplier invoice line. If the file already exists, a new revision is created.

Response Message has StatusCode Created if POST operation succeed. <br></br>  Response Message has StatusCode BadRequest if POST operation failed. <br></br>  The response headers include an ETag after a successful POST operation.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SupplierInvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$invoice_number = 'invoice_number_example'; // string | Identifies the supplier invoice
$line_number = 56; // int | Specifies line number
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content
$if_match = 'if_match_example'; // string | The If-Match HTTP header allows clients to update a resource only if its current version matches a specific ETag. This mechanism helps prevent conflicts when multiple clients attempt to modify the same resource simultaneously. The If-Match header should be included in the request headers using the following syntax: If-Match: \"etag_value\" * If the POST operation is successful, the server responds with 200 OK and includes the new ETag value in the response headers. * If the ETag on the server does not match the value provided in the If-Match header, the server responds with 412 Precondition Failed.

try {
    $result = $apiInstance->supplierInvoiceCreateLineAttachmentByinvoiceNumberlineNumber($invoice_number, $line_number, $erp_api_background, $if_match);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SupplierInvoiceApi->supplierInvoiceCreateLineAttachmentByinvoiceNumberlineNumber: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invoice_number** | **string**| Identifies the supplier invoice | |
| **line_number** | **int**| Specifies line number | |
| **erp_api_background** | **string**| Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \&quot;none\&quot; (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \&quot;subscription[:&lt;name_1&gt;&#x3D;&lt;value_1&gt;,..,&lt;name_n&gt;&#x3D;&lt;value_n&gt;]\&quot; (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription&#39;s url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content | [optional] |
| **if_match** | **string**| The If-Match HTTP header allows clients to update a resource only if its current version matches a specific ETag. This mechanism helps prevent conflicts when multiple clients attempt to modify the same resource simultaneously. The If-Match header should be included in the request headers using the following syntax: If-Match: \&quot;etag_value\&quot; * If the POST operation is successful, the server responds with 200 OK and includes the new ETag value in the response headers. * If the ETag on the server does not match the value provided in the If-Match header, the server responds with 412 Precondition Failed. | [optional] |

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

## `supplierInvoiceDeleteBydocumentTypeinvoiceNumber()`

```php
supplierInvoiceDeleteBydocumentTypeinvoiceNumber($document_type, $invoice_number, $erp_api_background): \OpenAPI\Client\Model\BackgroundApiAcceptedDto
```

Deletes a specific Supplier Invoice

Response Message has StatusCode NoContent if DELETE operation succeed

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SupplierInvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$document_type = 'document_type_example'; // string | Identifies the docType of Supplier Invoice to delete
$invoice_number = 'invoice_number_example'; // string | Identifies the Supplier Invoice to delete
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->supplierInvoiceDeleteBydocumentTypeinvoiceNumber($document_type, $invoice_number, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SupplierInvoiceApi->supplierInvoiceDeleteBydocumentTypeinvoiceNumber: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **document_type** | **string**| Identifies the docType of Supplier Invoice to delete | |
| **invoice_number** | **string**| Identifies the Supplier Invoice to delete | |
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

## `supplierInvoiceDeleteByinvoiceNumber()`

```php
supplierInvoiceDeleteByinvoiceNumber($invoice_number, $erp_api_background): \OpenAPI\Client\Model\BackgroundApiAcceptedDto
```

Deletes a specific Supplier Invoice

Response Message has StatusCode NoContent if DELETE operation succeed

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SupplierInvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$invoice_number = 'invoice_number_example'; // string | Identifies the Supplier Invoice to delete
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->supplierInvoiceDeleteByinvoiceNumber($invoice_number, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SupplierInvoiceApi->supplierInvoiceDeleteByinvoiceNumber: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invoice_number** | **string**| Identifies the Supplier Invoice to delete | |
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

## `supplierInvoiceGetAllInvoices()`

```php
supplierInvoiceGetAllInvoices($supplier, $expand_attachment, $expand_landed_costs, $document_type, $released, $project, $expand_approval, $expand_note, $number_to_read, $skip_records, $status, $expand_line_prebook_accounts, $branch, $financial_period, $due_date, $due_date_condition, $doc_date, $doc_date_condition, $item, $balance, $balance_condition, $greater_than_value, $last_modified_date_time, $last_modified_date_time_condition, $created_date_time, $created_date_time_condition, $page_number, $page_size, $erp_api_background): \OpenAPI\Client\Model\SupplierInvoiceDto[]
```

Get a range of Invoices - ScreenId=AP301000.   Request page size must be lower or equal to the allowed max page size which is returned as part of the metadata information.  If requested page size is greater than allowed max page size, request will be limited to max page size

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SupplierInvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$supplier = 'supplier_example'; // string | Filter by Supplier
$expand_attachment = True; // bool | Set to true if you want to see all attachments regarding this document.
$expand_landed_costs = True; // bool | Expland landed cost lines
$document_type = 'document_type_example'; // string | By type of document.
$released = 56; // int | Parameter for showing if invoice has been released or not.
$project = 'project_example'; // string | Filter by the project with which the document is associated.
$expand_approval = True; // bool | Set to true to include approval information.
$expand_note = True; // bool | Set to true to include description.
$number_to_read = 56; // int | This field has been deprecated and will be removed in future versions. Use pagenumber and pagesize for pagination purposes. Pagenumber and pagesize does not work with NumberToRead and SkipRecords.
$skip_records = 56; // int | This field has been deprecated and will be removed in future versions. Use pagenumber and pagesize for pagination purposes. Pagenumber and pagesize does not work with NumberToRead and SkipRecords.
$status = 'status_example'; // string | The status of the document
$expand_line_prebook_accounts = True; // bool | Expland line-level pre-booking account and sub-account information.
$branch = 'branch_example'; // string | Filter by Branch
$financial_period = 'financial_period_example'; // string | Filter by Financial Period, format YYYYPP
$due_date = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime | This value indicates the date the document is due for payment. Use it to retrieve all records that have the Due date since that time, up to the future.    Accepted format:  * ```yyyy-MM-dd```  * ```yyyy-MM-dd```  * ```yyyy-MM-dd```  * ```yyyy-MM-dd```  * ```yyyy-MM-dd```    _Note:_ __DueDate__ and __DueDateConditionCondition__ are __mutually inclusive__.
$due_date_condition = 'due_date_condition_example'; // string | This value represents the condition to be applied to the Due Date when retrieving records.    Accepted values (without the single quotes):  * '&gt;' for greater than  * '&lt;' for less than  * '&gt;=' for greater than or equal  * '&lt;=' for less than or equal    _Note:_ __DueDate__ and __DueDateCondition__ are __mutually inclusive__.
$doc_date = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime | This value indicates the document date. Use it to retrieve all records that have the Document Date since that time, up to the future.    Accepted format:  * ```yyyy-MM-dd```  * ```yyyy-MM-dd```  * ```yyyy-MM-dd```  * ```yyyy-MM-dd```  * ```yyyy-MM-dd```    _Note:_ __Docate__ and __DocDateCondition__ are __mutually inclusive__.
$doc_date_condition = 'doc_date_condition_example'; // string | This value represents the condition to be applied to the Document Date when retrieving records.    Accepted values (without the single quotes):  * '&gt;' for greater than  * '&lt;' for less than  * '&gt;=' for greater than or equal  * '&lt;=' for less than or equal    _Note:_ __DocumentDate__ and __DocumentDateCondition__ are __mutually inclusive__.
$item = 'item_example'; // string | Filter by Item used into the document lines
$balance = 3.4; // float | This value represents balance of the payment remaining to be applied and released. Only released applications will count towards the balance.    _Note:_ __Balance__ and __BalanceCondition__ are __mutually inclusive__.
$balance_condition = 'balance_condition_example'; // string | This value represents the condition to be applied to the Balance when retrieving records.    Accepted values (without the single quotes):  * '&gt;' for greater than  * '&lt;' for less than  * '&gt;=' for greater than or equal  * '&lt;=' for less than or equal    _Note:_ __Balance__ and __BalanceCondition__ are __mutually inclusive__.
$greater_than_value = 'greater_than_value_example'; // string | Greater than value. The item which is the object for this, varies from API to API.
$last_modified_date_time = 'last_modified_date_time_example'; // string | This value, generated by the system, indicates the last time the record was modified. Use it to retrieve all records that have been modified since that time, up to the present.    Accepted format:  * ```yyyy-MM-dd```  * ```yyyy-MM-dd HH:mm:ss```  * ```yyyy-MM-dd HH:mm:ss.FFF```  * ```yyyy-MM-ddTHH:mm:ss```  * ```yyyy-MM-ddTHH:mm:ss.FFF```    _Note:_ __LastModifiedDateTime__ and __LastModifiedDateTimeCondition__ are __mutually inclusive__.
$last_modified_date_time_condition = 'last_modified_date_time_condition_example'; // string | This value represents the condition to be applied when retrieving records.    Accepted values (without the single quotes):  * '&gt;' for greater than  * '&lt;' for less than  * '&gt;=' for greater than or equal  * '&lt;=' for less than or equal    _Note:_ __LastModifiedDateTime__ and __LastModifiedDateTimeCondition__ are __mutually inclusive__.
$created_date_time = 'created_date_time_example'; // string | Creation date and time.
$created_date_time_condition = 'created_date_time_condition_example'; // string | System-retrieved information for state/condition
$page_number = 56; // int | Pagination parameter. Page number.
$page_size = 56; // int | Pagination parameter. Number of items to be collected.  Please use a page size lower or equal to the allowed max page size which is returned as part of the metadata information.  If requested page size is greater than allowed max page size, request will be limited to max page size.
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->supplierInvoiceGetAllInvoices($supplier, $expand_attachment, $expand_landed_costs, $document_type, $released, $project, $expand_approval, $expand_note, $number_to_read, $skip_records, $status, $expand_line_prebook_accounts, $branch, $financial_period, $due_date, $due_date_condition, $doc_date, $doc_date_condition, $item, $balance, $balance_condition, $greater_than_value, $last_modified_date_time, $last_modified_date_time_condition, $created_date_time, $created_date_time_condition, $page_number, $page_size, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SupplierInvoiceApi->supplierInvoiceGetAllInvoices: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **supplier** | **string**| Filter by Supplier | [optional] |
| **expand_attachment** | **bool**| Set to true if you want to see all attachments regarding this document. | [optional] |
| **expand_landed_costs** | **bool**| Expland landed cost lines | [optional] |
| **document_type** | **string**| By type of document. | [optional] |
| **released** | **int**| Parameter for showing if invoice has been released or not. | [optional] |
| **project** | **string**| Filter by the project with which the document is associated. | [optional] |
| **expand_approval** | **bool**| Set to true to include approval information. | [optional] |
| **expand_note** | **bool**| Set to true to include description. | [optional] |
| **number_to_read** | **int**| This field has been deprecated and will be removed in future versions. Use pagenumber and pagesize for pagination purposes. Pagenumber and pagesize does not work with NumberToRead and SkipRecords. | [optional] |
| **skip_records** | **int**| This field has been deprecated and will be removed in future versions. Use pagenumber and pagesize for pagination purposes. Pagenumber and pagesize does not work with NumberToRead and SkipRecords. | [optional] |
| **status** | **string**| The status of the document | [optional] |
| **expand_line_prebook_accounts** | **bool**| Expland line-level pre-booking account and sub-account information. | [optional] |
| **branch** | **string**| Filter by Branch | [optional] |
| **financial_period** | **string**| Filter by Financial Period, format YYYYPP | [optional] |
| **due_date** | **\DateTime**| This value indicates the date the document is due for payment. Use it to retrieve all records that have the Due date since that time, up to the future.    Accepted format:  * &#x60;&#x60;&#x60;yyyy-MM-dd&#x60;&#x60;&#x60;  * &#x60;&#x60;&#x60;yyyy-MM-dd&#x60;&#x60;&#x60;  * &#x60;&#x60;&#x60;yyyy-MM-dd&#x60;&#x60;&#x60;  * &#x60;&#x60;&#x60;yyyy-MM-dd&#x60;&#x60;&#x60;  * &#x60;&#x60;&#x60;yyyy-MM-dd&#x60;&#x60;&#x60;    _Note:_ __DueDate__ and __DueDateConditionCondition__ are __mutually inclusive__. | [optional] |
| **due_date_condition** | **string**| This value represents the condition to be applied to the Due Date when retrieving records.    Accepted values (without the single quotes):  * &#39;&amp;gt;&#39; for greater than  * &#39;&amp;lt;&#39; for less than  * &#39;&amp;gt;&#x3D;&#39; for greater than or equal  * &#39;&amp;lt;&#x3D;&#39; for less than or equal    _Note:_ __DueDate__ and __DueDateCondition__ are __mutually inclusive__. | [optional] |
| **doc_date** | **\DateTime**| This value indicates the document date. Use it to retrieve all records that have the Document Date since that time, up to the future.    Accepted format:  * &#x60;&#x60;&#x60;yyyy-MM-dd&#x60;&#x60;&#x60;  * &#x60;&#x60;&#x60;yyyy-MM-dd&#x60;&#x60;&#x60;  * &#x60;&#x60;&#x60;yyyy-MM-dd&#x60;&#x60;&#x60;  * &#x60;&#x60;&#x60;yyyy-MM-dd&#x60;&#x60;&#x60;  * &#x60;&#x60;&#x60;yyyy-MM-dd&#x60;&#x60;&#x60;    _Note:_ __Docate__ and __DocDateCondition__ are __mutually inclusive__. | [optional] |
| **doc_date_condition** | **string**| This value represents the condition to be applied to the Document Date when retrieving records.    Accepted values (without the single quotes):  * &#39;&amp;gt;&#39; for greater than  * &#39;&amp;lt;&#39; for less than  * &#39;&amp;gt;&#x3D;&#39; for greater than or equal  * &#39;&amp;lt;&#x3D;&#39; for less than or equal    _Note:_ __DocumentDate__ and __DocumentDateCondition__ are __mutually inclusive__. | [optional] |
| **item** | **string**| Filter by Item used into the document lines | [optional] |
| **balance** | **float**| This value represents balance of the payment remaining to be applied and released. Only released applications will count towards the balance.    _Note:_ __Balance__ and __BalanceCondition__ are __mutually inclusive__. | [optional] |
| **balance_condition** | **string**| This value represents the condition to be applied to the Balance when retrieving records.    Accepted values (without the single quotes):  * &#39;&amp;gt;&#39; for greater than  * &#39;&amp;lt;&#39; for less than  * &#39;&amp;gt;&#x3D;&#39; for greater than or equal  * &#39;&amp;lt;&#x3D;&#39; for less than or equal    _Note:_ __Balance__ and __BalanceCondition__ are __mutually inclusive__. | [optional] |
| **greater_than_value** | **string**| Greater than value. The item which is the object for this, varies from API to API. | [optional] |
| **last_modified_date_time** | **string**| This value, generated by the system, indicates the last time the record was modified. Use it to retrieve all records that have been modified since that time, up to the present.    Accepted format:  * &#x60;&#x60;&#x60;yyyy-MM-dd&#x60;&#x60;&#x60;  * &#x60;&#x60;&#x60;yyyy-MM-dd HH:mm:ss&#x60;&#x60;&#x60;  * &#x60;&#x60;&#x60;yyyy-MM-dd HH:mm:ss.FFF&#x60;&#x60;&#x60;  * &#x60;&#x60;&#x60;yyyy-MM-ddTHH:mm:ss&#x60;&#x60;&#x60;  * &#x60;&#x60;&#x60;yyyy-MM-ddTHH:mm:ss.FFF&#x60;&#x60;&#x60;    _Note:_ __LastModifiedDateTime__ and __LastModifiedDateTimeCondition__ are __mutually inclusive__. | [optional] |
| **last_modified_date_time_condition** | **string**| This value represents the condition to be applied when retrieving records.    Accepted values (without the single quotes):  * &#39;&amp;gt;&#39; for greater than  * &#39;&amp;lt;&#39; for less than  * &#39;&amp;gt;&#x3D;&#39; for greater than or equal  * &#39;&amp;lt;&#x3D;&#39; for less than or equal    _Note:_ __LastModifiedDateTime__ and __LastModifiedDateTimeCondition__ are __mutually inclusive__. | [optional] |
| **created_date_time** | **string**| Creation date and time. | [optional] |
| **created_date_time_condition** | **string**| System-retrieved information for state/condition | [optional] |
| **page_number** | **int**| Pagination parameter. Page number. | [optional] |
| **page_size** | **int**| Pagination parameter. Number of items to be collected.  Please use a page size lower or equal to the allowed max page size which is returned as part of the metadata information.  If requested page size is greater than allowed max page size, request will be limited to max page size. | [optional] |
| **erp_api_background** | **string**| Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \&quot;none\&quot; (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \&quot;subscription[:&lt;name_1&gt;&#x3D;&lt;value_1&gt;,..,&lt;name_n&gt;&#x3D;&lt;value_n&gt;]\&quot; (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription&#39;s url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content | [optional] |

### Return type

[**\OpenAPI\Client\Model\SupplierInvoiceDto[]**](../Model/SupplierInvoiceDto.md)

### Authorization

[serviceapi](../../README.md#serviceapi)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `supplierInvoiceGetByApprovalDocumentId()`

```php
supplierInvoiceGetByApprovalDocumentId($system_id, $erp_api_background): \OpenAPI\Client\Model\SupplierInvoiceDto
```

Get an invoice based on the systemId. SystemID is used for approving supplier invoices

Data for a single invoice. <br></br>  The response headers include an ETag after a successful GET operation.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SupplierInvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$system_id = 'system_id_example'; // string | SystemID referes to the approval document id created when the document is sent to approval
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->supplierInvoiceGetByApprovalDocumentId($system_id, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SupplierInvoiceApi->supplierInvoiceGetByApprovalDocumentId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **system_id** | **string**| SystemID referes to the approval document id created when the document is sent to approval | |
| **erp_api_background** | **string**| Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \&quot;none\&quot; (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \&quot;subscription[:&lt;name_1&gt;&#x3D;&lt;value_1&gt;,..,&lt;name_n&gt;&#x3D;&lt;value_n&gt;]\&quot; (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription&#39;s url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content | [optional] |

### Return type

[**\OpenAPI\Client\Model\SupplierInvoiceDto**](../Model/SupplierInvoiceDto.md)

### Authorization

[serviceapi](../../README.md#serviceapi)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `supplierInvoiceGetByTypeBydocumentTypeinvoiceNumber()`

```php
supplierInvoiceGetByTypeBydocumentTypeinvoiceNumber($document_type, $invoice_number, $expand_line_prebook_accounts, $expand_landed_costs, $erp_api_background): \OpenAPI\Client\Model\SupplierInvoiceDto
```

Get a specific Invoice, DebitAdj, CreditAdj or Prepayment

Data for a single invoice. <br></br>  The response headers include an ETag after a successful GET operation.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SupplierInvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$document_type = 'document_type_example'; // string | Identifies the Invoice
$invoice_number = 'invoice_number_example'; // string | Identifies the Invoice
$expand_line_prebook_accounts = True; // bool | Expland line-level pre-booking account and sub-account information.
$expand_landed_costs = True; // bool | Expland landed costs information.
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->supplierInvoiceGetByTypeBydocumentTypeinvoiceNumber($document_type, $invoice_number, $expand_line_prebook_accounts, $expand_landed_costs, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SupplierInvoiceApi->supplierInvoiceGetByTypeBydocumentTypeinvoiceNumber: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **document_type** | **string**| Identifies the Invoice | |
| **invoice_number** | **string**| Identifies the Invoice | |
| **expand_line_prebook_accounts** | **bool**| Expland line-level pre-booking account and sub-account information. | [optional] |
| **expand_landed_costs** | **bool**| Expland landed costs information. | [optional] |
| **erp_api_background** | **string**| Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \&quot;none\&quot; (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \&quot;subscription[:&lt;name_1&gt;&#x3D;&lt;value_1&gt;,..,&lt;name_n&gt;&#x3D;&lt;value_n&gt;]\&quot; (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription&#39;s url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content | [optional] |

### Return type

[**\OpenAPI\Client\Model\SupplierInvoiceDto**](../Model/SupplierInvoiceDto.md)

### Authorization

[serviceapi](../../README.md#serviceapi)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `supplierInvoiceGetByinvoiceNumber()`

```php
supplierInvoiceGetByinvoiceNumber($invoice_number, $expand_line_prebook_accounts, $expand_landed_costs, $erp_api_background): \OpenAPI\Client\Model\SupplierInvoiceDto
```

GET a specific invoice. Only standard invoices are supported. Credit adjustments, credit notes or Prepayments are excluded.

Data for a single invoice. <br></br>  The response headers include an ETag after a successful GET operation.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SupplierInvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$invoice_number = 'invoice_number_example'; // string | Identifies the Invoice
$expand_line_prebook_accounts = True; // bool | Expland line-level pre-booking account and sub-account information.
$expand_landed_costs = True; // bool | Expland landed costs information.
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->supplierInvoiceGetByinvoiceNumber($invoice_number, $expand_line_prebook_accounts, $expand_landed_costs, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SupplierInvoiceApi->supplierInvoiceGetByinvoiceNumber: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invoice_number** | **string**| Identifies the Invoice | |
| **expand_line_prebook_accounts** | **bool**| Expland line-level pre-booking account and sub-account information. | [optional] |
| **expand_landed_costs** | **bool**| Expland landed costs information. | [optional] |
| **erp_api_background** | **string**| Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \&quot;none\&quot; (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \&quot;subscription[:&lt;name_1&gt;&#x3D;&lt;value_1&gt;,..,&lt;name_n&gt;&#x3D;&lt;value_n&gt;]\&quot; (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription&#39;s url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content | [optional] |

### Return type

[**\OpenAPI\Client\Model\SupplierInvoiceDto**](../Model/SupplierInvoiceDto.md)

### Authorization

[serviceapi](../../README.md#serviceapi)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `supplierInvoicePost()`

```php
supplierInvoicePost($supplier_invoice_update_dto, $erp_api_background): object
```

Create an SupplierInvoice

Response Message has StatusCode Created if POST operation succeed.<br></br>  Response Message has StatusCode BadRequest or InternalServerError if POST operation failed.<br></br>  The response headers include an ETag after a successful POST operation.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SupplierInvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$supplier_invoice_update_dto = new \OpenAPI\Client\Model\SupplierInvoiceUpdateDto(); // \OpenAPI\Client\Model\SupplierInvoiceUpdateDto | Defines the data for the SupplierInvoice to create
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->supplierInvoicePost($supplier_invoice_update_dto, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SupplierInvoiceApi->supplierInvoicePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **supplier_invoice_update_dto** | [**\OpenAPI\Client\Model\SupplierInvoiceUpdateDto**](../Model/SupplierInvoiceUpdateDto.md)| Defines the data for the SupplierInvoice to create | |
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

## `supplierInvoicePrebookInvoiceBydocumentTypeinvoiceNumber()`

```php
supplierInvoicePrebookInvoiceBydocumentTypeinvoiceNumber($document_type, $invoice_number, $prebooking_update_dto, $erp_api_background, $if_match): \OpenAPI\Client\Model\BackgroundApiAcceptedDto
```

Pre-Book invoice operation

The action result dto contains information about the result of running the action. <br></br>  Response Message has StatusCode BadRequest or InternalServerError if POST operation failed. <br></br>  In this endpoint, If-Match can be checked against resource current version when calling with 'erp-api-background' HTTP header.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SupplierInvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$document_type = 'document_type_example'; // string | Document type of the document to be Pre-Booked
$invoice_number = 'invoice_number_example'; // string | Reference number of the document to be Pre-Booked
$prebooking_update_dto = new \OpenAPI\Client\Model\PrebookingUpdateDto(); // \OpenAPI\Client\Model\PrebookingUpdateDto | Optional dto for updating the prebooking account and subaccount
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content
$if_match = 'if_match_example'; // string | The If-Match HTTP header allows clients to update a resource only if its current version matches a specific ETag. This mechanism helps prevent conflicts when multiple clients attempt to modify the same resource simultaneously. The If-Match header should be included in the request headers using the following syntax: If-Match: \"etag_value\" * If the POST operation is successful, the server responds with 200 OK and includes the new ETag value in the response headers. * If the ETag on the server does not match the value provided in the If-Match header, the server responds with 412 Precondition Failed.

try {
    $result = $apiInstance->supplierInvoicePrebookInvoiceBydocumentTypeinvoiceNumber($document_type, $invoice_number, $prebooking_update_dto, $erp_api_background, $if_match);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SupplierInvoiceApi->supplierInvoicePrebookInvoiceBydocumentTypeinvoiceNumber: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **document_type** | **string**| Document type of the document to be Pre-Booked | |
| **invoice_number** | **string**| Reference number of the document to be Pre-Booked | |
| **prebooking_update_dto** | [**\OpenAPI\Client\Model\PrebookingUpdateDto**](../Model/PrebookingUpdateDto.md)| Optional dto for updating the prebooking account and subaccount | |
| **erp_api_background** | **string**| Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \&quot;none\&quot; (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \&quot;subscription[:&lt;name_1&gt;&#x3D;&lt;value_1&gt;,..,&lt;name_n&gt;&#x3D;&lt;value_n&gt;]\&quot; (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription&#39;s url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content | [optional] |
| **if_match** | **string**| The If-Match HTTP header allows clients to update a resource only if its current version matches a specific ETag. This mechanism helps prevent conflicts when multiple clients attempt to modify the same resource simultaneously. The If-Match header should be included in the request headers using the following syntax: If-Match: \&quot;etag_value\&quot; * If the POST operation is successful, the server responds with 200 OK and includes the new ETag value in the response headers. * If the ETag on the server does not match the value provided in the If-Match header, the server responds with 412 Precondition Failed. | [optional] |

### Return type

[**\OpenAPI\Client\Model\BackgroundApiAcceptedDto**](../Model/BackgroundApiAcceptedDto.md)

### Authorization

[serviceapi](../../README.md#serviceapi)

### HTTP request headers

- **Content-Type**: `application/json`, `text/json`, `application/xml`, `text/xml`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`, `text/json`, `application/xml`, `text/xml`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `supplierInvoicePutByTypeBydocumentTypeinvoiceNumber()`

```php
supplierInvoicePutByTypeBydocumentTypeinvoiceNumber($document_type, $invoice_number, $supplier_invoice_update_dto, $erp_api_background, $if_match): \OpenAPI\Client\Model\BackgroundApiAcceptedDto
```

Update a specific SupplierInvoice

Response Message has StatusCode NoContent if PUT operation succeed. <br></br>  Response Message has StatusCode BadRequest if PUT operation failed. <br></br>  The response headers include an ETag after a successful PUT operation.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SupplierInvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$document_type = 'document_type_example'; // string | Identifies the SupplierInvoice to update
$invoice_number = 'invoice_number_example'; // string | Identifies the SupplierInvoice to update
$supplier_invoice_update_dto = new \OpenAPI\Client\Model\SupplierInvoiceUpdateDto(); // \OpenAPI\Client\Model\SupplierInvoiceUpdateDto | Defines the data for the Invoice to update
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content
$if_match = 'if_match_example'; // string | The If-Match HTTP header allows clients to update a resource only if its current version matches a specific ETag. This mechanism helps prevent conflicts when multiple clients attempt to modify the same resource simultaneously. The If-Match header should be included in the request headers using the following syntax: If-Match: \"etag_value\" * If the update is successful, the server responds with 204 No Content and includes the new ETag value in the response headers. * If the ETag on the server does not match the value provided in the If-Match header, the server responds with 412 Precondition Failed.

try {
    $result = $apiInstance->supplierInvoicePutByTypeBydocumentTypeinvoiceNumber($document_type, $invoice_number, $supplier_invoice_update_dto, $erp_api_background, $if_match);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SupplierInvoiceApi->supplierInvoicePutByTypeBydocumentTypeinvoiceNumber: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **document_type** | **string**| Identifies the SupplierInvoice to update | |
| **invoice_number** | **string**| Identifies the SupplierInvoice to update | |
| **supplier_invoice_update_dto** | [**\OpenAPI\Client\Model\SupplierInvoiceUpdateDto**](../Model/SupplierInvoiceUpdateDto.md)| Defines the data for the Invoice to update | |
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

## `supplierInvoicePutByinvoiceNumber()`

```php
supplierInvoicePutByinvoiceNumber($invoice_number, $supplier_invoice_update_dto, $erp_api_background, $if_match): \OpenAPI\Client\Model\BackgroundApiAcceptedDto
```

Update a specific SupplierInvoice

Response Message has StatusCode NoContent if PUT operation succeed. <br></br>  Response Message has StatusCode BadRequest if PUT operation failed. <br></br>  The response headers include an ETag after a successful PUT operation.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SupplierInvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$invoice_number = 'invoice_number_example'; // string | Identifies the SupplierInvoice to update
$supplier_invoice_update_dto = new \OpenAPI\Client\Model\SupplierInvoiceUpdateDto(); // \OpenAPI\Client\Model\SupplierInvoiceUpdateDto | Defines the data for the Invoice to update
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content
$if_match = 'if_match_example'; // string | The If-Match HTTP header allows clients to update a resource only if its current version matches a specific ETag. This mechanism helps prevent conflicts when multiple clients attempt to modify the same resource simultaneously. The If-Match header should be included in the request headers using the following syntax: If-Match: \"etag_value\" * If the update is successful, the server responds with 204 No Content and includes the new ETag value in the response headers. * If the ETag on the server does not match the value provided in the If-Match header, the server responds with 412 Precondition Failed.

try {
    $result = $apiInstance->supplierInvoicePutByinvoiceNumber($invoice_number, $supplier_invoice_update_dto, $erp_api_background, $if_match);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SupplierInvoiceApi->supplierInvoicePutByinvoiceNumber: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invoice_number** | **string**| Identifies the SupplierInvoice to update | |
| **supplier_invoice_update_dto** | [**\OpenAPI\Client\Model\SupplierInvoiceUpdateDto**](../Model/SupplierInvoiceUpdateDto.md)| Defines the data for the Invoice to update | |
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

## `supplierInvoiceReleaseInvoiceByTypeBydocumentTypeinvoiceNumber()`

```php
supplierInvoiceReleaseInvoiceByTypeBydocumentTypeinvoiceNumber($document_type, $invoice_number, $erp_api_background, $if_match): \OpenAPI\Client\Model\BackgroundApiAcceptedDto
```

Release invoice operation

The action result dto contains information about the result of running the action. <br></br>  Response Message has StatusCode BadRequest or InternalServerError if POST operation failed. <br></br>  In this endpoint, If-Match can be checked against resource current version when calling with 'erp-api-background' HTTP header.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SupplierInvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$document_type = 'document_type_example'; // string | Document type of the released document to be reversed
$invoice_number = 'invoice_number_example'; // string | Reference number of the document to be release
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content
$if_match = 'if_match_example'; // string | The If-Match HTTP header allows clients to update a resource only if its current version matches a specific ETag. This mechanism helps prevent conflicts when multiple clients attempt to modify the same resource simultaneously. The If-Match header should be included in the request headers using the following syntax: If-Match: \"etag_value\" * If the POST operation is successful, the server responds with 200 OK and includes the new ETag value in the response headers. * If the ETag on the server does not match the value provided in the If-Match header, the server responds with 412 Precondition Failed.

try {
    $result = $apiInstance->supplierInvoiceReleaseInvoiceByTypeBydocumentTypeinvoiceNumber($document_type, $invoice_number, $erp_api_background, $if_match);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SupplierInvoiceApi->supplierInvoiceReleaseInvoiceByTypeBydocumentTypeinvoiceNumber: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **document_type** | **string**| Document type of the released document to be reversed | |
| **invoice_number** | **string**| Reference number of the document to be release | |
| **erp_api_background** | **string**| Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \&quot;none\&quot; (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \&quot;subscription[:&lt;name_1&gt;&#x3D;&lt;value_1&gt;,..,&lt;name_n&gt;&#x3D;&lt;value_n&gt;]\&quot; (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription&#39;s url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content | [optional] |
| **if_match** | **string**| The If-Match HTTP header allows clients to update a resource only if its current version matches a specific ETag. This mechanism helps prevent conflicts when multiple clients attempt to modify the same resource simultaneously. The If-Match header should be included in the request headers using the following syntax: If-Match: \&quot;etag_value\&quot; * If the POST operation is successful, the server responds with 200 OK and includes the new ETag value in the response headers. * If the ETag on the server does not match the value provided in the If-Match header, the server responds with 412 Precondition Failed. | [optional] |

### Return type

[**\OpenAPI\Client\Model\BackgroundApiAcceptedDto**](../Model/BackgroundApiAcceptedDto.md)

### Authorization

[serviceapi](../../README.md#serviceapi)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `text/json`, `application/xml`, `text/xml`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `supplierInvoiceReleaseInvoiceByinvoiceNumber()`

```php
supplierInvoiceReleaseInvoiceByinvoiceNumber($invoice_number, $erp_api_background, $if_match): \OpenAPI\Client\Model\BackgroundApiAcceptedDto
```

Release invoice operation

The action result dto contains information about the result of running the action. <br></br>  Response Message has StatusCode BadRequest or InternalServerError if POST operation failed. <br></br>  In this endpoint, If-Match can be checked against resource current version when calling with 'erp-api-background' HTTP header.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SupplierInvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$invoice_number = 'invoice_number_example'; // string | Reference number of the document to be release
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content
$if_match = 'if_match_example'; // string | The If-Match HTTP header allows clients to update a resource only if its current version matches a specific ETag. This mechanism helps prevent conflicts when multiple clients attempt to modify the same resource simultaneously. The If-Match header should be included in the request headers using the following syntax: If-Match: \"etag_value\" * If the POST operation is successful, the server responds with 200 OK and includes the new ETag value in the response headers. * If the ETag on the server does not match the value provided in the If-Match header, the server responds with 412 Precondition Failed.

try {
    $result = $apiInstance->supplierInvoiceReleaseInvoiceByinvoiceNumber($invoice_number, $erp_api_background, $if_match);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SupplierInvoiceApi->supplierInvoiceReleaseInvoiceByinvoiceNumber: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invoice_number** | **string**| Reference number of the document to be release | |
| **erp_api_background** | **string**| Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \&quot;none\&quot; (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \&quot;subscription[:&lt;name_1&gt;&#x3D;&lt;value_1&gt;,..,&lt;name_n&gt;&#x3D;&lt;value_n&gt;]\&quot; (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription&#39;s url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content | [optional] |
| **if_match** | **string**| The If-Match HTTP header allows clients to update a resource only if its current version matches a specific ETag. This mechanism helps prevent conflicts when multiple clients attempt to modify the same resource simultaneously. The If-Match header should be included in the request headers using the following syntax: If-Match: \&quot;etag_value\&quot; * If the POST operation is successful, the server responds with 200 OK and includes the new ETag value in the response headers. * If the ETag on the server does not match the value provided in the If-Match header, the server responds with 412 Precondition Failed. | [optional] |

### Return type

[**\OpenAPI\Client\Model\BackgroundApiAcceptedDto**](../Model/BackgroundApiAcceptedDto.md)

### Authorization

[serviceapi](../../README.md#serviceapi)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `text/json`, `application/xml`, `text/xml`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `supplierInvoiceReverseInvoiceBydocumentTypeinvoiceNumber()`

```php
supplierInvoiceReverseInvoiceBydocumentTypeinvoiceNumber($document_type, $invoice_number, $erp_api_background, $if_match): \OpenAPI\Client\Model\BackgroundApiAcceptedDto
```

Provides an action for reversing a supplier invoice/adjustment

The response headers include an ETag after a successful POST operation.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SupplierInvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$document_type = 'document_type_example'; // string | Identifies the Invoice
$invoice_number = 'invoice_number_example'; // string | Identifies the Invoice
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content
$if_match = 'if_match_example'; // string | The If-Match HTTP header allows clients to update a resource only if its current version matches a specific ETag. This mechanism helps prevent conflicts when multiple clients attempt to modify the same resource simultaneously. The If-Match header should be included in the request headers using the following syntax: If-Match: \"etag_value\" * If the POST operation is successful, the server responds with 200 OK and includes the new ETag value in the response headers. * If the ETag on the server does not match the value provided in the If-Match header, the server responds with 412 Precondition Failed.

try {
    $result = $apiInstance->supplierInvoiceReverseInvoiceBydocumentTypeinvoiceNumber($document_type, $invoice_number, $erp_api_background, $if_match);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SupplierInvoiceApi->supplierInvoiceReverseInvoiceBydocumentTypeinvoiceNumber: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **document_type** | **string**| Identifies the Invoice | |
| **invoice_number** | **string**| Identifies the Invoice | |
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

## `supplierInvoiceSendToApprovalBydocumentTypeinvoiceNumber()`

```php
supplierInvoiceSendToApprovalBydocumentTypeinvoiceNumber($document_type, $invoice_number, $erp_api_background, $if_match): \OpenAPI\Client\Model\BackgroundApiAcceptedDto
```

Send invoice to approval

In this endpoint, If-Match can be checked against resource current version when calling with 'erp-api-background' HTTP header.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SupplierInvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$document_type = 'document_type_example'; // string | Document type
$invoice_number = 'invoice_number_example'; // string | Document number
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content
$if_match = 'if_match_example'; // string | The If-Match HTTP header allows clients to update a resource only if its current version matches a specific ETag. This mechanism helps prevent conflicts when multiple clients attempt to modify the same resource simultaneously. The If-Match header should be included in the request headers using the following syntax: If-Match: \"etag_value\" * If the POST operation is successful, the server responds with 200 OK and includes the new ETag value in the response headers. * If the ETag on the server does not match the value provided in the If-Match header, the server responds with 412 Precondition Failed.

try {
    $result = $apiInstance->supplierInvoiceSendToApprovalBydocumentTypeinvoiceNumber($document_type, $invoice_number, $erp_api_background, $if_match);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SupplierInvoiceApi->supplierInvoiceSendToApprovalBydocumentTypeinvoiceNumber: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **document_type** | **string**| Document type | |
| **invoice_number** | **string**| Document number | |
| **erp_api_background** | **string**| Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \&quot;none\&quot; (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \&quot;subscription[:&lt;name_1&gt;&#x3D;&lt;value_1&gt;,..,&lt;name_n&gt;&#x3D;&lt;value_n&gt;]\&quot; (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription&#39;s url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content | [optional] |
| **if_match** | **string**| The If-Match HTTP header allows clients to update a resource only if its current version matches a specific ETag. This mechanism helps prevent conflicts when multiple clients attempt to modify the same resource simultaneously. The If-Match header should be included in the request headers using the following syntax: If-Match: \&quot;etag_value\&quot; * If the POST operation is successful, the server responds with 200 OK and includes the new ETag value in the response headers. * If the ETag on the server does not match the value provided in the If-Match header, the server responds with 412 Precondition Failed. | [optional] |

### Return type

[**\OpenAPI\Client\Model\BackgroundApiAcceptedDto**](../Model/BackgroundApiAcceptedDto.md)

### Authorization

[serviceapi](../../README.md#serviceapi)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `text/json`, `application/xml`, `text/xml`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `supplierInvoiceVoidInvoiceBydocumentTypeinvoiceNumber()`

```php
supplierInvoiceVoidInvoiceBydocumentTypeinvoiceNumber($document_type, $invoice_number, $erp_api_background, $if_match): \OpenAPI\Client\Model\BackgroundApiAcceptedDto
```

Void invoice operation

The action result dto contains information about the result of running the action. <br></br>  Response Message has StatusCode BadRequest or InternalServerError if POST operation failed. <br></br>  In this endpoint, If-Match can be checked against resource current version when calling with 'erp-api-background' HTTP header.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SupplierInvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$document_type = 'document_type_example'; // string | Document type of the document to be Voided
$invoice_number = 'invoice_number_example'; // string | Reference number of the document to be Voided
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content
$if_match = 'if_match_example'; // string | The If-Match HTTP header allows clients to update a resource only if its current version matches a specific ETag. This mechanism helps prevent conflicts when multiple clients attempt to modify the same resource simultaneously. The If-Match header should be included in the request headers using the following syntax: If-Match: \"etag_value\" * If the POST operation is successful, the server responds with 200 OK and includes the new ETag value in the response headers. * If the ETag on the server does not match the value provided in the If-Match header, the server responds with 412 Precondition Failed.

try {
    $result = $apiInstance->supplierInvoiceVoidInvoiceBydocumentTypeinvoiceNumber($document_type, $invoice_number, $erp_api_background, $if_match);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SupplierInvoiceApi->supplierInvoiceVoidInvoiceBydocumentTypeinvoiceNumber: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **document_type** | **string**| Document type of the document to be Voided | |
| **invoice_number** | **string**| Reference number of the document to be Voided | |
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

## `supplierInvoiceWriteoffInvoiceBydocumentTypeinvoiceNumber()`

```php
supplierInvoiceWriteoffInvoiceBydocumentTypeinvoiceNumber($document_type, $invoice_number, $erp_api_background, $if_match): \OpenAPI\Client\Model\BackgroundApiAcceptedDto
```

Write-off invoice operation

The action result dto contains information about the result of running the action. <br></br>  Response Message has StatusCode BadRequest or InternalServerError if POST operation failed. <br></br>  In this endpoint, If-Match can be checked against resource current version when calling with 'erp-api-background' HTTP header.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SupplierInvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$document_type = 'document_type_example'; // string | Document type of the document to be Written Off
$invoice_number = 'invoice_number_example'; // string | Reference number of the document to be Written Off
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content
$if_match = 'if_match_example'; // string | The If-Match HTTP header allows clients to update a resource only if its current version matches a specific ETag. This mechanism helps prevent conflicts when multiple clients attempt to modify the same resource simultaneously. The If-Match header should be included in the request headers using the following syntax: If-Match: \"etag_value\" * If the POST operation is successful, the server responds with 200 OK and includes the new ETag value in the response headers. * If the ETag on the server does not match the value provided in the If-Match header, the server responds with 412 Precondition Failed.

try {
    $result = $apiInstance->supplierInvoiceWriteoffInvoiceBydocumentTypeinvoiceNumber($document_type, $invoice_number, $erp_api_background, $if_match);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SupplierInvoiceApi->supplierInvoiceWriteoffInvoiceBydocumentTypeinvoiceNumber: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **document_type** | **string**| Document type of the document to be Written Off | |
| **invoice_number** | **string**| Reference number of the document to be Written Off | |
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

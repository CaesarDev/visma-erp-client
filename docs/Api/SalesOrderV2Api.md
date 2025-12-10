# OpenAPI\Client\SalesOrderV2Api



All URIs are relative to https://api.finance.visma.net, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**salesOrderV2CancelSalesOrderBysaleOrderNumber()**](SalesOrderV2Api.md#salesOrderV2CancelSalesOrderBysaleOrderNumber) | **POST** /v2/salesorder/{saleOrderNumber}/action/cancelSalesOrder | Cancel Order action |
| [**salesOrderV2CreateHeaderAttachmentByorderNumber()**](SalesOrderV2Api.md#salesOrderV2CreateHeaderAttachmentByorderNumber) | **POST** /v2/salesorder/{orderNumber}/attachment | Creates an attachment and associates it with a sales order. If the file already exists, a new revision is created.  - Method is deprecated and will be removed in a future version. Please start using the new method with order type. |
| [**salesOrderV2CreateHeaderAttachmentByorderNumberorderType()**](SalesOrderV2Api.md#salesOrderV2CreateHeaderAttachmentByorderNumberorderType) | **POST** /v2/salesorder/orderType/{orderType}/{orderNumber}/attachment | Creates an attachment and associates it with a sales order on a specific order type. If the file already exists, a new revision is created. |
| [**salesOrderV2CreateLineAttachmentByorderNumberlineNumber()**](SalesOrderV2Api.md#salesOrderV2CreateLineAttachmentByorderNumberlineNumber) | **POST** /v2/salesorder/{orderNumber}/{lineNumber}/attachment | Creates an attachment and associates it with a certain sales order line. If the file already exists, a new revision is created.  - Method is deprecated and will be removed in a future version. Please start using the new method with order type. |
| [**salesOrderV2CreateLineAttachmentByorderNumberorderTypelineNumber()**](SalesOrderV2Api.md#salesOrderV2CreateLineAttachmentByorderNumberorderTypelineNumber) | **POST** /v2/salesorder/orderType/{orderType}/{orderNumber}/{lineNumber}/attachment | Creates an attachment and associates it with a certain sales order line on a specific order type. If the file already exists, a new revision is created. |
| [**salesOrderV2CreatePurchaseOrdersActionBysaleOrderNumber()**](SalesOrderV2Api.md#salesOrderV2CreatePurchaseOrdersActionBysaleOrderNumber) | **POST** /v2/salesorder/{saleOrderNumber}/action/createPurchaseOrders | This will create 0..n PO based on SO according to the following rules for the lines on the SO  - Only issue lines  - Only create PO based on lines with supplier  - Create PO (0..n) for each supplier on the SO lines  - Create PO type purchase/drop shipment based on PO Source on SO line  - If no supplier on inventory item exist the SO line will not have a corresponding PO line (response should point to lines with no supplier in either SO line or inventory item)  - If &#39;createPurchaseOrderActionDto.preferSupplierFromSOLine&#39; is false then the default supplier for SOLine inventory item will be used if any  - If &#39;createPurchaseOrderActionDto.preferSupplierFromSOLine&#39; is true then the supplier from the SOLine inventory item will be used; if there is no supplier on SOLine then the default supplier for SOLine inventory item will be used if any |
| [**salesOrderV2CreateShipmentActionBysaleOrderNumber()**](SalesOrderV2Api.md#salesOrderV2CreateShipmentActionBysaleOrderNumber) | **POST** /v2/salesorder/{saleOrderNumber}/action/createShipment | Create shipment operation |
| [**salesOrderV2GetAllOrdersV2()**](SalesOrderV2Api.md#salesOrderV2GetAllOrdersV2) | **GET** /v2/salesorder | Get a range of SO Orders - ScreenId&#x3D;SO301000  Request page size must be lower or equal to the allowed max page size which is returned as part of the metadata information.  If requested page size is greater than allowed max page size, request will be limited to max page size |
| [**salesOrderV2GetByorderNbr()**](SalesOrderV2Api.md#salesOrderV2GetByorderNbr) | **GET** /v2/salesorder/{orderNbr} | Get a specific SO Order |
| [**salesOrderV2Post()**](SalesOrderV2Api.md#salesOrderV2Post) | **POST** /v2/salesorder | Create a Sale Order |
| [**salesOrderV2PrepareInvoiceActionByorderTypeorderNumber()**](SalesOrderV2Api.md#salesOrderV2PrepareInvoiceActionByorderTypeorderNumber) | **POST** /v2/salesorder/{orderType}/{orderNumber}/action/prepareInvoice | Prepare Invoice operation |
| [**salesOrderV2ReopenSalesOrderBysalesOrderNumber()**](SalesOrderV2Api.md#salesOrderV2ReopenSalesOrderBysalesOrderNumber) | **POST** /v2/salesorder/{salesOrderNumber}/action/reopenSalesOrder | Reopen and update a specific Sales Order. This method requires a sales order update dto where the order type is initialised. |
| [**salesOrderV2SendEmailActionByorderTypeorderNumber()**](SalesOrderV2Api.md#salesOrderV2SendEmailActionByorderTypeorderNumber) | **POST** /v2/salesorder/{orderType}/{orderNumber}/action/sendbymail | Send by mail operation |


## `salesOrderV2CancelSalesOrderBysaleOrderNumber()`

```php
salesOrderV2CancelSalesOrderBysaleOrderNumber($sale_order_number, $cancel_sales_order_action_dto, $erp_api_background): \OpenAPI\Client\Model\CancelSalesOrderActionResultDto
```

Cancel Order action

The action result dto contains information about the result of running the action

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SalesOrderV2Api(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sale_order_number = 'sale_order_number_example'; // string | Reference number of the sale oreder that will be cancelled
$cancel_sales_order_action_dto = new \OpenAPI\Client\Model\CancelSalesOrderActionDto(); // \OpenAPI\Client\Model\CancelSalesOrderActionDto | Defines the data for the action
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->salesOrderV2CancelSalesOrderBysaleOrderNumber($sale_order_number, $cancel_sales_order_action_dto, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SalesOrderV2Api->salesOrderV2CancelSalesOrderBysaleOrderNumber: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sale_order_number** | **string**| Reference number of the sale oreder that will be cancelled | |
| **cancel_sales_order_action_dto** | [**\OpenAPI\Client\Model\CancelSalesOrderActionDto**](../Model/CancelSalesOrderActionDto.md)| Defines the data for the action | |
| **erp_api_background** | **string**| Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \&quot;none\&quot; (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \&quot;subscription[:&lt;name_1&gt;&#x3D;&lt;value_1&gt;,..,&lt;name_n&gt;&#x3D;&lt;value_n&gt;]\&quot; (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription&#39;s url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content | [optional] |

### Return type

[**\OpenAPI\Client\Model\CancelSalesOrderActionResultDto**](../Model/CancelSalesOrderActionResultDto.md)

### Authorization

[serviceapi](../../README.md#serviceapi)

### HTTP request headers

- **Content-Type**: `application/json`, `text/json`, `application/xml`, `text/xml`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`, `text/json`, `application/xml`, `text/xml`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `salesOrderV2CreateHeaderAttachmentByorderNumber()`

```php
salesOrderV2CreateHeaderAttachmentByorderNumber($order_number, $erp_api_background): object
```

Creates an attachment and associates it with a sales order. If the file already exists, a new revision is created.  - Method is deprecated and will be removed in a future version. Please start using the new method with order type.

Response Message has StatusCode Created if POST operation succeed

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SalesOrderV2Api(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$order_number = 'order_number_example'; // string | Identifies the sales order
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->salesOrderV2CreateHeaderAttachmentByorderNumber($order_number, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SalesOrderV2Api->salesOrderV2CreateHeaderAttachmentByorderNumber: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **order_number** | **string**| Identifies the sales order | |
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

## `salesOrderV2CreateHeaderAttachmentByorderNumberorderType()`

```php
salesOrderV2CreateHeaderAttachmentByorderNumberorderType($order_number, $order_type, $erp_api_background): object
```

Creates an attachment and associates it with a sales order on a specific order type. If the file already exists, a new revision is created.

Response Message has StatusCode Created if POST operation succeed

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SalesOrderV2Api(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$order_number = 'order_number_example'; // string | Identifies the sales order
$order_type = 'order_type_example'; // string | 
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->salesOrderV2CreateHeaderAttachmentByorderNumberorderType($order_number, $order_type, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SalesOrderV2Api->salesOrderV2CreateHeaderAttachmentByorderNumberorderType: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **order_number** | **string**| Identifies the sales order | |
| **order_type** | **string**|  | |
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

## `salesOrderV2CreateLineAttachmentByorderNumberlineNumber()`

```php
salesOrderV2CreateLineAttachmentByorderNumberlineNumber($order_number, $line_number, $erp_api_background): object
```

Creates an attachment and associates it with a certain sales order line. If the file already exists, a new revision is created.  - Method is deprecated and will be removed in a future version. Please start using the new method with order type.

Response Message has StatusCode Created if POST operation succeed

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SalesOrderV2Api(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$order_number = 'order_number_example'; // string | Identifies the sales order
$line_number = 56; // int | Specifies line number
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->salesOrderV2CreateLineAttachmentByorderNumberlineNumber($order_number, $line_number, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SalesOrderV2Api->salesOrderV2CreateLineAttachmentByorderNumberlineNumber: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **order_number** | **string**| Identifies the sales order | |
| **line_number** | **int**| Specifies line number | |
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

## `salesOrderV2CreateLineAttachmentByorderNumberorderTypelineNumber()`

```php
salesOrderV2CreateLineAttachmentByorderNumberorderTypelineNumber($order_number, $order_type, $line_number, $erp_api_background): object
```

Creates an attachment and associates it with a certain sales order line on a specific order type. If the file already exists, a new revision is created.

Response Message has StatusCode Created if POST operation succeed

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SalesOrderV2Api(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$order_number = 'order_number_example'; // string | Identifies the sales order
$order_type = 'order_type_example'; // string | 
$line_number = 56; // int | Specifies line number
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->salesOrderV2CreateLineAttachmentByorderNumberorderTypelineNumber($order_number, $order_type, $line_number, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SalesOrderV2Api->salesOrderV2CreateLineAttachmentByorderNumberorderTypelineNumber: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **order_number** | **string**| Identifies the sales order | |
| **order_type** | **string**|  | |
| **line_number** | **int**| Specifies line number | |
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

## `salesOrderV2CreatePurchaseOrdersActionBysaleOrderNumber()`

```php
salesOrderV2CreatePurchaseOrdersActionBysaleOrderNumber($sale_order_number, $create_purchase_order_action_dto, $erp_api_background): object
```

This will create 0..n PO based on SO according to the following rules for the lines on the SO  - Only issue lines  - Only create PO based on lines with supplier  - Create PO (0..n) for each supplier on the SO lines  - Create PO type purchase/drop shipment based on PO Source on SO line  - If no supplier on inventory item exist the SO line will not have a corresponding PO line (response should point to lines with no supplier in either SO line or inventory item)  - If 'createPurchaseOrderActionDto.preferSupplierFromSOLine' is false then the default supplier for SOLine inventory item will be used if any  - If 'createPurchaseOrderActionDto.preferSupplierFromSOLine' is true then the supplier from the SOLine inventory item will be used; if there is no supplier on SOLine then the default supplier for SOLine inventory item will be used if any

The action result dto contains list of created purchase order numbers and list of errors if any

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SalesOrderV2Api(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sale_order_number = 'sale_order_number_example'; // string | Reference number of the sale oreder from which the purchase order will be created
$create_purchase_order_action_dto = new \OpenAPI\Client\Model\CreatePurchaseOrderActionDto(); // \OpenAPI\Client\Model\CreatePurchaseOrderActionDto | Defines the data for the action
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->salesOrderV2CreatePurchaseOrdersActionBysaleOrderNumber($sale_order_number, $create_purchase_order_action_dto, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SalesOrderV2Api->salesOrderV2CreatePurchaseOrdersActionBysaleOrderNumber: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sale_order_number** | **string**| Reference number of the sale oreder from which the purchase order will be created | |
| **create_purchase_order_action_dto** | [**\OpenAPI\Client\Model\CreatePurchaseOrderActionDto**](../Model/CreatePurchaseOrderActionDto.md)| Defines the data for the action | |
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

## `salesOrderV2CreateShipmentActionBysaleOrderNumber()`

```php
salesOrderV2CreateShipmentActionBysaleOrderNumber($sale_order_number, $create_shipment_action_dto, $erp_api_background): \OpenAPI\Client\Model\BackgroundApiAcceptedDto
```

Create shipment operation

The action result dto contains information about the result of running the action

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SalesOrderV2Api(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sale_order_number = 'sale_order_number_example'; // string | Reference number of the sale oreder from which the shipment will be created
$create_shipment_action_dto = new \OpenAPI\Client\Model\CreateShipmentActionDto(); // \OpenAPI\Client\Model\CreateShipmentActionDto | Defines the data for the action
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->salesOrderV2CreateShipmentActionBysaleOrderNumber($sale_order_number, $create_shipment_action_dto, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SalesOrderV2Api->salesOrderV2CreateShipmentActionBysaleOrderNumber: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sale_order_number** | **string**| Reference number of the sale oreder from which the shipment will be created | |
| **create_shipment_action_dto** | [**\OpenAPI\Client\Model\CreateShipmentActionDto**](../Model/CreateShipmentActionDto.md)| Defines the data for the action | |
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

## `salesOrderV2GetAllOrdersV2()`

```php
salesOrderV2GetAllOrdersV2($order_type, $status, $greater_than_value, $show_notes, $last_modified_date_time, $last_modified_date_time_condition, $page_number, $page_size, $erp_api_background): \OpenAPI\Client\Model\SalesOrderDto[]
```

Get a range of SO Orders - ScreenId=SO301000  Request page size must be lower or equal to the allowed max page size which is returned as part of the metadata information.  If requested page size is greater than allowed max page size, request will be limited to max page size

Data for all Sales Orders

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SalesOrderV2Api(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$order_type = 'order_type_example'; // string | Filter by Order type.
$status = 'status_example'; // string | Select to filter on status on order.
$greater_than_value = 'greater_than_value_example'; // string | Filter on Order no. greater than value.
$show_notes = True; // bool | Set to true to include notes.
$last_modified_date_time = 'last_modified_date_time_example'; // string | This value, generated by the system, indicates the last time the record was modified. Use it to retrieve all records that have been modified since that time, up to the present.    Accepted format:  * ```yyyy-MM-dd```  * ```yyyy-MM-dd HH:mm:ss```  * ```yyyy-MM-dd HH:mm:ss.FFF```  * ```yyyy-MM-ddTHH:mm:ss```  * ```yyyy-MM-ddTHH:mm:ss.FFF```    _Note:_ __LastModifiedDateTime__ and __LastModifiedDateTimeCondition__ are __mutually inclusive__.
$last_modified_date_time_condition = 'last_modified_date_time_condition_example'; // string | This value represents the condition to be applied when retrieving records.    Accepted values (without the single quotes):  * '&gt;' for greater than  * '&lt;' for less than  * '&gt;=' for greater than or equal  * '&lt;=' for less than or equal    _Note:_ __LastModifiedDateTime__ and __LastModifiedDateTimeCondition__ are __mutually inclusive__.
$page_number = 56; // int | Pagination parameter. Page number.
$page_size = 56; // int | Pagination parameter. Number of items to be collected.  Please use a page size lower or equal to the allowed max page size which is returned as part of the metadata information.  If requested page size is greater than allowed max page size, request will be limited to max page size.
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->salesOrderV2GetAllOrdersV2($order_type, $status, $greater_than_value, $show_notes, $last_modified_date_time, $last_modified_date_time_condition, $page_number, $page_size, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SalesOrderV2Api->salesOrderV2GetAllOrdersV2: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **order_type** | **string**| Filter by Order type. | [optional] |
| **status** | **string**| Select to filter on status on order. | [optional] |
| **greater_than_value** | **string**| Filter on Order no. greater than value. | [optional] |
| **show_notes** | **bool**| Set to true to include notes. | [optional] |
| **last_modified_date_time** | **string**| This value, generated by the system, indicates the last time the record was modified. Use it to retrieve all records that have been modified since that time, up to the present.    Accepted format:  * &#x60;&#x60;&#x60;yyyy-MM-dd&#x60;&#x60;&#x60;  * &#x60;&#x60;&#x60;yyyy-MM-dd HH:mm:ss&#x60;&#x60;&#x60;  * &#x60;&#x60;&#x60;yyyy-MM-dd HH:mm:ss.FFF&#x60;&#x60;&#x60;  * &#x60;&#x60;&#x60;yyyy-MM-ddTHH:mm:ss&#x60;&#x60;&#x60;  * &#x60;&#x60;&#x60;yyyy-MM-ddTHH:mm:ss.FFF&#x60;&#x60;&#x60;    _Note:_ __LastModifiedDateTime__ and __LastModifiedDateTimeCondition__ are __mutually inclusive__. | [optional] |
| **last_modified_date_time_condition** | **string**| This value represents the condition to be applied when retrieving records.    Accepted values (without the single quotes):  * &#39;&amp;gt;&#39; for greater than  * &#39;&amp;lt;&#39; for less than  * &#39;&amp;gt;&#x3D;&#39; for greater than or equal  * &#39;&amp;lt;&#x3D;&#39; for less than or equal    _Note:_ __LastModifiedDateTime__ and __LastModifiedDateTimeCondition__ are __mutually inclusive__. | [optional] |
| **page_number** | **int**| Pagination parameter. Page number. | [optional] |
| **page_size** | **int**| Pagination parameter. Number of items to be collected.  Please use a page size lower or equal to the allowed max page size which is returned as part of the metadata information.  If requested page size is greater than allowed max page size, request will be limited to max page size. | [optional] |
| **erp_api_background** | **string**| Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \&quot;none\&quot; (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \&quot;subscription[:&lt;name_1&gt;&#x3D;&lt;value_1&gt;,..,&lt;name_n&gt;&#x3D;&lt;value_n&gt;]\&quot; (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription&#39;s url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content | [optional] |

### Return type

[**\OpenAPI\Client\Model\SalesOrderDto[]**](../Model/SalesOrderDto.md)

### Authorization

[serviceapi](../../README.md#serviceapi)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `salesOrderV2GetByorderNbr()`

```php
salesOrderV2GetByorderNbr($order_nbr, $erp_api_background): \OpenAPI\Client\Model\SalesOrderDto
```

Get a specific SO Order

Data for a single Sales Order

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SalesOrderV2Api(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$order_nbr = 'order_nbr_example'; // string | Identifies the Sales Order Number
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->salesOrderV2GetByorderNbr($order_nbr, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SalesOrderV2Api->salesOrderV2GetByorderNbr: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **order_nbr** | **string**| Identifies the Sales Order Number | |
| **erp_api_background** | **string**| Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \&quot;none\&quot; (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \&quot;subscription[:&lt;name_1&gt;&#x3D;&lt;value_1&gt;,..,&lt;name_n&gt;&#x3D;&lt;value_n&gt;]\&quot; (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription&#39;s url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content | [optional] |

### Return type

[**\OpenAPI\Client\Model\SalesOrderDto**](../Model/SalesOrderDto.md)

### Authorization

[serviceapi](../../README.md#serviceapi)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `salesOrderV2Post()`

```php
salesOrderV2Post($sales_order_update_dto, $erp_api_background): object
```

Create a Sale Order

Response Message has StatusCode Created if POST operation succeed

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SalesOrderV2Api(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sales_order_update_dto = new \OpenAPI\Client\Model\SalesOrderUpdateDto(); // \OpenAPI\Client\Model\SalesOrderUpdateDto | Defines the data for the Sale Order to create
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->salesOrderV2Post($sales_order_update_dto, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SalesOrderV2Api->salesOrderV2Post: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sales_order_update_dto** | [**\OpenAPI\Client\Model\SalesOrderUpdateDto**](../Model/SalesOrderUpdateDto.md)| Defines the data for the Sale Order to create | |
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

## `salesOrderV2PrepareInvoiceActionByorderTypeorderNumber()`

```php
salesOrderV2PrepareInvoiceActionByorderTypeorderNumber($order_type, $order_number, $erp_api_background): \OpenAPI\Client\Model\BackgroundApiAcceptedDto
```

Prepare Invoice operation

The action result dto contains information about the result of running the action

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SalesOrderV2Api(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$order_type = 'order_type_example'; // string | Order Type of the sale order from which the invoice will be created
$order_number = 'order_number_example'; // string | Reference number of the sale order from which the invoice will be created
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->salesOrderV2PrepareInvoiceActionByorderTypeorderNumber($order_type, $order_number, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SalesOrderV2Api->salesOrderV2PrepareInvoiceActionByorderTypeorderNumber: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **order_type** | **string**| Order Type of the sale order from which the invoice will be created | |
| **order_number** | **string**| Reference number of the sale order from which the invoice will be created | |
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

## `salesOrderV2ReopenSalesOrderBysalesOrderNumber()`

```php
salesOrderV2ReopenSalesOrderBysalesOrderNumber($sales_order_number, $reopen_sales_order_action_dto, $erp_api_background): \OpenAPI\Client\Model\ReopenSalesOrderActionResultDto
```

Reopen and update a specific Sales Order. This method requires a sales order update dto where the order type is initialised.

The action result dto contains information about the result of running the action

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SalesOrderV2Api(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sales_order_number = 'sales_order_number_example'; // string | Identifies the Sale Order to reopen
$reopen_sales_order_action_dto = new \OpenAPI\Client\Model\ReopenSalesOrderActionDto(); // \OpenAPI\Client\Model\ReopenSalesOrderActionDto | 
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->salesOrderV2ReopenSalesOrderBysalesOrderNumber($sales_order_number, $reopen_sales_order_action_dto, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SalesOrderV2Api->salesOrderV2ReopenSalesOrderBysalesOrderNumber: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sales_order_number** | **string**| Identifies the Sale Order to reopen | |
| **reopen_sales_order_action_dto** | [**\OpenAPI\Client\Model\ReopenSalesOrderActionDto**](../Model/ReopenSalesOrderActionDto.md)|  | |
| **erp_api_background** | **string**| Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \&quot;none\&quot; (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \&quot;subscription[:&lt;name_1&gt;&#x3D;&lt;value_1&gt;,..,&lt;name_n&gt;&#x3D;&lt;value_n&gt;]\&quot; (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription&#39;s url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content | [optional] |

### Return type

[**\OpenAPI\Client\Model\ReopenSalesOrderActionResultDto**](../Model/ReopenSalesOrderActionResultDto.md)

### Authorization

[serviceapi](../../README.md#serviceapi)

### HTTP request headers

- **Content-Type**: `application/json`, `text/json`, `application/xml`, `text/xml`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`, `text/json`, `application/xml`, `text/xml`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `salesOrderV2SendEmailActionByorderTypeorderNumber()`

```php
salesOrderV2SendEmailActionByorderTypeorderNumber($order_type, $order_number, $erp_api_background): \OpenAPI\Client\Model\BackgroundApiAcceptedDto
```

Send by mail operation

The action result dto contains information about the result of running the action

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SalesOrderV2Api(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$order_type = 'order_type_example'; // string | The type of sale order from which the email will be dispatched.
$order_number = 'order_number_example'; // string | The number of sale order from which the email will be dispatched.
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->salesOrderV2SendEmailActionByorderTypeorderNumber($order_type, $order_number, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SalesOrderV2Api->salesOrderV2SendEmailActionByorderTypeorderNumber: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **order_type** | **string**| The type of sale order from which the email will be dispatched. | |
| **order_number** | **string**| The number of sale order from which the email will be dispatched. | |
| **erp_api_background** | **string**| Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \&quot;none\&quot; (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \&quot;subscription[:&lt;name_1&gt;&#x3D;&lt;value_1&gt;,..,&lt;name_n&gt;&#x3D;&lt;value_n&gt;]\&quot; (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription&#39;s url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content | [optional] |

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

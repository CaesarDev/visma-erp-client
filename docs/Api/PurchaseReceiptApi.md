# OpenAPI\Client\PurchaseReceiptApi



All URIs are relative to https://api.finance.visma.net, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**purchaseReceiptAddPurchaseOrderLinesByreceiptNumber()**](PurchaseReceiptApi.md#purchaseReceiptAddPurchaseOrderLinesByreceiptNumber) | **POST** /v1/PurchaseReceipt/{receiptNumber}/action/addpurchaseorderlines | Add purchase order lines to receipt |
| [**purchaseReceiptAddPurchaseOrdersByreceiptNumber()**](PurchaseReceiptApi.md#purchaseReceiptAddPurchaseOrdersByreceiptNumber) | **POST** /v1/PurchaseReceipt/{receiptNumber}/action/addpurchaseorder | Add purchase orders to receipt |
| [**purchaseReceiptCancelReceiptByreceiptNumber()**](PurchaseReceiptApi.md#purchaseReceiptCancelReceiptByreceiptNumber) | **POST** /v1/PurchaseReceipt/{receiptNumber}/action/cancelReceipt | Cancel purchase receipt operation |
| [**purchaseReceiptGetAllReceiptBasic()**](PurchaseReceiptApi.md#purchaseReceiptGetAllReceiptBasic) | **GET** /v1/PurchaseReceipt | Get a range of Purchase Receipts - ScreenId&#x3D;PO302000  Please use a page size lower or equal to the allowed max page size which is 500 |
| [**purchaseReceiptGetPurchaseReceiptBasicByreceiptNumber()**](PurchaseReceiptApi.md#purchaseReceiptGetPurchaseReceiptBasicByreceiptNumber) | **GET** /v1/PurchaseReceipt/{receiptNumber} | Get a specific Purchase Receipt |
| [**purchaseReceiptPost()**](PurchaseReceiptApi.md#purchaseReceiptPost) | **POST** /v1/PurchaseReceipt | Create a Purchase Receipt |
| [**purchaseReceiptPrintPurchaseReceiptByreceiptNumber()**](PurchaseReceiptApi.md#purchaseReceiptPrintPurchaseReceiptByreceiptNumber) | **GET** /v1/PurchaseReceipt/{receiptNumber}/print | Get the print report of a Purchase Receipt |
| [**purchaseReceiptPutByreceiptNumber()**](PurchaseReceiptApi.md#purchaseReceiptPutByreceiptNumber) | **PUT** /v1/PurchaseReceipt/{receiptNumber} | Update a specific Purchase Receipt |
| [**purchaseReceiptReleaseReceiptByreceiptNumber()**](PurchaseReceiptApi.md#purchaseReceiptReleaseReceiptByreceiptNumber) | **POST** /v1/PurchaseReceipt/{receiptNumber}/action/release | Release purchase receipt operation |


## `purchaseReceiptAddPurchaseOrderLinesByreceiptNumber()`

```php
purchaseReceiptAddPurchaseOrderLinesByreceiptNumber($receipt_number, $purchase_receipt_order_lines_list_update_dto, $erp_api_background): \OpenAPI\Client\Model\AddOrderLinesToPurchaseReceiptActionResultDto
```

Add purchase order lines to receipt

The action result dto contains information about the result of running the action

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PurchaseReceiptApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$receipt_number = 'receipt_number_example'; // string | Reference number of the receipt to which to add the orders
$purchase_receipt_order_lines_list_update_dto = new \OpenAPI\Client\Model\PurchaseReceiptOrderLinesListUpdateDto(); // \OpenAPI\Client\Model\PurchaseReceiptOrderLinesListUpdateDto | Object containing an array of reference numbers of the orders to be added to the receipt
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->purchaseReceiptAddPurchaseOrderLinesByreceiptNumber($receipt_number, $purchase_receipt_order_lines_list_update_dto, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PurchaseReceiptApi->purchaseReceiptAddPurchaseOrderLinesByreceiptNumber: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **receipt_number** | **string**| Reference number of the receipt to which to add the orders | |
| **purchase_receipt_order_lines_list_update_dto** | [**\OpenAPI\Client\Model\PurchaseReceiptOrderLinesListUpdateDto**](../Model/PurchaseReceiptOrderLinesListUpdateDto.md)| Object containing an array of reference numbers of the orders to be added to the receipt | |
| **erp_api_background** | **string**| Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \&quot;none\&quot; (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \&quot;subscription[:&lt;name_1&gt;&#x3D;&lt;value_1&gt;,..,&lt;name_n&gt;&#x3D;&lt;value_n&gt;]\&quot; (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription&#39;s url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content | [optional] |

### Return type

[**\OpenAPI\Client\Model\AddOrderLinesToPurchaseReceiptActionResultDto**](../Model/AddOrderLinesToPurchaseReceiptActionResultDto.md)

### Authorization

[serviceapi](../../README.md#serviceapi)

### HTTP request headers

- **Content-Type**: `application/json`, `text/json`, `application/xml`, `text/xml`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`, `text/json`, `application/xml`, `text/xml`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `purchaseReceiptAddPurchaseOrdersByreceiptNumber()`

```php
purchaseReceiptAddPurchaseOrdersByreceiptNumber($receipt_number, $purchase_receipt_order_list_update_dto, $erp_api_background): \OpenAPI\Client\Model\AddOrdersToPurchaseReceiptActionResultDto
```

Add purchase orders to receipt

The action result DTO contains information about the result of running the action

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PurchaseReceiptApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$receipt_number = 'receipt_number_example'; // string | Reference number of the receipt to which to add the orders
$purchase_receipt_order_list_update_dto = new \OpenAPI\Client\Model\PurchaseReceiptOrderListUpdateDto(); // \OpenAPI\Client\Model\PurchaseReceiptOrderListUpdateDto | Object containing an array of reference numbers of the orders to be added to the receipt
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->purchaseReceiptAddPurchaseOrdersByreceiptNumber($receipt_number, $purchase_receipt_order_list_update_dto, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PurchaseReceiptApi->purchaseReceiptAddPurchaseOrdersByreceiptNumber: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **receipt_number** | **string**| Reference number of the receipt to which to add the orders | |
| **purchase_receipt_order_list_update_dto** | [**\OpenAPI\Client\Model\PurchaseReceiptOrderListUpdateDto**](../Model/PurchaseReceiptOrderListUpdateDto.md)| Object containing an array of reference numbers of the orders to be added to the receipt | |
| **erp_api_background** | **string**| Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \&quot;none\&quot; (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \&quot;subscription[:&lt;name_1&gt;&#x3D;&lt;value_1&gt;,..,&lt;name_n&gt;&#x3D;&lt;value_n&gt;]\&quot; (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription&#39;s url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content | [optional] |

### Return type

[**\OpenAPI\Client\Model\AddOrdersToPurchaseReceiptActionResultDto**](../Model/AddOrdersToPurchaseReceiptActionResultDto.md)

### Authorization

[serviceapi](../../README.md#serviceapi)

### HTTP request headers

- **Content-Type**: `application/json`, `text/json`, `application/xml`, `text/xml`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`, `text/json`, `application/xml`, `text/xml`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `purchaseReceiptCancelReceiptByreceiptNumber()`

```php
purchaseReceiptCancelReceiptByreceiptNumber($receipt_number, $erp_api_background): object
```

Cancel purchase receipt operation

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PurchaseReceiptApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$receipt_number = 'receipt_number_example'; // string | 
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->purchaseReceiptCancelReceiptByreceiptNumber($receipt_number, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PurchaseReceiptApi->purchaseReceiptCancelReceiptByreceiptNumber: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **receipt_number** | **string**|  | |
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

## `purchaseReceiptGetAllReceiptBasic()`

```php
purchaseReceiptGetAllReceiptBasic($receipt_type, $status, $greater_than_value, $number_to_read, $skip_records, $last_modified_date_time, $last_modified_date_time_condition, $supplier, $po_order_nbr, $branch, $fin_period, $receipt_date, $receipt_date_condition, $due_date, $due_date_condition, $include_custom_free_fields, $page_number, $page_size, $erp_api_background): \OpenAPI\Client\Model\PurchaseReceiptDto[]
```

Get a range of Purchase Receipts - ScreenId=PO302000  Please use a page size lower or equal to the allowed max page size which is 500

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PurchaseReceiptApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$receipt_type = 'receipt_type_example'; // string
$status = 'status_example'; // string
$greater_than_value = 'greater_than_value_example'; // string
$number_to_read = 56; // int | This field has been deprecated and will be removed in future versions. Use pagenumber and pagesize for pagination purposes. Pagenumber and pagesize does not work with NumberToRead and SkipRecords.
$skip_records = 56; // int | This field has been deprecated and will be removed in future versions. Use pagenumber and pagesize for pagination purposes. Pagenumber and pagesize does not work with NumberToRead and SkipRecords.
$last_modified_date_time = 'last_modified_date_time_example'; // string | This value, generated by the system, indicates the last time the record was modified. Use it to retrieve all records that have been modified since that time, up to the present.    Accepted format:  * ```yyyy-MM-dd```  * ```yyyy-MM-dd HH:mm:ss```  * ```yyyy-MM-dd HH:mm:ss.FFF```  * ```yyyy-MM-ddTHH:mm:ss```  * ```yyyy-MM-ddTHH:mm:ss.FFF```    _Note:_ __LastModifiedDateTime__ and __LastModifiedDateTimeCondition__ are __mutually inclusive__.
$last_modified_date_time_condition = 'last_modified_date_time_condition_example'; // string | This value represents the condition to be applied when retrieving records.    Accepted values (without the single quotes):  * '&gt;' for greater than  * '&lt;' for less than  * '&gt;=' for greater than or equal  * '&lt;=' for less than or equal    _Note:_ __LastModifiedDateTime__ and __LastModifiedDateTimeCondition__ are __mutually inclusive__.
$supplier = 'supplier_example'; // string
$po_order_nbr = 'po_order_nbr_example'; // string
$branch = 'branch_example'; // string
$fin_period = 'fin_period_example'; // string | Filter by financial period, format YYYYPP
$receipt_date = 'receipt_date_example'; // string
$receipt_date_condition = 'receipt_date_condition_example'; // string | This value represents the condition to be applied to the order date when retrieving records.    Accepted values (without the single quotes):  * '&gt;' for greater than  * '&lt;' for less than  * '&gt;=' for greater than or equal  * '&lt;=' for less than or equal    _Note:_ __ReceiptDate__ and __ReceiptDateCondition__ are __mutually inclusive__.
$due_date = 'due_date_example'; // string | This value indicates the date the document is due. Use it to retrieve all records that have the due date since that time, up to the future.    Accepted format:  * ```yyyy-MM-dd```  * ```yyyy-MM-dd HH:mm:ss```  * ```yyyy-MM-dd HH:mm:ss.FFF```  * ```yyyy-MM-ddTHH:mm:ss```  * ```yyyy-MM-ddTHH:mm:ss.FFF```    _Note:_ __DueDate__ and __DueDateCondition__ are __mutually inclusive__.
$due_date_condition = 'due_date_condition_example'; // string | This value represents the condition to be applied to the Due Date when retrieving records.    Accepted values (without the single quotes):  * '&gt;' for greater than  * '&lt;' for less than  * '&gt;=' for greater than or equal  * '&lt;=' for less than or equal    _Note:_ __DueDate__ and __DueDateCondition__ are __mutually inclusive__.
$include_custom_free_fields = True; // bool | Parameter to include custom free fields information in the result set, if true then custom free fields will be included in the result set  Works only with PurchaseRecieptBasic and v2 of PurchaseReceipts.
$page_number = 56; // int | Pagination parameter. Page number.
$page_size = 56; // int | Pagination parameter. Number of items to be collected.  Please use a page size lower or equal to the allowed max page size which is returned as part of the metadata information.  If requested page size is greater than allowed max page size, request will be limited to max page size.
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->purchaseReceiptGetAllReceiptBasic($receipt_type, $status, $greater_than_value, $number_to_read, $skip_records, $last_modified_date_time, $last_modified_date_time_condition, $supplier, $po_order_nbr, $branch, $fin_period, $receipt_date, $receipt_date_condition, $due_date, $due_date_condition, $include_custom_free_fields, $page_number, $page_size, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PurchaseReceiptApi->purchaseReceiptGetAllReceiptBasic: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **receipt_type** | **string**|  | [optional] |
| **status** | **string**|  | [optional] |
| **greater_than_value** | **string**|  | [optional] |
| **number_to_read** | **int**| This field has been deprecated and will be removed in future versions. Use pagenumber and pagesize for pagination purposes. Pagenumber and pagesize does not work with NumberToRead and SkipRecords. | [optional] |
| **skip_records** | **int**| This field has been deprecated and will be removed in future versions. Use pagenumber and pagesize for pagination purposes. Pagenumber and pagesize does not work with NumberToRead and SkipRecords. | [optional] |
| **last_modified_date_time** | **string**| This value, generated by the system, indicates the last time the record was modified. Use it to retrieve all records that have been modified since that time, up to the present.    Accepted format:  * &#x60;&#x60;&#x60;yyyy-MM-dd&#x60;&#x60;&#x60;  * &#x60;&#x60;&#x60;yyyy-MM-dd HH:mm:ss&#x60;&#x60;&#x60;  * &#x60;&#x60;&#x60;yyyy-MM-dd HH:mm:ss.FFF&#x60;&#x60;&#x60;  * &#x60;&#x60;&#x60;yyyy-MM-ddTHH:mm:ss&#x60;&#x60;&#x60;  * &#x60;&#x60;&#x60;yyyy-MM-ddTHH:mm:ss.FFF&#x60;&#x60;&#x60;    _Note:_ __LastModifiedDateTime__ and __LastModifiedDateTimeCondition__ are __mutually inclusive__. | [optional] |
| **last_modified_date_time_condition** | **string**| This value represents the condition to be applied when retrieving records.    Accepted values (without the single quotes):  * &#39;&amp;gt;&#39; for greater than  * &#39;&amp;lt;&#39; for less than  * &#39;&amp;gt;&#x3D;&#39; for greater than or equal  * &#39;&amp;lt;&#x3D;&#39; for less than or equal    _Note:_ __LastModifiedDateTime__ and __LastModifiedDateTimeCondition__ are __mutually inclusive__. | [optional] |
| **supplier** | **string**|  | [optional] |
| **po_order_nbr** | **string**|  | [optional] |
| **branch** | **string**|  | [optional] |
| **fin_period** | **string**| Filter by financial period, format YYYYPP | [optional] |
| **receipt_date** | **string**|  | [optional] |
| **receipt_date_condition** | **string**| This value represents the condition to be applied to the order date when retrieving records.    Accepted values (without the single quotes):  * &#39;&amp;gt;&#39; for greater than  * &#39;&amp;lt;&#39; for less than  * &#39;&amp;gt;&#x3D;&#39; for greater than or equal  * &#39;&amp;lt;&#x3D;&#39; for less than or equal    _Note:_ __ReceiptDate__ and __ReceiptDateCondition__ are __mutually inclusive__. | [optional] |
| **due_date** | **string**| This value indicates the date the document is due. Use it to retrieve all records that have the due date since that time, up to the future.    Accepted format:  * &#x60;&#x60;&#x60;yyyy-MM-dd&#x60;&#x60;&#x60;  * &#x60;&#x60;&#x60;yyyy-MM-dd HH:mm:ss&#x60;&#x60;&#x60;  * &#x60;&#x60;&#x60;yyyy-MM-dd HH:mm:ss.FFF&#x60;&#x60;&#x60;  * &#x60;&#x60;&#x60;yyyy-MM-ddTHH:mm:ss&#x60;&#x60;&#x60;  * &#x60;&#x60;&#x60;yyyy-MM-ddTHH:mm:ss.FFF&#x60;&#x60;&#x60;    _Note:_ __DueDate__ and __DueDateCondition__ are __mutually inclusive__. | [optional] |
| **due_date_condition** | **string**| This value represents the condition to be applied to the Due Date when retrieving records.    Accepted values (without the single quotes):  * &#39;&amp;gt;&#39; for greater than  * &#39;&amp;lt;&#39; for less than  * &#39;&amp;gt;&#x3D;&#39; for greater than or equal  * &#39;&amp;lt;&#x3D;&#39; for less than or equal    _Note:_ __DueDate__ and __DueDateCondition__ are __mutually inclusive__. | [optional] |
| **include_custom_free_fields** | **bool**| Parameter to include custom free fields information in the result set, if true then custom free fields will be included in the result set  Works only with PurchaseRecieptBasic and v2 of PurchaseReceipts. | [optional] |
| **page_number** | **int**| Pagination parameter. Page number. | [optional] |
| **page_size** | **int**| Pagination parameter. Number of items to be collected.  Please use a page size lower or equal to the allowed max page size which is returned as part of the metadata information.  If requested page size is greater than allowed max page size, request will be limited to max page size. | [optional] |
| **erp_api_background** | **string**| Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \&quot;none\&quot; (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \&quot;subscription[:&lt;name_1&gt;&#x3D;&lt;value_1&gt;,..,&lt;name_n&gt;&#x3D;&lt;value_n&gt;]\&quot; (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription&#39;s url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content | [optional] |

### Return type

[**\OpenAPI\Client\Model\PurchaseReceiptDto[]**](../Model/PurchaseReceiptDto.md)

### Authorization

[serviceapi](../../README.md#serviceapi)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `purchaseReceiptGetPurchaseReceiptBasicByreceiptNumber()`

```php
purchaseReceiptGetPurchaseReceiptBasicByreceiptNumber($receipt_number, $erp_api_background): \OpenAPI\Client\Model\PurchaseReceiptDto
```

Get a specific Purchase Receipt

Data for a single Purchase Receipt. <br></br>  The response headers include an ETag after a successful GET operation.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PurchaseReceiptApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$receipt_number = 'receipt_number_example'; // string | Identifies the Purchase Receipt
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->purchaseReceiptGetPurchaseReceiptBasicByreceiptNumber($receipt_number, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PurchaseReceiptApi->purchaseReceiptGetPurchaseReceiptBasicByreceiptNumber: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **receipt_number** | **string**| Identifies the Purchase Receipt | |
| **erp_api_background** | **string**| Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \&quot;none\&quot; (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \&quot;subscription[:&lt;name_1&gt;&#x3D;&lt;value_1&gt;,..,&lt;name_n&gt;&#x3D;&lt;value_n&gt;]\&quot; (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription&#39;s url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content | [optional] |

### Return type

[**\OpenAPI\Client\Model\PurchaseReceiptDto**](../Model/PurchaseReceiptDto.md)

### Authorization

[serviceapi](../../README.md#serviceapi)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `purchaseReceiptPost()`

```php
purchaseReceiptPost($purchase_receipt_update_dto, $erp_api_background): object
```

Create a Purchase Receipt

Response Message has StatusCode Created if POST operation succeed. <br></br>  Response Message has StatusCode BadRequest or InternalServerError if POST operation failed. <br></br>  The response headers include an ETag after a successful POST operation. <br></br>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PurchaseReceiptApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$purchase_receipt_update_dto = new \OpenAPI\Client\Model\PurchaseReceiptUpdateDto(); // \OpenAPI\Client\Model\PurchaseReceiptUpdateDto | Defines the data for the  Purchase Receipt to create
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->purchaseReceiptPost($purchase_receipt_update_dto, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PurchaseReceiptApi->purchaseReceiptPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **purchase_receipt_update_dto** | [**\OpenAPI\Client\Model\PurchaseReceiptUpdateDto**](../Model/PurchaseReceiptUpdateDto.md)| Defines the data for the  Purchase Receipt to create | |
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

## `purchaseReceiptPrintPurchaseReceiptByreceiptNumber()`

```php
purchaseReceiptPrintPurchaseReceiptByreceiptNumber($receipt_number, $erp_api_background): object
```

Get the print report of a Purchase Receipt

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PurchaseReceiptApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$receipt_number = 'receipt_number_example'; // string | Identifies the receipt
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->purchaseReceiptPrintPurchaseReceiptByreceiptNumber($receipt_number, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PurchaseReceiptApi->purchaseReceiptPrintPurchaseReceiptByreceiptNumber: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **receipt_number** | **string**| Identifies the receipt | |
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

## `purchaseReceiptPutByreceiptNumber()`

```php
purchaseReceiptPutByreceiptNumber($receipt_number, $purchase_receipt_update_dto, $erp_api_background, $if_match): \OpenAPI\Client\Model\BackgroundApiAcceptedDto
```

Update a specific Purchase Receipt

Response Message has StatusCode NoContent if PUT operation succeed. <br></br>  Response Message has StatusCode BadRequest if PUT operation failed. <br></br>  The response headers include an ETag after a successful PUT operation. <br></br>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PurchaseReceiptApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$receipt_number = 'receipt_number_example'; // string | Identifies the  Purchase Receipt  to update
$purchase_receipt_update_dto = new \OpenAPI\Client\Model\PurchaseReceiptUpdateDto(); // \OpenAPI\Client\Model\PurchaseReceiptUpdateDto | Defines the data for the  Purchase Receipt  to update
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content
$if_match = 'if_match_example'; // string | The If-Match HTTP header allows clients to update a resource only if its current version matches a specific ETag. This mechanism helps prevent conflicts when multiple clients attempt to modify the same resource simultaneously. The If-Match header should be included in the request headers using the following syntax: If-Match: \"etag_value\" * If the update is successful, the server responds with 204 No Content and includes the new ETag value in the response headers. * If the ETag on the server does not match the value provided in the If-Match header, the server responds with 412 Precondition Failed.

try {
    $result = $apiInstance->purchaseReceiptPutByreceiptNumber($receipt_number, $purchase_receipt_update_dto, $erp_api_background, $if_match);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PurchaseReceiptApi->purchaseReceiptPutByreceiptNumber: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **receipt_number** | **string**| Identifies the  Purchase Receipt  to update | |
| **purchase_receipt_update_dto** | [**\OpenAPI\Client\Model\PurchaseReceiptUpdateDto**](../Model/PurchaseReceiptUpdateDto.md)| Defines the data for the  Purchase Receipt  to update | |
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

## `purchaseReceiptReleaseReceiptByreceiptNumber()`

```php
purchaseReceiptReleaseReceiptByreceiptNumber($receipt_number, $erp_api_background): \OpenAPI\Client\Model\ReleasePurchaseReceiptActionResultDto
```

Release purchase receipt operation

The action result dto contains information about the result of running the action

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PurchaseReceiptApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$receipt_number = 'receipt_number_example'; // string | Reference number of the receipt to be released
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->purchaseReceiptReleaseReceiptByreceiptNumber($receipt_number, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PurchaseReceiptApi->purchaseReceiptReleaseReceiptByreceiptNumber: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **receipt_number** | **string**| Reference number of the receipt to be released | |
| **erp_api_background** | **string**| Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \&quot;none\&quot; (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \&quot;subscription[:&lt;name_1&gt;&#x3D;&lt;value_1&gt;,..,&lt;name_n&gt;&#x3D;&lt;value_n&gt;]\&quot; (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription&#39;s url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content | [optional] |

### Return type

[**\OpenAPI\Client\Model\ReleasePurchaseReceiptActionResultDto**](../Model/ReleasePurchaseReceiptActionResultDto.md)

### Authorization

[serviceapi](../../README.md#serviceapi)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `text/json`, `application/xml`, `text/xml`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

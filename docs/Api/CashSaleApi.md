# OpenAPI\Client\CashSaleApi



All URIs are relative to https://api.finance.visma.net, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**cashSaleGetAllCashSales()**](CashSaleApi.md#cashSaleGetAllCashSales) | **GET** /v1/cashsale | Get a range of Cash Sales - ScreenId&#x3D;AR304000  Request page size must be lower or equal to the allowed max page size which is returned as part of the metadata information.  If requested page size is greater than allowed max page size, request will be limited to max page size  Change log:  2021-October:Added forced pagination |
| [**cashSaleGetBydocumentNumber()**](CashSaleApi.md#cashSaleGetBydocumentNumber) | **GET** /v1/cashsale/{documentNumber} | Get a specific Cash Sale |
| [**cashSalePost()**](CashSaleApi.md#cashSalePost) | **POST** /v1/cashsale | Create a Cash Sale |
| [**cashSalePutBydocumentNumber()**](CashSaleApi.md#cashSalePutBydocumentNumber) | **PUT** /v1/cashsale/{documentNumber} | Update a specific Cash Sale |


## `cashSaleGetAllCashSales()`

```php
cashSaleGetAllCashSales($document_type, $released, $dunning_level, $closed_financial_period, $dunning_letter_date_time, $dunning_letter_date_time_condition, $project, $expand_applications, $expand_dunning_information, $expand_attachments, $expand_tax_details, $expand_invoice_address, $financial_period, $document_due_date, $document_due_date_condition, $status, $number_to_read, $skip_records, $external_reference, $payment_reference, $customer_ref_number, $customer, $branch, $document_date, $document_date_condition, $greater_than_value, $last_modified_date_time, $last_modified_date_time_condition, $created_date_time, $created_date_time_condition, $page_number, $page_size, $erp_api_background): \OpenAPI\Client\Model\CashSaleDto[]
```

Get a range of Cash Sales - ScreenId=AR304000  Request page size must be lower or equal to the allowed max page size which is returned as part of the metadata information.  If requested page size is greater than allowed max page size, request will be limited to max page size  Change log:  2021-October:Added forced pagination

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CashSaleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$document_type = 'document_type_example'; // string | The field is deprecated for specific customer document endpoints. It will only be usable from customer document endpoint.
$released = 56; // int | Parameter for showing if invoice has been released or not.
$dunning_level = 56; // int | The dunning level of the document.
$closed_financial_period = 'closed_financial_period_example'; // string | The date of the closing of the financial period.
$dunning_letter_date_time = 'dunning_letter_date_time_example'; // string | The date and time for when the document last released a dunning letter.
$dunning_letter_date_time_condition = 'dunning_letter_date_time_condition_example'; // string | Set time/date as before (&lt;), after (&gt;), before and including (=&lt;) OR after and including (=&gt;) to filter on time frame.
$project = 'project_example'; // string | The project with which the document is associated.
$expand_applications = True; // bool | True if you want to see all dunning information regarding this document.
$expand_dunning_information = True; // bool
$expand_attachments = True; // bool | True if you want to see all attachments regarding this document.
$expand_tax_details = True; // bool | True if you want to see all VAT details regarding this document.
$expand_invoice_address = True; // bool | True if you want to see all information regarding the invoice address for this document.
$financial_period = 'financial_period_example'; // string | The financial period to which the transactions recorded in the document is posted. Format YYYYMM.
$document_due_date = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime | The date when payment for the document is due, in accordance with the credit terms.
$document_due_date_condition = 'document_due_date_condition_example'; // string | This value represents the condition to be applied to the Due Date when retrieving records.    Accepted values (without the single quotes):  * '&gt;' for greater than  * '&lt;' for less than  * '&gt;=' for greater than or equal  * '&lt;=' for less than or equal
$status = 'status_example'; // string | The status of the document. Use the dropdown to select status.
$number_to_read = 56; // int | This field has been deprecated and will be removed in future versions. Use pagenumber and pagesize for pagination purposes. Pagenumber and pagesize does not work with NumberToRead and SkipRecords.
$skip_records = 56; // int | This field has been deprecated and will be removed in future versions. Use pagenumber and pagesize for pagination purposes. Pagenumber and pagesize does not work with NumberToRead and SkipRecords.
$external_reference = 'external_reference_example'; // string | The top part &gt; External reference &gt; The external reference used in AutoInvoice.
$payment_reference = 'payment_reference_example'; // string | The top part &gt; Payment ref. &gt; The reference number of the document, as automatically generated by the system in accordance with the number series assigned to cash sales in the Customer ledger preferences window..
$customer_ref_number = 'customer_ref_number_example'; // string | The top part &gt; External reference &gt; The external reference used in AutoInvoice.
$customer = 'customer_example'; // string | Filter by Customer
$branch = 'branch_example'; // string | Filter by Branch
$document_date = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime | This value indicates the document date. Use it to retrieve all records that have the Document Date since that time, up to the future.    Accepted format:  * ```yyyy-MM-dd```  * ```yyyy-MM-dd```  * ```yyyy-MM-dd```  * ```yyyy-MM-dd```  * ```yyyy-MM-dd```    _Note:_ __DocumentDate__ and __DocumentDateCondition__ are __mutually inclusive__.
$document_date_condition = 'document_date_condition_example'; // string | This value represents the condition to be applied to the Document Date when retrieving records.    Accepted values (without the single quotes):  * '&gt;' for greater than  * '&lt;' for less than  * '&gt;=' for greater than or equal  * '&lt;=' for less than or equal    _Note:_ __DocumentDate__ and __DocumentDateCondition__ are __mutually inclusive__.
$greater_than_value = 'greater_than_value_example'; // string | Greater than value. The item which is the object for this, varies from API to API.
$last_modified_date_time = 'last_modified_date_time_example'; // string | This value, generated by the system, indicates the last time the record was modified. Use it to retrieve all records that have been modified since that time, up to the present.    Accepted format:  * ```yyyy-MM-dd```  * ```yyyy-MM-dd HH:mm:ss```  * ```yyyy-MM-dd HH:mm:ss.FFF```  * ```yyyy-MM-ddTHH:mm:ss```  * ```yyyy-MM-ddTHH:mm:ss.FFF```    _Note:_ __LastModifiedDateTime__ and __LastModifiedDateTimeCondition__ are __mutually inclusive__.
$last_modified_date_time_condition = 'last_modified_date_time_condition_example'; // string | This value represents the condition to be applied when retrieving records.    Accepted values (without the single quotes):  * '&gt;' for greater than  * '&lt;' for less than  * '&gt;=' for greater than or equal  * '&lt;=' for less than or equal    _Note:_ __LastModifiedDateTime__ and __LastModifiedDateTimeCondition__ are __mutually inclusive__.
$created_date_time = 'created_date_time_example'; // string | Creation date and time.
$created_date_time_condition = 'created_date_time_condition_example'; // string | System-retrieved information for state/condition
$page_number = 56; // int | Pagination parameter. Page number.
$page_size = 56; // int | Pagination parameter. Number of items to be collected.  Please use a page size lower or equal to the allowed max page size which is returned as part of the metadata information.  If requested page size is greater than allowed max page size, request will be limited to max page size.
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->cashSaleGetAllCashSales($document_type, $released, $dunning_level, $closed_financial_period, $dunning_letter_date_time, $dunning_letter_date_time_condition, $project, $expand_applications, $expand_dunning_information, $expand_attachments, $expand_tax_details, $expand_invoice_address, $financial_period, $document_due_date, $document_due_date_condition, $status, $number_to_read, $skip_records, $external_reference, $payment_reference, $customer_ref_number, $customer, $branch, $document_date, $document_date_condition, $greater_than_value, $last_modified_date_time, $last_modified_date_time_condition, $created_date_time, $created_date_time_condition, $page_number, $page_size, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CashSaleApi->cashSaleGetAllCashSales: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **document_type** | **string**| The field is deprecated for specific customer document endpoints. It will only be usable from customer document endpoint. | [optional] |
| **released** | **int**| Parameter for showing if invoice has been released or not. | [optional] |
| **dunning_level** | **int**| The dunning level of the document. | [optional] |
| **closed_financial_period** | **string**| The date of the closing of the financial period. | [optional] |
| **dunning_letter_date_time** | **string**| The date and time for when the document last released a dunning letter. | [optional] |
| **dunning_letter_date_time_condition** | **string**| Set time/date as before (&amp;lt;), after (&amp;gt;), before and including (&#x3D;&amp;lt;) OR after and including (&#x3D;&amp;gt;) to filter on time frame. | [optional] |
| **project** | **string**| The project with which the document is associated. | [optional] |
| **expand_applications** | **bool**| True if you want to see all dunning information regarding this document. | [optional] |
| **expand_dunning_information** | **bool**|  | [optional] |
| **expand_attachments** | **bool**| True if you want to see all attachments regarding this document. | [optional] |
| **expand_tax_details** | **bool**| True if you want to see all VAT details regarding this document. | [optional] |
| **expand_invoice_address** | **bool**| True if you want to see all information regarding the invoice address for this document. | [optional] |
| **financial_period** | **string**| The financial period to which the transactions recorded in the document is posted. Format YYYYMM. | [optional] |
| **document_due_date** | **\DateTime**| The date when payment for the document is due, in accordance with the credit terms. | [optional] |
| **document_due_date_condition** | **string**| This value represents the condition to be applied to the Due Date when retrieving records.    Accepted values (without the single quotes):  * &#39;&amp;gt;&#39; for greater than  * &#39;&amp;lt;&#39; for less than  * &#39;&amp;gt;&#x3D;&#39; for greater than or equal  * &#39;&amp;lt;&#x3D;&#39; for less than or equal | [optional] |
| **status** | **string**| The status of the document. Use the dropdown to select status. | [optional] |
| **number_to_read** | **int**| This field has been deprecated and will be removed in future versions. Use pagenumber and pagesize for pagination purposes. Pagenumber and pagesize does not work with NumberToRead and SkipRecords. | [optional] |
| **skip_records** | **int**| This field has been deprecated and will be removed in future versions. Use pagenumber and pagesize for pagination purposes. Pagenumber and pagesize does not work with NumberToRead and SkipRecords. | [optional] |
| **external_reference** | **string**| The top part &amp;gt; External reference &amp;gt; The external reference used in AutoInvoice. | [optional] |
| **payment_reference** | **string**| The top part &amp;gt; Payment ref. &amp;gt; The reference number of the document, as automatically generated by the system in accordance with the number series assigned to cash sales in the Customer ledger preferences window.. | [optional] |
| **customer_ref_number** | **string**| The top part &amp;gt; External reference &amp;gt; The external reference used in AutoInvoice. | [optional] |
| **customer** | **string**| Filter by Customer | [optional] |
| **branch** | **string**| Filter by Branch | [optional] |
| **document_date** | **\DateTime**| This value indicates the document date. Use it to retrieve all records that have the Document Date since that time, up to the future.    Accepted format:  * &#x60;&#x60;&#x60;yyyy-MM-dd&#x60;&#x60;&#x60;  * &#x60;&#x60;&#x60;yyyy-MM-dd&#x60;&#x60;&#x60;  * &#x60;&#x60;&#x60;yyyy-MM-dd&#x60;&#x60;&#x60;  * &#x60;&#x60;&#x60;yyyy-MM-dd&#x60;&#x60;&#x60;  * &#x60;&#x60;&#x60;yyyy-MM-dd&#x60;&#x60;&#x60;    _Note:_ __DocumentDate__ and __DocumentDateCondition__ are __mutually inclusive__. | [optional] |
| **document_date_condition** | **string**| This value represents the condition to be applied to the Document Date when retrieving records.    Accepted values (without the single quotes):  * &#39;&amp;gt;&#39; for greater than  * &#39;&amp;lt;&#39; for less than  * &#39;&amp;gt;&#x3D;&#39; for greater than or equal  * &#39;&amp;lt;&#x3D;&#39; for less than or equal    _Note:_ __DocumentDate__ and __DocumentDateCondition__ are __mutually inclusive__. | [optional] |
| **greater_than_value** | **string**| Greater than value. The item which is the object for this, varies from API to API. | [optional] |
| **last_modified_date_time** | **string**| This value, generated by the system, indicates the last time the record was modified. Use it to retrieve all records that have been modified since that time, up to the present.    Accepted format:  * &#x60;&#x60;&#x60;yyyy-MM-dd&#x60;&#x60;&#x60;  * &#x60;&#x60;&#x60;yyyy-MM-dd HH:mm:ss&#x60;&#x60;&#x60;  * &#x60;&#x60;&#x60;yyyy-MM-dd HH:mm:ss.FFF&#x60;&#x60;&#x60;  * &#x60;&#x60;&#x60;yyyy-MM-ddTHH:mm:ss&#x60;&#x60;&#x60;  * &#x60;&#x60;&#x60;yyyy-MM-ddTHH:mm:ss.FFF&#x60;&#x60;&#x60;    _Note:_ __LastModifiedDateTime__ and __LastModifiedDateTimeCondition__ are __mutually inclusive__. | [optional] |
| **last_modified_date_time_condition** | **string**| This value represents the condition to be applied when retrieving records.    Accepted values (without the single quotes):  * &#39;&amp;gt;&#39; for greater than  * &#39;&amp;lt;&#39; for less than  * &#39;&amp;gt;&#x3D;&#39; for greater than or equal  * &#39;&amp;lt;&#x3D;&#39; for less than or equal    _Note:_ __LastModifiedDateTime__ and __LastModifiedDateTimeCondition__ are __mutually inclusive__. | [optional] |
| **created_date_time** | **string**| Creation date and time. | [optional] |
| **created_date_time_condition** | **string**| System-retrieved information for state/condition | [optional] |
| **page_number** | **int**| Pagination parameter. Page number. | [optional] |
| **page_size** | **int**| Pagination parameter. Number of items to be collected.  Please use a page size lower or equal to the allowed max page size which is returned as part of the metadata information.  If requested page size is greater than allowed max page size, request will be limited to max page size. | [optional] |
| **erp_api_background** | **string**| Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \&quot;none\&quot; (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \&quot;subscription[:&lt;name_1&gt;&#x3D;&lt;value_1&gt;,..,&lt;name_n&gt;&#x3D;&lt;value_n&gt;]\&quot; (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription&#39;s url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content | [optional] |

### Return type

[**\OpenAPI\Client\Model\CashSaleDto[]**](../Model/CashSaleDto.md)

### Authorization

[serviceapi](../../README.md#serviceapi)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `cashSaleGetBydocumentNumber()`

```php
cashSaleGetBydocumentNumber($document_number, $erp_api_background): \OpenAPI\Client\Model\CashSaleDto
```

Get a specific Cash Sale

Data for Cash Sale <br></br>              The response headers include an ETag after a successful GET operation.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CashSaleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$document_number = 'document_number_example'; // string | Identifies the Cash Sale Document
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->cashSaleGetBydocumentNumber($document_number, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CashSaleApi->cashSaleGetBydocumentNumber: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **document_number** | **string**| Identifies the Cash Sale Document | |
| **erp_api_background** | **string**| Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \&quot;none\&quot; (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \&quot;subscription[:&lt;name_1&gt;&#x3D;&lt;value_1&gt;,..,&lt;name_n&gt;&#x3D;&lt;value_n&gt;]\&quot; (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription&#39;s url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content | [optional] |

### Return type

[**\OpenAPI\Client\Model\CashSaleDto**](../Model/CashSaleDto.md)

### Authorization

[serviceapi](../../README.md#serviceapi)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `cashSalePost()`

```php
cashSalePost($cash_sale_update_dto, $erp_api_background): object
```

Create a Cash Sale

Response Message has StatusCode Created if POST operation succeed <br></br>  Response Message has StatusCode BadRequest or InternalServerError if POST operation failed <br></br>  The response headers include an ETag after a successful POST operation.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CashSaleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$cash_sale_update_dto = new \OpenAPI\Client\Model\CashSaleUpdateDto(); // \OpenAPI\Client\Model\CashSaleUpdateDto | Defines the data for the Cash Sale to create
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->cashSalePost($cash_sale_update_dto, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CashSaleApi->cashSalePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **cash_sale_update_dto** | [**\OpenAPI\Client\Model\CashSaleUpdateDto**](../Model/CashSaleUpdateDto.md)| Defines the data for the Cash Sale to create | |
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

## `cashSalePutBydocumentNumber()`

```php
cashSalePutBydocumentNumber($document_number, $cash_sale_update_dto, $erp_api_background, $if_match): \OpenAPI\Client\Model\BackgroundApiAcceptedDto
```

Update a specific Cash Sale

Response Message has StatusCode NoContent if PUT operation succeed <br></br>  Response Message has StatusCode BadRequest if PUT operation failed <br></br>  In this endpoint, If-Match can be checked against resource current version when calling with 'erp-api-background' HTTP header.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CashSaleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$document_number = 'document_number_example'; // string | Identifies the Cash Sale to update
$cash_sale_update_dto = new \OpenAPI\Client\Model\CashSaleUpdateDto(); // \OpenAPI\Client\Model\CashSaleUpdateDto | Defines the data for the Cash Sale to update
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content
$if_match = 'if_match_example'; // string | The If-Match HTTP header allows clients to update a resource only if its current version matches a specific ETag. This mechanism helps prevent conflicts when multiple clients attempt to modify the same resource simultaneously. The If-Match header should be included in the request headers using the following syntax: If-Match: \"etag_value\" * If the update is successful, the server responds with 204 No Content and includes the new ETag value in the response headers. * If the ETag on the server does not match the value provided in the If-Match header, the server responds with 412 Precondition Failed.

try {
    $result = $apiInstance->cashSalePutBydocumentNumber($document_number, $cash_sale_update_dto, $erp_api_background, $if_match);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CashSaleApi->cashSalePutBydocumentNumber: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **document_number** | **string**| Identifies the Cash Sale to update | |
| **cash_sale_update_dto** | [**\OpenAPI\Client\Model\CashSaleUpdateDto**](../Model/CashSaleUpdateDto.md)| Defines the data for the Cash Sale to update | |
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

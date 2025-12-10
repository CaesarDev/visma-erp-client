# OpenAPI\Client\SupplierAccountApi



All URIs are relative to https://api.finance.visma.net, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**supplierAccountGetBysupplierId()**](SupplierAccountApi.md#supplierAccountGetBysupplierId) | **GET** /v1/supplieraccount/{supplierId} | Get expense accounts for a supplier |


## `supplierAccountGetBysupplierId()`

```php
supplierAccountGetBysupplierId($supplier_id, $supplier_item_id, $vat_registration_id, $lines_non_taxable, $erp_api_background): \OpenAPI\Client\Model\SupplierAccountsDto
```

Get expense accounts for a supplier

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: serviceapi
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SupplierAccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$supplier_id = 'supplier_id_example'; // string | The id of the supplier
$supplier_item_id = array('supplier_item_id_example'); // string[] | The list of supplier itemIds to search the expense account for. If the list empty, then the general expense account for the specific supplier is returned
$vat_registration_id = 'vat_registration_id_example'; // string | The vat registration id of the supplier
$lines_non_taxable = True; // bool | Indicates if all lines are taxable or not. Default is false
$erp_api_background = 'erp_api_background_example'; // string | Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \"none\" (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \"subscription[:<name_1>=<value_1>,..,<name_n>=<value_n>]\" (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription's url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content

try {
    $result = $apiInstance->supplierAccountGetBysupplierId($supplier_id, $supplier_item_id, $vat_registration_id, $lines_non_taxable, $erp_api_background);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SupplierAccountApi->supplierAccountGetBysupplierId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **supplier_id** | **string**| The id of the supplier | |
| **supplier_item_id** | [**string[]**](../Model/string.md)| The list of supplier itemIds to search the expense account for. If the list empty, then the general expense account for the specific supplier is returned | [optional] |
| **vat_registration_id** | **string**| The vat registration id of the supplier | [optional] |
| **lines_non_taxable** | **bool**| Indicates if all lines are taxable or not. Default is false | [optional] |
| **erp_api_background** | **string**| Accepts the request and queues it to be executed in the background by our least busy worker. Responds with 202 Accepted and a document containing a JobId reference and details state location. Supported values: * a URL: when the background operation is finished, a notification will be posted to the URL with a document containing a reference id, status code and a details state location. * \&quot;none\&quot; (without quotes): Fire and forget; no notification will be sent when background operation is finished. * \&quot;subscription[:&lt;name_1&gt;&#x3D;&lt;value_1&gt;,..,&lt;name_n&gt;&#x3D;&lt;value_n&gt;]\&quot; (without quotes): when the background operation is finsihed, a notification is posted to the Webhook subscription set up in Developer Portal for your integration client. Optionally a set of name-value pairs can be added. These will be sent as headers in the POST request to the Webhook subscription&#39;s url.  To find status and details of a background-api operation, GET .. v1/background/{id}. To get the response payload of a background-api operation, if any, GET .. v1/background/{id}/content | [optional] |

### Return type

[**\OpenAPI\Client\Model\SupplierAccountsDto**](../Model/SupplierAccountsDto.md)

### Authorization

[serviceapi](../../README.md#serviceapi)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

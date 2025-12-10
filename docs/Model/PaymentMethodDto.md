# # PaymentMethodDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**payment_method_id** | **string** | Mandatory field: The top part &amp;gt; Payment method ID* &amp;gt; The unique identifier of the payment method. | [optional]
**active** | **bool** | The top part &amp;gt; Active &amp;gt; A check box that indicates whether the payment method is active in the system. | [optional]
**means_of_payment** | **string** | The top part &amp;gt; Means of payment &amp;gt; One of the system&#39;s built-in payment templates. The following options are available: Credit card, Cash, Direct deposit. | [optional]
**description** | **string** | Mandatory field: The top part &amp;gt; Description* &amp;gt; A description of the payment method. | [optional]
**use_in_ap** | **bool** | The top part &amp;gt; Use for supplier &amp;gt; A check box that indicates whether the payment method will be used in Supplier ledger. | [optional]
**details** | [**\OpenAPI\Client\Model\PaymentMethodDetailDto[]**](PaymentMethodDetailDto.md) | The settings for Customer ledger and The settings of Supplier ledger tab &amp;gt; The table | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

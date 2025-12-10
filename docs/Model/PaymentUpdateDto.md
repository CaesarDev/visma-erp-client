# # PaymentUpdateDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**reference_number** | [**\OpenAPI\Client\Model\ReferenceNumberInPaymentUpdateDto**](ReferenceNumberInPaymentUpdateDto.md) |  | [optional]
**type** | [**\OpenAPI\Client\Model\TypeInPaymentUpdateDto**](TypeInPaymentUpdateDto.md) |  | [optional]
**hold** | [**\OpenAPI\Client\Model\HoldInPaymentUpdateDto**](HoldInPaymentUpdateDto.md) |  | [optional]
**application_date** | [**\OpenAPI\Client\Model\ApplicationDateInPaymentUpdateDto**](ApplicationDateInPaymentUpdateDto.md) |  | [optional]
**application_period** | [**\OpenAPI\Client\Model\ApplicationPeriodInPaymentUpdateDto**](ApplicationPeriodInPaymentUpdateDto.md) |  | [optional]
**payment_ref** | [**\OpenAPI\Client\Model\PaymentRefInPaymentUpdateDto**](PaymentRefInPaymentUpdateDto.md) |  | [optional]
**customer** | [**\OpenAPI\Client\Model\CustomerInPaymentUpdateDto**](CustomerInPaymentUpdateDto.md) |  | [optional]
**location** | [**\OpenAPI\Client\Model\LocationInPaymentUpdateDto**](LocationInPaymentUpdateDto.md) |  | [optional]
**payment_method** | [**\OpenAPI\Client\Model\PaymentMethodInPaymentUpdateDto**](PaymentMethodInPaymentUpdateDto.md) |  | [optional]
**cash_account** | [**\OpenAPI\Client\Model\CashAccountInPaymentUpdateDto**](CashAccountInPaymentUpdateDto.md) |  | [optional]
**currency** | [**\OpenAPI\Client\Model\CurrencyInPaymentUpdateDto**](CurrencyInPaymentUpdateDto.md) |  | [optional]
**payment_amount** | [**\OpenAPI\Client\Model\PaymentAmountInPaymentUpdateDto**](PaymentAmountInPaymentUpdateDto.md) |  | [optional]
**invoice_text** | [**\OpenAPI\Client\Model\InvoiceTextInPaymentUpdateDto**](InvoiceTextInPaymentUpdateDto.md) |  | [optional]
**branch** | [**\OpenAPI\Client\Model\DtoValueOfString**](DtoValueOfString.md) |  | [optional]
**override_number_series** | [**\OpenAPI\Client\Model\DtoValueOfBoolean**](DtoValueOfBoolean.md) |  | [optional]
**orders_to_apply** | [**\OpenAPI\Client\Model\PaymentOrdersLinesUpdateDto[]**](PaymentOrdersLinesUpdateDto.md) | The top part &amp;gt; Applied to orders &amp;gt; The total of the orders for which payment is reserved, minus the amount transferred to invoice. | [optional]
**finance_charges** | [**\OpenAPI\Client\Model\FinanceChargesUpdateDto[]**](FinanceChargesUpdateDto.md) | Financial Charges | [optional]
**payment_lines** | [**\OpenAPI\Client\Model\PaymentLinesUpdateDto[]**](PaymentLinesUpdateDto.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

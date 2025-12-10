# # CustomerPaymentMethodDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**customer** | [**\OpenAPI\Client\Model\CustomerInCustomerPaymentMethodDto**](CustomerInCustomerPaymentMethodDto.md) |  | [optional]
**payment_method** | [**\OpenAPI\Client\Model\PaymentMethodInCustomerPaymentMethodDto**](PaymentMethodInCustomerPaymentMethodDto.md) |  | [optional]
**active** | **bool** | The top part &amp;gt; Active &amp;gt; A check box that indicates (if selected) that the selected customer payment method is active (that is, available for recording payments). | [optional]
**cash_account** | [**\OpenAPI\Client\Model\CashAccountInCustomerPaymentMethodDto**](CashAccountInCustomerPaymentMethodDto.md) |  | [optional]
**card_or_account_no** | **string** | The top part &amp;gt; Card/account no. &amp;gt; The identifier for the customer&#39;s payment method. | [optional]
**payment_method_details** | [**\OpenAPI\Client\Model\CustomerPaymentMethodDetailDto[]**](CustomerPaymentMethodDetailDto.md) | Payment method details tab &amp;gt; The specific elements on this tab depend on the selected payment method, which is defined in the window. | [optional]
**time_stamp** | **string** | Identifier that represents a specific version of the resource.  It helps to prevent simultaneous updates of the resource from overwriting each other (by using ETags and If-Match headers) | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

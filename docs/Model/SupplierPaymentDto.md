# # SupplierPaymentDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **string** | The top part &amp;gt; Type &amp;gt;The type of supplier ledger payment document. The following types are available: Payment, PUrchase credit note, Prepayment, Supplier refund, Voided payment. | [optional]
**document_type** | **string** | The top part &amp;gt; Voucher no. &amp;gt; The unique identifier of the supplier ledger document. | [optional]
**ref_nbr** | **string** | The top part &amp;gt; Voucher no. &amp;gt; The unique identifier of the supplier ledger document. | [optional]
**status** | **string** | The top part &amp;gt; Status &amp;gt; The status of the supplier ledger document, which can be one of the following: On Hold, Printed, Open, Reserved, Closed, Voided, Released. | [optional]
**hold** | **bool** | The top part &amp;gt; Hold &amp;gt; A check box that means (if selected) that the status of the document is On hold. | [optional]
**application_date** | **\DateTime** | Mandatory field: The top part &amp;gt; Date* &amp;gt; The date when the payment is applied. The default value is the current business date. | [optional]
**application_period** | **string** | MAndatory field: The top part &amp;gt; Financial period* &amp;gt; The financial period of payment application. | [optional]
**payment_ref** | **string** | The top part &amp;gt; Payment ref. &amp;gt; A payment reference number. | [optional]
**supplier** | [**\OpenAPI\Client\Model\SupplierInSupplierPaymentDto**](SupplierInSupplierPaymentDto.md) |  | [optional]
**location** | [**\OpenAPI\Client\Model\LocationInSupplierPaymentDto**](LocationInSupplierPaymentDto.md) |  | [optional]
**payment_method** | **string** | Mandatory field: The top part &amp;gt; Payment method* &amp;gt; The payment method associated with the supplier. | [optional]
**cash_account** | **string** | Mandatory field: The top part &amp;gt; Cash account* &amp;gt; The cash account associated with the payment method. | [optional]
**currency** | [**\OpenAPI\Client\Model\CurrencyInSupplierPaymentDto**](CurrencyInSupplierPaymentDto.md) |  | [optional]
**description** | **string** | The top part &amp;gt; Description &amp;gt; A description for the payment. You may use up to 50 alphanumeric characters. | [optional]
**payment_amount** | **float** | The top part &amp;gt; Payment amount &amp;gt; The total payment amount that should be applied to the documents. | [optional]
**finance_charges** | **float** | The top part &amp;gt; Finance charges &amp;gt; The total on all finance charges applied to this document. | [optional]
**balance** | **float** | Balance of the payment remaining to be applied and released. Only released applications will count towards the balance. | [optional]
**unapplied_balance** | **float** | The top part &amp;gt; Unapplied balance &amp;gt; The balance that has not been applied. This will be a non-zero value if the payment amount is not equal to a document&#39;s total amount. Checks shall always have a zero unapplied balance. | [optional]
**applied_amount** | **float** | The top part &amp;gt; Amount &amp;gt; The amount to be applied on the application date. | [optional]
**released** | **bool** | Background information: if this check box is selected, the document has been released. | [optional]
**last_modified_date_time** | **\DateTime** | Background information: The date and time when the document has been last modified. | [optional]
**branch** | **string** |  | [optional]
**payment_lines** | [**\OpenAPI\Client\Model\SupplierPaymentAdjustmentDto[]**](SupplierPaymentAdjustmentDto.md) |  | [optional]
**time_stamp** | **string** | Identifier that represents a specific version of the resource.  It helps to prevent simultaneous updates of the resource from overwriting each other (by using ETags and If-Match headers) | [optional]
**error_info** | **string** |  | [optional]
**metadata** | [**\OpenAPI\Client\Model\MetadataDto**](MetadataDto.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

# # PaymentLineDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**document_type** | **string** | Doc. type &amp;gt; The type of document to which the payment is applied. | [optional]
**ref_nbr** | **string** | Mandatory field: Ref. no.* &amp;gt; The reference number of the invoice or note to which the payment is applied. | [optional]
**amount_paid** | **float** | Amount paid &amp;gt; The amount to be paid which is displayed in the currency of the document that is selected in the window. | [optional]
**cash_discount_taken** | **float** | Cash discount taken &amp;gt; The cash discount to be taken. | [optional]
**balance_write_off** | **float** | Balance write-off &amp;gt; The amount to be written off. | [optional]
**write_off_reason_code** | [**\OpenAPI\Client\Model\WriteOffReasonCodeInPaymentLineDto**](WriteOffReasonCodeInPaymentLineDto.md) |  | [optional]
**date** | **\DateTime** | Date &amp;gt; The creation date of the customer ledger document. | [optional]
**due_date** | **\DateTime** | Due date &amp;gt; The due date of the customer ledger document. | [optional]
**cash_discount_date** | **\DateTime** | Cash disount date &amp;gt; The date through which the customer can take a cash discount. | [optional]
**balance** | **float** | Balance &amp;gt; The balance of the document after the cash discount is taken and the amount is paid. | [optional]
**cash_discount_balance** | **float** | Cash discount balance &amp;gt; The unused amount of the cash discount, in case of partial payment. | [optional]
**description** | **string** | Description &amp;gt; A description of the document. | [optional]
**currency** | **string** | Currency &amp;gt; The currency of the customer ledger document. | [optional]
**post_period** | **string** | Post period &amp;gt; The financial period to which the transactions recorded in the document should be posted. Format MMYYYY. | [optional]
**customer_order** | **string** | Customer order &amp;gt; A reference to a document of the customer, such as a purchase order number. | [optional]
**cross_rate** | **float** | Cross rate &amp;gt; A cross rate that you can optionally specify between the currency of the payment and currency of the original document. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

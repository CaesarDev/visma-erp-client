# # OrderToApplyDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**order_type** | **string** | Mandatory field: Order type* &amp;gt; The order type for which the payment is to be reserved. | [optional]
**order_no** | **string** | Mandatory field: Order no.* &amp;gt; The reference number of the order for which the payment is reserved. | [optional]
**status** | **string** | Status &amp;gt; The status of the document, which is assigned automatically. | [optional]
**applied_to_order** | **float** | Applied to order &amp;gt; The total amount reserved for the order. | [optional]
**transferred_to_invoice** | **float** | Transferred to invoice &amp;gt; The amount that has been applied to invoice. | [optional]
**date** | **\DateTime** | Date &amp;gt; The creation date of the order. | [optional]
**due_date** | **\DateTime** | Due date &amp;gt; The due date of the order. | [optional]
**cash_discount_date** | **\DateTime** | Cash discount date &amp;gt; The date through which the customer can take a cash discount. | [optional]
**balance** | **float** | Balance &amp;gt; The balance of the order after the cash discount is taken and the amount is paid. | [optional]
**description** | **string** | Description &amp;gt; A description of the order. | [optional]
**order_total** | **float** | Order total &amp;gt; The total amount of the document. | [optional]
**currency** | **string** | Currency &amp;gt; The currency of the document. | [optional]
**invoice_nbr** | **string** | Invoice no. &amp;gt; The reference number of the invoice generated for the order. | [optional]
**invoice_date** | **\DateTime** | Invoice date &amp;gt; The date of the invoice. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

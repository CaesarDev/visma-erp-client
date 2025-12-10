# # PurchaseReceiptsDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **string** | The top part &amp;gt; Type &amp;gt; The type of the document, which can be Receipt, Return, or Transfer receipt. | [optional]
**receipt_number** | **string** | The top part &amp;gt; Receipt no. &amp;gt; The unique reference number of the purchase receipt, transfer receipt, or return, which the system automatically assigns according to its number series. | [optional]
**status** | **string** | The top part &amp;gt; Status &amp;gt; The current status of the purchase or transfer receipt, or return, which the system assigns automatically. | [optional]
**supplier_name** | **string** | The top part &amp;gt; Supplier &amp;gt; The supplier from which the items have been received or to which they will be returned. | [optional]
**currency** | **string** | The top part &amp;gt; Currency &amp;gt; The currency the supplier uses for invoicing. | [optional]
**total_qty** | **float** | The top part &amp;gt; Total qty. &amp;gt; The total quantity of items received from or returned to the supplier; the sum of all quantities of all stock items listed on the Document details tab. | [optional]
**total_amt** | **float** | The top part &amp;gt; Total amt. &amp;gt; The total amount calculated for items received from or returned to the supplier; the sum of all amounts of all stock items listed on the Document details tab. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

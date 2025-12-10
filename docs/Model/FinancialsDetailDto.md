# # FinancialsDetailDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**batch_number** | **string** | Link to general ledger section &amp;gt; Batch number &amp;gt; The number of the batch generated to implement the cash transaction. | [optional]
**branch** | [**\OpenAPI\Client\Model\BranchInFinancialsDetailDto**](BranchInFinancialsDetailDto.md) |  | [optional]
**cleared** | **bool** | Link to general ledger section &amp;gt; Cleared &amp;gt; A check box that indicates (if selected) that the transaction was cleared. | [optional]
**clear_date** | **\DateTime** | Link to general ledger section &amp;gt; Clear date &amp;gt;  The date when the transaction was cleared. | [optional]
**tax_zone** | [**\OpenAPI\Client\Model\TaxZoneInFinancialsDetailDto**](TaxZoneInFinancialsDetailDto.md) |  | [optional]
**tax_calc_mode** | **string** | VAT settings section &amp;gt; VAT calculation &amp;gt; The VAT calculation mode, which defines which amounts (VAT-inclusive or VAT-exclusive) should be entered in the detail lines of a document. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

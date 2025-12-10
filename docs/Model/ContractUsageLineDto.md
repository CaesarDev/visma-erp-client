# # ContractUsageLineDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**transaction_number** | **int** |  | [optional]
**billed** | **bool** | Information indicating that the contract is collected from the Transaction history tab and the contract is invoiced. Not indicated on screen CT303000. | [optional]
**branch** | [**\OpenAPI\Client\Model\BranchInContractUsageLineDto**](BranchInContractUsageLineDto.md) |  | [optional]
**item** | [**\OpenAPI\Client\Model\ItemInContractUsageLineDto**](ItemInContractUsageLineDto.md) |  | [optional]
**description** | **string** | Both tabs &amp;gt; Description &amp;gt; A description of the non-stock item. | [optional]
**uom** | **string** | Both tabs &amp;gt; UoM &amp;gt; The unit of measure used for the item. | [optional]
**quantity** | **float** | Both tabs &amp;gt; Quantity &amp;gt; A number of units used for the item. | [optional]
**date** | **\DateTime** | Mandatory field: Both tabs &amp;gt; Date* &amp;gt; The date of the activity, case, applied labour, or other usage (for the item). | [optional]
**type** | **string** | Transaction history tab &amp;gt; Type &amp;gt; The type of the customer ledger document. | [optional]
**reference_nbr** | **string** | Transaction history tab &amp;gt; Ref. no. &amp;gt; The reference number of the document/invoice. | [optional]
**billing_date** | **\DateTime** | Transaction history tab &amp;gt; Invoicing date &amp;gt; The date when the invoice was issued. | [optional]
**last_modified_date_time** | **\DateTime** | A system generated date/time that indicates the last change for the document. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

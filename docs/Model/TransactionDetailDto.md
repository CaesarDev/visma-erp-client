# # TransactionDetailDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**line_number** | **int** | The line number in the table. | [optional]
**branch** | [**\OpenAPI\Client\Model\BranchInTransactionDetailDto**](BranchInTransactionDetailDto.md) |  | [optional]
**item** | [**\OpenAPI\Client\Model\ItemInTransactionDetailDto**](ItemInTransactionDetailDto.md) |  | [optional]
**description** | **string** | Description &amp;gt; The description provided for the item. | [optional]
**quantity** | **float** | Quantity &amp;gt; The quantity of the item. | [optional]
**uom** | **string** | UoM &amp;gt; The unit of measure of the item. | [optional]
**price** | **float** | Price &amp;gt; The unit price for the item. | [optional]
**amount** | **float** | Amount &amp;gt; The total amount for all units or items. | [optional]
**offset_cash_account** | [**\OpenAPI\Client\Model\OffsetCashAccountInTransactionDetailDto**](OffsetCashAccountInTransactionDetailDto.md) |  | [optional]
**offset_account** | [**\OpenAPI\Client\Model\OffsetAccountInTransactionDetailDto**](OffsetAccountInTransactionDetailDto.md) |  | [optional]
**offset_sub_account** | [**\OpenAPI\Client\Model\OffsetSubAccountInTransactionDetailDto**](OffsetSubAccountInTransactionDetailDto.md) |  | [optional]
**tax_category** | [**\OpenAPI\Client\Model\TaxCategoryInTransactionDetailDto**](TaxCategoryInTransactionDetailDto.md) |  | [optional]
**non_billable** | **bool** | Non-invoiceable &amp;gt; A check box that indicates (if selected) that this transaction is non-invoiceable in the project. | [optional]
**project** | [**\OpenAPI\Client\Model\ProjectInTransactionDetailDto**](ProjectInTransactionDetailDto.md) |  | [optional]
**project_task** | [**\OpenAPI\Client\Model\ProjectTaskInTransactionDetailDto**](ProjectTaskInTransactionDetailDto.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

# # InventoryUpdateDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**inventory_number** | [**\OpenAPI\Client\Model\InventoryNumberInInventoryUpdateDto**](InventoryNumberInInventoryUpdateDto.md) |  | [optional]
**status** | [**\OpenAPI\Client\Model\DtoValueOfInventoryStatus**](DtoValueOfInventoryStatus.md) |  | [optional]
**type** | [**\OpenAPI\Client\Model\DtoValueOfInventoryType**](DtoValueOfInventoryType.md) |  | [optional]
**description** | [**\OpenAPI\Client\Model\DtoValueOfString**](DtoValueOfString.md) |  | [optional]
**body** | [**\OpenAPI\Client\Model\DtoValueOfString**](DtoValueOfString.md) |  | [optional]
**item_class** | [**\OpenAPI\Client\Model\ItemClassInInventoryUpdateDto**](ItemClassInInventoryUpdateDto.md) |  | [optional]
**posting_class** | [**\OpenAPI\Client\Model\PostingClassInInventoryUpdateDto**](PostingClassInInventoryUpdateDto.md) |  | [optional]
**vat_code** | [**\OpenAPI\Client\Model\VatCodeInInventoryUpdateDto**](VatCodeInInventoryUpdateDto.md) |  | [optional]
**default_price** | [**\OpenAPI\Client\Model\DefaultPriceInInventoryUpdateDto**](DefaultPriceInInventoryUpdateDto.md) |  | [optional]
**base_unit** | [**\OpenAPI\Client\Model\DtoValueOfString**](DtoValueOfString.md) |  | [optional]
**sales_unit** | [**\OpenAPI\Client\Model\DtoValueOfString**](DtoValueOfString.md) |  | [optional]
**purchase_unit** | [**\OpenAPI\Client\Model\DtoValueOfString**](DtoValueOfString.md) |  | [optional]
**expense_accrual_account** | [**\OpenAPI\Client\Model\ExpenseAccrualAccountInInventoryUpdateDto**](ExpenseAccrualAccountInInventoryUpdateDto.md) |  | [optional]
**inventory_account** | [**\OpenAPI\Client\Model\InventoryAccountInInventoryUpdateDto**](InventoryAccountInInventoryUpdateDto.md) |  | [optional]
**expense_account** | [**\OpenAPI\Client\Model\ExpenseAccountInInventoryUpdateDto**](ExpenseAccountInInventoryUpdateDto.md) |  | [optional]
**cogs_account** | [**\OpenAPI\Client\Model\CogsAccountInInventoryUpdateDto**](CogsAccountInInventoryUpdateDto.md) |  | [optional]
**expense_non_taxable_account** | [**\OpenAPI\Client\Model\DtoValueOfString**](DtoValueOfString.md) |  | [optional]
**expense_eu_account** | [**\OpenAPI\Client\Model\DtoValueOfString**](DtoValueOfString.md) |  | [optional]
**expense_import_account** | [**\OpenAPI\Client\Model\DtoValueOfString**](DtoValueOfString.md) |  | [optional]
**expense_subaccount** | [**\OpenAPI\Client\Model\SegmentUpdateDto[]**](SegmentUpdateDto.md) | Only used for Non-stock items | [optional]
**cogs_subaccount** | [**\OpenAPI\Client\Model\SegmentUpdateDto[]**](SegmentUpdateDto.md) | Only used for Stock items | [optional]
**sales_account** | [**\OpenAPI\Client\Model\DtoValueOfString**](DtoValueOfString.md) |  | [optional]
**sales_non_taxable_account** | [**\OpenAPI\Client\Model\DtoValueOfString**](DtoValueOfString.md) |  | [optional]
**sales_eu_account** | [**\OpenAPI\Client\Model\DtoValueOfString**](DtoValueOfString.md) |  | [optional]
**sales_export_account** | [**\OpenAPI\Client\Model\DtoValueOfString**](DtoValueOfString.md) |  | [optional]
**sales_subaccount** | [**\OpenAPI\Client\Model\SegmentUpdateDto[]**](SegmentUpdateDto.md) |  | [optional]
**attribute_lines** | [**\OpenAPI\Client\Model\AttributeLineUpdateDto[]**](AttributeLineUpdateDto.md) |  | [optional]
**packaging** | [**\OpenAPI\Client\Model\PackagingUpdateDto**](PackagingUpdateDto.md) |  | [optional]
**supplier_details** | [**\OpenAPI\Client\Model\SupplierDetailsDto[]**](SupplierDetailsDto.md) |  | [optional]
**intrastat** | [**\OpenAPI\Client\Model\IntrastatUpdateDto**](IntrastatUpdateDto.md) |  | [optional]
**cross_references** | [**\OpenAPI\Client\Model\CrossReferenceUpdateDto[]**](CrossReferenceUpdateDto.md) |  | [optional]
**default_warehouse** | [**\OpenAPI\Client\Model\DefaultWarehouseInInventoryUpdateDto**](DefaultWarehouseInInventoryUpdateDto.md) |  | [optional]
**default_issue_from** | [**\OpenAPI\Client\Model\DefaultIssueFromInInventoryUpdateDto**](DefaultIssueFromInInventoryUpdateDto.md) |  | [optional]
**default_receipt_to** | [**\OpenAPI\Client\Model\DefaultReceiptToInInventoryUpdateDto**](DefaultReceiptToInInventoryUpdateDto.md) |  | [optional]
**kit_item** | [**\OpenAPI\Client\Model\DtoValueOfNullableOfBoolean**](DtoValueOfNullableOfBoolean.md) |  | [optional]
**note** | [**\OpenAPI\Client\Model\DtoValueOfString**](DtoValueOfString.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

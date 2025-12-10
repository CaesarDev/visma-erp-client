# # SupplierInvoiceLineUpdateDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**operation** | **string** |  | [optional]
**line_number** | [**\OpenAPI\Client\Model\DtoValueOfInt32**](DtoValueOfInt32.md) |  | [optional]
**inventory_number** | [**\OpenAPI\Client\Model\DtoValueOfString**](DtoValueOfString.md) |  | [optional]
**transaction_description** | [**\OpenAPI\Client\Model\DtoValueOfString**](DtoValueOfString.md) |  | [optional]
**quantity** | [**\OpenAPI\Client\Model\DtoValueOfDecimal**](DtoValueOfDecimal.md) |  | [optional]
**uom** | [**\OpenAPI\Client\Model\DtoValueOfString**](DtoValueOfString.md) |  | [optional]
**unit_cost_in_currency** | [**\OpenAPI\Client\Model\DtoValueOfNullableOfDecimal**](DtoValueOfNullableOfDecimal.md) |  | [optional]
**cost_in_currency** | [**\OpenAPI\Client\Model\DtoValueOfNullableOfDecimal**](DtoValueOfNullableOfDecimal.md) |  | [optional]
**discount_percent** | [**\OpenAPI\Client\Model\DtoValueOfNullableOfDecimal**](DtoValueOfNullableOfDecimal.md) |  | [optional]
**discount_amount_in_currency** | [**\OpenAPI\Client\Model\DtoValueOfNullableOfDecimal**](DtoValueOfNullableOfDecimal.md) |  | [optional]
**discount_unit_cost_in_currency** | [**\OpenAPI\Client\Model\DtoValueOfNullableOfDecimal**](DtoValueOfNullableOfDecimal.md) |  | [optional]
**manual_discount** | [**\OpenAPI\Client\Model\DtoValueOfNullableOfBoolean**](DtoValueOfNullableOfBoolean.md) |  | [optional]
**account_number** | [**\OpenAPI\Client\Model\DtoValueOfString**](DtoValueOfString.md) |  | [optional]
**subaccount** | [**\OpenAPI\Client\Model\SegmentUpdateDto[]**](SegmentUpdateDto.md) |  | [optional]
**deferral_schedule** | [**\OpenAPI\Client\Model\DtoValueOfNullableOfInt32**](DtoValueOfNullableOfInt32.md) |  | [optional]
**deferral_code** | [**\OpenAPI\Client\Model\DtoValueOfString**](DtoValueOfString.md) |  | [optional]
**vat_code_id** | [**\OpenAPI\Client\Model\DtoValueOfString**](DtoValueOfString.md) |  | [optional]
**branch** | [**\OpenAPI\Client\Model\BranchInSupplierInvoiceLineUpdateDto**](BranchInSupplierInvoiceLineUpdateDto.md) |  | [optional]
**branch_number** | [**\OpenAPI\Client\Model\DtoValueOfString**](DtoValueOfString.md) |  | [optional]
**note** | [**\OpenAPI\Client\Model\DtoValueOfString**](DtoValueOfString.md) |  | [optional]
**project_id** | [**\OpenAPI\Client\Model\DtoValueOfString**](DtoValueOfString.md) |  | [optional]
**project_internal_id** | [**\OpenAPI\Client\Model\DtoValueOfNullableOfInt32**](DtoValueOfNullableOfInt32.md) |  | [optional]
**project_task_id** | [**\OpenAPI\Client\Model\DtoValueOfString**](DtoValueOfString.md) |  | [optional]
**project_task_internal_id** | [**\OpenAPI\Client\Model\DtoValueOfNullableOfInt32**](DtoValueOfNullableOfInt32.md) |  | [optional]
**split_line** | [**\OpenAPI\Client\Model\DtoValueOfBoolean**](DtoValueOfBoolean.md) |  | [optional]
**undo_split_line** | [**\OpenAPI\Client\Model\DtoValueOfBoolean**](DtoValueOfBoolean.md) |  | [optional]
**split_hierarchy** | [**\OpenAPI\Client\Model\DtoValueOfString**](DtoValueOfString.md) |  | [optional]
**retainage_pct** | [**\OpenAPI\Client\Model\DtoValueOfNullableOfDecimal**](DtoValueOfNullableOfDecimal.md) |  | [optional]
**cury_retainage_amt** | [**\OpenAPI\Client\Model\DtoValueOfNullableOfDecimal**](DtoValueOfNullableOfDecimal.md) |  | [optional]
**link_line** | [**\OpenAPI\Client\Model\LinkLineDto**](LinkLineDto.md) |  | [optional]
**term_start_date** | [**\OpenAPI\Client\Model\DtoValueOfNullableOfDateTime**](DtoValueOfNullableOfDateTime.md) |  | [optional]
**term_end_date** | [**\OpenAPI\Client\Model\DtoValueOfNullableOfDateTime**](DtoValueOfNullableOfDateTime.md) |  | [optional]
**external_inventory_id** | [**\OpenAPI\Client\Model\DtoValueOfString**](DtoValueOfString.md) |  | [optional]
**prebook_account_number** | [**\OpenAPI\Client\Model\PrebookAccountNumberInSupplierInvoiceLineUpdateDto**](PrebookAccountNumberInSupplierInvoiceLineUpdateDto.md) |  | [optional]
**prebook_subaccount** | [**\OpenAPI\Client\Model\SegmentUpdateDto[]**](SegmentUpdateDto.md) | Subaccount used for prebooking. Note that this feature is not available for all countries. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

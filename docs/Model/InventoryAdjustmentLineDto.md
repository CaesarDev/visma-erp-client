# # InventoryAdjustmentLineDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**warehouse** | [**\OpenAPI\Client\Model\WarehouseInInventoryAdjustmentLineDto**](WarehouseInInventoryAdjustmentLineDto.md) |  | [optional]
**unit_cost** | **float** | Unit cost &amp;gt; The cost of the unit used as base unit for the stock item. | [optional]
**ext_cost** | **float** | Cost &amp;gt; The cost of the item. | [optional]
**receipt_number** | **string** | Receipt no. &amp;gt; Reference number for the receipt for the stock item. | [optional]
**po_receipt_number** | **string** | Purchase order receipt number | [optional]
**line_number** | **int** |  | [optional]
**inventory_item** | [**\OpenAPI\Client\Model\InventoryItemInInventoryAdjustmentLineDto**](InventoryItemInInventoryAdjustmentLineDto.md) |  | [optional]
**location** | [**\OpenAPI\Client\Model\LocationInInventoryAdjustmentLineDto**](LocationInInventoryAdjustmentLineDto.md) |  | [optional]
**quantity** | **float** | Quantity &amp;gt; The quantity of the transferred goods (in the units indicated below). | [optional]
**uom** | **string** | Mandatory field: UoM* &amp;gt; The unit of measure (UoM) used for the goods to be transferred. | [optional]
**reason_code** | [**\OpenAPI\Client\Model\ReasonCodeInInventoryAdjustmentLineDto**](ReasonCodeInInventoryAdjustmentLineDto.md) |  | [optional]
**description** | **string** | Description &amp;gt; A brief description of the goods transfer transaction. | [optional]
**attachments** | [**\OpenAPI\Client\Model\AttachmentDto[]**](AttachmentDto.md) |  | [optional]
**branch_number** | [**\OpenAPI\Client\Model\BranchNumberDto**](BranchNumberDto.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

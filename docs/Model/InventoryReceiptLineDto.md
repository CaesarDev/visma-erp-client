# # InventoryReceiptLineDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**warehouse** | [**\OpenAPI\Client\Model\WarehouseInInventoryReceiptLineDto**](WarehouseInInventoryReceiptLineDto.md) |  | [optional]
**unit_cost** | **float** | Unit cost &amp;gt; The cost of a unit of the received stock item. | [optional]
**ext_cost** | **float** | Cost &amp;gt; The extended cost of the received stock item. An extended cost is calculated automatically as the unit cost multiplied by the quantity (or amount) of item that was received. | [optional]
**project** | [**\OpenAPI\Client\Model\ProjectInInventoryReceiptLineDto**](ProjectInInventoryReceiptLineDto.md) |  | [optional]
**project_task** | [**\OpenAPI\Client\Model\ProjectTaskInInventoryReceiptLineDto**](ProjectTaskInInventoryReceiptLineDto.md) |  | [optional]
**allocations** | [**\OpenAPI\Client\Model\INAllocationsDto[]**](INAllocationsDto.md) |  | [optional]
**po_receipt_number** | **string** | Purchase order receipt number | [optional]
**line_number** | **int** |  | [optional]
**inventory_item** | [**\OpenAPI\Client\Model\InventoryItemInInventoryReceiptLineDto**](InventoryItemInInventoryReceiptLineDto.md) |  | [optional]
**location** | [**\OpenAPI\Client\Model\LocationInInventoryReceiptLineDto**](LocationInInventoryReceiptLineDto.md) |  | [optional]
**quantity** | **float** | Quantity &amp;gt; The quantity of the transferred goods (in the units indicated below). | [optional]
**uom** | **string** | Mandatory field: UoM* &amp;gt; The unit of measure (UoM) used for the goods to be transferred. | [optional]
**reason_code** | [**\OpenAPI\Client\Model\ReasonCodeInInventoryReceiptLineDto**](ReasonCodeInInventoryReceiptLineDto.md) |  | [optional]
**description** | **string** | Description &amp;gt; A brief description of the goods transfer transaction. | [optional]
**attachments** | [**\OpenAPI\Client\Model\AttachmentDto[]**](AttachmentDto.md) |  | [optional]
**branch_number** | [**\OpenAPI\Client\Model\BranchNumberDto**](BranchNumberDto.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

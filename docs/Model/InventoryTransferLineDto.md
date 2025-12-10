# # InventoryTransferLineDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**to_location** | [**\OpenAPI\Client\Model\LocationDescriptionDto**](LocationDescriptionDto.md) |  | [optional]
**lot_serial_number** | **string** |  | [optional]
**expiration_date** | **\DateTime** |  | [optional]
**allocations** | [**\OpenAPI\Client\Model\AllocationsBasicDto[]**](AllocationsBasicDto.md) |  | [optional]
**line_number** | **int** |  | [optional]
**inventory_item** | [**\OpenAPI\Client\Model\InventoryItemInInventoryTransferLineDto**](InventoryItemInInventoryTransferLineDto.md) |  | [optional]
**location** | [**\OpenAPI\Client\Model\LocationInInventoryTransferLineDto**](LocationInInventoryTransferLineDto.md) |  | [optional]
**quantity** | **float** | Quantity &amp;gt; The quantity of the transferred goods (in the units indicated below). | [optional]
**uom** | **string** | Mandatory field: UoM* &amp;gt; The unit of measure (UoM) used for the goods to be transferred. | [optional]
**reason_code** | [**\OpenAPI\Client\Model\ReasonCodeInInventoryTransferLineDto**](ReasonCodeInInventoryTransferLineDto.md) |  | [optional]
**description** | **string** | Description &amp;gt; A brief description of the goods transfer transaction. | [optional]
**attachments** | [**\OpenAPI\Client\Model\AttachmentDto[]**](AttachmentDto.md) |  | [optional]
**branch_number** | [**\OpenAPI\Client\Model\BranchNumberDto**](BranchNumberDto.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

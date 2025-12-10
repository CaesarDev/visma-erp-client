# # InventoryTransferDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**warehouse** | [**\OpenAPI\Client\Model\WarehouseInInventoryTransferDto**](WarehouseInInventoryTransferDto.md) |  | [optional]
**to_warehouse** | [**\OpenAPI\Client\Model\ToWarehouseInInventoryTransferDto**](ToWarehouseInInventoryTransferDto.md) |  | [optional]
**transfer_lines** | [**\OpenAPI\Client\Model\InventoryTransferLineDto[]**](InventoryTransferLineDto.md) | The Transaction details tab &amp;gt; The inventory transfer lines | [optional]
**reference_number** | **string** | The unique reference number of the receipt, which the system automatically assigns according to the numbering sequence selected for receipts on the Inventory Preferences IN.10.10.00) form. | [optional]
**status** | **string** | The current status of the receipt. The following options are available:   On Hold:The receipt/issue is a draft and can be edited. Receipts with this status cannot be released.  Balanced: The receipt/issue data has been validated by the system and the receipt can be released. It also can be modified or deleted, but changes can be saved only if the receipt is balanced.  Released: The receipt/issue has been released and cannot be edited or deleted. | [optional]
**hold** | **bool** | A check box that you select to give the receipt the On Hold status. Clear the check box to save the receipt with the Balanced status. | [optional]
**date** | **\DateTime** | The date when the inventory document was created. All transactions included in this document will have this transaction date. | [optional]
**post_period** | **string** | The financial period to which the transactions recorded in the document should be posted. Format MMYYYY. | [optional]
**external_reference** | **string** | The external reference number of the inventory issue document (for example, the vendor’s reference code). | [optional]
**description** | **string** | A brief description of the inventory issue or its transactions. | [optional]
**total_quantity** | **float** | The total quantity of inventory items, which the system calculates automatically, for the document. | [optional]
**control_quantity** | **float** | The manually entered quantity of inventory items. Control Qty. is available only if the Validate Document Totals on Entry option is selected on the Inventory Preferences form. If the Control Qty. and Total Qty.values do not match, the system generates a warning message and the issue cannot be saved. | [optional]
**batch_number** | **string** | The reference number of the batch generated for the receipt. Click the number to open the Journal Transactions (GL.30.10.00) form and view the details of the transactions. | [optional]
**last_modified_date_time** | **\DateTime** | The date when the document was last modified. | [optional]
**branch_number** | [**\OpenAPI\Client\Model\BranchNumberInInventoryTransferDto**](BranchNumberInInventoryTransferDto.md) |  | [optional]
**attachments** | [**\OpenAPI\Client\Model\AttachmentDto[]**](AttachmentDto.md) | The data containing information about the document attachments | [optional]
**timestamp** | **string** | Timestamp of the inventory document | [optional]
**error_info** | **string** |  | [optional]
**metadata** | [**\OpenAPI\Client\Model\MetadataDto**](MetadataDto.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

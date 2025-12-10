# # InventoryIssueLineDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**transaction_type** | **string** | Trans. type &amp;gt; The type of inventory issue transaction. Select one of the following types: Issue, Return, Invoice, Debit note, Credit note. | [optional]
**warehouse** | [**\OpenAPI\Client\Model\WarehouseInInventoryIssueLineDto**](WarehouseInInventoryIssueLineDto.md) |  | [optional]
**unit_cost** | **float** | Unit cost &amp;gt; The cost of the specified unit of this stock item. | [optional]
**ext_cost** | **float** | Ext. cost &amp;gt; The extended cost of the specified stock item. An extended cost is calculated automatically as the unit cost multiplied by the quantity of units involved in this transaction. | [optional]
**unit_price** | **float** | Unit price &amp;gt; The price of the specified unit of this stock item. | [optional]
**ext_price** | **float** | Ext. price &amp;gt; The extended price of the specified stock item, calculated automatically as the unit price multiplied by the quantity of the stock item involved in the inventory issue operation. | [optional]
**project** | [**\OpenAPI\Client\Model\ProjectInInventoryIssueLineDto**](ProjectInInventoryIssueLineDto.md) |  | [optional]
**project_task** | [**\OpenAPI\Client\Model\ProjectTaskInInventoryIssueLineDto**](ProjectTaskInInventoryIssueLineDto.md) |  | [optional]
**lot_serial_number** | **string** |  | [optional]
**expiration_date** | **\DateTime** |  | [optional]
**allocations** | [**\OpenAPI\Client\Model\INAllocationsDto[]**](INAllocationsDto.md) |  | [optional]
**po_receipt_number** | **string** | Purchase order receipt number | [optional]
**line_number** | **int** |  | [optional]
**inventory_item** | [**\OpenAPI\Client\Model\InventoryItemInInventoryIssueLineDto**](InventoryItemInInventoryIssueLineDto.md) |  | [optional]
**location** | [**\OpenAPI\Client\Model\LocationInInventoryIssueLineDto**](LocationInInventoryIssueLineDto.md) |  | [optional]
**quantity** | **float** | Quantity &amp;gt; The quantity of the transferred goods (in the units indicated below). | [optional]
**uom** | **string** | Mandatory field: UoM* &amp;gt; The unit of measure (UoM) used for the goods to be transferred. | [optional]
**reason_code** | [**\OpenAPI\Client\Model\ReasonCodeInInventoryIssueLineDto**](ReasonCodeInInventoryIssueLineDto.md) |  | [optional]
**description** | **string** | Description &amp;gt; A brief description of the goods transfer transaction. | [optional]
**attachments** | [**\OpenAPI\Client\Model\AttachmentDto[]**](AttachmentDto.md) |  | [optional]
**branch_number** | [**\OpenAPI\Client\Model\BranchNumberDto**](BranchNumberDto.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

# # WarehouseLocationDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**location_id** | **string** | Location ID &amp;gt; The unique ID of the warehouse location. | [optional]
**description** | **string** | Description &amp;gt; A brief description of the warehouse location. | [optional]
**active** | **bool** | Active &amp;gt; This check box indicates whether this location is active. | [optional]
**incl_qty_avail** | **bool** | Include in qty. available &amp;gt; You select this check box if the quantities of goods available at this location will be included in the quantities of available goods and used in inventory transactions, such as issues and transfers. | [optional]
**is_costed** | **bool** | Cost separately &amp;gt; You select this check box if the costs for goods available at this location will be calculated separately from costs calculated at the system-level; that is, for FIFO and specific valuation methods, separate cost layers will be created for this location. | [optional]
**sales_valid** | **bool** | Sales allowed &amp;gt; You select this check box if sales are allowed from this location. | [optional]
**receipts_valid** | **bool** | Receipts allowed &amp;gt; You select this check box if receipts are allowed at this location. | [optional]
**transfers_valid** | **bool** | Transfers allowed &amp;gt; You select this check box if transfers are allowed for this location. | [optional]
**assembly_valid** | **bool** | Assembly allowed &amp;gt; You select this check box if assembly operations are allowed at this location. | [optional]
**primary_item_valid** | **string** | Primary item validation &amp;gt; An option indicating whether the operations with the primary item should be validated for this location and how. | [optional]
**primary_item** | [**\OpenAPI\Client\Model\PrimaryItemInWarehouseLocationDto**](PrimaryItemInWarehouseLocationDto.md) |  | [optional]
**primary_item_class** | [**\OpenAPI\Client\Model\PrimaryItemClassInWarehouseLocationDto**](PrimaryItemClassInWarehouseLocationDto.md) |  | [optional]
**project** | [**\OpenAPI\Client\Model\ProjectInWarehouseLocationDto**](ProjectInWarehouseLocationDto.md) |  | [optional]
**project_task** | [**\OpenAPI\Client\Model\ProjectTaskInWarehouseLocationDto**](ProjectTaskInWarehouseLocationDto.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

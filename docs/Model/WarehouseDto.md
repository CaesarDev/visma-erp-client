# # WarehouseDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**warehouse_id** | **string** | Mandatory field: The top part &amp;gt; Warehouse ID* &amp;gt; The unique ID of the warehouse. | [optional]
**branch** | [**\OpenAPI\Client\Model\BranchInWarehouseDto**](BranchInWarehouseDto.md) |  | [optional]
**replenishment_class** | [**\OpenAPI\Client\Model\ReplenishmentClassInWarehouseDto**](ReplenishmentClassInWarehouseDto.md) |  | [optional]
**active** | **bool** | The top part &amp;gt; Active &amp;gt; This check box indicates (if selected) that the warehouse is active. | [optional]
**lock_site_pi_count_entry** | **bool** | The top part &amp;gt; Freeze the inventory when the stocktaking is in data entry state &amp;gt; This check box indicates (if selected) that the inventory in the warehouse will be frozen during the stocktaking and data entry stages of stocktaking. | [optional]
**description** | **string** | The top part &amp;gt; Description &amp;gt; A brief description of the warehouse. | [optional]
**location_entry** | **string** | The top part &amp;gt; Location entry &amp;gt; An option indicating whether warehouse locations can be added directly on any inventory document or only by using this window. | [optional]
**avg_default_cost** | **string** | The top part &amp;gt; Avg. default return cost &amp;gt; For items with the Average valuation method, the option that defines which of costs should be used for returns and receipts. | [optional]
**fifo_default_cost** | **string** | The top part &amp;gt; FIFO default returns cost &amp;gt; For items with the FIFO valuation method, the option that defines which of costs should be used for returns and receipts. | [optional]
**receipt_location** | [**\OpenAPI\Client\Model\ReceiptLocationInWarehouseDto**](ReceiptLocationInWarehouseDto.md) |  | [optional]
**ship_location** | [**\OpenAPI\Client\Model\ShipLocationInWarehouseDto**](ShipLocationInWarehouseDto.md) |  | [optional]
**return_location** | [**\OpenAPI\Client\Model\ReturnLocationInWarehouseDto**](ReturnLocationInWarehouseDto.md) |  | [optional]
**drop_ship_location** | [**\OpenAPI\Client\Model\DropShipLocationInWarehouseDto**](DropShipLocationInWarehouseDto.md) |  | [optional]
**contact** | [**\OpenAPI\Client\Model\ContactInWarehouseDto**](ContactInWarehouseDto.md) |  | [optional]
**address** | [**\OpenAPI\Client\Model\AddressInWarehouseDto**](AddressInWarehouseDto.md) |  | [optional]
**locations** | [**\OpenAPI\Client\Model\WarehouseLocationDto[]**](WarehouseLocationDto.md) | Location table tab &amp;gt; The location table &amp;gt; | [optional]
**timestamp** | **string** | Timestamp of the warehouse record | [optional]
**metadata** | [**\OpenAPI\Client\Model\MetadataDto**](MetadataDto.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

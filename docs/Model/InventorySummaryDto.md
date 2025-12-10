# # InventorySummaryDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**inventory** | [**\OpenAPI\Client\Model\InventoryInInventorySummaryDto**](InventoryInInventorySummaryDto.md) |  | [optional]
**warehouse** | [**\OpenAPI\Client\Model\WarehouseInInventorySummaryDto**](WarehouseInInventorySummaryDto.md) |  | [optional]
**location** | [**\OpenAPI\Client\Model\LocationInInventorySummaryDto**](LocationInInventorySummaryDto.md) |  | [optional]
**available** | **float** | The table &amp;gt; Available &amp;gt; The quantity of the stock items available at the specific warehouse and location. | [optional]
**available_for_shipment** | **float** | The table &amp;gt; Available for shipment &amp;gt; The quantity of the stock items available at the specific warehouse and location calculated based on the quantity on hand with the quantities shipped and on shipping deducted. | [optional]
**not_available** | **float** | The table &amp;gt; Not available &amp;gt; The quantity of the stock items on locations for which the Include in qty. available option is not selected. | [optional]
**so_booked** | **float** | The table &amp;gt; Sales order booked &amp;gt; The quantity of the stock items booked according to sales orders. | [optional]
**so_allocated** | **float** | The table &amp;gt; Sales order allocated &amp;gt; The quantity of stock items set aside according to sales orders. | [optional]
**so_shipped** | **float** | The table &amp;gt; Sales orders shipped &amp;gt; The quantity of the stock items shipped according to the confirmed shipments. | [optional]
**so_back_ordered** | **float** | The table &amp;gt; Back orders &amp;gt; The quantity of the stock items on sales orders with the Back order status. | [optional]
**in_issues** | **float** | The table &amp;gt; Inventory issues &amp;gt; The quantity of the stock items included in the inventory issue documents that have not yet been released. | [optional]
**in_receipts** | **float** | The table &amp;gt; Invnetory receipts &amp;gt; The quantity of the stock items included in the inventory receipt documents that have not yet been released. | [optional]
**in_transit** | **float** | The table &amp;gt; In transit &amp;gt; The quantity of the stock items included as in transit quantities in the inventory transfer documents that have not yet been released. | [optional]
**in_assembly_demand** | **float** | The table &amp;gt; In assembly demand &amp;gt; The quantity of the stock items included in unreleased kit assembly documents as components or kits, depending on whether the item is a kit or a kit component. | [optional]
**in_assembly_supply** | **float** | The table &amp;gt; In assembly supply &amp;gt; The quantity of the stock items listed on unreleased kit assembly documents. | [optional]
**purchase_prepared** | **float** | The table &amp;gt; Purchase prepared &amp;gt; The quantity of the stock items listed on purchase orders pending approval and on hold. | [optional]
**purchase_orders** | **float** | The table &amp;gt; Purchase orders &amp;gt; The quantity of the stock items included in open purchase orders. To view the purchase orders, open the Purchase orders (PO301000) window. | [optional]
**po_receipts** | **float** | The table &amp;gt; Purchase order receipts &amp;gt; The quantity of the stock items included in the purchase receipts that have not yet been released. To view the purchase receipts, open the Purchase receipts (PO302000) window. | [optional]
**expired** | **float** | The table &amp;gt; Expired &amp;gt; The quantity of the stock items that has reached its expiration date. | [optional]
**on_hand** | **float** | The table &amp;gt; On hand &amp;gt; The quantity of the stock items available on hand at the specified warehouse and location. | [optional]
**so_to_purchase** | **float** | The table &amp;gt; Sales order to purchase &amp;gt; The quantity of the stock items included in unreleased sales orders requiring creating purchase orders. | [optional]
**purchase_for_so** | **float** | The table &amp;gt; Purchase for sales order. &amp;gt; The quantity of the stock items listed on open purchase orders created for sales orders. | [optional]
**purchase_for_so_prepared** | **float** | The table &amp;gt; Purchase for sales order prepared &amp;gt; The quantity of the stock items listed on purchase orders yet on hold or pending approval and created for back orders. | [optional]
**purchase_for_so_receipts** | **float** | The table &amp;gt; Purchase for sales order receipts &amp;gt; The quantity of the stock items listed on purchase receipts for orders that were created for sales orders. | [optional]
**so_to_drop_ship** | **float** | The table &amp;gt; Sales order to drop-ship &amp;gt; The quantity of the stock items included in open purchase orders created for drop-ship orders. | [optional]
**drop_ship_for_so** | **float** | The table &amp;gt; Drop-ship for sales order &amp;gt; The quantity of the stock items listed on open drop-ship orders. This value is not included in the quantity available. | [optional]
**drop_ship_for_so_prepared** | **float** | The table &amp;gt; Drop-ship for sales order, prepared &amp;gt; The quantity of the stock items listed on drop-ship sales orders with a status of On hold or Pending approval; this value is not included in the quantity available. | [optional]
**drop_ship_for_so_receipts** | **float** | The table &amp;gt; Drop-ship for sales order, receipts &amp;gt; The quantity of the stock items listed on receipts for drop-ship sales orders; this value is not included in the quantity available. | [optional]
**base_unit** | **string** | The table &amp;gt; Base unit &amp;gt; The unit of measure (UoM) selected as the base unit for the stock items in the Stock items (IN202500) window. | [optional]
**estimated_unit_cost** | **float** | The table &amp;gt; Estimated unit cost &amp;gt; The estimated unit cost of the selected stock items. | [optional]
**estimated_total_cost** | **float** | The table &amp;gt; Estimated total cost &amp;gt; The estimated total cost of the stock items available at the specified warehouse and location. | [optional]
**error_info** | **string** |  | [optional]
**metadata** | [**\OpenAPI\Client\Model\MetadataDto**](MetadataDto.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

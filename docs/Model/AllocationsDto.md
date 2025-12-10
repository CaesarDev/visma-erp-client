# # AllocationsDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**line_nbr** | **int** | Line no. &amp;gt; The line of the purchase order that contains the selected item. | [optional]
**item_id** | **string** | ItemId &amp;gt; The id of the item. | [optional]
**location** | [**\OpenAPI\Client\Model\LocationInAllocationsDto**](LocationInAllocationsDto.md) |  | [optional]
**lot_serial_number** | **string** | Lot/Serial no. &amp;gt; The lot or serial number of the item. | [optional]
**quantity** | **float** | Quantity &amp;gt; The quantity of the stock item with the same lot number. It is 1 for items with serial numbers. | [optional]
**uom** | **string** | UoM &amp;gt; The unit of measure for the specified quantity of the inventory item. | [optional]
**expiration_date** | **\DateTime** | Expiration date &amp;gt; The expiration date of the specified quantity of the stock item. | [optional]
**description** | **string** | Description &amp;gt; The description of the stock item. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

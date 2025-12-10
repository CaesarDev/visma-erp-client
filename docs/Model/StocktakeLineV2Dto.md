# # StocktakeLineV2Dto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | **string** | Stocktaking details tab &amp;gt; Status &amp;gt; The status of the line of the stocktaking document, which indicates whether the actual physical quantity has been specified for the line. | [optional]
**line_nbr** | **int** | Stocktaking details tab &amp;gt; Line no. &amp;gt; The number of the line in the stocktaking document. | [optional]
**tag_nbr** | **int** | Stocktaking details tab &amp;gt; Tag no. &amp;gt; The tag number for the line item, which is the stock item with the properties specified in the line, such as location, subitem, and lot or serial number. | [optional]
**inventory** | [**\OpenAPI\Client\Model\InventoryInStocktakeLineV2Dto**](InventoryInStocktakeLineV2Dto.md) |  | [optional]
**location** | [**\OpenAPI\Client\Model\LocationInStocktakeLineV2Dto**](LocationInStocktakeLineV2Dto.md) |  | [optional]
**warehouse** | [**\OpenAPI\Client\Model\WarehouseInStocktakeLineV2Dto**](WarehouseInStocktakeLineV2Dto.md) |  | [optional]
**lot_serial_nbr** | **string** | Stocktaking details tab &amp;gt; Lot/serial number &amp;gt; The lot or serial number of the item. | [optional]
**expiration_date** | **\DateTime** | Stocktaking details tab &amp;gt; Expiration date &amp;gt; The expiration date of the item with this specific lot or serial number. | [optional]
**book_quantity** | **float** | Stocktaking details tab &amp;gt; Book quantity &amp;gt; The book quantity of the item, which is calculated based on the system records. | [optional]
**physical_quantity** | **float** | Stocktaking details tab &amp;gt; Physical quantity &amp;gt; The physical quantity of the item as entered manually. | [optional]
**variance_quantity** | **float** | Stocktaking details tab &amp;gt; Variance quantity &amp;gt; The difference between the book quantity and the physical quantity for the line item. | [optional]
**unit_cost** | **float** | Stocktaking details tab &amp;gt; Unit cost &amp;gt; The last cost of the item’s base unit as approximation of its unit cost during the count. | [optional]
**ext_variance_cost** | **float** | Stocktaking details tab &amp;gt; Variance cost &amp;gt; The difference between the extended cost calculated based on the book quantity and the extended cost calculated based on the physical quantity for the item. | [optional]
**reason_code** | **string** | Stocktaking details tab &amp;gt; Reason code &amp;gt; The reason code for the item. | [optional]
**last_modified_date_time** | **\DateTime** | System generated information. | [optional]
**base_unit** | **string** | Stocktaking details tab &amp;gt; Base Unit &amp;gt; The base unit for the item. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

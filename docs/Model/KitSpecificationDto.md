# # KitSpecificationDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**kit_inventory_id** | **string** |  | [optional]
**revision** | **string** |  | [optional]
**description** | **string** |  | [optional]
**is_active** | **bool** |  | [optional]
**allow_component_addition** | **bool** |  | [optional]
**is_non_stock** | **bool** |  | [optional]
**created_date_time** | **\DateTime** |  | [optional]
**last_modified_date_time** | **\DateTime** |  | [optional]
**stock_component_lines** | [**\OpenAPI\Client\Model\KitSpecificationStockComponentsDto[]**](KitSpecificationStockComponentsDto.md) |  | [optional]
**non_stock_component_lines** | [**\OpenAPI\Client\Model\KitSpecificationNonStockComponentDto[]**](KitSpecificationNonStockComponentDto.md) |  | [optional]
**timestamp** | **string** | Timestamp of the kit specification record | [optional]
**error_info** | **string** |  | [optional]
**metadata** | [**\OpenAPI\Client\Model\MetadataDto**](MetadataDto.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

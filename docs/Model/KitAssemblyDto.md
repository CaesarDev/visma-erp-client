# # KitAssemblyDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **string** | Type, possible values: P - Production, D - Disassembly | [optional]
**ref_no** | **string** |  | [optional]
**status** | **string** | Status, possible values: H - On Hold, B - Balanced, R - Released | [optional]
**hold** | **bool** |  | [optional]
**date** | **\DateTime** |  | [optional]
**post_period** | **string** |  | [optional]
**item_id** | **string** |  | [optional]
**revision** | **string** |  | [optional]
**reason_code** | **string** |  | [optional]
**description** | **string** |  | [optional]
**warehouse** | **string** |  | [optional]
**location** | **string** |  | [optional]
**uo_m** | **string** |  | [optional]
**quantity** | **float** |  | [optional]
**created_date_time** | **\DateTime** |  | [optional]
**last_modified_date_time** | **\DateTime** |  | [optional]
**sales_order_link** | **string** |  | [optional]
**stock_component_lines** | [**\OpenAPI\Client\Model\KitAssemblyStockComponentsDto[]**](KitAssemblyStockComponentsDto.md) |  | [optional]
**non_stock_component_lines** | [**\OpenAPI\Client\Model\KitAssemblyNonStockComponentDto[]**](KitAssemblyNonStockComponentDto.md) |  | [optional]
**kit_allocations** | [**\OpenAPI\Client\Model\INAllocationsDto[]**](INAllocationsDto.md) |  | [optional]
**timestamp** | **string** | Timestamp of the kit assembly record | [optional]
**error_info** | **string** |  | [optional]
**metadata** | [**\OpenAPI\Client\Model\MetadataDto**](MetadataDto.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

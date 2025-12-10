# # KitAssemblyInsertDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**kit_assembly_link** | [**\OpenAPI\Client\Model\KitAssemblyLinkInsertDto**](KitAssemblyLinkInsertDto.md) |  | [optional]
**type** | **string** | Type, possible values: P - Production, D - Disassembly | [optional]
**ref_no** | **string** |  | [optional]
**hold** | [**\OpenAPI\Client\Model\DtoValueOfBoolean**](DtoValueOfBoolean.md) |  | [optional]
**date** | [**\OpenAPI\Client\Model\DtoValueOfDateTime**](DtoValueOfDateTime.md) |  | [optional]
**post_period** | [**\OpenAPI\Client\Model\DtoValueOfString**](DtoValueOfString.md) |  | [optional]
**item_id** | [**\OpenAPI\Client\Model\DtoValueOfString**](DtoValueOfString.md) |  | [optional]
**revision** | [**\OpenAPI\Client\Model\DtoValueOfString**](DtoValueOfString.md) |  | [optional]
**reason_code** | [**\OpenAPI\Client\Model\DtoValueOfString**](DtoValueOfString.md) |  | [optional]
**description** | [**\OpenAPI\Client\Model\DtoValueOfString**](DtoValueOfString.md) |  | [optional]
**warehouse** | [**\OpenAPI\Client\Model\DtoValueOfString**](DtoValueOfString.md) |  | [optional]
**location** | [**\OpenAPI\Client\Model\DtoValueOfString**](DtoValueOfString.md) |  | [optional]
**uo_m** | [**\OpenAPI\Client\Model\DtoValueOfString**](DtoValueOfString.md) |  | [optional]
**quantity** | [**\OpenAPI\Client\Model\DtoValueOfDecimal**](DtoValueOfDecimal.md) |  | [optional]
**stock_component_lines** | [**\OpenAPI\Client\Model\KitAssemblyStockComponentsUpdateDto[]**](KitAssemblyStockComponentsUpdateDto.md) |  | [optional]
**stock_component_allocations** | [**\OpenAPI\Client\Model\KitAssemblyStockComponentAllocationsUpdateDto[]**](KitAssemblyStockComponentAllocationsUpdateDto.md) | This property is deprecated and will be removed in a future version.   Use StockComponentLineAllocations within each StockComponentLine instead. | [optional]
**non_stock_component_lines** | [**\OpenAPI\Client\Model\KitAssemblyNonStockComponentsUpdateDto[]**](KitAssemblyNonStockComponentsUpdateDto.md) |  | [optional]
**kit_allocations** | [**\OpenAPI\Client\Model\INAllocationsUpdateDto[]**](INAllocationsUpdateDto.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

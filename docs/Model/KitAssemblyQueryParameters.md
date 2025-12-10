# # KitAssemblyQueryParameters

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**last_modified_date_time** | **string** |  | [optional]
**last_modified_date_time_condition** | **string** | System retrieved information for state/condition. | [optional]
**created_date_time** | **string** | System retrieved information for created date and time. | [optional]
**created_date_time_condition** | **string** | System retrieved information for state/condition. | [optional]
**type** | **string** |  | [optional]
**ref_no** | **string** |  | [optional]
**status** | **string** | Filter by Kit Assembly Status. Possible values: H (Hold), B (Balanced), R (Released) | [optional]
**expand_stock_components** | **bool** |  | [optional]
**expand_non_stock_components** | **bool** |  | [optional]
**expand_kit_allocations** | **bool** |  | [optional]
**page_number** | **int** | Pagination parameter. Page number. | [optional]
**page_size** | **int** | Pagination parameter. Number of items to be collected.  Please use a page size lower or equal to the allowed max page size which is returned as part of the metadata information.  If requested page size is greater than allowed max page size, request will be limited to max page size. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

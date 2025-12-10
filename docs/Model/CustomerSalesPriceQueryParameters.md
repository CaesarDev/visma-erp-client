# # CustomerSalesPriceQueryParameters

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**greater_than_value** | **string** |  | [optional]
**number_to_read** | **int** | This field has been deprecated and will be removed in future versions. Use pagenumber and pagesize for pagination purposes. Pagenumber and pagesize does not work with NumberToRead and SkipRecords. | [optional]
**skip_records** | **int** | This field has been deprecated and will be removed in future versions. Use pagenumber and pagesize for pagination purposes. Pagenumber and pagesize does not work with NumberToRead and SkipRecords. | [optional]
**price_type** | **string** |  | [optional]
**price_code** | **string** |  | [optional]
**inventory_id** | **string** |  | [optional]
**effective_as_of** | **\DateTime** |  | [optional]
**last_modified_date_time** | **string** |  | [optional]
**last_modified_date_time_condition** | **string** |  | [optional]
**page_number** | **int** | Pagination parameter. Page number. | [optional]
**page_size** | **int** | Pagination parameter. Number of items to be collected.  Please use a page size lower or equal to the allowed max page size which is returned as part of the metadata information.  If requested page size is greater than allowed max page size, request will be limited to max page size. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

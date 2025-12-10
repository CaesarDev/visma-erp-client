# # CustomerBalanceV2QueryParameters

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**branch_number** | **string** | Filter by Branch | [optional]
**customer** | **string** | Filter by Customer | [optional]
**from_fin_period** | **string** | Filter from financial period, format YYYYPP  The filte is inclusive, the records for the specified period will be included in the results.  This filter is required. |
**to_fin_period** | **string** | Filter to financial period, format YYYYPP  The filte is inclusive, the records for the specified period will be included in the results.  This filter is required. |
**page_number** | **int** | Pagination parameter. Page number. | [optional]
**page_size** | **int** | Pagination parameter. Number of items to be collected.  Please use a page size lower or equal to the allowed max page size which is returned as part of the metadata information.  If requested page size is greater than allowed max page size, request will be limited to max page size. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

# # StocktakePagingQueryParameters

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**warehouse** | **string** | Filter by Warehouse. | [optional]
**location** | **string** | Filter by Location. | [optional]
**inventory** | **string** | Filter by Inventory. | [optional]
**lot_serial_number** | **string** | Filter by LotSerialNumber. | [optional]
**summary_status** | **string** | Filter by SummaryStatus. | [optional]
**start_with_line** | **int** | Filter by LineNumber GreaterEqual StartWithLine. | [optional]
**end_with_line** | **int** | Filter by by LineNumber LessEqual EndWithLine. | [optional]
**freeze_date_time** | **string** | Filter by FreezeDateTime. | [optional]
**freeze_date_time_condition** | **string** | Filter by FreezeDateTimeCondition. | [optional]
**last_modified_date_time** | **string** | System generated value for last modification of transaction/record. Use format: YYYY-MM-DD HH:MM (date and time) to filter from date to present.. | [optional]
**last_modified_date_time_condition** | **string** | System retrieved information for state/condition. | [optional]
**expiration_date_time** | **string** | Filter by ExpirationDateTime. | [optional]
**expiration_date_time_condition** | **string** | Filter by ExpirationDateTimeCondition. | [optional]
**status** | **string** | Filter by StocktakeLineStatus. | [optional]
**page_number** | **int** | Pagination parameter. Page number. | [optional]
**page_size** | **int** | Pagination parameter. Number of items to be collected.  Please use a page size lower or equal to the allowed max page size which is returned as part of the metadata information.  If requested page size is greater than allowed max page size, request will be limited to max page size. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

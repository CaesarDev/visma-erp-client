# # CarrierQueryParameters

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**number_to_read** | **int** | This field has been deprecated and will be removed in future versions. | [optional]
**skip_records** | **int** | This field has been deprecated and will be removed in future versions. | [optional]
**last_modified_date_time** | **string** | System generated value for last modification of transaction/record. Use format: YYYY-MM-DD HH:MM (date and time) to filter from date to present. | [optional]
**last_modified_date_time_condition** | **string** | System retrieved information for state/condition. | [optional]
**page_number** | **int** | Pagination parameter. Page number. | [optional]
**page_size** | **int** | Pagination parameter. Number of items to be collected.  Please use a page size lower or equal to the allowed max page size which is returned as part of the metadata information.  If requested page size is greater than allowed max page size, request will be limited to max page size. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

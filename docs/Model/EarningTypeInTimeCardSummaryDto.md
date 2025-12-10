# # EarningTypeInTimeCardSummaryDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**code** | **string** | Mandatory field: Code* &amp;gt; The unique ID of the type of hour. | [optional]
**description** | **string** | Mandatory field: Description &amp;gt; The brief description of the type of hour. | [optional]
**is_overtime** | **bool** | Overtime &amp;gt; A check box that indicates (if selected) that the type of hour is treated as overtime. | [optional]
**is_billable** | **bool** | Invoicable &amp;gt; A check box that indicates (if selected) that the type is treated as invoiceable by default. | [optional]
**is_active** | **bool** | Active &amp;gt; A check box that indicates (if selected) that the type of hour is active and can be used. | [optional]
**overtime_multiplier** | **float** | Multiplier &amp;gt; The value by which the employee cost for this type of hour is multiplied when the time activity is released. | [optional]
**last_modified_date_time** | **\DateTime** | System generated information. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

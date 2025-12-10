# # DepartmentDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**department_id** | **string** | Mandatory field : The table &amp;gt; Department ID* &amp;gt; The unique identifier for the department. | [optional]
**public_id** | **string** | Identifies the Department by its publicId | [optional]
**description** | **string** | The table &amp;gt; Description &amp;gt; A detailed description of the department. | [optional]
**expense_account** | [**\OpenAPI\Client\Model\ExpenseAccountInDepartmentDto**](ExpenseAccountInDepartmentDto.md) |  | [optional]
**expense_subaccount** | [**\OpenAPI\Client\Model\ExpenseSubaccountInDepartmentDto**](ExpenseSubaccountInDepartmentDto.md) |  | [optional]
**last_modified_date_time** | **\DateTime** | A system generated date/time that indicates the last change for the department. | [optional]
**time_stamp** | **string** | Identifier that represents a specific version of the resource.  It helps to prevent simultaneous updates of the resource from overwriting each other (by using ETags and If-Match headers) | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

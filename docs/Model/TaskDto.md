# # TaskDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**task_id** | **string** | Mandatory field: &amp;gt; Task ID* &amp;gt; The ID of the task. | [optional]
**description** | **string** | Mandatory field: Description &amp;gt; The description of the task. | [optional]
**planned_start** | **\DateTime** |  | [optional]
**planned_end** | **\DateTime** |  | [optional]
**start_date** | **\DateTime** | Start date &amp;gt; The date when the task was actually started. | [optional]
**end_date** | **\DateTime** | End date &amp;gt; The date when the task was actually finished. | [optional]
**branch** | [**\OpenAPI\Client\Model\BranchInTaskDto**](BranchInTaskDto.md) |  | [optional]
**rate_table** | [**\OpenAPI\Client\Model\RateTableIdDescriptionDto**](RateTableIdDescriptionDto.md) |  | [optional]
**status** | **string** | Mandatory field: Status* &amp;gt; The status of the task, which can be one of the following: In planning, Active, Cancelled, Completed. | [optional]
**restrict_employees** | **bool** | Summary tab &amp;gt; Task properties section &amp;gt; Restrict employees &amp;gt; A check box that indicates (if selected) that only the employees listed on the Employees tab of this window can create activities and documents associated with the current task. | [optional]
**visibility** | [**\OpenAPI\Client\Model\VisibilityDto**](VisibilityDto.md) |  | [optional]
**time_stamp** | **string** | Identifier that represents a specific version of the resource.  It helps to prevent simultaneous updates of the resource from overwriting each other (by using ETags and If-Match headers) | [optional]
**employees** | [**\OpenAPI\Client\Model\EmployeeDto[]**](EmployeeDto.md) | The Employees tab &amp;gt; Information in this tab is retreived from EP203000 (Employees) | [optional]
**attributes** | [**\OpenAPI\Client\Model\AttributeIdValueDto[]**](AttributeIdValueDto.md) | Attributes | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

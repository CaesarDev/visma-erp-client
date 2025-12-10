# # ClaimedByInExpenseReceiptDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**employee_user_id** | **string** | Employee internal user ID. This is the ID of the user linked to the employee | [optional]
**employee_id** | **int** | Mandatory field: The top part &amp;gt; Employee ID* &amp;gt; The unique identifier, which is assigned to the employee in accordance with the configuration of the EMPLOYEE segmented key. | [optional]
**employee_number** | **string** | General information tab &amp;gt; Employee settings section &amp;gt; Employee ref. no. &amp;gt; A reference number for the employee. | [optional]
**employee_name** | **string** | The top part &amp;gt; Employee name &amp;gt; The name of this employee. | [optional]
**status** | **string** | Mandatory field: The top part &amp;gt; Status &amp;gt; The status of the employee. The following options are available: Active, On hold, Hold payments, Inactive, One-time. | [optional]
**department** | **string** | Mandatory field: General information tab &amp;gt; Employee section &amp;gt; Department* &amp;gt; The department the employee works for. | [optional]
**contact** | [**\OpenAPI\Client\Model\ContactInEmployeeDto**](ContactInEmployeeDto.md) |  | [optional]
**address** | [**\OpenAPI\Client\Model\AddressInEmployeeDto**](AddressInEmployeeDto.md) |  | [optional]
**last_modified_date_time** | **\DateTime** |  | [optional]
**employee_class** | [**\OpenAPI\Client\Model\EmployeeClassInEmployeeDto**](EmployeeClassInEmployeeDto.md) |  | [optional]
**branch** | [**\OpenAPI\Client\Model\BranchNumberDto**](BranchNumberDto.md) |  | [optional]
**calendar_id** | **string** |  | [optional]
**employee_login** | **string** |  | [optional]
**work_group_description** | **string[]** |  | [optional]
**time_stamp** | **string** | Identifier that represents a specific version of the resource.  It helps to prevent simultaneous updates of the resource from overwriting each other (by using ETags and If-Match headers) | [optional]
**error_info** | **string** |  | [optional]
**metadata** | [**\OpenAPI\Client\Model\MetadataDto**](MetadataDto.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

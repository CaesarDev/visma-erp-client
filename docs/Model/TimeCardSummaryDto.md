# # TimeCardSummaryDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**line_number** | **int** | The time card line number | [optional]
**line_id** | **string** | The time card line id | [optional]
**earning_type** | [**\OpenAPI\Client\Model\EarningTypeInTimeCardSummaryDto**](EarningTypeInTimeCardSummaryDto.md) |  | [optional]
**project** | [**\OpenAPI\Client\Model\ProjectInTimeCardSummaryDto**](ProjectInTimeCardSummaryDto.md) |  | [optional]
**mon** | **int** | Mon &amp;gt; The work time reported for Monday, including overtime. | [optional]
**tue** | **int** | Tue &amp;gt; The work time reported for Tuesday, including overtime. | [optional]
**wed** | **int** | Wed &amp;gt; The work time reported for Wednesday, including overtime. | [optional]
**thu** | **int** | Thu &amp;gt; The work time reported for Thursday, including overtime. | [optional]
**fri** | **int** | Fri &amp;gt; The work time reported for Friday, including overtime. | [optional]
**sat** | **int** | Sat &amp;gt; The work time reported for Saturday, including overtime. | [optional]
**sun** | **int** | Sun &amp;gt; The work time reported for Sunday, including overtime. | [optional]
**invoiceable** | **bool** | Invoicable &amp;gt; A check box that you select to indicate that these work hours are invoiceable. | [optional]
**project_task** | [**\OpenAPI\Client\Model\ProjectTaskInTimeCardSummaryDto**](ProjectTaskInTimeCardSummaryDto.md) |  | [optional]
**time_spent** | **int** | Time spent &amp;gt; The work time (regular and overtime) that the employee spent on the project and task during the week. | [optional]
**description** | **string** | Description &amp;gt; The description of the reported work hours. | [optional]
**approval_status** | **string** | Approval status &amp;gt; The approval status, which indicates whether the summary row requires approval and, if it does, what the current state of approval is. | [optional]
**approver** | **string** | The identifier of the person authorized to approve the activity, if approval is required. This is either the approver of the project task or, if no approver is assigned to the project task, the project manager. | [optional]
**approval_status_text** | **string** | last approval comment &amp;gt; The approval status text suitable for display | [optional]
**last_modified_date_time** | **\DateTime** | The last time the time card line was modified | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

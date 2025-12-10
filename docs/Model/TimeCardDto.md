# # TimeCardDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ref_nbr** | **string** | The top part &amp;gt; Ref. no. &amp;gt; The unique reference number of the time card, which Acumatica ERP automatically assigns according to the numbering sequence specified as the Time Card Numbering Sequence on the Time and Expenses Preferences (EP.10.10.00) form. | [optional]
**status** | **string** | The top part &amp;gt; Status &amp;gt; The status of the time card | [optional]
**approval_status** | **string** | The top part &amp;gt; Approval status &amp;gt; The approval status of the time card | [optional]
**week** | [**\OpenAPI\Client\Model\WeekInTimeCardDto**](WeekInTimeCardDto.md) |  | [optional]
**employee** | [**\OpenAPI\Client\Model\EmployeeInTimeCardDto**](EmployeeInTimeCardDto.md) |  | [optional]
**type** | **string** | The top part &amp;gt; Type &amp;gt; The type of the time card. The following options are available:• Normal: Regular time card• Correction: Corrective time card, which is a time card that updates a released time card | [optional]
**orig_ref_nbr** | **string** | The top part &amp;gt; Orig. ref. no. &amp;gt; The reference number of the time card being corrected. This box is filled in only when Correction is specified in the Type box | [optional]
**time_spent** | **int** | The top part &amp;gt; Regular column: Time spent &amp;gt; The work hours spent by the employee during the week on activities with the Regular Hours earning type. | [optional]
**invoiceable** | **int** | The top part &amp;gt; Regular column: Invoicable &amp;gt; The invoiceable work hours spent by the employee during the week | [optional]
**overtime_spent** | **int** | The top part &amp;gt; Overtime column: Time spent &amp;gt; The work hours spent by the employee during the week on activities with the Overtime earning type. | [optional]
**invoiceable_overtime** | **int** | The top part &amp;gt; Overtime column: Invoicable &amp;gt; The invoiceable overtime spent by the employee during the week | [optional]
**total_time_spent** | **int** | The top part &amp;gt; Total column: Time spent &amp;gt; The total working time (regular and overtime) for the week | [optional]
**invoiceable_total_time** | **int** | The top part &amp;gt; Total column: Invoicable &amp;gt; The total invoiceable working time (regular and overtime) for the week | [optional]
**last_modified_date_time** | **\DateTime** | System generated information: The last time the time card line was modified | [optional]
**summary** | [**\OpenAPI\Client\Model\TimeCardSummaryDto[]**](TimeCardSummaryDto.md) | Summary tab &amp;gt; Time Card summary information | [optional]
**materials** | [**\OpenAPI\Client\Model\TimeCardMaterialsDto[]**](TimeCardMaterialsDto.md) | Summary tab &amp;gt; Time Card materials information | [optional]
**approval_status_text** | **string** |  | [optional]
**time_stamp** | **string** | Identifier that represents a specific version of the resource.  It helps to prevent simultaneous updates of the resource from overwriting each other (by using ETags and If-Match headers) | [optional]
**error_info** | **string** |  | [optional]
**metadata** | [**\OpenAPI\Client\Model\MetadataDto**](MetadataDto.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

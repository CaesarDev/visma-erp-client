# # ProjectUpdateDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | [**\OpenAPI\Client\Model\DtoValueOfString**](DtoValueOfString.md) |  | [optional]
**internal_id** | [**\OpenAPI\Client\Model\DtoValueOfNullableOfInt32**](DtoValueOfNullableOfInt32.md) |  | [optional]
**customer** | [**\OpenAPI\Client\Model\DtoValueOfString**](DtoValueOfString.md) |  | [optional]
**description** | [**\OpenAPI\Client\Model\DescriptionInProjectUpdateDto**](DescriptionInProjectUpdateDto.md) |  |
**hold** | [**\OpenAPI\Client\Model\DtoValueOfNullableOfBoolean**](DtoValueOfNullableOfBoolean.md) |  | [optional]
**template** | [**\OpenAPI\Client\Model\DtoValueOfString**](DtoValueOfString.md) |  | [optional]
**status** | [**\OpenAPI\Client\Model\DtoValueOfNullableOfProjectStatus**](DtoValueOfNullableOfProjectStatus.md) |  | [optional]
**def_account** | [**\OpenAPI\Client\Model\DtoValueOfString**](DtoValueOfString.md) |  | [optional]
**def_sub** | [**\OpenAPI\Client\Model\SegmentUpdateDto[]**](SegmentUpdateDto.md) | Mandatory field when Project Template is not specified. | [optional]
**def_accrual_account** | [**\OpenAPI\Client\Model\DtoValueOfString**](DtoValueOfString.md) |  | [optional]
**def_accrual_sub** | [**\OpenAPI\Client\Model\SegmentUpdateDto[]**](SegmentUpdateDto.md) |  | [optional]
**start_date** | [**\OpenAPI\Client\Model\StartDateInProjectUpdateDto**](StartDateInProjectUpdateDto.md) |  |
**end_date** | [**\OpenAPI\Client\Model\DtoValueOfNullableOfDateTime**](DtoValueOfNullableOfDateTime.md) |  | [optional]
**billing_period** | [**\OpenAPI\Client\Model\DtoValueOfNullableOfBillingPeriod**](DtoValueOfNullableOfBillingPeriod.md) |  | [optional]
**allocation_rule** | [**\OpenAPI\Client\Model\DtoValueOfString**](DtoValueOfString.md) |  | [optional]
**billing_rule** | [**\OpenAPI\Client\Model\DtoValueOfString**](DtoValueOfString.md) |  | [optional]
**branch** | [**\OpenAPI\Client\Model\BranchInProjectUpdateDto**](BranchInProjectUpdateDto.md) |  | [optional]
**rate_table** | [**\OpenAPI\Client\Model\DtoValueOfString**](DtoValueOfString.md) |  | [optional]
**project_manger** | [**\OpenAPI\Client\Model\DtoValueOfString**](DtoValueOfString.md) |  | [optional]
**project_manager_internal_id** | [**\OpenAPI\Client\Model\DtoValueOfNullableOfInt32**](DtoValueOfNullableOfInt32.md) |  | [optional]
**auto_allocate** | [**\OpenAPI\Client\Model\DtoValueOfNullableOfBoolean**](DtoValueOfNullableOfBoolean.md) |  | [optional]
**automatic_release_ar_doc** | [**\OpenAPI\Client\Model\DtoValueOfNullableOfBoolean**](DtoValueOfNullableOfBoolean.md) |  | [optional]
**restric_employees** | [**\OpenAPI\Client\Model\DtoValueOfNullableOfBoolean**](DtoValueOfNullableOfBoolean.md) |  | [optional]
**restric_equipment** | [**\OpenAPI\Client\Model\DtoValueOfNullableOfBoolean**](DtoValueOfNullableOfBoolean.md) |  | [optional]
**customer_location** | [**\OpenAPI\Client\Model\DtoValueOfString**](DtoValueOfString.md) |  | [optional]
**visibility** | [**\OpenAPI\Client\Model\VisibilityUpdateDto**](VisibilityUpdateDto.md) |  | [optional]
**tasks** | [**\OpenAPI\Client\Model\TaskUpdateDto[]**](TaskUpdateDto.md) |  | [optional]
**employees** | [**\OpenAPI\Client\Model\ProjectEmployeeUpdateDto[]**](ProjectEmployeeUpdateDto.md) |  | [optional]
**note** | [**\OpenAPI\Client\Model\DtoValueOfString**](DtoValueOfString.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

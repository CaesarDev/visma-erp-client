# # CustomerContractDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**contract_id** | **string** | Mandatory field: The top part &amp;gt; Contract ID* &amp;gt; The unique identifier of a contract. | [optional]
**contract_template** | [**\OpenAPI\Client\Model\ContractTemplateInCustomerContractDto**](ContractTemplateInCustomerContractDto.md) |  | [optional]
**status** | **string** | The top part &amp;gt; Status &amp;gt; The status of the contract, which is one of the following: Draft, Pending activation, Active, Expired, Cancelled, Pending update. | [optional]
**customer** | [**\OpenAPI\Client\Model\CustomerInCustomerContractDto**](CustomerInCustomerContractDto.md) |  | [optional]
**location** | [**\OpenAPI\Client\Model\LocationInCustomerContractDto**](LocationInCustomerContractDto.md) |  | [optional]
**description** | **string** | Mandatory field: The top part &amp;gt; Description* &amp;gt; The description of the contract, which includes any related comments. | [optional]
**balance** | **float** | The top part &amp;gt; Balance &amp;gt; A read-only field that displays the sum of the balances of open invoices associated with the contract. | [optional]
**last_modified_date_time** | **\DateTime** | System generated information | [optional]
**summary** | [**\OpenAPI\Client\Model\SummaryInCustomerContractDto**](SummaryInCustomerContractDto.md) |  | [optional]
**details** | [**\OpenAPI\Client\Model\DetailsInCustomerContractDto**](DetailsInCustomerContractDto.md) |  | [optional]
**attributes** | [**\OpenAPI\Client\Model\AttributeIdValueDto[]**](AttributeIdValueDto.md) | Project attributes tab | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

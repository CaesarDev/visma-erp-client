# # CustomerContractSummaryDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**setup_date** | **\DateTime** | Mandatory field: Contract settings section &amp;gt; Setup date* &amp;gt; The date of contract setup. | [optional]
**activation_date** | **\DateTime** | Contract settings section &amp;gt; Activation date &amp;gt; The date to initiate the provision of the contract services. | [optional]
**expiration_date** | **\DateTime** | Contract settings section &amp;gt; Expiration date &amp;gt; The date when the contract expires. | [optional]
**termination_date** | **\DateTime** | Contract settings section &amp;gt; Termination date &amp;gt; The date when the contract will be cancelled; no services will be provided. | [optional]
**mass_renewal** | **bool** | Contract settings section &amp;gt; Mass renewal &amp;gt; A check box indicating renewal of all contract at expiration date. | [optional]
**renewal_point** | **int** | Contract settings section &amp;gt; Renewal point &amp;gt; The number of days before expiration where the renewal process are to begin. | [optional]
**grace_period** | **int** | Contract settings section &amp;gt; Grace period &amp;gt; The number of days after the expiration date where the contract can still be renewed. | [optional]
**currency** | **string** | Mandatory field: Contract settings section &amp;gt; Currency* &amp;gt; The currency used in the contract. | [optional]
**invoicing_schedule_starts_on** | **\DateTime** | Invoicing schedule section &amp;gt; Invoice schedule starts on &amp;gt; A read-only field that displays the start date of the first invoicing period. | [optional]
**invoicing_period** | **string** | Mandatory field: Invoicing schedule section &amp;gt; Invoicing period* &amp;gt; The type of invoicing schedule, which can be one of the following options: Weekly, Monthly; Quarterly, Half a year, Yearly, On demand, Statement based. | [optional]
**last_invoicing_date** | **\DateTime** | Invoicing schedule section &amp;gt; Last invoicing date &amp;gt; A read-only field that shows the date when the invoicing was performed most recently. | [optional]
**next_invoicing_date** | **\DateTime** | Invoicing schedule section &amp;gt; Next invoicing date &amp;gt; The date of the next invoicing invoice, according to the invoicing schedule. | [optional]
**invoice_to** | **string** | Invoice information section &amp;gt; Invoice to &amp;gt; The setting that defines the customer account to be invoiced for a contract. The following options are available: Parent account, Customer account, Specific account. | [optional]
**invoice_account** | [**\OpenAPI\Client\Model\InvoiceAccountInCustomerContractSummaryDto**](InvoiceAccountInCustomerContractSummaryDto.md) |  | [optional]
**invoice_location** | [**\OpenAPI\Client\Model\LocationNameDescriptionDto**](LocationNameDescriptionDto.md) |  | [optional]
**owner** | [**\OpenAPI\Client\Model\OwnerInCustomerContractSummaryDto**](OwnerInCustomerContractSummaryDto.md) |  | [optional]
**sales_person** | [**\OpenAPI\Client\Model\SalesPersonInCustomerContractSummaryDto**](SalesPersonInCustomerContractSummaryDto.md) |  | [optional]
**case_count_item** | [**\OpenAPI\Client\Model\CaseCountItemInCustomerContractSummaryDto**](CaseCountItemInCustomerContractSummaryDto.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

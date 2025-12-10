# # GeneralLedgerBalanceDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**branch** | [**\OpenAPI\Client\Model\BranchNumberDto**](BranchNumberDto.md) |  | [optional]
**ledger** | [**\OpenAPI\Client\Model\LedgerDescriptionDto**](LedgerDescriptionDto.md) |  | [optional]
**balance_type** | **string** |  | [optional]
**financial_period** | **string** | The financial period to which the transactions recorded in the document should be posted. Format YYYYMM. | [optional]
**account** | [**\OpenAPI\Client\Model\AccountNumberDescriptionDto**](AccountNumberDescriptionDto.md) |  | [optional]
**subaccount_id** | **string** |  | [optional]
**sub_account_cd** | **string** |  | [optional]
**currency_id** | **string** |  | [optional]
**period_to_date_debit** | **float** | The total of all debit movements for the selected period. | [optional]
**period_to_date_credit** | **float** | The total of all credit movements for the selected period. | [optional]
**beginning_balance** | **float** | The total account balance at the start of the selected period. | [optional]
**year_to_date_balance** | **float** | The total account balance at the end of the selected period. | [optional]
**period_to_date_debit_in_currency** | **float** | The total of all debit movements in the currency of the selected account for the selected period. | [optional]
**period_to_date_credit_in_currency** | **float** | The total of all credit movements in the currency of the selected account for the selected period. | [optional]
**beginning_balance_in_currency** | **float** | The total account balance in the currency of the selected account at the start of the selected period. | [optional]
**year_to_date_balance_in_currency** | **float** | The total account balance in the currency of the selected account at the end of the selected period. | [optional]
**year_closed** | **bool** | True when the last period of a financial year is  closed in all modules. | [optional]
**last_modified_date_time** | **\DateTime** |  | [optional]
**error_info** | **string** |  | [optional]
**metadata** | [**\OpenAPI\Client\Model\MetadataDto**](MetadataDto.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

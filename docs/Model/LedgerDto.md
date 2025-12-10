# # LedgerDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**internal_id** | **int** |  | [optional]
**number** | **string** | Mandatory field: The top part &amp;gt; Ledger ID* &amp;gt; An alphanumeric string of up to 10 characters used to identify the ledger. | [optional]
**description** | **string** | The top part &amp;gt; Description &amp;gt; A detailed ledger description. | [optional]
**balance_type** | **string** | The top part &amp;gt; Balance type &amp;gt; The type of balance in the ledger. Select one of the following predefined types: Actual, Budget, Reporting, Statistical. | [optional]
**currency_id** | **string** | Mandatory field: The top part &amp;gt; Currency* &amp;gt; The default currency of the ledger. | [optional]
**consolidation_source** | **bool** | The top part &amp;gt; Consolidation source &amp;gt; A check box that specifies, if selected, that the ledger should be used as a source ledger for consolidation. | [optional]
**consol_branch** | [**\OpenAPI\Client\Model\ConsolBranchInLedgerDto**](ConsolBranchInLedgerDto.md) |  | [optional]
**branch_accounting** | **bool** | The top part &amp;gt; Branch accounting &amp;gt; A check box that you select to indicate that the system should automatically generate inter-branch transactions for this ledger to balance transactions for all branches involved. | [optional]
**last_modified_date_time** | **\DateTime** | System generated information. | [optional]
**post_inter_company** | **bool** | Branch accounting &amp;gt; True/False | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

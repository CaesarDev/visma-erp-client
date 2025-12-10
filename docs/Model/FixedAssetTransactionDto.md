# # FixedAssetTransactionDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ref_no** | **string** | The referance number for this fixed asset transaction | [optional]
**line_no** | **int** | The line number of this fixed asset transaction | [optional]
**branch_id** | **string** | The branch id for this fixed asset transaction | [optional]
**origin** | **string** | The origin of this fixed asset transaction. Origin can be | [optional]
**asset_id** | **string** | The asset id this fixed asset transaction belongs to | [optional]
**transaction_description** | **string** | The description of this fixed asset transaction | [optional]
**book_id** | **string** | The book id for this fixed asset transaction | [optional]
**transaction_type** | **string** | Type can be | [optional]
**accounts** | [**\OpenAPI\Client\Model\AccountsInFixedAssetTransactionDto**](AccountsInFixedAssetTransactionDto.md) |  | [optional]
**transaction_amount** | **float** | The amount of this fixed asset transaction | [optional]
**batch_no** | **string** | The batch number of the general ledger transaction for this fixed asset transaction | [optional]
**transaction_period_id** | **string** | The transaction period id for this fixed asset transaction | [optional]
**transaction_date** | **\DateTime** | The transaction date for this fixed asset transaction | [optional]
**register** | [**\OpenAPI\Client\Model\RegisterInFixedAssetTransactionDto**](RegisterInFixedAssetTransactionDto.md) |  | [optional]
**last_modified_date_time** | **\DateTime** | A system generated date/time that indicates the last change for this fixed asset transaction | [optional]
**error_info** | **string** |  | [optional]
**metadata** | [**\OpenAPI\Client\Model\MetadataDto**](MetadataDto.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

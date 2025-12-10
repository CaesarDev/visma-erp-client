# # FixedAssetClassDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**class_id** | **string** | The id that identifies this fixed asset class | [optional]
**record_type** | **string** | The type of the record. This value is &#39;C&#39; for fixed asset classes | [optional]
**description** | **string** | The description of this fixed asset class | [optional]
**active** | **bool** | Indicates whether this fixed asset class is active or not | [optional]
**asset_type_id** | **string** | The type id of this fixed asset class | [optional]
**is_tangible** | **bool** | Indicates whether the fixed asset using this fixed asset class is tangible or not by default | [optional]
**depreciable** | **bool** | Indicates whether the fixed asset using this fixed asset class can be depreciated or not by default | [optional]
**useful_life** | **float** | Default useful life in years of the fixed asset using this fixed asset class | [optional]
**accelerated_depreciation** | **bool** | Indicates whether the fixed asset using this fixed asset class will use accelerated depreciation depending on selected depreciation method | [optional]
**book_settings** | [**\OpenAPI\Client\Model\BookSettingsInFixedAssetClassDto**](BookSettingsInFixedAssetClassDto.md) |  | [optional]
**accounts** | [**\OpenAPI\Client\Model\AccountsInFixedAssetClassDto**](AccountsInFixedAssetClassDto.md) |  | [optional]
**sub_account_mask** | **string** | The sub account mask for this fixed asset class | [optional]
**accumulated_depreciation_sub_account_mask** | **string** | The accumulated depreciation sub account mask for this fixed asset class | [optional]
**depreciated_expense_sub_account_mask** | **string** | The depreciated expense sub account mask for this fixed asset class | [optional]
**proceed_sub_account_mask** | **string** | The proceed sub account mask for this fixed asset class | [optional]
**gain_loss_sub_account_mask** | **string** | The gain/loss sub account mask for this fixed asset class | [optional]
**error_info** | **string** |  | [optional]
**metadata** | [**\OpenAPI\Client\Model\MetadataDto**](MetadataDto.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

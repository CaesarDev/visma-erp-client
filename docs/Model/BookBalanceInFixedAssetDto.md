# # BookBalanceInFixedAssetDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**acquisition_cost** | **float** | The acquisition cost of this fixed asset | [optional]
**depreciation_method_id** | **string** | The depreciation method id of this fixed asset | [optional]
**depreciation_from_date** | **\DateTime** | The date this asset is placed in service | [optional]
**depreciation_from_period** | **string** | The first period this fixed asset will start/has started depreciating | [optional]
**depreciation_to_period** | **string** | The last period this fixed asset will depreciate/ was depreciated | [optional]
**last_depreciation_period** | **string** | The last period this asset has been depreciated | [optional]
**salvage_amount** | **float** | The salvage amount of this fixed asset | [optional]
**useful_life** | **float** | The useful life of this fixed asset in years | [optional]
**book** | [**\OpenAPI\Client\Model\BookInBookBalanceDto**](BookInBookBalanceDto.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

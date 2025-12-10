# # FixedAssetDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**asset_id** | **string** | The id that identifies this fixed asset | [optional]
**record_type** | **string** | The type of the record. This value is &#39;A&#39; for fixed assets | [optional]
**parent_asset_id** | **string** | The asset id of the parent of this fixed asset | [optional]
**description** | **string** | The description of this fixed asset | [optional]
**class_id** | **string** | The class id of this fixed asset | [optional]
**is_tangible** | **bool** | Indicates whether this fixed asset is tangible or not | [optional]
**quantity** | **float** | The quantity of this fixed asset | [optional]
**depreciable** | **bool** | Indicates if this fixed asset can be depreciated or not | [optional]
**useful_life** | **float** | Useful life of this fixed asset in years | [optional]
**accounts** | [**\OpenAPI\Client\Model\AccountsInFixedAssetDto**](AccountsInFixedAssetDto.md) |  | [optional]
**details** | [**\OpenAPI\Client\Model\DetailsInFixedAssetDto**](DetailsInFixedAssetDto.md) |  | [optional]
**book_balance** | [**\OpenAPI\Client\Model\BookBalanceInFixedAssetDto**](BookBalanceInFixedAssetDto.md) |  | [optional]
**location** | [**\OpenAPI\Client\Model\LocationInFixedAssetDto**](LocationInFixedAssetDto.md) |  | [optional]
**property_tax** | [**\OpenAPI\Client\Model\PropertyTaxInFixedAssetDto**](PropertyTaxInFixedAssetDto.md) |  | [optional]
**type** | [**\OpenAPI\Client\Model\TypeInFixedAssetDto**](TypeInFixedAssetDto.md) |  | [optional]
**last_modified_date_time** | **\DateTime** | A system generated date/time that indicates the last change for this fixed asset | [optional]
**error_info** | **string** |  | [optional]
**metadata** | [**\OpenAPI\Client\Model\MetadataDto**](MetadataDto.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

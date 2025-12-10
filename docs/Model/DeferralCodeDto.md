# # DeferralCodeDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**deferral_code** | **string** | Mandatory field: Deferral code* &amp;gt;  The unique code for the deferral type. | [optional]
**description** | **string** | Description &amp;gt; The description of the deferral code. | [optional]
**deferred_revenue_from_item** | **bool** | Deferred revenue from item &amp;gt; When this check box is selected, the deferred revenue of the code will be retrieved from the connected item. | [optional]
**recognition_method** | **string** | Recognition method &amp;gt; The method used to distribute the document amount over the periods. | [optional]
**code_type** | **string** | Code type &amp;gt; The type of the deferral code. | [optional]
**deferral_account** | [**\OpenAPI\Client\Model\DeferralAccountInDeferralCodeDto**](DeferralAccountInDeferralCodeDto.md) |  | [optional]
**deferral_sub** | [**\OpenAPI\Client\Model\DeferralSubInDeferralCodeDto**](DeferralSubInDeferralCodeDto.md) |  | [optional]
**error_info** | **string** |  | [optional]
**metadata** | [**\OpenAPI\Client\Model\MetadataDto**](MetadataDto.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

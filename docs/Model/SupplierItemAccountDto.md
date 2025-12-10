# # SupplierItemAccountDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**supplier_item_id** | **string** | The supplier item id for which the account is displayed. | [optional]
**item_id** | **string** | The item id matched to the SupplierItemId. If null, this means that no itemId was found for the corresponding {Visma.net.ERP.Web.Api.Model.V1.SupplierItemAccountDto.SupplierItemId} | [optional]
**account_id** | **string** | The Account ID is the actual ID of the expense account for the SupplierItemID or of the supplier if no SUpplierItemId was specified in the request. If null, this means that no account was found for the {Visma.net.ERP.Web.Api.Model.V1.SupplierItemAccountDto.SupplierItemId} | [optional]
**subaccount** | [**\OpenAPI\Client\Model\SubaccountInSupplierItemAccountDto**](SubaccountInSupplierItemAccountDto.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

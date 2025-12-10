# # LinkLineDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**purchase_type** | **string** | PurchaseTye can be either {Visma.net.ERP.Web.Api.Model.V1.Enum.PurchaseType.PurchaseOrder} or {Visma.net.ERP.Web.Api.Model.V1.Enum.PurchaseType.PurchaseReceipt}&lt;para&gt;  It should be noted that for stock-items, its only limited to {Visma.net.ERP.Web.Api.Model.V1.Enum.PurchaseType.PurchaseReceipt}, however,  for non-stock items we can choose either {Visma.net.ERP.Web.Api.Model.V1.Enum.PurchaseType.PurchaseReceipt} or {Visma.net.ERP.Web.Api.Model.V1.Enum.PurchaseType.PurchaseOrder}&lt;/para&gt; | [optional]
**purchase_number** | [**\OpenAPI\Client\Model\PurchaseNumberInLinkLineDto**](PurchaseNumberInLinkLineDto.md) |  | [optional]
**purchase_line_nbr** | [**\OpenAPI\Client\Model\PurchaseLineNbrInLinkLineDto**](PurchaseLineNbrInLinkLineDto.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

# # VatCategoryLineDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**vat_id** | **string** | Mandatory field: VAT ID* &amp;gt; The ID of the VAT included in the category. | [optional]
**vendor_cd** | **string** | Vendor code &amp;gt; The vendor number associated with the VAT category line. | [optional]
**description** | **string** | Description &amp;gt; The detailed description of the VAT item. | [optional]
**type** | **string** | VAT type &amp;gt; The type of VAT, which defines how it is processed. | [optional]
**calculate_on** | **string** | Calculate on &amp;gt; The way the VAT amount is calculated, which can be one of the following options: Extract from item amount, Document amount, Document and VAT amount. | [optional]
**cash_discount** | **string** | Cash discount &amp;gt; The method of calculating the taxable amount if a discount is applied (based on the credit terms). It can be one of the following options: Reduce VAT amount, Does not affect VAT amount. | [optional]
**vat_rates** | [**\OpenAPI\Client\Model\VatRateLineDto[]**](VatRateLineDto.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

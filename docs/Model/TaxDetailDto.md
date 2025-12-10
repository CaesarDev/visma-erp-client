# # TaxDetailDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tax_id** | **string** | Mandatory field: VAT ID* &amp;gt; The ID of the VAT applied to the document. | [optional]
**record_id** | **int** | The id as stored in the database. It can be used when we want to update a VAT record. | [optional]
**vat_id** | [**\OpenAPI\Client\Model\VatIdInTaxDetailDto**](VatIdInTaxDetailDto.md) |  | [optional]
**vat_rate** | **float** | VAT rate &amp;gt; The rate of the VAT. | [optional]
**taxable_amount** | **float** | Taxable amount &amp;gt; The taxable amount for the VAT, which is calculated at the document level. | [optional]
**vat_amount** | **float** | VAT &amp;gt; The VAT amount for the specific VAT, which is calculated at the document level. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

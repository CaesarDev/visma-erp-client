# # VatCategoryDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**vat_category_id** | **string** | Mandatory field: The top part &amp;gt; VAT category ID* &amp;gt; The unique ID of the VAT category. An alphanumeric string of up to six characters can be used. | [optional]
**description** | **string** | The top part &amp;gt; Description &amp;gt; A detailed description of the category. | [optional]
**active** | **bool** | The top part &amp;gt; Active &amp;gt; A check box that means (if selected) that this VAT category is active. | [optional]
**exclude_listed_taxes** | **bool** | The top part &amp;gt; Exclude listed taxes &amp;gt; A check box that indicates (if selected) this VAT category should exclude the listed taxes from VAT zones. | [optional]
**last_modified_date_time** | **\DateTime** | Systemgenerated information. | [optional]
**vat_category_lines** | [**\OpenAPI\Client\Model\VatCategoryLineDto[]**](VatCategoryLineDto.md) | The table &amp;gt; | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

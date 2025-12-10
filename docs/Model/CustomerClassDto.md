# # CustomerClassDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The top part &amp;gt; Class ID &amp;gt; The unique identifier of the class. You can use an alphanumeric string of up to 10 characters. | [optional]
**description** | **string** | The top part &amp;gt; Description &amp;gt; A detailed description of the customer class. | [optional]
**tax_zone_id** | **string** | The General information tab &amp;gt; VAT zone ID &amp;gt; The default VAT zone for customers of the class. | [optional]
**required_taxzone_id** | **bool** | The General information tab &amp;gt; Require VAT zone &amp;gt; A check box that means (if selected) that the VAT zone value is required for customers of the class. | [optional]
**payment_method_id** | **string** | The General information tab &amp;gt; Payment method &amp;gt; The payment method used by default in relations with these customers. | [optional]
**attributes** | [**\OpenAPI\Client\Model\ClassAttributeDto[]**](ClassAttributeDto.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

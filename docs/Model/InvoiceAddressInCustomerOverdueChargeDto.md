# # InvoiceAddressInCustomerOverdueChargeDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**address_id** | **int** |  | [optional]
**address_line1** | **string** | Address 1 &amp;gt; The first line of the customer&#39;s contact address. | [optional]
**address_line2** | **string** | Address 2 &amp;gt; The second line of the address. | [optional]
**address_line3** | **string** | Address 3 &amp;gt; The third line of the address. | [optional]
**postal_code** | **string** | Postcode &amp;gt; The postcode. | [optional]
**city** | **string** | City &amp;gt; The city. | [optional]
**country** | [**\OpenAPI\Client\Model\CountryInCustomerDocumentAddressDto**](CountryInCustomerDocumentAddressDto.md) |  | [optional]
**county** | [**\OpenAPI\Client\Model\CountyInCustomerDocumentAddressDto**](CountyInCustomerDocumentAddressDto.md) |  | [optional]
**override_address** | **bool** | Override address &amp;gt; A check box that indicates (if selected) that the invoice address is not the default invoice address of the customer. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

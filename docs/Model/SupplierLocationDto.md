# # SupplierLocationDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**baccount** | [**\OpenAPI\Client\Model\BaccountInSupplierLocationDto**](BaccountInSupplierLocationDto.md) |  | [optional]
**location_id** | **string** | Mandatory field: The top part &amp;gt; Location ID* &amp;gt; The identifier of the location. Click the magnifier. | [optional]
**location_name** | **string** | The top part &amp;gt; Location name &amp;gt; A descriptive name to help users recognize the location. | [optional]
**active** | **bool** | The top part &amp;gt; Active &amp;gt; A check box that you select if the location is active. | [optional]
**address** | [**\OpenAPI\Client\Model\AddressInSupplierLocationDto**](AddressInSupplierLocationDto.md) |  | [optional]
**contact** | [**\OpenAPI\Client\Model\ContactInSupplierLocationDto**](ContactInSupplierLocationDto.md) |  | [optional]
**vat_registration_id** | **string** | General information tab &amp;gt; Location address section &amp;gt; VAT registration ID &amp;gt; The optional VAT registration ID associated with the location. | [optional]
**vat_zone** | [**\OpenAPI\Client\Model\VatZoneInSupplierLocationDto**](VatZoneInSupplierLocationDto.md) |  | [optional]
**edi_code** | **string** | General information tab &amp;gt; Location address section &amp;gt; EDI code &amp;gt; The EDI code to be used for the customer location. | [optional]
**gln** | **string** | General information tab &amp;gt; Location address section &amp;gt; GLN &amp;gt; The GLN to be used for the customer location. | [optional]
**corporate_id** | **string** | General information tab &amp;gt; Location address section &amp;gt; Corporate ID &amp;gt; The corporate ID associated with the customer location. | [optional]
**last_modified_date_time** | **\DateTime** | System generation information | [optional]
**supplier_payment_method_details** | [**\OpenAPI\Client\Model\SupplierPaymentMethodDetailDto[]**](SupplierPaymentMethodDetailDto.md) | Supplier payment method details from the supplier location page. | [optional]
**time_stamp** | **string** | Identifier that represents a specific version of the resource.  It helps to prevent simultaneous updates of the resource from overwriting each other (by using ETags and If-Match headers) | [optional]
**error_info** | **string** |  | [optional]
**metadata** | [**\OpenAPI\Client\Model\MetadataDto**](MetadataDto.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

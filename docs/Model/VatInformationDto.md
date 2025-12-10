# # VatInformationDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**vat_category_id** | **string** | VatCategoryId is deprecated, please use Vat Id instead | [optional]
**vat_id** | **string** | Mandatory field: VAT settings tab &amp;gt; VAT ID* &amp;gt; The unique ID of the VAT. | [optional]
**description** | **string** | VAT settings tab &amp;gt; Description &amp;gt; A detailed description of the VAT. | [optional]
**type** | **string** | VAT settings tab &amp;gt; VAT type &amp;gt; The type of VAT. | [optional]
**deductible_vat** | **bool** | VAT settings tab &amp;gt; Partially deductible VAT &amp;gt; A check box that indicates (if selected) that this is a deductible value-added VAT. | [optional]
**reverse_vat** | **bool** | VAT settings tab &amp;gt; Reverse VAT &amp;gt; A check box that indicates (if selected) that this is a reverse VAT. | [optional]
**statistical_vat** | **bool** | VAT settings tab &amp;gt; Statistical VAT &amp;gt; A check box that indicates (if selected) that the VAT on documents will be calculated only for statistical purposes or will be reported only but not actually paid. | [optional]
**pending_vat** | **bool** | VAT settings tab &amp;gt; Pendig VAT &amp;gt; A check box that indicates (if selected) that the VAT that should be calculated in documents, but should not be recorded to the VAT report until the VAT invoice is received. | [optional]
**includein_vat_exempt_total** | **bool** | VAT settings tab &amp;gt; Include in VAT exempt total &amp;gt; A check box that indicates (if selected) that this value-added VAT has a zero rate and is used to calculate a document subtotal that is actually exempt from VAT. | [optional]
**includein_vat_total** | **bool** | VAT settings tab &amp;gt; Include in VAT taxable total &amp;gt; A check box that indicates (if selected) that the VAT taxable amount should appear in the VAT taxable total field in the documents (such as invoices). | [optional]
**enter_from_vat_invoice** | **bool** | VAT settings tab &amp;gt; Enter from VAT invoice &amp;gt; A check box that indicates (if selected) that this VAT should be calculated for documents only if the documents are added to a VAT invoice or VAT adjustment. | [optional]
**calculate_on** | **string** | VAT settings tab &amp;gt; Calculate on &amp;gt; The method of calculating the tax amount, which is one of the following options: Extract from item amount, Item amount, Item and VAT amount, Document amount, Document and VAT amount. | [optional]
**cash_discount** | **string** | VAT settings tab &amp;gt; Cash discount &amp;gt; The method of calculating the tax base amount if a cash discount is applied. | [optional]
**vat_agency_id** | [**\OpenAPI\Client\Model\VatAgencyIdInVatInformationDto**](VatAgencyIdInVatInformationDto.md) |  | [optional]
**not_valid_after** | **\DateTime** | VAT settings tab &amp;gt; Not valid after &amp;gt; The date after which the VAT is not effective. | [optional]
**eu_report_code** | **string** | VAT settings tab &amp;gt; EU report code &amp;gt; The EU reporting code for the VAT. | [optional]
**document_text** | **string** | VAT Settings tab &amp;gt; Document text tab &amp;gt; Document text &amp;gt; The text to be printed to the VAT document. | [optional]
**default_non_stock_item** | [**\OpenAPI\Client\Model\DefaultNonStockItemInVatInformationDto**](DefaultNonStockItemInVatInformationDto.md) |  | [optional]
**visma_xml_vat_type** | **string** | VAT settings tab &amp;gt; Visma XML VAT type &amp;gt; The VAT type to be used in Visma XML files. | [optional]
**last_modified_date_time** | **\DateTime** | System generated information. | [optional]
**gl_accounts** | [**\OpenAPI\Client\Model\GlAccountsInVatInformationDto**](GlAccountsInVatInformationDto.md) |  | [optional]
**schedules** | [**\OpenAPI\Client\Model\VatInformationScheduleDto[]**](VatInformationScheduleDto.md) | Both tabs &amp;gt; VAT schedule &amp;gt; | [optional]
**categories** | [**\OpenAPI\Client\Model\VatCategoryDto[]**](VatCategoryDto.md) | Both tabs &amp;gt; Categories tab &amp;gt; | [optional]
**zones** | [**\OpenAPI\Client\Model\VatZoneDto[]**](VatZoneDto.md) | Both tabs &amp;gt; Zones tab &amp;gt; | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

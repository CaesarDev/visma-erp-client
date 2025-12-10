# # VatInformationScheduleDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**start_date** | **\DateTime** | Mandatory field: Start date &amp;gt; The date when the VAT at the rate in the current row becomes effective. | [optional]
**vat_rate** | **float** | VAT rate &amp;gt; The VAT rate (%) that is used to calculate the VAT amount. | [optional]
**min_taxable_amt** | **float** | Min. taxable amount &amp;gt; The minimum taxable amount for which this rate is applicable. | [optional]
**max_taxable_amt** | **float** | Max. taxable amount &amp;gt; The maximum taxable amount for which this rate applies. | [optional]
**reporting_group** | **string** | Reporting group &amp;gt; The reporting group for the VAT. | [optional]
**deductible_vat_rate** | **float** | Deductible VAT rate &amp;gt; The VAT rate (%) that is used to calculate the amount deductible from the output VAT. | [optional]
**group_type** | **string** | Group type &amp;gt; The type of the reporting group. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

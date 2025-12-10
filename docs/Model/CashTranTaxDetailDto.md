# # CashTranTaxDetailDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tax** | [**\OpenAPI\Client\Model\TaxInCashTranTaxDetailDto**](TaxInCashTranTaxDetailDto.md) |  | [optional]
**tax_rate** | **float** | VAT rate &amp;gt; The rate of the VAT. | [optional]
**taxable_amount** | **float** | Taxable amount &amp;gt; The taxable amount of the transaction. | [optional]
**tax_amount** | **float** | VAT amount &amp;gt; The VAT amount calculated for the transaction. | [optional]
**deductible_tax_rate** | **float** | Deductible VAT rate &amp;gt; The percent of deduction that applies to the VAT amount paid to the supplier for specific purchases. | [optional]
**expense_amount** | **float** | Expense amount &amp;gt; The percentage that is deducted from the VAT amount paid to the supplier for specific purchases. | [optional]
**include_in_vat_exempt_total** | **bool** | Include in VAT exempt total &amp;gt; A check box that indicates (if selected) that this value-added VAT has a zero rate and is used to calculate a document subtotal that is actually exempt from VAT. | [optional]
**pending_vat** | **bool** | Pending VAT &amp;gt; A check box that indicates (if selected) that the VAT that should be calculated in documents, but should not be recorded to the VAT report until the VAT invoice is received. | [optional]
**statistical_vat** | **bool** | Statistical VAT &amp;gt; A check box that indicates (if selected) that the VAT on documents will be calculated only for statistical purposes or will be reported only but not actually paid. | [optional]
**reverse_vat** | **bool** | Reverse VAT &amp;gt; A check box that indicates (if selected) that this is a reverse VAT. | [optional]
**tax_type** | **string** | VAT type &amp;gt; The type of VAT. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

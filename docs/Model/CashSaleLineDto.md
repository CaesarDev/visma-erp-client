# # CashSaleLineDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**line_number** | **int** | Line no. &amp;gt; A counter of lines in the overview of cash sales document overview. | [optional]
**inventory_number** | **string** | Item ID &amp;gt; The item ID of the line item, if applicable. Only a non-stock item can be selected. | [optional]
**description** | **string** | Transaction descr. &amp;gt; Any brief comment relevant to the transaction.The alphanumeric string may contain up to 30 characters. | [optional]
**quantity** | **float** | Quantity &amp;gt; The quantity of items (goods or services) of a particular type sold to the customer. | [optional]
**unit_price** | **float** | Unit price &amp;gt; The unit price set for the item or service. If you want to update the unit price  automatically to the current value(that is, the applicable sales or default price),  you can use the Recalculate Prices and Discounts action.If you have modified  the unit price and saved the document, the value will not be updated by the  system if you change the document date. | [optional]
**unit_price_in_currency** | **float** | Background calculation giving you the Unit price in your default currency. This field is applicable if the amount is given in another currency than your default. | [optional]
**manual_amount** | **float** | Manual amount &amp;gt; a check box indicating that the amount has been entered manually. | [optional]
**manual_amount_in_currency** | **float** | Background calculation giving you the Manual amount in your default currency. This field is applicable if the amount is given in another currency than your default. | [optional]
**amount** | **float** | Amount &amp;gt; The amount after the discount has been applied. The value of this read-only box  is calculated automatically by deducting the discount amount from the extended price. | [optional]
**cost** | **float** | Cost &amp;gt; The total cost of the line in default currency.   The value will always be 0 for unreleased documents. | [optional]
**amount_in_currency** | **float** | Background calculation giving you the Amount in your default currency. This field is applicable if the amount is given in another currency than your default. | [optional]
**account** | [**\OpenAPI\Client\Model\AccountInCashSaleLineDto**](AccountInCashSaleLineDto.md) |  | [optional]
**vat_code** | [**\OpenAPI\Client\Model\VatCodeInCashSaleLineDto**](VatCodeInCashSaleLineDto.md) |  | [optional]
**uom** | **string** | UoM &amp;gt; The unit of measure (UoM) for the item. | [optional]
**discount_percent** | **float** | Discount percent &amp;gt; The percent of the line-level discount that has been applied manually or  automatically.The system selects the Manual Discount check box and  calculates the discount amount after you have entered the percent manually and  saved your changes or added a new line. | [optional]
**discount_amount** | **float** | Discount amount &amp;gt; The amount of the line-level discount that has been applied manually or  automatically to this line.The system selects the Manual Discount check box  and calculates the line amount after you have entered the discount amount  manually and save your changes or added a new line. | [optional]
**discount_amount_in_currency** | **float** | Background calculation giving you the Discount amount in your default currency. This field is applicable if the amount is given in another currency than your default. | [optional]
**manual_discount** | **bool** | Manual discount &amp;gt; A check box that indicates (if selected) that the discount has been applied  manually.If you clear the check box, the system clears entered discount percent,  or discount amount, or selected discount code. | [optional]
**subaccount** | [**\OpenAPI\Client\Model\SubaccountInCashSaleLineDto**](SubaccountInCashSaleLineDto.md) |  | [optional]
**salesperson** | **string** | The field is deprecated for customer document endpoints, please use Seller instead | [optional]
**seller** | [**\OpenAPI\Client\Model\SellerInCashSaleLineDto**](SellerInCashSaleLineDto.md) |  | [optional]
**deferral_schedule** | **int** | Original deferral schedule &amp;gt; A read-only column filled in by the system in the Cash return documents created by the reversing process. It shows the identifier of the deferral schedule associated with the original Cash sale document. | [optional]
**deferral_code** | **string** | The deferral code assigned to the stock item or non-stock item specified in this  document line.Upon release of the document, the system generates a deferral  schedule (or schedules) based on the settings defined in this deferral code. | [optional]
**discount_code** | **string** | The code of the line discount that has been applied to this line automatically or manually. | [optional]
**note** | **string** | Table &amp;gt; Icon Notes &amp;gt; Pop-up window for providing any user-defined text connected to the order. | [optional]
**branch_number** | [**\OpenAPI\Client\Model\BranchNumberInCashSaleLineDto**](BranchNumberInCashSaleLineDto.md) |  | [optional]
**external_link** | **string** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

# # DiscountBreakpointDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**line_nbr** | **int** |  | [optional]
**active** | **bool** | The top part &amp;gt; Active &amp;gt; A check box that indicates (if selected) that the series is active. | [optional]
**break_amount** | **float** | Discount breakpoints tab &amp;gt; Break amount &amp;gt; The line amount (break point) that starts the new range for the currently effective series. | [optional]
**amount_to** | **float** |  | [optional]
**last_break_amount** | **float** | Discount breakpoints tab &amp;gt; Last break amount &amp;gt; The amount (break point) that started the new range for the previously effective series (the one that was used before the effective date). | [optional]
**last_amount_to** | **float** |  | [optional]
**pending_break_amount** | **float** | Discount breakpoints tab &amp;gt; Pending break amount &amp;gt; The amount (break point) that starts the new range for the pending series (one that is not yet in effect). | [optional]
**break_quantity** | **float** | Discount breakpoints tab &amp;gt; Break quantity &amp;gt; The quantity of items (break quantity) that starts the new range for a discount level for the currently effective series. Any break quantity should be specified in the base units. | [optional]
**quantity_to** | **float** |  | [optional]
**last_break_quantity** | **float** | Discount breakpoints tab &amp;gt; Last break quantity &amp;gt; The quantity of item (break point) that started the range for the discount series used before the effective date. | [optional]
**last_quantity_to** | **float** |  | [optional]
**pending_break_quantity** | **float** | Discount breakpoints tab &amp;gt; Pending break quantity &amp;gt; The quantity of items (break point) that starts the new range for the pending (not yet effective) series. | [optional]
**discount_amount** | **float** | Discount breakpoints tab &amp;gt; Discount amount &amp;gt; The discount amount to be used for the quantities that exceed this break quantity if the Amount option is selected as Discount by. | [optional]
**discount_percent** | **float** | Discount breakpoints tab &amp;gt; Discount percent &amp;gt; The discount percent to be currently used for the quantities that exceed this break quantity if the Percent option is selected as Discount by. | [optional]
**last_discount_amount** | **float** | Discount breakpoints tab &amp;gt; Last discount amount &amp;gt; The amount used as the discount for the discount series that was in effect before the effective date. | [optional]
**last_discount_percent** | **float** | Discount breakpoints tab &amp;gt; Last discount percent &amp;gt; The percentage used for the break point in the previously effective series. | [optional]
**last_discount** | **float** | Discount breakpoints tab &amp;gt; Last discount amount &amp;gt; The amount used as the discount for the discount series that was in effect before the effective date. | [optional]
**pending_discount_amount** | **float** | Discount breakpoints tab &amp;gt; Pending discount amount &amp;gt; The amount to be used as the discount for the pending series if the Amount option is selected as Discount by. | [optional]
**pending_discount_percent** | **float** | Discount breakpoints tab &amp;gt; Pending discount percent &amp;gt; The discount percent to be used for the break point in the pending series. | [optional]
**free_item_qty** | **float** | Discount breakpoints tab &amp;gt; Free item qty. &amp;gt; The quantity of the free item to be added as the discount to orders for this discount series. | [optional]
**last_free_item_qty** | **float** | Discount breakpoints tab &amp;gt; Last free item qty. &amp;gt; The quantity of the free item that was used as the discount for the previously effective series. | [optional]
**pending_free_item_qty** | **float** | Discount breakpoints tab &amp;gt; Pending free item qty. &amp;gt; The quantity of the free item to be added as the discount to orders for the pending discount series. | [optional]
**pending_date** | **\DateTime** |  | [optional]
**effective_date** | **\DateTime** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

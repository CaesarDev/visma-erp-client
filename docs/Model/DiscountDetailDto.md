# # DiscountDetailDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**line_nbr** | **int** | The table &amp;gt; Line number. | [optional]
**skip_discount** | **bool** | The table &amp;gt; Skip discount &amp;gt; A check box that you select to cancel a Group or Document level discount for the document. | [optional]
**discount_code** | **string** | Mandatory field: The table &amp;gt; Discount code* &amp;gt; The discount code of the supplier discount applied to the document automatically or manually. | [optional]
**sequance_id** | **string** | Mandatory field: The table &amp;gt; Series ID* &amp;gt; The ID of the discount sequence applied to the document. | [optional]
**type** | **string** | The table &amp;gt; Type &amp;gt; The type of discount applied to the document (Group or Document). | [optional]
**manual_discount** | **bool** | The table &amp;gt; Manual discount &amp;gt; A check box that indicates (if selected) that the supplier discount shown in this row has been applied manually . | [optional]
**discountable_amt** | **float** | The table &amp;gt; Discountable amt. &amp;gt; The amount used as a base for discount calculation if the discount is defined as based on the amount. | [optional]
**discountable_qty** | **float** | The table &amp;gt; Discountable qty. &amp;gt; The quantity used as a base for discount calculation if the discount is defined as based on the item quantity. | [optional]
**discount_amt** | **float** | The table &amp;gt; Discount amt. &amp;gt; The amount of the discount. | [optional]
**discount** | **float** | The table &amp;gt; Discount percent &amp;gt; The discount percent if by definition the discount is calculated as a percentage. | [optional]
**free_item** | **int** | The table &amp;gt; Free item &amp;gt; The item ID of the free item, if one is specified by the discount applied to the document. | [optional]
**free_item_qty** | **float** | The table &amp;gt; Free item qty.&amp;gt; The quantity of the free item to be added as the discount. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

# # DiscountCodeDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**discount_code** | **string** |  | [optional]
**description** | **string** |  | [optional]
**discount_type** | **string** | DiscountType: L - Line, G - Group, D - Document | [optional]
**applicable_to** | **string** | Mandatory field: Discount codes table &amp;gt; Applicable to &amp;gt; The entity to which the discount may be applied.  Applicable To values:   CU - Customer,  CI - Customer and Item,  CP - Customer and Item Price Class,  CE - Customer Price Class,  PI - Customer Price Class and Item,  PP - Customer Price Class and Item Price Class,  CB - Customer and Branch,  PB - Customer Price Class and Branch,  WH - Warehouse,  WI - Warehouse and Item,  WC - Warehouse and Customer,  WP - Warehouse and Item Price Class,  WE - Warehouse and Customer Price Class,  BR - Branch,  IN - Item,  IE - Item Price Class,  UN - Unconditional | [optional]
**apply_to_deferred_revenue** | **bool** | Discount codes table &amp;gt; Apply to deferred revenue &amp;gt; A check box that (if selected) indicates that a discount should be applied to a component price while computing a deferred revenue for the component. | [optional]
**manual** | **bool** | Discount codes table &amp;gt; Manual &amp;gt; A check box that (if selected) indicates that this discount is excluded from automatic searches for the best available discount. | [optional]
**exclude_from_discountable_amount** | **bool** | Discount codes table &amp;gt; Exclude from discountable amount &amp;gt; A check box that (if selected) indicates that the line amount is excluded from the amount that is the base for any applicable Group or Document discount. | [optional]
**skip_document_discounts** | **bool** | Discount codes table &amp;gt; Skip document discounts &amp;gt; A check box that indicates (if selected) that after this discount has been applied, no other applicable discounts should be applied. | [optional]
**auto_numbering** | **bool** | Discount codes table &amp;gt; Auto numbering &amp;gt; A check box that you select to use auto-numbering for generating IDs for series based on this discount code. | [optional]
**last_number** | **string** | Discount codes table &amp;gt; Last number &amp;gt; The last ID used for the series if series IDs are auto-numbered. | [optional]
**created_date_time** | **\DateTime** | System generated value. | [optional]
**last_modified_date_time** | **\DateTime** | System generated value. | [optional]
**error_info** | **string** |  | [optional]
**metadata** | [**\OpenAPI\Client\Model\MetadataDto**](MetadataDto.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

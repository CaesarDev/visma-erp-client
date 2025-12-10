# # CustomerSalesPriceDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**record_id** | **int** | Mandatory field: The Sales price table &amp;gt; Item ID* &amp;gt; The ID of the stock or non-stock stock item for which price information is listed. | [optional]
**price_type** | **string** | The Sales price table or the top part &amp;gt; Price type &amp;gt; The type of prices you want to view: All prices, Base, Customer, Customer price class. | [optional]
**price_code** | **string** | The Sales price table or the top part &amp;gt; Price code &amp;gt; The customer or a customer price class for which you want to create or edit a price list. | [optional]
**inventory_id** | **string** | The Sales price table or the top part &amp;gt; Warehouse &amp;gt; The warehouse in which the price applies. | [optional]
**description** | **string** | The Sales price table &amp;gt; Description &amp;gt; The description of the stock item. | [optional]
**uo_m** | **string** | Mandatory field: The Sales price table &amp;gt; UoM* &amp;gt; The unit of measure (UoM) used for the item. | [optional]
**promotion** | **bool** | The Sales price table &amp;gt; Promotion &amp;gt; A check box that indicates (if selected) that the price for this item is promotional. | [optional]
**break_qty** | **float** | The Sales price table &amp;gt; Break quantity &amp;gt; The quantity to define a lower bound for a quantity tier with the specific price. | [optional]
**price** | **float** | The Sales Price table &amp;gt; Price &amp;gt; The price for the item. | [optional]
**currency** | **string** | Mandatory field: The Sales price table &amp;gt; Currency* &amp;gt; The currency in which this price is specified. | [optional]
**vat** | **string** | The Sales price table &amp;gt; VAT &amp;gt; The VAT amount that is included in the sales price. | [optional]
**effective_date** | **\DateTime** | The Sales price table &amp;gt; Effective date &amp;gt; The date when the price became effective. | [optional]
**expiration_date** | **\DateTime** | The Sales price table &amp;gt; Ecpiration date &amp;gt; The date when the price expires. | [optional]
**last_modified_date_time** | **\DateTime** |  | [optional]
**warehouse** | **string** |  | [optional]
**time_stamp** | **string** | Identifier that represents a specific version of the resource.  It helps to prevent simultaneous updates of the resource from overwriting each other (by using ETags and If-Match headers) | [optional]
**error_info** | **string** |  | [optional]
**metadata** | [**\OpenAPI\Client\Model\MetadataDto**](MetadataDto.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

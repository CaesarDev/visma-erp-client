# # PackagingTypeDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**box_id** | **string** | Mandatory field: The table &amp;gt; Box ID* &amp;gt; The ID of the type of box. | [optional]
**description** | **string** | The table &amp;gt; Description &amp;gt; A description of the box. | [optional]
**box_weight** | **float** | The table &amp;gt; Tare weight &amp;gt; The weight of an empty box of this type, which may include the weight of any packaging material used to pack items inside the box. | [optional]
**max_weight** | **float** | The table &amp;gt; Max weight &amp;gt; The maximum weight a box of the type can hold. | [optional]
**weight_uo_m** | **string** | The table &amp;gt; Weight UoM &amp;gt; The unit of measure used for the weight. | [optional]
**max_volume** | **float** | The table &amp;gt; Max. volume &amp;gt; The maximum volume of items that can fit into a package of the type. | [optional]
**volume_uo_m** | **string** | The table &amp;gt; Volume UoM &amp;gt; The unit of measure used for the volume as specified in the Inventory preferences (IN101000) window. | [optional]
**length** | **int** | The table &amp;gt; Length &amp;gt; The length of the package. | [optional]
**width** | **int** | The table &amp;gt; Width &amp;gt; The width of the package. | [optional]
**height** | **int** | The table &amp;gt; Height &amp;gt; The height of the package. | [optional]
**active_by_default** | **bool** | The table &amp;gt; Active by default &amp;gt; If you select this check box, the package will be added by default to the list of packages for each new ship via code. | [optional]
**last_modified_date_time** | **\DateTime** | The table &amp;gt; The date and time when the type was last modified. | [optional]
**metadata** | [**\OpenAPI\Client\Model\MetadataDto**](MetadataDto.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

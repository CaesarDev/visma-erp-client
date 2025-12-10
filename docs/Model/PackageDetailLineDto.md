# # PackageDetailLineDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**line_number** | **int** | Packages tab &amp;gt; Line number. The sequence of the lines. | [optional]
**confirmed** | **bool** | Packages tab &amp;gt; Confirmed &amp;gt; This check box indicates (if selected) that shipping of the package specified on the line has been confirmed. | [optional]
**box_id** | **string** | Mandatory field: Packages tab &amp;gt; Box ID* &amp;gt; The box used for the package. | [optional]
**type** | **string** | Packages tab &amp;gt; Type &amp;gt; The type of package: Auto or Manual. | [optional]
**description** | **string** | Packages tab &amp;gt; Description &amp;gt; The description of the item or description of the box contents. | [optional]
**weight** | **float** | Packages tab &amp;gt; Weight &amp;gt; The gross weight of the package. | [optional]
**uom** | **string** | Packages tab &amp;gt; UoM &amp;gt; The unit of measure in which the weight of the package is specified. | [optional]
**volume** | **float** | Packages tab &amp;gt; Volume &amp;gt; The gross volume of the package. | [optional]
**volume_uom** | **string** | Packages tab &amp;gt; VolumeUoM &amp;gt; The unit of measure in which the volume of the package is specified. | [optional]
**declared_value** | **float** | Packages tab &amp;gt; Declared value &amp;gt; The amount of the package specified for insurance, you can edit the value if needed. | [optional]
**co_d_amount** | **float** | Packages tab &amp;gt; Cost of delivery amount &amp;gt; The amount to be charged on delivery of the package, you can edit the value if needed. | [optional]
**tracking_number** | **string** | Packages tab &amp;gt; Tracking number &amp;gt; The tracking number provided for the package by the carrier if integration with carrier is configured. | [optional]
**custom_ref_nbr1** | **string** | Packages tab &amp;gt; Customer ref. no. 1 &amp;gt; An auxiliary reference number to appear on the carrier label for the box. | [optional]
**custom_ref_nbr2** | **string** | Packages tab &amp;gt; Customer ref. no. 2 &amp;gt; An additional auxiliary reference number to appear on the carrier label for the box. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

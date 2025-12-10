# # DtoSegment

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**internal_id** | **string** | Unique identifier for the segment. | [optional]
**segment_id** | **int** | Segment ID &amp;gt; The system-generated number representing the order of the segment in the segmented key. | [optional]
**description** | **string** | Mandatory field: Description &amp;gt; The user-defined segment description. | [optional]
**length** | **int** | Length &amp;gt; The maximum length of the segment. | [optional]
**public_id** | **string** |  | [optional]
**time_stamp** | **string** |  | [optional]
**last_modified** | **\DateTime** | System generated information. | [optional]
**validate** | **bool** | Validate &amp;gt; A check box that indicates (if selected) that validation of segment values is turned on. | [optional]
**segment_values** | [**\OpenAPI\Client\Model\DtoSegmentValue[]**](DtoSegmentValue.md) | The table &amp;gt; | [optional]
**is_auto_number** | **bool** | Select segment and click View segment &amp;gt; Auto number &amp;gt; A check box that indicates (if selected) that the number series selected in the Number series ID field will be used to generate values for this segment in IDs. | [optional]
**consol_num_char** | **int** | Select segment and click View segment &amp;gt; Number of characters &amp;gt; The length (in characters) of the string in the parent&#39;s subaccount to which the segment value is mapped; this column is displayed for only the SUBACCOUNT key. | [optional]
**consol_order** | **int** | Select segment and click View segment &amp;gt; Consol. order &amp;gt; The number that represents the order of this string among other strings in the parent company&#39;s subaccount; this column is displayed for only the SUBACCOUNT key. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

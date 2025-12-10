# # NumberingDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**numbering_id** | **string** | Mandatory field: The top part &amp;gt; Numbering ID &amp;gt; The unique ID of the numbering series, which is an alphanumeric string of up to 10 characters. | [optional]
**description** | **string** | Mandatory field: The top part &amp;gt; Description* &amp;gt; The description of the numbering series. | [optional]
**manual_numbering** | **bool** | The top part &amp;gt; Manual numbering &amp;gt; A check box that indicates (if selected) that the system will not generate numbers for the series and users will need to specify document numbers manually. | [optional]
**new_number_symbol** | **string** | Mandatory field: The top part &amp;gt; New number symbol* &amp;gt; An alphanumeric string used to indicate that a new number for an object will be assigned. | [optional]
**sequence** | [**\OpenAPI\Client\Model\NumberingSequenceDto[]**](NumberingSequenceDto.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

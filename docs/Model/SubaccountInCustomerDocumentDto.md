# # SubaccountInCustomerDocumentDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**subaccount_number** | **string** | Mandatory field: Subaccount* &amp;gt; The subaccount number. Format 9-XX. | [optional]
**subaccount_id** | **int** | SubID &amp;gt; The  identifier of the subaccount. | [optional]
**description** | **string** | Description &amp;gt; The description of the identifier. | [optional]
**last_modified_date_time** | **\DateTime** | System generated information. | [optional]
**active** | **bool** | Active &amp;gt; The status of the identifier. | [optional]
**segments** | [**\OpenAPI\Client\Model\SegmentDto[]**](SegmentDto.md) | Segments are entities that you use to define the structure of IDs for the subaccount.  This information is collected from window CS202000. | [optional]
**time_stamp** | **string** | The timestamp of the subaccount, used for concurrency control. | [optional]
**error_info** | **string** |  | [optional]
**metadata** | [**\OpenAPI\Client\Model\MetadataDto**](MetadataDto.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

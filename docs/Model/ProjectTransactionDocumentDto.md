# # ProjectTransactionDocumentDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ref_nbr** | **string** | The top part &amp;gt; Ref. no. &amp;gt; The reference number of the transaction. | [optional]
**description** | **string** | The top part &amp;gt; Description &amp;gt; The description provided for the transaction. | [optional]
**orig_doc_nbr** | **string** | The top part &amp;gt; Orig. doc. no. &amp;gt; The reference number of the underlying document for the transaction. | [optional]
**status** | **string** | The top part &amp;gt; Status &amp;gt; The status of the transaction. The following statuses are possible: Balanced, Released. | [optional]
**module** | **string** | The top part &amp;gt; Module &amp;gt; The module you create the transactions in. | [optional]
**orig_doc_type** | **string** | The top part &amp;gt; Orig. doc. no. &amp;gt; The type of the document the transaction is based on. It has one of the following values: Allocation, Time card, Case, Expense claim, Allocation reversal, Reversal, Credit note. | [optional]
**note** | **string** |  | [optional]
**time_stamp** | **string** | Identifier that represents a specific version of the resource.  It helps to prevent simultaneous updates of the resource from overwriting each other (by using ETags and If-Match headers) | [optional]
**lines** | [**\OpenAPI\Client\Model\ProjectTransactionLineDto[]**](ProjectTransactionLineDto.md) | The table &amp;gt; | [optional]
**error_info** | **string** |  | [optional]
**metadata** | [**\OpenAPI\Client\Model\MetadataDto**](MetadataDto.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

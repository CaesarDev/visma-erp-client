# # SalesOrderTypeDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**order_type** | **string** | Mandatory field: The top part &amp;gt; Order type* &amp;gt; The ID of the order type, which is a two-character alphanumeric string. | [optional]
**active** | **bool** | The top part &amp;gt; Active &amp;gt; A check box that indicates (if selected) that the order type is active, | [optional]
**description** | **string** | The top part &amp;gt; Description &amp;gt; The brief description of the order type. | [optional]
**behavior** | **string** | Template settings tab &amp;gt; Automation behaviour &amp;gt; An automation behaviour is a set of automation steps. The type of automation behaviour used for the template, which can be Sales order, Invoice, Quote, Credit note, or RMA order. | [optional]
**default_operation** | **string** | Template settings tab &amp;gt; Default operation &amp;gt; The default inventory operation for the order type, which can be Receipt or Issue. | [optional]
**customer_document_type** | **string** | Template settings tab &amp;gt; Customer document type &amp;gt; The type of customer ledger document to be generated on release of a document of this type. | [optional]
**error_info** | **string** |  | [optional]
**metadata** | [**\OpenAPI\Client\Model\MetadataDto**](MetadataDto.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

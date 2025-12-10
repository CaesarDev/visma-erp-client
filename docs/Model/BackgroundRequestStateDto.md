# # BackgroundRequestStateDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Identifies a started background API operation | [optional]
**status** | **string** | Current status of a background API operation. Possible values are &#39;Started&#39;, &#39;Finished&#39; and &#39;Failed&#39;. | [optional]
**status_code** | **int** | The Http Status Code of the finished background API operation. Value is 0 when operation is not done. | [optional]
**received_utc** | **\DateTime** | Time when background API operation was requested | [optional]
**started_utc** | **\DateTime** | Time when processing of background API operation was started | [optional]
**finished_utc** | **\DateTime** | Time when background API operation was finished processing | [optional]
**webhook_address** | **string** | The webhook uri used to notify when background API operation is finished, or &#39;none&#39; if no notification is configured | [optional]
**error_message** | **string** | Any error message during processing of background API operation request. Note that any error response from the actual endpoint can be obtained by calling the ContentLocation address from the webhook notifaction response or the background state document. | [optional]
**reference** | **string** |  | [optional]
**original_uri** | **string** | The endpoint that was requested to be processed as a background API operation. | [optional]
**has_response_content** | **bool** | Indicates whether or not the background API operation ended with a response content. Value is updated only when background API operation is finished. | [optional]
**has_request_content** | **bool** | Indicates whether or not the background API operation request has a request content. | [optional]
**content_location** | **string** | The uri from where the client can get the response from the background API operation, if any is available. | [optional] [readonly]
**response_headers** | **array<string,string>** | Any response headers from the finished background API operation. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

# # ExpenseClaimDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ref_nbr** | **string** | The top part &amp;gt; Ref. no. &amp;gt; The unique reference number of the expense claim document. | [optional]
**status** | **string** | The top part &amp;gt; Status &amp;gt; The current status of the expense claim: On Hold/Pending Approval/Approved/Rejected/Released. | [optional]
**approval_status** | **string** | The top part &amp;gt; Approval status &amp;gt; The status of the claim in Approval. | [optional]
**date** | **\DateTime** | Mandatory field: The top part &amp;gt; Date* &amp;gt; The date when the claim was entered. | [optional]
**description** | **string** | Mandatory field: The top part &amp;gt; Description &amp;gt; A description of the claim. | [optional]
**claimed_by** | [**\OpenAPI\Client\Model\ClaimedByInExpenseClaimDto**](ClaimedByInExpenseClaimDto.md) |  | [optional]
**claim_total** | **float** | The top part &amp;gt; Claim total &amp;gt; The total amount of the claim. | [optional]
**vat_taxable_total** | **float** | The top part &amp;gt; VAT taxable total &amp;gt; The document total that is subjected to VAT. | [optional]
**vat_exempt_total** | **float** | The top part &amp;gt; VAT exempt total &amp;gt; The document total that is exempt from VAT. | [optional]
**customer** | [**\OpenAPI\Client\Model\CustomerInExpenseClaimDto**](CustomerInExpenseClaimDto.md) |  | [optional]
**currency** | **string** | The top part &amp;gt; Currency &amp;gt; The currency of the claim. | [optional]
**approval_date** | **\DateTime** | The top part &amp;gt; Approval date &amp;gt; The date when the claim was approved. | [optional]
**department** | [**\OpenAPI\Client\Model\DepartmentInExpenseClaimDto**](DepartmentInExpenseClaimDto.md) |  | [optional]
**location** | [**\OpenAPI\Client\Model\LocationInExpenseClaimDto**](LocationInExpenseClaimDto.md) |  | [optional]
**last_modified_date_time** | **\DateTime** | System generated information: The lastest time the expense claim was modified | [optional]
**details** | [**\OpenAPI\Client\Model\ExpenseClaimDetailDto[]**](ExpenseClaimDetailDto.md) | Expence claim details tab &amp;gt; | [optional]
**approval_status_text** | **string** | The top part &amp;gt; Approval status &amp;gt; A text field. | [optional]
**time_stamp** | **string** | Identifier that represents a specific version of the resource.  It helps to prevent simultaneous updates of the resource from overwriting each other (by using ETags and If-Match headers) | [optional]
**error_info** | **string** |  | [optional]
**metadata** | [**\OpenAPI\Client\Model\MetadataDto**](MetadataDto.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

# # ExpenseClaimDetailDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**claim_detail_id** | **int** | Identifies the expense claim detail id, necessary when updating detail information | [optional]
**line_id** | **string** | The expense claim line id | [optional]
**date** | **\DateTime** | Mandatory field: Date &amp;gt; The date when the expense was incurred. | [optional]
**expense_item** | [**\OpenAPI\Client\Model\ExpenseItemInExpenseClaimDetailDto**](ExpenseItemInExpenseClaimDetailDto.md) |  | [optional]
**description** | **string** | Mandatory field: Description* &amp;gt; A description of the transaction. | [optional]
**quantity** | **float** | Quantity &amp;gt; The quantity of this expense item. | [optional]
**uom** | **string** | Mandatory field: UoM &amp;gt; The unit of measure in which the quantity is shown. | [optional]
**unit_cost** | **float** | Unit cost &amp;gt; The cost of a unit of the item. | [optional]
**currency** | **string** | Currency &amp;gt; The currency of the expense receipt. However, if you enter a claim line directly, the currency value is read-only and matching the claim currency. | [optional]
**total_amount** | **float** | Amount &amp;gt; The total amount paid for the expense item in the specified quantity. | [optional]
**invoiceable** | **bool** | Invoicable &amp;gt; A check box that, if selected, indicates that the claim amount is invoiceable to the customer (the total amount minus the employee&#39;s part). | [optional]
**claim_amount** | **float** | Claim amount &amp;gt; The amount claimed by the employee, which is calculated as the total claim amount minus the employee part. | [optional]
**amount_in_claim_curr** | **float** | Amount in claim currency &amp;gt; The amount claimed by the employee, which is expressed in the currency of the expense claim. | [optional]
**project** | [**\OpenAPI\Client\Model\ProjectInExpenseClaimDetailDto**](ProjectInExpenseClaimDetailDto.md) |  | [optional]
**project_task** | [**\OpenAPI\Client\Model\ProjectTaskInExpenseClaimDetailDto**](ProjectTaskInExpenseClaimDetailDto.md) |  | [optional]
**expense_account** | [**\OpenAPI\Client\Model\ExpenseAccountInExpenseClaimDetailDto**](ExpenseAccountInExpenseClaimDetailDto.md) |  | [optional]
**expense_subaccount** | [**\OpenAPI\Client\Model\ExpenseSubaccountInExpenseClaimDetailDto**](ExpenseSubaccountInExpenseClaimDetailDto.md) |  | [optional]
**branch** | [**\OpenAPI\Client\Model\BranchInExpenseClaimDetailDto**](BranchInExpenseClaimDetailDto.md) |  | [optional]
**tax_category** | [**\OpenAPI\Client\Model\TaxCategoryInExpenseClaimDetailDto**](TaxCategoryInExpenseClaimDetailDto.md) |  | [optional]
**ref_nbr** | **string** | Ref. no. &amp;gt; The identifier of the transaction. | [optional]
**sales_account** | [**\OpenAPI\Client\Model\SalesAccountInExpenseClaimDetailDto**](SalesAccountInExpenseClaimDetailDto.md) |  | [optional]
**sales_subaccount** | [**\OpenAPI\Client\Model\SalesSubaccountInExpenseClaimDetailDto**](SalesSubaccountInExpenseClaimDetailDto.md) |  | [optional]
**employee_part** | **float** | Employee part &amp;gt; The part of the total amount that will not be paid back to the employee. The percentage depends on the company policy. | [optional]
**customer** | [**\OpenAPI\Client\Model\CustomerInExpenseClaimDetailDto**](CustomerInExpenseClaimDetailDto.md) |  | [optional]
**location** | [**\OpenAPI\Client\Model\LocationInExpenseClaimDetailDto**](LocationInExpenseClaimDetailDto.md) |  | [optional]
**ar_reference_nbr** | **string** | REef.no. customer &amp;gt; The reference number of the customer ledger document. | [optional]
**approval_status** | **string** | Approval status &amp;gt; The approval status, which indicates whether the detail row requires approval and, if it does, what the current state of approval is. | [optional]
**approval_status_text** | **string** | Last approval comment &amp;gt; The approval status text suitable for display | [optional]
**approver** | **string** | Pending approver &amp;gt; The identifier of the person authorized to approve the activity, if approval is required. This is either the approver of the project task or, if no approver is assigned to the project task, the project manager. | [optional]
**attachments** | [**\OpenAPI\Client\Model\AttachmentDto[]**](AttachmentDto.md) | Expense claim detail line attachtments | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

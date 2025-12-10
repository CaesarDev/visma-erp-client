# # ExpenseReceiptDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**internal_id** | **int** |  | [optional]
**receipt_id** | **string** | The top part &amp;gt; Employee &amp;gt;  The identifier of the employee whose expense receipts you want to manage. | [optional]
**date** | **\DateTime** | Both tabs &amp;gt; Date &amp;gt; The date of the expense receipt. | [optional]
**tax_total** | **float** | The top part &amp;gt; VAT total &amp;gt; The total amount of VAT or taxes calculated for the expense receipt. | [optional]
**currency** | [**\OpenAPI\Client\Model\CurrencyInExpenseReceiptDto**](CurrencyInExpenseReceiptDto.md) |  | [optional]
**ref_nbr** | **string** | Both tabs &amp;gt; Ref. no. &amp;gt; The reference number, which usually matches the number of the original receipt. | [optional]
**inventory** | [**\OpenAPI\Client\Model\InventoryNumberDescriptionDto**](InventoryNumberDescriptionDto.md) |  | [optional]
**description** | **string** | Open the receipt  Mandatory field: Receipt details tab &amp;gt; Expense details section &amp;gt; Description* &amp;gt; The expense description, which is displayed as a link. | [optional]
**uom** | **string** | Receipt details tab &amp;gt; Expense details section &amp;gt; UoM &amp;gt; The unit of measure of the expense item. | [optional]
**quantity** | **float** | Receipt details tab &amp;gt; Expense details section &amp;gt; Quantity &amp;gt; The quantity of the expense item that the employee purchased according to the receipt. | [optional]
**unit_cost** | **float** | Receipt details tab &amp;gt; Expense details section &amp;gt; Unit cost &amp;gt; The cost of one unit of the expense item. | [optional]
**total_amount** | **float** | Receipt details tab &amp;gt; Expense details section &amp;gt; Amount &amp;gt; The total amount of the receipt (for VAT-inclusive taxes), or the total amount before taxes (for VAT-exclusive taxes). | [optional]
**employee_part** | **float** | Receipt details tab &amp;gt; Expense details section &amp;gt; Employee part  &amp;gt; The part of the total amount that will not be paid back to the employee. | [optional]
**claim_amount** | **float** | Receipt details tab &amp;gt; Expense details section &amp;gt; Expense claim &amp;gt; The expense claim with which the expense receipt is associated. | [optional]
**status** | **string** | Receipt details tab &amp;gt; Expense details section &amp;gt; Expense claim status &amp;gt; The current status of the associated expense claim, which can be one of the following options: On hold, Pending apporval, Approved, Rejected, Released. | [optional]
**claimed_by** | [**\OpenAPI\Client\Model\ClaimedByInExpenseReceiptDto**](ClaimedByInExpenseReceiptDto.md) |  | [optional]
**branch** | [**\OpenAPI\Client\Model\BranchInExpenseReceiptDto**](BranchInExpenseReceiptDto.md) |  | [optional]
**expense_claim** | [**\OpenAPI\Client\Model\ExpenseClaimInExpenseReceiptDto**](ExpenseClaimInExpenseReceiptDto.md) |  | [optional]
**invoiceable** | **bool** | Receipt details tab &amp;gt; Financial details section &amp;gt; Invoiceable &amp;gt; A check box that indicates (if selected) that the customer should be invoiced for the claim amount. | [optional]
**project** | [**\OpenAPI\Client\Model\ProjectInExpenseReceiptDto**](ProjectInExpenseReceiptDto.md) |  | [optional]
**project_task** | [**\OpenAPI\Client\Model\ProjectTaskInExpenseReceiptDto**](ProjectTaskInExpenseReceiptDto.md) |  | [optional]
**customer** | [**\OpenAPI\Client\Model\CustomerInExpenseReceiptDto**](CustomerInExpenseReceiptDto.md) |  | [optional]
**location** | [**\OpenAPI\Client\Model\LocationInExpenseReceiptDto**](LocationInExpenseReceiptDto.md) |  | [optional]
**expense_account** | [**\OpenAPI\Client\Model\ExpenseAccountInExpenseReceiptDto**](ExpenseAccountInExpenseReceiptDto.md) |  | [optional]
**expense_sub** | [**\OpenAPI\Client\Model\ExpenseSubInExpenseReceiptDto**](ExpenseSubInExpenseReceiptDto.md) |  | [optional]
**sales_account** | [**\OpenAPI\Client\Model\SalesAccountInExpenseReceiptDto**](SalesAccountInExpenseReceiptDto.md) |  | [optional]
**sales_sub** | [**\OpenAPI\Client\Model\SalesSubInExpenseReceiptDto**](SalesSubInExpenseReceiptDto.md) |  | [optional]
**tax_category** | [**\OpenAPI\Client\Model\TaxCategoryInExpenseReceiptDto**](TaxCategoryInExpenseReceiptDto.md) |  | [optional]
**image** | [**\OpenAPI\Client\Model\ImageInExpenseReceiptDto**](ImageInExpenseReceiptDto.md) |  | [optional]
**time_stamp** | **string** | Identifier that represents a specific version of the resource.  It helps to prevent simultaneous updates of the resource from overwriting each other (by using ETags and If-Match headers) | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

# # BudgetDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**financial_year** | **string** | Mandatory field: The top part &amp;gt; Financial year* &amp;gt; The financial year of the budget. | [optional]
**released** | **bool** | The budget area &amp;gt; The budget articles pane &amp;gt; Released &amp;gt; A check box that indicates (if selected) that the budget article has been released. | [optional]
**released_amount** | **float** | The budget area &amp;gt; The budget articles pane &amp;gt; Released amount &amp;gt; The amount that has been released for this article. | [optional]
**account** | [**\OpenAPI\Client\Model\AccountInBudgetDto**](AccountInBudgetDto.md) |  | [optional]
**subaccount** | [**\OpenAPI\Client\Model\SubaccountInBudgetDto**](SubaccountInBudgetDto.md) |  | [optional]
**description** | **string** | Mandatory field: The budget area &amp;gt; The budget articles pane &amp;gt; Description* &amp;gt; A description of the budget article.By default, this column displays the account description. | [optional]
**amount** | **float** | The budget area &amp;gt; The budget articles pane &amp;gt; Amount &amp;gt; The article amount. | [optional]
**distributed_amount** | **float** | The budget area  The budget articles pane &amp;gt; Distributed amount &amp;gt; The amount distributed over the periods. | [optional]
**periods** | [**\OpenAPI\Client\Model\FinancialPeriodAmountDto[]**](FinancialPeriodAmountDto.md) | The budget area The budget articles pane &amp;gt; Period XX &amp;gt; Amount per period within the financial year. | [optional]
**last_modified_date_time** | **\DateTime** | A system generated date/time not visible in the window. | [optional]
**branch_number** | [**\OpenAPI\Client\Model\BranchNumberInBudgetDto**](BranchNumberInBudgetDto.md) |  | [optional]
**time_stamp** | **string** | The timestamp of the budget article, used for concurrency control. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

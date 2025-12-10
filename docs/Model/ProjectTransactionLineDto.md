# # ProjectTransactionLineDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tran_id** | **int** |  | [optional]
**date** | **\DateTime** | Date &amp;gt; The date the transaction was created. | [optional]
**inventory_id** | [**\OpenAPI\Client\Model\InventoryIdInProjectTransactionLineDto**](InventoryIdInProjectTransactionLineDto.md) |  | [optional]
**description** | **string** | Description &amp;gt; The description of the transaction. | [optional]
**uom** | **string** | UoM &amp;gt; The unit of measure used to estimate the quantity for the transaction, such as HOUR or BOX. | [optional]
**quantity** | **float** | Quantity &amp;gt;  The quantity for the transaction, such as the number of service hours provided to the customer. | [optional]
**unit_rate** | **float** | Unit rate &amp;gt; The price of the item or the rate of the service. | [optional]
**amount** | **float** | Amount &amp;gt; The amount of the transaction. | [optional]
**billable** | **bool** | Invoiceable &amp;gt; A check box indicating whether the transaction is used in calculating the amount charged to the customer for the project task. | [optional]
**released** | **bool** | Released &amp;gt; A check box indicating whether the transaction has been released. | [optional]
**allocated** | **bool** | Allocated &amp;gt; A check box that indicates whether the amounts of the transactions were allocated for the project. | [optional]
**billable_quantity** | **float** | Qty. that can be invoiced &amp;gt; The total invoiceable quantity for the transactions listed in the table. | [optional]
**financial_period** | **string** | Period &amp;gt; The financial period associated with the transaction. | [optional]
**batch_nbr** | **string** | Batch no. &amp;gt; The batch number of the transaction in the General ledger workspace. | [optional]
**use_billable_qty** | **bool** | Use the quantity that can be invoiced in the amount formula &amp;gt; A check box that you select if you want the system to use the invoiceable quantity (the Invoiceable quantity column) instead of the overall quantity (the Quantity column) of the transaction when calculating the amount of transaction. | [optional]
**start_date** | **\DateTime** | Start date &amp;gt; The start date for this transaction. | [optional]
**end_date** | **\DateTime** | End date &amp;gt; The end date for this transaction | [optional]
**last_modified_date_time** | **\DateTime** | System generated information | [optional]
**earning_type** | [**\OpenAPI\Client\Model\EarningTypeInProjectTransactionLineDto**](EarningTypeInProjectTransactionLineDto.md) |  | [optional]
**overtime_multiplier** | **float** | Multiplier &amp;gt; The multiplier by which the unit rate is multiplied when the labour cost is calculated. | [optional]
**project** | [**\OpenAPI\Client\Model\ProjectInProjectTransactionLineDto**](ProjectInProjectTransactionLineDto.md) |  | [optional]
**project_task** | [**\OpenAPI\Client\Model\ProjectTaskInProjectTransactionLineDto**](ProjectTaskInProjectTransactionLineDto.md) |  | [optional]
**debit_account** | [**\OpenAPI\Client\Model\DebitAccountInProjectTransactionLineDto**](DebitAccountInProjectTransactionLineDto.md) |  | [optional]
**debit_subaccount** | [**\OpenAPI\Client\Model\DebitSubaccountInProjectTransactionLineDto**](DebitSubaccountInProjectTransactionLineDto.md) |  | [optional]
**credit_account** | [**\OpenAPI\Client\Model\CreditAccountInProjectTransactionLineDto**](CreditAccountInProjectTransactionLineDto.md) |  | [optional]
**credit_subaccount** | [**\OpenAPI\Client\Model\CreditSubaccountInProjectTransactionLineDto**](CreditSubaccountInProjectTransactionLineDto.md) |  | [optional]
**branch** | [**\OpenAPI\Client\Model\BranchInProjectTransactionLineDto**](BranchInProjectTransactionLineDto.md) |  | [optional]
**employee** | [**\OpenAPI\Client\Model\EmployeeInProjectTransactionLineDto**](EmployeeInProjectTransactionLineDto.md) |  | [optional]
**customer_vendor** | [**\OpenAPI\Client\Model\CustomerVendorInProjectTransactionLineDto**](CustomerVendorInProjectTransactionLineDto.md) |  | [optional]
**account_group** | [**\OpenAPI\Client\Model\AccountGroupInProjectTransactionLineDto**](AccountGroupInProjectTransactionLineDto.md) |  | [optional]
**debit_account_group** | [**\OpenAPI\Client\Model\DebitAccountGroupInProjectTransactionLineDto**](DebitAccountGroupInProjectTransactionLineDto.md) |  | [optional]
**credit_account_group** | [**\OpenAPI\Client\Model\CreditAccountGroupInProjectTransactionLineDto**](CreditAccountGroupInProjectTransactionLineDto.md) |  | [optional]
**location** | [**\OpenAPI\Client\Model\LocationInProjectTransactionLineDto**](LocationInProjectTransactionLineDto.md) |  | [optional]
**note** | **string** |  | [optional]
**error_info** | **string** |  | [optional]
**metadata** | [**\OpenAPI\Client\Model\MetadataDto**](MetadataDto.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

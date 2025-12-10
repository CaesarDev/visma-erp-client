# # FinancialPeriodDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**year** | **int** | Mandatory field: The top part &amp;gt; Financial year* &amp;gt; The financial year. | [optional]
**period** | **string** | The table &amp;gt; Period &amp;gt; The period no and the year. | [optional]
**start_date** | **\DateTime** | The table &amp;gt; Start date &amp;gt; The date when the financial period starts. | [optional]
**end_date** | **\DateTime** | The table &amp;gt; End date &amp;gt; The date when the financial period ends. | [optional]
**description** | **string** | The table &amp;gt; Description &amp;gt; The description of the financial period (such as the name of the month or the number of the quarter). | [optional]
**active** | **bool** | The table &amp;gt; Active &amp;gt; A check box that indicates (if selected) that the period can be used for posting transactions. | [optional]
**closed_in_supplier_ledger** | **bool** | The table &amp;gt; Closed in Supplier ledger &amp;gt; A read-only check box that indicates (if selected) that the financial period is closed in the Supplier ledger workspace; if this check box is cleared, the period is active in the this workspace. | [optional]
**closed_in_customer_ledger** | **bool** | The table &amp;gt; Closed in Customer ledger &amp;gt; A read-only check box that indicates (if selected) that the financial period is closed in the Customer ledger workspace; if this check box is cleared, the period is active in this workspace. | [optional]
**closed_in_inventory_management** | **bool** | The table &amp;gt; Closed in Inventory management &amp;gt; Inventory management A read-only check box that indicates (if selected) that the financial period is closed in the Inventory workspace; if this check box is cleared, the period is active in the workspace. | [optional]
**closed_in_general_ledger** | **bool** | The table &amp;gt; Closed in General ledger &amp;gt; A read-only check box that indicates (if selected) that the financial period is closed in the General ledger workspace; if this check box is cleared, the period is active in the this workspace. | [optional]
**closed_in_cash_management** | **bool** | The table &amp;gt; Closed in Cash management &amp;gt; A read-only check box that indicates (if selected) that the financial period is closed in the Cash management; if this check box is cleared, the period is active in this workspace. | [optional]
**closed_in_fixed_assets** | **bool** | The table &amp;gt; Closed in Fixed assets &amp;gt; A read-only check box that indicates (if selected) that the financial period is closed in the Fixed assets workspace; if this check box is cleared, the period is active in the this workspace. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

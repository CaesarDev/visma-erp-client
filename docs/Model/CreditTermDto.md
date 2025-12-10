# # CreditTermDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**terms_id** | **string** |  | [optional]
**description** | **string** |  | [optional]
**visible_to** | **string** | VisibleTo: AL - All, VE - Suppliers, CU - Customers, DS - Disabled | [optional]
**due_date_type** | **string** | Due Date Type , values:  N - Fixed Number of Days,   D - Day of Next Month,   E - End of the Month,   M - End of Next Month,   T - Day of the Month,   P - Fixed Number of Days starting Next Month,   C - Custom. | [optional]
**move_due_date_if_on_the_weekend** | **string** | Move Due Date If On The Weekend, values:  1 - Keep the exact date,   2 - Day before (Friday),    3 - Day after (Monday). | [optional]
**due_day1** | **int** |  | [optional]
**due_day1_day_from1** | **int** |  | [optional]
**due_day1_day_to1** | **int** |  | [optional]
**due_day2** | **int** |  | [optional]
**due_day2_day_from1** | **int** |  | [optional]
**due_day2_day_to1** | **int** |  | [optional]
**discount_type** | **string** | Discount Type , values:  N - Fixed Number of Days,   D - Day of Next Month,   E - End of the Month,   M - End of Next Month,   T - Day of the Month,   P - Fixed Number of Days starting Next Month. | [optional]
**discount_day** | **int** |  | [optional]
**discount_percent** | **float** |  | [optional]
**delay_days** | **int** |  | [optional]
**calculation_type** | **string** | Calculation Type: G - Gross amount, N - Net amount | [optional]
**instalment_type** | **string** | Instalment Type: S - Simple, M - Multiple | [optional]
**number_of_instalments** | **int** |  | [optional]
**instalment_frequency** | **string** | Instalment Frequency, values:  W - Weekly,  M - Monthly,  B - Semi-monthly (the second installment comes a half a month after the first one, and so on). | [optional]
**instalment_method** | **string** | Instalment Method, values:  E - Equal Parts,  A - All Tax in First Installment (the total amount before tax is split equally between installments and the entire amount of tax is added to the first installment),  S - Split by Percents in Table (the days and amounts of installments are defined by the related Instalments Schedule records). | [optional]
**instalments_schedule** | [**\OpenAPI\Client\Model\InstalmentSchedule[]**](InstalmentSchedule.md) |  | [optional]
**created_date_time** | **\DateTime** |  | [optional]
**last_modified_date_time** | **\DateTime** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

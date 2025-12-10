# # EntryTypeDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**entry_type_id** | **string** | Entry type ID* &amp;gt; The entry type, selected by its identifier. | [optional]
**disable_receipt** | **string** | Disb/receipt &amp;gt; The basic type of cash transaction designated by this entry type: Receipt or Disbursement. | [optional]
**module** | **string** | Module &amp;gt; The way the entry type is used in the system. | [optional]
**default_offset_account_branch** | [**\OpenAPI\Client\Model\DefaultOffsetAccountBranchInEntryTypeDto**](DefaultOffsetAccountBranchInEntryTypeDto.md) |  | [optional]
**default_offset_account** | [**\OpenAPI\Client\Model\DefaultOffsetAccountInEntryTypeDto**](DefaultOffsetAccountInEntryTypeDto.md) |  | [optional]
**default_offset_subaccount** | [**\OpenAPI\Client\Model\DefaultOffsetSubaccountInEntryTypeDto**](DefaultOffsetSubaccountInEntryTypeDto.md) |  | [optional]
**reclasification_account** | [**\OpenAPI\Client\Model\ReclasificationAccountInEntryTypeDto**](ReclasificationAccountInEntryTypeDto.md) |  | [optional]
**business_account** | [**\OpenAPI\Client\Model\BusinessAccountInEntryTypeDto**](BusinessAccountInEntryTypeDto.md) |  | [optional]
**description** | **string** | Description &amp;gt; A detailed description of the entry type that is used as transaction description by default. | [optional]
**use_for_payments_reclasification** | **bool** | A check box that you select if this entry type is used to record unknown payments that need to be reclassified later. | [optional]
**reclasification_account_override** | [**\OpenAPI\Client\Model\ReclasificationAccountOverrideInEntryTypeDto**](ReclasificationAccountOverrideInEntryTypeDto.md) |  | [optional]
**offset_account_override** | [**\OpenAPI\Client\Model\OffsetAccountOverrideInEntryTypeDto**](OffsetAccountOverrideInEntryTypeDto.md) |  | [optional]
**offset_subaccount_override** | [**\OpenAPI\Client\Model\OffsetSubaccountOverrideInEntryTypeDto**](OffsetSubaccountOverrideInEntryTypeDto.md) |  | [optional]
**offset_account_branch** | [**\OpenAPI\Client\Model\OffsetAccountBranchInEntryTypeDto**](OffsetAccountBranchInEntryTypeDto.md) |  | [optional]
**vat_zone** | [**\OpenAPI\Client\Model\VatZoneInEntryTypeDto**](VatZoneInEntryTypeDto.md) |  | [optional]
**tax_calculation_mode** | **string** | Tax calculation mode &amp;gt; The tax calculation mode to be used by default with this entry type | [optional]
**last_modified_date_time** | **\DateTime** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

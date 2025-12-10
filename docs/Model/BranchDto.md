# # BranchDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**branch_id** | **int** | The top part &amp;gt; Branch ID* &amp;gt; The unique identifier of the Branch | [optional]
**number** | **string** | Mandatory field: The top part &amp;gt; Branch CD* &amp;gt; The branch number , which you compose according to the rules defined by the BIZACCT segmented key. | [optional]
**name** | **string** | The top part &amp;gt; Company name &amp;gt; The name of the company. | [optional]
**organization_id** | **int** |  | [optional]
**is_main_branch** | **bool** | The top part &amp;gt; Is main organisation &amp;gt; If you want this company to be the main company of your branches, select this check box. | [optional]
**is_active** | **bool** | The top part &amp;gt; Is active branch. | [optional]
**last_modified_date_time** | **\DateTime** | System generated information. This information is not visible in the window. | [optional]
**corporate_id** | **string** | The Organisation details tab &amp;gt; VAT registration info section &amp;gt; Corporate ID &amp;gt; The corporate ID of the company. | [optional]
**vat_registration_id** | **string** | The Organisation details tab &amp;gt; VAT registration info section &amp;gt; VAT registration ID &amp;gt; The company registration ID for the country’s tax authority. | [optional]
**main_address** | [**\OpenAPI\Client\Model\MainAddressInBranchDto**](MainAddressInBranchDto.md) |  | [optional]
**main_contact** | [**\OpenAPI\Client\Model\MainContactInBranchDto**](MainContactInBranchDto.md) |  | [optional]
**delivery_address** | [**\OpenAPI\Client\Model\DeliveryAddressInBranchDto**](DeliveryAddressInBranchDto.md) |  | [optional]
**delivery_contact** | [**\OpenAPI\Client\Model\DeliveryContactInBranchDto**](DeliveryContactInBranchDto.md) |  | [optional]
**default_country** | [**\OpenAPI\Client\Model\DefaultCountryInBranchDto**](DefaultCountryInBranchDto.md) |  | [optional]
**industry_code** | [**\OpenAPI\Client\Model\IndustryCodeInBranchDto**](IndustryCodeInBranchDto.md) |  | [optional]
**currency** | [**\OpenAPI\Client\Model\CurrencyInBranchDto**](CurrencyInBranchDto.md) |  | [optional]
**vat_zone** | [**\OpenAPI\Client\Model\VatZoneInBranchDto**](VatZoneInBranchDto.md) |  | [optional]
**ledger** | [**\OpenAPI\Client\Model\LedgerInBranchDto**](LedgerInBranchDto.md) |  | [optional]
**bank_settings** | [**\OpenAPI\Client\Model\BankSettingsInBranchDto**](BankSettingsInBranchDto.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

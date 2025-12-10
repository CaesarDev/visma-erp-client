# # ContactDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**display_name** | **string** |  | [optional]
**active** | **bool** | The top part &amp;gt; Active &amp;gt; A check box that indicates (if selected) that the contact is active. | [optional]
**title** | **string** | The top part &amp;gt; First name &amp;gt; The contact&#39;s courtesy title. | [optional]
**first_name** | **string** | The top part &amp;gt; First name &amp;gt; The first name of the contact. | [optional]
**last_name** | **string** | Mandatory field: The top part &amp;gt; Last name* &amp;gt; The last name of the contact. | [optional]
**position** | **string** | The top part &amp;gt; Job title &amp;gt; The contact’s job title or position. | [optional]
**business_account** | **string** | The top part &amp;gt; Business account &amp;gt; The business account associated with the contact. | [optional]
**business_account_type** | **string** | The top part &amp;gt; Business account &amp;gt; The business account type of the business account associated with the contact. | [optional]
**same_as_account** | **bool** | The Details tab &amp;gt; Same as in account &amp;gt; A check box that indicates (if selected) that the contact&#39;s address is the same as the address of the business account. | [optional]
**address** | [**\OpenAPI\Client\Model\AddressInContactDto**](AddressInContactDto.md) |  | [optional]
**email** | **string** | The Details tab &amp;gt; Contact section &amp;gt; Email &amp;gt; The email address of the contact. | [optional]
**web** | **string** | The Details tab &amp;gt; Contact section &amp;gt; Web &amp;gt; The website of the contact, if any. | [optional]
**phone1** | **string** | The Details tab &amp;gt; Contact section &amp;gt; Business 1/Business 2/Business 3/Business assistant 1/Business fax /Home/Home fax/Mobile &amp;gt; The primary phone number of the contact. Select the type from the drop down. | [optional]
**phone2** | **string** | The Details tab &amp;gt; Contact section &amp;gt; Business 1/Business 2/Business 3/Business assistant 1/Business fax /Home/Home fax/Mobile &amp;gt; The primary phone number of the contact. Select the type from the drop down. | [optional]
**phone3** | **string** | The Details tab &amp;gt; Contact section &amp;gt; Business 1/Business 2/Business 3/Business assistant 1/Business fax /Home/Home fax/Mobile &amp;gt; The primary phone number of the contact. Select the type from the drop down. | [optional]
**fax** | **string** | The Details tab &amp;gt; Contact section &amp;gt; Business fax &amp;gt; The fax number of the contact. | [optional]
**contact_method** | **string** | CRM section not available in Visma.net ERP | [optional]
**do_not_call** | **bool** | CRM section not available in Visma.net ERP | [optional]
**do_not_fax** | **bool** | CRM section not available in Visma.net ERP | [optional]
**do_not_email** | **bool** | CRM section not available in Visma.net ERP | [optional]
**do_not_mail** | **bool** | CRM section not available in Visma.net ERP | [optional]
**no_mass_mail** | **bool** | CRM section not available in Visma.net ERP | [optional]
**no_marketing** | **bool** | CRM section not available in Visma.net ERP | [optional]
**last_modified_date_time** | **\DateTime** | Background information: The date and time when the details of the contact were last updated. | [optional]
**contact_id** | **int** | The top part &amp;gt; Contact ID &amp;gt; The unique identifier of the contact, which the system generates automatically. | [optional]
**time_stamp** | **string** | Identifier that represents a specific version of the resource.  It helps to prevent simultaneous updates of the resource from overwriting each other (by using ETags and If-Match headers) | [optional]
**error_info** | **string** |  | [optional]
**metadata** | [**\OpenAPI\Client\Model\MetadataDto**](MetadataDto.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

# # NumberingSequenceDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**numbering_id** | **string** | Mandatory field: The top part &amp;gt; Numbering ID &amp;gt; The unique ID of the numbering series, which is an alphanumeric string of up to 10 characters. | [optional]
**branch** | [**\OpenAPI\Client\Model\BranchInNumberingSequenceDto**](BranchInNumberingSequenceDto.md) |  | [optional]
**start_nbr** | **string** | Mandatory field: The table &amp;gt; Start number* &amp;gt; The number to be used first in this numbering series or subsequence. | [optional]
**end_nbr** | **string** | Mandatory field: The table &amp;gt; End number* &amp;gt; The number to be used at the end of this series. The end number cannot be less than the Start number. | [optional]
**start_date** | **\DateTime** | Mandatory field: The table &amp;gt; Start dat*e &amp;gt; The date when this series will first be used. | [optional]
**last_nbr** | **string** | Mandatory field: The table &amp;gt; Last number* &amp;gt; The most recent allocated number used for an object in this series. | [optional]
**warn_nbr** | **string** | Mandatory field: The table &amp;gt; Warning number* &amp;gt; The minimum number that triggers a warning that available numbers will be used up soon. | [optional]
**nbr_step** | **int** | Mandatory field: The table &amp;gt; Numbering step* &amp;gt; The increment this series uses to generate the next number. | [optional]
**next_number** | **string** | Next number that will be assigned | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

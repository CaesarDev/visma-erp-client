# # LotSerialClassDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The Id of the Lot Serial Class | [optional]
**description** | **string** | The description of the Lot Serial Class | [optional]
**tracking_method** | **string** | Method used to track the Lot Serial Class | [optional]
**track_expiration_date** | **bool** | Option for enable/disable expiration date tracking of the Lot Serial Class | [optional]
**required_for_drop_ship** | **bool** | Option for enable/disable require drop shipping of the Lot Serial Class | [optional]
**assignment_method** | **string** | Assignment method used for the Lot Serial Class (When Used, When Received) | [optional]
**issue_method** | **string** | Issue method used for the Lot Serial Class (FIFO, LIFO, Sequential, Expiration, User-Enterable) | [optional]
**auto_incremental_value_between_classes** | **bool** | Option for enable/disable auto incremental values between classes for the Lot Serial Class | [optional]
**auto_incremental_value** | **string** | Value used for the auto incremental value when AutoIncrementalValueBetweenClasses is enabled | [optional]
**auto_generate_next_number** | **bool** | Option for enable/disable auto generating the next number for the Lot Serial Class | [optional]
**last_modified_date_time** | **\DateTime** | System generated information. | [optional]
**details** | [**\OpenAPI\Client\Model\LotSerialClassDetailDto[]**](LotSerialClassDetailDto.md) | Lot Serial Class details (Segment Number, Type, Value) | [optional]
**error_info** | **string** |  | [optional]
**metadata** | [**\OpenAPI\Client\Model\MetadataDto**](MetadataDto.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

# OpenChannelMetadataEntry

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**key** | **string** |  | [optional]
**value** | **string** |  | [optional]
**metadata_owner_id** | **string** | KV entry owner; serializes as &#x60;metadataOwnerId&#x60; from the source map key &#x60;userId&#x60; (&#x60;OpenChannelMetadataListResult.MetadataItem&#x60;). | [optional]
**should_auto_delete** | **int** | Parsed from source &#x60;autoDelete&#x60; string. &#x60;1&#x60; enables auto-delete and &#x60;0&#x60; disables it. | [optional]
**updated_at** | **int** | Parsed from source &#x60;lastSetTime&#x60; (milliseconds). | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

# OpenChannelMetadataBatchSetRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channel_id** | **string** |  |
**metadata_owner_id** | **string** | Legacy &#x60;entryOwnerId&#x60;. |
**metadata** | **array<string,string>** | Legacy &#x60;entryInfo&#x60;. Up to 20 metadata entries per request. |
**should_auto_delete** | **int** | &#x60;0&#x60; keeps metadata after the owner leaves and &#x60;1&#x60; removes it automatically. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

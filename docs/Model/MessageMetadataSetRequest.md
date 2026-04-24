# MessageMetadataSetRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message_id** | **string** |  |
**user_id** | **string** |  |
**channel_type** | **int** | Supports &#x60;1&#x60; and &#x60;3&#x60;. |
**channel_id** | **string** |  |
**metadata** | **array<string,string>** | Message metadata to set. Keys support letters, digits, and &#x60;+ &#x3D; - _&#x60;, with a maximum key length of 32 characters. Each request can set up to 100 entries. |
**is_echo_to_sender** | **int** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

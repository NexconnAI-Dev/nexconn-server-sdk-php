# StreamMessageContent

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**content** | **string** | Stream data chunk. Total message size must not exceed 128 KB across all chunks. |
**seq** | **int** | Sequence number. Must be greater than 0, starting from 1, strictly incrementing and continuous. |
**complete** | **bool** | Whether this is the final chunk in the stream. &#x60;true&#x60; marks the end of the stream. |
**complete_reason** | **int** | Custom completion reason code. Only effective when &#x60;complete&#x60; is &#x60;true&#x60;. | [optional]
**type** | **string** | Stream content type. Supported on the first chunk only. Default: text. Supported values: text, markdown, html. | [optional]
**message_id** | **string** | Stream message unique ID. Not required for the first chunk. Required for subsequent chunks (use the value returned in the first chunk response). | [optional]
**user** | **array<string,mixed>** | Sender user information object. Supported on the first chunk only. | [optional]
**mentioned_info** | **array<string,mixed>** | @mention information. Supported on the first chunk only. | [optional]
**extra** | **array<string,mixed>** | Extension information. Supported on the first chunk only. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

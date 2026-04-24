# OpenChannelCreateRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channel_id** | **string** | Legacy &#x60;chatroomId&#x60;. |
**destroy_type** | **int** | &#39;0&#39; for inactive-time destroy and &#39;1&#39; for fixed-time destroy. | [optional]
**ttl_minutes** | **int** | Legacy &#x60;destroyTime&#x60;. Valid range is 60 to 10080 minutes according to the PDF. | [optional]
**should_freeze** | **bool** | Whether whole-channel freeze is enabled when the chatroom is created. | [optional]
**allowed_senders_list** | **string[]** | Allowed senders list applied when the chatroom is frozen. | [optional]
**metadata_owner_id** | **string** | Legacy &#x60;entryOwnerId&#x60;. | [optional]
**metadata** | **array<string,string>** | Legacy &#x60;entryInfo&#x60;. Open-channel metadata key/value pairs. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

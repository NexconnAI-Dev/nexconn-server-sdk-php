# OpenChannelBroadcastRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**from_user_id** | **string** | Sender user ID. |
**message_type** | **string** | Message type. Supports built-in types and custom types registered in the client SDK. Custom types must not start with &#x60;RC:&#x60; and must not exceed 32 characters. |
**content** | **string** | Broadcast message payload serialized as a string. Maximum size is 128 KB. |
**is_echo_to_sender** | **int** | Whether to sync the broadcast message to the sender&#39;s client while the sender is online. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

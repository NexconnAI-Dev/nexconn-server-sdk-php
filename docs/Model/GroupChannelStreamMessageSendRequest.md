# GroupChannelStreamMessageSendRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**from_user_id** | **string** | Sender user ID. |
**to_channel_id** | **string** | Target group channel ID. |
**message_type** | **string** | Message type. Fixed value &#x60;RC:StreamMsg&#x60; for stream messages. |
**content** | [**\NexConnServerSdkPhp\Model\StreamMessageContent**](StreamMessageContent.md) |  |
**to_user_ids** | **string[]** | Recipient member user IDs for a targeted group message. Up to 10 users. | [optional]
**is_echo_to_sender** | **int** | Whether to sync the message to the sender&#39;s client while the sender is online. &#x60;1&#x60; enables sync and &#x60;0&#x60; disables it. | [optional]
**should_persist** | **int** | Whether to store the message in cloud message history. &#x60;0&#x60; means do not store and &#x60;1&#x60; means store. | [optional]
**has_mention** | **int** | Whether this is an @mention message. Set to &#x60;1&#x60; when &#x60;content&#x60; contains &#x60;mentionedInfo&#x60;. | [optional]
**metadata** | **array<string,string>** | Custom message metadata entries. Keys are limited to 32 characters and values to 4096 characters. Up to 100 key-value pairs. | [optional]
**disable_update_last_msg** | **bool** | Whether to keep this message from updating the channel&#39;s last-message preview. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

# GroupChannelMessageSendRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**from_user_id** | **string** | Sender user ID. Server-side sending does not require the sender to be a group member, but push display works best when the sender has an access token. |
**to_channel_ids** | **string[]** | Target group channel IDs. Up to 3 groups are supported per request. Targeted messages support only one group. |
**to_user_ids** | **string[]** | Recipient member user IDs for a targeted group message. Only effective when sending to a single group. | [optional]
**message_type** | **string** | Message type. Supports built-in types and custom types registered in the client SDK. Custom types must not start with &#x60;RC:&#x60; and must not exceed 32 characters. |
**content** | **string** | Message content payload serialized as a string. Built-in message types should use a JSON object string. Maximum size is 128 KB. |
**push_content** | **string** | Push notification text for offline recipients. Optional for built-in user content messages and required for push-enabled custom or notification messages. | [optional]
**push_data** | **string** | Custom push payload data. Exposed as &#x60;appData&#x60; on mobile push payloads. | [optional]
**is_echo_to_sender** | **int** | Whether to sync the sent message to the sender&#39;s client while online. &#x60;1&#x60; enables sync and &#x60;0&#x60; disables it. | [optional]
**should_persist** | **int** | Whether to store the message in cloud message history. &#x60;0&#x60; means do not store and &#x60;1&#x60; means store. | [optional]
**has_mention** | **int** | Whether this is an @mention message. Set to &#x60;1&#x60; when &#x60;content&#x60; contains &#x60;mentionedInfo&#x60;. | [optional]
**content_available** | **int** | iOS silent-push flag. &#x60;1&#x60; enables background delivery and &#x60;0&#x60; disables it. | [optional]
**has_metadata** | **bool** | Whether to enable message metadata for this message. Only effective when sending to a single group channel. | [optional]
**metadata** | **array<string,mixed>** | Custom message metadata entries. Only effective when &#x60;hasMetadata&#x60; is &#x60;true&#x60; and the request targets a single group. | [optional]
**disable_push** | **bool** | Whether to suppress push notifications. Only effective when the request targets a single group channel. | [optional]
**push_ext** | **string** | Extended push configuration (JSON string as accepted by &#x60;GroupChannelMsgSendInput&#x60;). | [optional]
**disable_update_last_msg** | **bool** | Whether to keep this message from updating the channel&#39;s last-message preview. | [optional]
**need_read_receipt** | **int** | Whether to request read receipts for this persisted message. &#x60;1&#x60; requests read receipts and &#x60;0&#x60; disables them. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

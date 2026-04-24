# SystemChannelMessageSendRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**from_user_id** | **string** | Sender user ID. The sender should have an access token. |
**to_user_ids** | **string[]** | Recipient user IDs. Up to 100 users are supported in a single request. |
**message_type** | **string** | Message type. Supports built-in types and custom types. Custom types must not start with &#x60;RC:&#x60; and must not exceed 32 characters. |
**content** | **string** | Message content payload serialized as a string. Built-in message types should use a JSON object string. Maximum size is 128 KB. |
**push_content** | **string** | Push notification text for offline recipients. Required for custom or notification messages that need push delivery. | [optional]
**push_data** | **string** | Custom push payload data. Exposed as &#x60;appData&#x60; on iOS and Android. | [optional]
**should_persist** | **int** | Whether to store the message in cloud message history. &#x60;0&#x60; means do not store and &#x60;1&#x60; means store. | [optional]
**content_available** | **int** | iOS silent-push flag. &#x60;1&#x60; enables background delivery and &#x60;0&#x60; disables it. | [optional]
**disable_push** | **bool** | Whether to suppress push notifications for offline recipients. | [optional]
**push_ext** | **string** | Extended push configuration (JSON string as accepted by &#x60;SystemChannelMsgSendInput&#x60;). | [optional]
**disable_update_last_msg** | **bool** | Whether to keep this message from updating the system channel&#39;s last-message preview. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

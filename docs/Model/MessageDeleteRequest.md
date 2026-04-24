# MessageDeleteRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**from_user_id** | **string** | Sender user ID of the original message that is being deleted. |
**channel_type** | **int** | Channel type of the original message. Supports &#x60;1&#x60; direct, &#x60;3&#x60; group, &#x60;4&#x60; open channel, &#x60;6&#x60; system, and &#x60;10&#x60; community. |
**channel_id** | **string** | Target identifier of the original message. Depending on &#x60;channelType&#x60;, this can be a user ID, group ID, open channel ID, community channel ID, or system target ID. |
**subchannel_id** | **string** | Community subchannel ID. Required only when deleting a community-channel message that was sent to a specific subchannel. | [optional]
**message_id** | **string** | Unique message ID to delete. This corresponds to the message UID returned by send or routing services. |
**sent_at** | **int** | Send timestamp of the original message in milliseconds. Providing it helps the service locate the original message precisely. | [optional]
**is_admin** | **int** | Whether the deletion is performed as an admin operation. &#x60;1&#x60; shows an admin recall indicator and &#x60;0&#x60; performs a normal sender recall. | [optional]
**disable_push** | **bool** | Whether to suppress push notifications for the recall event. Not supported for open channels or community channels. | [optional]
**extra** | **string** | Custom extension data carried with the recall operation. Not supported for community channels. | [optional]
**disable_update_last_msg** | **bool** | Whether to keep the recall operation from updating the channel&#39;s last-message preview. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

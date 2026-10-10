# OpenChannelHistoryMessageRecord

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channel_id** | **string** | Channel identifier of the stored message. | [optional]
**from_user_id** | **string** | Sender user ID of the stored message. | [optional]
**message_id** | **string** | Unique message ID. | [optional]
**sent_at** | **int** | Message send timestamp in milliseconds. | [optional]
**message_type** | **string** | Message type of the stored message. | [optional]
**content** | **string** | Raw message content payload as stored by the service. | [optional]
**quote** | **string** | Quoted message details as a JSON string containing msgUID, objectName and fromUserId. Omitted for messages without a quote. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

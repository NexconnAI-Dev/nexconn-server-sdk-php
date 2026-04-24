# MessageRecord

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channel_id** | **string** | Channel identifier of the stored message. | [optional]
**subchannel_id** | **string** | Community subchannel ID associated with the stored message, when applicable. | [optional]
**from_user_id** | **string** | Sender user ID of the stored message. | [optional]
**message_id** | **string** | Unique message ID. | [optional]
**sent_at** | **int** | Message send timestamp in milliseconds. | [optional]
**message_type** | **string** | Message type of the stored message. | [optional]
**channel_type** | **int** | Channel type of the stored message. | [optional]
**content** | **string** | Raw message content payload as stored by the service. | [optional]
**has_metadata** | **bool** | Whether the message has metadata entries attached. | [optional]
**metadata** | [**\NexConnServerSdkPhp\Model\MessageMetadataListItem[]**](MessageMetadataListItem.md) | List of metadata entries (&#x60;CommunityHistoryMessage&#x60; uses &#x60;List&lt;MetadataItem&gt;&#x60;, not a map). | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

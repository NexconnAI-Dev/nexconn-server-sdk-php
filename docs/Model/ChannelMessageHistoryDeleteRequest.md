# ChannelMessageHistoryDeleteRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channel_type** | **int** | Channel type. Supports &#x60;1&#x60; direct, &#x60;3&#x60; group, &#x60;4&#x60; open channel, and &#x60;6&#x60; system (&#x60;HistoryCleanInput&#x60;). |
**from_user_id** | **string** | User whose server-side history is operated on. For open channels, this is the operator ID. |
**channel_id** | **string** | Target channel ID (&#x60;targetId&#x60; / conversation target). |
**sent_at** | **string** | Optional cutoff (&#x60;msgTimestamp&#x60;). Serialized as string in &#x60;HistoryCleanInput&#x60;. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

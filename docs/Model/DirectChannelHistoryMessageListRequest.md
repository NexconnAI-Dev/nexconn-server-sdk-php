# DirectChannelHistoryMessageListRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**user_id** | **string** | User ID of the direct-channel participant. |
**channel_id** | **string** | Direct channel ID. |
**start_at** | **int** | Query start timestamp in Unix milliseconds. Must be greater than or equal to &#x60;endAt&#x60;; the range cannot exceed 14 days. |
**end_at** | **int** | Query end timestamp in Unix milliseconds. Messages are returned in descending timestamp order. |
**page_size** | **int** | Number of messages to return. Must be between 1 and 100. | [optional] [default to 10]
**include_start** | **bool** | Whether to include the message at &#x60;startAt&#x60; when it matches the query boundary. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

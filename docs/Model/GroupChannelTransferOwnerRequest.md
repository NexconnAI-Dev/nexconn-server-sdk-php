# GroupChannelTransferOwnerRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channel_id** | **string** |  |
**new_owner** | **string** |  |
**should_leave** | **int** | &#x60;0&#x60; means keep the previous owner in the group and &#x60;1&#x60; means leave the group. | [optional]
**should_delete_mute** | **int** | &#x60;0&#x60; means keep the previous owner&#39;s mute state and &#x60;1&#x60; means remove it. | [optional]
**should_delete_allowed_senders_list** | **int** | &#x60;0&#x60; means keep the previous owner&#39;s allowed-senders-list state and &#x60;1&#x60; means remove it. | [optional]
**should_delete_favorites** | **int** | &#x60;0&#x60; means keep favorites and &#x60;1&#x60; means remove them. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

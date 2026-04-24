# GroupChannelJoinedItem

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channel_id** | **string** | Group channel ID. | [optional]
**name** | **string** | Group name. | [optional]
**group_profile** | **array<string,mixed>** | Group basic profile JSON object. | [optional]
**group_ext_profile** | **array<string,mixed>** | Group extended profile JSON object. | [optional]
**permissions** | **array<string,mixed>** | Group permission settings JSON object. | [optional]
**alias** | **string** | Group alias or remark name set by the querying user. | [optional]
**owner** | **string** | User ID of the current group owner. | [optional]
**member_count** | **int** | Number of members in the group. | [optional]
**joined_at** | **int** | Timestamp when the querying user joined the group. | [optional]
**role** | **int** | The querying user&#39;s role in the group. &#x60;1&#x60; regular member, &#x60;2&#x60; admin, &#x60;3&#x60; owner. | [optional]
**created_at** | **int** | Timestamp when the group was created. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

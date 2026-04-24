# GroupChannelProfileItem

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channel_id** | **string** | Group channel ID. | [optional]
**name** | **string** | Group name. | [optional]
**group_profile** | **array<string,mixed>** | Group basic profile JSON object, such as introduction, announcement, and portrait URL. | [optional]
**group_ext_profile** | **array<string,mixed>** | Extended group profile JSON object. Keys are typically custom fields prefixed with &#x60;ext_&#x60;. | [optional]
**permissions** | **array<string,mixed>** | Group permission settings JSON object, including join, invite, and profile-management permissions. | [optional]
**owner** | **string** | User ID of the current group owner. | [optional]
**created_at** | **int** | Timestamp when the group was created. | [optional]
**member_count** | **int** | Current number of group members. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

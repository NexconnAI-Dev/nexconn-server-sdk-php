# GroupChannelCreateRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channel_id** | **string** | Legacy &#x60;groupId&#x60;. |
**name** | **string** |  |
**owner** | **string** | Group owner user ID. |
**user_ids** | **string[]** | Invited user IDs. The PDF limits this array to 30 users per request. | [optional]
**group_profile** | **array<string,mixed>** | Group basic profile object. Common keys include &#x60;introduction&#x60;, &#x60;announcement&#x60;, and &#x60;portraitUrl&#x60;. | [optional]
**permissions** | **array<string,mixed>** | Group permission object defined by the source API. | [optional]
**group_ext_profile** | **array<string,mixed>** | Group extra profile object. Keys must start with &#x60;ext_&#x60; according to the PDF. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

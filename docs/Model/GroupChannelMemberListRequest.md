# GroupChannelMemberListRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channel_id** | **string** | Group channel ID. |
**member_role** | **int** | Member role filter. &#x60;0&#x60; all members, &#x60;1&#x60; regular members, &#x60;2&#x60; admins, &#x60;3&#x60; owner. | [optional]
**page_token** | **string** | Pagination token returned by the previous request. Omit it for the first page. | [optional]
**page_size** | **int** | Number of members to return per page. The official default is 50 and the maximum is 100. | [optional]
**order** | **int** | Sort order by join time. &#x60;0&#x60; ascending and &#x60;1&#x60; descending. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

# GroupChannelJoinedListRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**user_id** | **string** | User ID whose joined groups should be listed. |
**role** | **int** | Role filter. &#x60;0&#x60; all roles, &#x60;1&#x60; regular member, &#x60;2&#x60; admin, &#x60;3&#x60; owner. | [optional]
**page_token** | **string** | Pagination token returned by the previous request. Omit it for the first page. | [optional]
**page_size** | **int** | Number of groups to return per page. The official default is 50 and the maximum is 100. | [optional]
**order** | **int** | Sort order by join time. &#x60;0&#x60; ascending and &#x60;1&#x60; descending. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

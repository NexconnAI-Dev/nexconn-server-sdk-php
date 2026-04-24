# ChannelPushSetRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channel_type** | **string** | Session / channel type as a string (&#x60;1&#x60; to &#x60;10&#x60; as accepted by the server). Matches &#x60;ChannelTypeRequestInput&#x60; in the service. |
**request_id** | **string** | User ID whose channel notification setting is updated. |
**channel_id** | **string** | Legacy &#x60;targetId&#x60;. |
**subchannel_id** | **string** | Legacy &#x60;busChannel&#x60;. Used for community-channel subchannel level settings. | [optional]
**no_disturb_level** | **int** | Do-not-disturb level (required by service validation; range &#x60;-1&#x60; to &#x60;5&#x60;). |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

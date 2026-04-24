# NexConnServerSdkPhp\CommunityChannelManagementApi

All requests use the primary/backup domains configured by the caller.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**addCommunityChannelUserGroupUsers()**](CommunityChannelManagementApi.md#addCommunityChannelUserGroupUsers) | **POST** /v4/community-channel/user-group/user/add | Add community channel user group users |
| [**addCommunityChannelUserGroups()**](CommunityChannelManagementApi.md#addCommunityChannelUserGroups) | **POST** /v4/community-channel/user-group/add | Add community channel user groups |
| [**addPrivateSubchannelMembers()**](CommunityChannelManagementApi.md#addPrivateSubchannelMembers) | **POST** /v4/community-channel/private-subchannel/member/add | Add private subchannel members |
| [**bindCommunityChannelUserGroup()**](CommunityChannelManagementApi.md#bindCommunityChannelUserGroup) | **POST** /v4/community-channel/channel/user-group/bind | Bind community channel user group |
| [**checkCommunityChannelMemberExist()**](CommunityChannelManagementApi.md#checkCommunityChannelMemberExist) | **POST** /v4/community-channel/member/exist | Check community channel member exist |
| [**createCommunityChannel()**](CommunityChannelManagementApi.md#createCommunityChannel) | **POST** /v4/community-channel/create | Create community channel |
| [**createCommunitySubchannel()**](CommunityChannelManagementApi.md#createCommunitySubchannel) | **POST** /v4/community-channel/subchannel/create | Create community subchannel |
| [**deleteCommunitySubchannel()**](CommunityChannelManagementApi.md#deleteCommunitySubchannel) | **POST** /v4/community-channel/subchannel/delete | Delete community subchannel |
| [**dismissCommunityChannel()**](CommunityChannelManagementApi.md#dismissCommunityChannel) | **POST** /v4/community-channel/dismiss | Dismiss community channel |
| [**joinCommunityChannel()**](CommunityChannelManagementApi.md#joinCommunityChannel) | **POST** /v4/community-channel/join | Join community channel |
| [**listCommunityChannelHistoryMessages()**](CommunityChannelManagementApi.md#listCommunityChannelHistoryMessages) | **POST** /v4/community-channel/history-message/list | List community-channel history messages |
| [**listCommunityChannelSubchannelUserGroups()**](CommunityChannelManagementApi.md#listCommunityChannelSubchannelUserGroups) | **POST** /v4/community-channel/channel/user-group/list | List community channel subchannel user groups |
| [**listCommunityChannelUserGroupSubchannels()**](CommunityChannelManagementApi.md#listCommunityChannelUserGroupSubchannels) | **POST** /v4/community-channel/user-group/subchannel/list | List community channel user group subchannels |
| [**listCommunityChannelUserGroups()**](CommunityChannelManagementApi.md#listCommunityChannelUserGroups) | **POST** /v4/community-channel/user-group/list | List community channel user groups |
| [**listCommunityChannelUserUserGroups()**](CommunityChannelManagementApi.md#listCommunityChannelUserUserGroups) | **POST** /v4/community-channel/user/user-group/list | List community channel user user groups |
| [**listCommunitySubchannels()**](CommunityChannelManagementApi.md#listCommunitySubchannels) | **POST** /v4/community-channel/subchannel/list | List community subchannels |
| [**listCommunityUserSubchannels()**](CommunityChannelManagementApi.md#listCommunityUserSubchannels) | **POST** /v4/community-channel/user/subchannel/list | List community user subchannels |
| [**listPrivateSubchannelMembers()**](CommunityChannelManagementApi.md#listPrivateSubchannelMembers) | **POST** /v4/community-channel/private-subchannel/member/list | List private subchannel members |
| [**quitCommunityChannel()**](CommunityChannelManagementApi.md#quitCommunityChannel) | **POST** /v4/community-channel/leave | Leave community channel |
| [**removeCommunityChannelUserGroupUsers()**](CommunityChannelManagementApi.md#removeCommunityChannelUserGroupUsers) | **POST** /v4/community-channel/user-group/user/remove | Remove community channel user group users |
| [**removeCommunityChannelUserGroups()**](CommunityChannelManagementApi.md#removeCommunityChannelUserGroups) | **POST** /v4/community-channel/user-group/remove | Delete community channel user groups |
| [**removePrivateSubchannelMembers()**](CommunityChannelManagementApi.md#removePrivateSubchannelMembers) | **POST** /v4/community-channel/private-subchannel/member/remove | Remove private subchannel members |
| [**unbindCommunityChannelUserGroup()**](CommunityChannelManagementApi.md#unbindCommunityChannelUserGroup) | **POST** /v4/community-channel/channel/user-group/unbind | Unbind community channel user group |
| [**updateCommunityChannelInfo()**](CommunityChannelManagementApi.md#updateCommunityChannelInfo) | **POST** /v4/community-channel/update | Update community channel info |
| [**updateCommunitySubchannelType()**](CommunityChannelManagementApi.md#updateCommunitySubchannelType) | **POST** /v4/community-channel/subchannel-type/update | Update community subchannel type |


## `addCommunityChannelUserGroupUsers()`

```php
addCommunityChannelUserGroupUsers($community_channel_user_group_users_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Add community channel user group users

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\CommunityChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$community_channel_user_group_users_request = new \NexConnServerSdkPhp\Model\CommunityChannelUserGroupUsersRequest(); // \NexConnServerSdkPhp\Model\CommunityChannelUserGroupUsersRequest

try {
    $result = $apiInstance->addCommunityChannelUserGroupUsers($community_channel_user_group_users_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CommunityChannelManagementApi->addCommunityChannelUserGroupUsers: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **community_channel_user_group_users_request** | [**\NexConnServerSdkPhp\Model\CommunityChannelUserGroupUsersRequest**](../Model/CommunityChannelUserGroupUsersRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\CodeOnlyResponse**](../Model/CodeOnlyResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `addCommunityChannelUserGroups()`

```php
addCommunityChannelUserGroups($community_channel_user_group_add_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Add community channel user groups

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\CommunityChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$community_channel_user_group_add_request = new \NexConnServerSdkPhp\Model\CommunityChannelUserGroupAddRequest(); // \NexConnServerSdkPhp\Model\CommunityChannelUserGroupAddRequest

try {
    $result = $apiInstance->addCommunityChannelUserGroups($community_channel_user_group_add_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CommunityChannelManagementApi->addCommunityChannelUserGroups: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **community_channel_user_group_add_request** | [**\NexConnServerSdkPhp\Model\CommunityChannelUserGroupAddRequest**](../Model/CommunityChannelUserGroupAddRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\CodeOnlyResponse**](../Model/CodeOnlyResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `addPrivateSubchannelMembers()`

```php
addPrivateSubchannelMembers($community_private_subchannel_members_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Add private subchannel members

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\CommunityChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$community_private_subchannel_members_request = new \NexConnServerSdkPhp\Model\CommunityPrivateSubchannelMembersRequest(); // \NexConnServerSdkPhp\Model\CommunityPrivateSubchannelMembersRequest

try {
    $result = $apiInstance->addPrivateSubchannelMembers($community_private_subchannel_members_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CommunityChannelManagementApi->addPrivateSubchannelMembers: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **community_private_subchannel_members_request** | [**\NexConnServerSdkPhp\Model\CommunityPrivateSubchannelMembersRequest**](../Model/CommunityPrivateSubchannelMembersRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\CodeOnlyResponse**](../Model/CodeOnlyResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `bindCommunityChannelUserGroup()`

```php
bindCommunityChannelUserGroup($community_channel_user_group_binding_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Bind community channel user group

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\CommunityChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$community_channel_user_group_binding_request = new \NexConnServerSdkPhp\Model\CommunityChannelUserGroupBindingRequest(); // \NexConnServerSdkPhp\Model\CommunityChannelUserGroupBindingRequest

try {
    $result = $apiInstance->bindCommunityChannelUserGroup($community_channel_user_group_binding_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CommunityChannelManagementApi->bindCommunityChannelUserGroup: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **community_channel_user_group_binding_request** | [**\NexConnServerSdkPhp\Model\CommunityChannelUserGroupBindingRequest**](../Model/CommunityChannelUserGroupBindingRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\CodeOnlyResponse**](../Model/CodeOnlyResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `checkCommunityChannelMemberExist()`

```php
checkCommunityChannelMemberExist($community_channel_member_request): \NexConnServerSdkPhp\Model\CommunityChannelMemberExistResponse
```

Check community channel member exist

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\CommunityChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$community_channel_member_request = new \NexConnServerSdkPhp\Model\CommunityChannelMemberRequest(); // \NexConnServerSdkPhp\Model\CommunityChannelMemberRequest

try {
    $result = $apiInstance->checkCommunityChannelMemberExist($community_channel_member_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CommunityChannelManagementApi->checkCommunityChannelMemberExist: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **community_channel_member_request** | [**\NexConnServerSdkPhp\Model\CommunityChannelMemberRequest**](../Model/CommunityChannelMemberRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\CommunityChannelMemberExistResponse**](../Model/CommunityChannelMemberExistResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createCommunityChannel()`

```php
createCommunityChannel($community_channel_create_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Create community channel

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\CommunityChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$community_channel_create_request = new \NexConnServerSdkPhp\Model\CommunityChannelCreateRequest(); // \NexConnServerSdkPhp\Model\CommunityChannelCreateRequest

try {
    $result = $apiInstance->createCommunityChannel($community_channel_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CommunityChannelManagementApi->createCommunityChannel: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **community_channel_create_request** | [**\NexConnServerSdkPhp\Model\CommunityChannelCreateRequest**](../Model/CommunityChannelCreateRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\CodeOnlyResponse**](../Model/CodeOnlyResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createCommunitySubchannel()`

```php
createCommunitySubchannel($community_subchannel_create_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Create community subchannel

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\CommunityChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$community_subchannel_create_request = new \NexConnServerSdkPhp\Model\CommunitySubchannelCreateRequest(); // \NexConnServerSdkPhp\Model\CommunitySubchannelCreateRequest

try {
    $result = $apiInstance->createCommunitySubchannel($community_subchannel_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CommunityChannelManagementApi->createCommunitySubchannel: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **community_subchannel_create_request** | [**\NexConnServerSdkPhp\Model\CommunitySubchannelCreateRequest**](../Model/CommunitySubchannelCreateRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\CodeOnlyResponse**](../Model/CodeOnlyResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteCommunitySubchannel()`

```php
deleteCommunitySubchannel($community_subchannel_key_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Delete community subchannel

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\CommunityChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$community_subchannel_key_request = new \NexConnServerSdkPhp\Model\CommunitySubchannelKeyRequest(); // \NexConnServerSdkPhp\Model\CommunitySubchannelKeyRequest

try {
    $result = $apiInstance->deleteCommunitySubchannel($community_subchannel_key_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CommunityChannelManagementApi->deleteCommunitySubchannel: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **community_subchannel_key_request** | [**\NexConnServerSdkPhp\Model\CommunitySubchannelKeyRequest**](../Model/CommunitySubchannelKeyRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\CodeOnlyResponse**](../Model/CodeOnlyResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `dismissCommunityChannel()`

```php
dismissCommunityChannel($community_channel_dismiss_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Dismiss community channel

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\CommunityChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$community_channel_dismiss_request = new \NexConnServerSdkPhp\Model\CommunityChannelDismissRequest(); // \NexConnServerSdkPhp\Model\CommunityChannelDismissRequest

try {
    $result = $apiInstance->dismissCommunityChannel($community_channel_dismiss_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CommunityChannelManagementApi->dismissCommunityChannel: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **community_channel_dismiss_request** | [**\NexConnServerSdkPhp\Model\CommunityChannelDismissRequest**](../Model/CommunityChannelDismissRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\CodeOnlyResponse**](../Model/CodeOnlyResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `joinCommunityChannel()`

```php
joinCommunityChannel($community_channel_member_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Join community channel

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\CommunityChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$community_channel_member_request = new \NexConnServerSdkPhp\Model\CommunityChannelMemberRequest(); // \NexConnServerSdkPhp\Model\CommunityChannelMemberRequest

try {
    $result = $apiInstance->joinCommunityChannel($community_channel_member_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CommunityChannelManagementApi->joinCommunityChannel: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **community_channel_member_request** | [**\NexConnServerSdkPhp\Model\CommunityChannelMemberRequest**](../Model/CommunityChannelMemberRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\CodeOnlyResponse**](../Model/CodeOnlyResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listCommunityChannelHistoryMessages()`

```php
listCommunityChannelHistoryMessages($community_channel_history_message_list_request): \NexConnServerSdkPhp\Model\MessageHistoryResponse
```

List community-channel history messages

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\CommunityChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$community_channel_history_message_list_request = new \NexConnServerSdkPhp\Model\CommunityChannelHistoryMessageListRequest(); // \NexConnServerSdkPhp\Model\CommunityChannelHistoryMessageListRequest

try {
    $result = $apiInstance->listCommunityChannelHistoryMessages($community_channel_history_message_list_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CommunityChannelManagementApi->listCommunityChannelHistoryMessages: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **community_channel_history_message_list_request** | [**\NexConnServerSdkPhp\Model\CommunityChannelHistoryMessageListRequest**](../Model/CommunityChannelHistoryMessageListRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\MessageHistoryResponse**](../Model/MessageHistoryResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listCommunityChannelSubchannelUserGroups()`

```php
listCommunityChannelSubchannelUserGroups($community_channel_subchannel_user_group_list_request): \NexConnServerSdkPhp\Model\CommunityChannelSubchannelUserGroupListResponse
```

List community channel subchannel user groups

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\CommunityChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$community_channel_subchannel_user_group_list_request = new \NexConnServerSdkPhp\Model\CommunityChannelSubchannelUserGroupListRequest(); // \NexConnServerSdkPhp\Model\CommunityChannelSubchannelUserGroupListRequest

try {
    $result = $apiInstance->listCommunityChannelSubchannelUserGroups($community_channel_subchannel_user_group_list_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CommunityChannelManagementApi->listCommunityChannelSubchannelUserGroups: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **community_channel_subchannel_user_group_list_request** | [**\NexConnServerSdkPhp\Model\CommunityChannelSubchannelUserGroupListRequest**](../Model/CommunityChannelSubchannelUserGroupListRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\CommunityChannelSubchannelUserGroupListResponse**](../Model/CommunityChannelSubchannelUserGroupListResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listCommunityChannelUserGroupSubchannels()`

```php
listCommunityChannelUserGroupSubchannels($community_channel_user_group_subchannel_list_request): \NexConnServerSdkPhp\Model\CommunityChannelUserGroupSubchannelListResponse
```

List community channel user group subchannels

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\CommunityChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$community_channel_user_group_subchannel_list_request = new \NexConnServerSdkPhp\Model\CommunityChannelUserGroupSubchannelListRequest(); // \NexConnServerSdkPhp\Model\CommunityChannelUserGroupSubchannelListRequest

try {
    $result = $apiInstance->listCommunityChannelUserGroupSubchannels($community_channel_user_group_subchannel_list_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CommunityChannelManagementApi->listCommunityChannelUserGroupSubchannels: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **community_channel_user_group_subchannel_list_request** | [**\NexConnServerSdkPhp\Model\CommunityChannelUserGroupSubchannelListRequest**](../Model/CommunityChannelUserGroupSubchannelListRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\CommunityChannelUserGroupSubchannelListResponse**](../Model/CommunityChannelUserGroupSubchannelListResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listCommunityChannelUserGroups()`

```php
listCommunityChannelUserGroups($community_channel_user_group_list_request): \NexConnServerSdkPhp\Model\CommunityChannelUserGroupListResponse
```

List community channel user groups

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\CommunityChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$community_channel_user_group_list_request = new \NexConnServerSdkPhp\Model\CommunityChannelUserGroupListRequest(); // \NexConnServerSdkPhp\Model\CommunityChannelUserGroupListRequest

try {
    $result = $apiInstance->listCommunityChannelUserGroups($community_channel_user_group_list_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CommunityChannelManagementApi->listCommunityChannelUserGroups: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **community_channel_user_group_list_request** | [**\NexConnServerSdkPhp\Model\CommunityChannelUserGroupListRequest**](../Model/CommunityChannelUserGroupListRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\CommunityChannelUserGroupListResponse**](../Model/CommunityChannelUserGroupListResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listCommunityChannelUserUserGroups()`

```php
listCommunityChannelUserUserGroups($community_channel_user_user_group_list_request): \NexConnServerSdkPhp\Model\CommunityChannelUserUserGroupListResponse
```

List community channel user user groups

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\CommunityChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$community_channel_user_user_group_list_request = new \NexConnServerSdkPhp\Model\CommunityChannelUserUserGroupListRequest(); // \NexConnServerSdkPhp\Model\CommunityChannelUserUserGroupListRequest

try {
    $result = $apiInstance->listCommunityChannelUserUserGroups($community_channel_user_user_group_list_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CommunityChannelManagementApi->listCommunityChannelUserUserGroups: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **community_channel_user_user_group_list_request** | [**\NexConnServerSdkPhp\Model\CommunityChannelUserUserGroupListRequest**](../Model/CommunityChannelUserUserGroupListRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\CommunityChannelUserUserGroupListResponse**](../Model/CommunityChannelUserUserGroupListResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listCommunitySubchannels()`

```php
listCommunitySubchannels($community_subchannel_list_request): \NexConnServerSdkPhp\Model\CommunitySubchannelListResponse
```

List community subchannels

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\CommunityChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$community_subchannel_list_request = new \NexConnServerSdkPhp\Model\CommunitySubchannelListRequest(); // \NexConnServerSdkPhp\Model\CommunitySubchannelListRequest

try {
    $result = $apiInstance->listCommunitySubchannels($community_subchannel_list_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CommunityChannelManagementApi->listCommunitySubchannels: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **community_subchannel_list_request** | [**\NexConnServerSdkPhp\Model\CommunitySubchannelListRequest**](../Model/CommunitySubchannelListRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\CommunitySubchannelListResponse**](../Model/CommunitySubchannelListResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listCommunityUserSubchannels()`

```php
listCommunityUserSubchannels($community_user_subchannel_list_request): \NexConnServerSdkPhp\Model\CommunityUserSubchannelListResponse
```

List community user subchannels

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\CommunityChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$community_user_subchannel_list_request = new \NexConnServerSdkPhp\Model\CommunityUserSubchannelListRequest(); // \NexConnServerSdkPhp\Model\CommunityUserSubchannelListRequest

try {
    $result = $apiInstance->listCommunityUserSubchannels($community_user_subchannel_list_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CommunityChannelManagementApi->listCommunityUserSubchannels: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **community_user_subchannel_list_request** | [**\NexConnServerSdkPhp\Model\CommunityUserSubchannelListRequest**](../Model/CommunityUserSubchannelListRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\CommunityUserSubchannelListResponse**](../Model/CommunityUserSubchannelListResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listPrivateSubchannelMembers()`

```php
listPrivateSubchannelMembers($community_private_subchannel_member_list_request): \NexConnServerSdkPhp\Model\CommunityPrivateSubchannelMemberListResponse
```

List private subchannel members

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\CommunityChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$community_private_subchannel_member_list_request = new \NexConnServerSdkPhp\Model\CommunityPrivateSubchannelMemberListRequest(); // \NexConnServerSdkPhp\Model\CommunityPrivateSubchannelMemberListRequest

try {
    $result = $apiInstance->listPrivateSubchannelMembers($community_private_subchannel_member_list_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CommunityChannelManagementApi->listPrivateSubchannelMembers: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **community_private_subchannel_member_list_request** | [**\NexConnServerSdkPhp\Model\CommunityPrivateSubchannelMemberListRequest**](../Model/CommunityPrivateSubchannelMemberListRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\CommunityPrivateSubchannelMemberListResponse**](../Model/CommunityPrivateSubchannelMemberListResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `quitCommunityChannel()`

```php
quitCommunityChannel($community_channel_member_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Leave community channel

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\CommunityChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$community_channel_member_request = new \NexConnServerSdkPhp\Model\CommunityChannelMemberRequest(); // \NexConnServerSdkPhp\Model\CommunityChannelMemberRequest

try {
    $result = $apiInstance->quitCommunityChannel($community_channel_member_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CommunityChannelManagementApi->quitCommunityChannel: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **community_channel_member_request** | [**\NexConnServerSdkPhp\Model\CommunityChannelMemberRequest**](../Model/CommunityChannelMemberRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\CodeOnlyResponse**](../Model/CodeOnlyResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `removeCommunityChannelUserGroupUsers()`

```php
removeCommunityChannelUserGroupUsers($community_channel_user_group_users_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Remove community channel user group users

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\CommunityChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$community_channel_user_group_users_request = new \NexConnServerSdkPhp\Model\CommunityChannelUserGroupUsersRequest(); // \NexConnServerSdkPhp\Model\CommunityChannelUserGroupUsersRequest

try {
    $result = $apiInstance->removeCommunityChannelUserGroupUsers($community_channel_user_group_users_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CommunityChannelManagementApi->removeCommunityChannelUserGroupUsers: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **community_channel_user_group_users_request** | [**\NexConnServerSdkPhp\Model\CommunityChannelUserGroupUsersRequest**](../Model/CommunityChannelUserGroupUsersRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\CodeOnlyResponse**](../Model/CodeOnlyResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `removeCommunityChannelUserGroups()`

```php
removeCommunityChannelUserGroups($community_channel_user_group_delete_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Delete community channel user groups

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\CommunityChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$community_channel_user_group_delete_request = new \NexConnServerSdkPhp\Model\CommunityChannelUserGroupDeleteRequest(); // \NexConnServerSdkPhp\Model\CommunityChannelUserGroupDeleteRequest

try {
    $result = $apiInstance->removeCommunityChannelUserGroups($community_channel_user_group_delete_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CommunityChannelManagementApi->removeCommunityChannelUserGroups: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **community_channel_user_group_delete_request** | [**\NexConnServerSdkPhp\Model\CommunityChannelUserGroupDeleteRequest**](../Model/CommunityChannelUserGroupDeleteRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\CodeOnlyResponse**](../Model/CodeOnlyResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `removePrivateSubchannelMembers()`

```php
removePrivateSubchannelMembers($community_private_subchannel_members_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Remove private subchannel members

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\CommunityChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$community_private_subchannel_members_request = new \NexConnServerSdkPhp\Model\CommunityPrivateSubchannelMembersRequest(); // \NexConnServerSdkPhp\Model\CommunityPrivateSubchannelMembersRequest

try {
    $result = $apiInstance->removePrivateSubchannelMembers($community_private_subchannel_members_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CommunityChannelManagementApi->removePrivateSubchannelMembers: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **community_private_subchannel_members_request** | [**\NexConnServerSdkPhp\Model\CommunityPrivateSubchannelMembersRequest**](../Model/CommunityPrivateSubchannelMembersRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\CodeOnlyResponse**](../Model/CodeOnlyResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `unbindCommunityChannelUserGroup()`

```php
unbindCommunityChannelUserGroup($community_channel_user_group_binding_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Unbind community channel user group

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\CommunityChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$community_channel_user_group_binding_request = new \NexConnServerSdkPhp\Model\CommunityChannelUserGroupBindingRequest(); // \NexConnServerSdkPhp\Model\CommunityChannelUserGroupBindingRequest

try {
    $result = $apiInstance->unbindCommunityChannelUserGroup($community_channel_user_group_binding_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CommunityChannelManagementApi->unbindCommunityChannelUserGroup: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **community_channel_user_group_binding_request** | [**\NexConnServerSdkPhp\Model\CommunityChannelUserGroupBindingRequest**](../Model/CommunityChannelUserGroupBindingRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\CodeOnlyResponse**](../Model/CodeOnlyResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateCommunityChannelInfo()`

```php
updateCommunityChannelInfo($community_channel_update_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Update community channel info

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\CommunityChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$community_channel_update_request = new \NexConnServerSdkPhp\Model\CommunityChannelUpdateRequest(); // \NexConnServerSdkPhp\Model\CommunityChannelUpdateRequest

try {
    $result = $apiInstance->updateCommunityChannelInfo($community_channel_update_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CommunityChannelManagementApi->updateCommunityChannelInfo: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **community_channel_update_request** | [**\NexConnServerSdkPhp\Model\CommunityChannelUpdateRequest**](../Model/CommunityChannelUpdateRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\CodeOnlyResponse**](../Model/CodeOnlyResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateCommunitySubchannelType()`

```php
updateCommunitySubchannelType($community_subchannel_type_update_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Update community subchannel type

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\CommunityChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$community_subchannel_type_update_request = new \NexConnServerSdkPhp\Model\CommunitySubchannelTypeUpdateRequest(); // \NexConnServerSdkPhp\Model\CommunitySubchannelTypeUpdateRequest

try {
    $result = $apiInstance->updateCommunitySubchannelType($community_subchannel_type_update_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CommunityChannelManagementApi->updateCommunitySubchannelType: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **community_subchannel_type_update_request** | [**\NexConnServerSdkPhp\Model\CommunitySubchannelTypeUpdateRequest**](../Model/CommunitySubchannelTypeUpdateRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\CodeOnlyResponse**](../Model/CodeOnlyResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

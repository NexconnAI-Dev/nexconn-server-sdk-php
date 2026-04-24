# NexConnServerSdkPhp\GroupChannelManagementApi

All requests use the primary/backup domains configured by the caller.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**addGroupChannelAdmins()**](GroupChannelManagementApi.md#addGroupChannelAdmins) | **POST** /v4/group-channel/admin/add | Add group admins |
| [**addGroupChannelMemberFavorites()**](GroupChannelManagementApi.md#addGroupChannelMemberFavorites) | **POST** /v4/group-channel/member/favorites/add | Add favorite group members |
| [**batchGetGroupChannelMembers()**](GroupChannelManagementApi.md#batchGetGroupChannelMembers) | **POST** /v4/group-channel/member/batch/get | Get specific group members |
| [**batchGetGroupChannelProfiles()**](GroupChannelManagementApi.md#batchGetGroupChannelProfiles) | **POST** /v4/group-channel/profile/list | List group profiles |
| [**createGroupChannel()**](GroupChannelManagementApi.md#createGroupChannel) | **POST** /v4/group-channel/create | Create a group |
| [**deleteGroupChannelAlias()**](GroupChannelManagementApi.md#deleteGroupChannelAlias) | **POST** /v4/group-channel/alias/delete | Delete group alias |
| [**dismissGroupChannel()**](GroupChannelManagementApi.md#dismissGroupChannel) | **POST** /v4/group-channel/dismiss | Dismiss a group |
| [**getGroupChannelAlias()**](GroupChannelManagementApi.md#getGroupChannelAlias) | **POST** /v4/group-channel/alias/get | Get group alias |
| [**joinGroupChannel()**](GroupChannelManagementApi.md#joinGroupChannel) | **POST** /v4/group-channel/join | Join a group |
| [**kickUserFromAllGroupChannels()**](GroupChannelManagementApi.md#kickUserFromAllGroupChannels) | **POST** /v4/group-channel/member/kickout-all | Remove a user from all groups |
| [**listGroupChannelMemberFavorites()**](GroupChannelManagementApi.md#listGroupChannelMemberFavorites) | **POST** /v4/group-channel/member/favorites/list | List favorite group members |
| [**listGroupChannelMembers()**](GroupChannelManagementApi.md#listGroupChannelMembers) | **POST** /v4/group-channel/member/list | Query group members |
| [**listGroupChannels()**](GroupChannelManagementApi.md#listGroupChannels) | **POST** /v4/group-channel/list | List group channels |
| [**listUserJoinedGroupChannels()**](GroupChannelManagementApi.md#listUserJoinedGroupChannels) | **POST** /v4/group-channel/joined/list | Query user&#39;s groups |
| [**quitGroupChannel()**](GroupChannelManagementApi.md#quitGroupChannel) | **POST** /v4/group-channel/leave | Leave a group |
| [**removeGroupChannelAdmins()**](GroupChannelManagementApi.md#removeGroupChannelAdmins) | **POST** /v4/group-channel/admin/remove | Remove group admins |
| [**removeGroupChannelMemberFavorites()**](GroupChannelManagementApi.md#removeGroupChannelMemberFavorites) | **POST** /v4/group-channel/member/favorites/remove | Remove favorite group members |
| [**setGroupChannelAlias()**](GroupChannelManagementApi.md#setGroupChannelAlias) | **POST** /v4/group-channel/alias/set | Set group alias |
| [**setGroupChannelMember()**](GroupChannelManagementApi.md#setGroupChannelMember) | **POST** /v4/group-channel/member/set | Set group member profile |
| [**transferGroupChannelOwner()**](GroupChannelManagementApi.md#transferGroupChannelOwner) | **POST** /v4/group-channel/transfer/owner | Transfer group ownership |
| [**updateGroupChannelProfile()**](GroupChannelManagementApi.md#updateGroupChannelProfile) | **POST** /v4/group-channel/profile/update | Update group info |


## `addGroupChannelAdmins()`

```php
addGroupChannelAdmins($group_channel_admin_users_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Add group admins

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\GroupChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$group_channel_admin_users_request = new \NexConnServerSdkPhp\Model\GroupChannelAdminUsersRequest(); // \NexConnServerSdkPhp\Model\GroupChannelAdminUsersRequest

try {
    $result = $apiInstance->addGroupChannelAdmins($group_channel_admin_users_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupChannelManagementApi->addGroupChannelAdmins: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group_channel_admin_users_request** | [**\NexConnServerSdkPhp\Model\GroupChannelAdminUsersRequest**](../Model/GroupChannelAdminUsersRequest.md)|  | |


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

## `addGroupChannelMemberFavorites()`

```php
addGroupChannelMemberFavorites($group_channel_member_favorites_update_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Add favorite group members

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\GroupChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$group_channel_member_favorites_update_request = new \NexConnServerSdkPhp\Model\GroupChannelMemberFavoritesUpdateRequest(); // \NexConnServerSdkPhp\Model\GroupChannelMemberFavoritesUpdateRequest

try {
    $result = $apiInstance->addGroupChannelMemberFavorites($group_channel_member_favorites_update_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupChannelManagementApi->addGroupChannelMemberFavorites: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group_channel_member_favorites_update_request** | [**\NexConnServerSdkPhp\Model\GroupChannelMemberFavoritesUpdateRequest**](../Model/GroupChannelMemberFavoritesUpdateRequest.md)|  | |


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

## `batchGetGroupChannelMembers()`

```php
batchGetGroupChannelMembers($group_channel_member_batch_get_request): \NexConnServerSdkPhp\Model\GroupChannelMemberBatchGetResponse
```

Get specific group members

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\GroupChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$group_channel_member_batch_get_request = new \NexConnServerSdkPhp\Model\GroupChannelMemberBatchGetRequest(); // \NexConnServerSdkPhp\Model\GroupChannelMemberBatchGetRequest

try {
    $result = $apiInstance->batchGetGroupChannelMembers($group_channel_member_batch_get_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupChannelManagementApi->batchGetGroupChannelMembers: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group_channel_member_batch_get_request** | [**\NexConnServerSdkPhp\Model\GroupChannelMemberBatchGetRequest**](../Model/GroupChannelMemberBatchGetRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\GroupChannelMemberBatchGetResponse**](../Model/GroupChannelMemberBatchGetResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `batchGetGroupChannelProfiles()`

```php
batchGetGroupChannelProfiles($group_channel_profile_list_request): \NexConnServerSdkPhp\Model\GroupChannelProfileListResponse
```

List group profiles

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\GroupChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$group_channel_profile_list_request = new \NexConnServerSdkPhp\Model\GroupChannelProfileListRequest(); // \NexConnServerSdkPhp\Model\GroupChannelProfileListRequest

try {
    $result = $apiInstance->batchGetGroupChannelProfiles($group_channel_profile_list_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupChannelManagementApi->batchGetGroupChannelProfiles: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group_channel_profile_list_request** | [**\NexConnServerSdkPhp\Model\GroupChannelProfileListRequest**](../Model/GroupChannelProfileListRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\GroupChannelProfileListResponse**](../Model/GroupChannelProfileListResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createGroupChannel()`

```php
createGroupChannel($group_channel_create_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Create a group

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\GroupChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$group_channel_create_request = new \NexConnServerSdkPhp\Model\GroupChannelCreateRequest(); // \NexConnServerSdkPhp\Model\GroupChannelCreateRequest

try {
    $result = $apiInstance->createGroupChannel($group_channel_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupChannelManagementApi->createGroupChannel: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group_channel_create_request** | [**\NexConnServerSdkPhp\Model\GroupChannelCreateRequest**](../Model/GroupChannelCreateRequest.md)|  | |


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

## `deleteGroupChannelAlias()`

```php
deleteGroupChannelAlias($group_channel_alias_get_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Delete group alias

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\GroupChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$group_channel_alias_get_request = new \NexConnServerSdkPhp\Model\GroupChannelAliasGetRequest(); // \NexConnServerSdkPhp\Model\GroupChannelAliasGetRequest

try {
    $result = $apiInstance->deleteGroupChannelAlias($group_channel_alias_get_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupChannelManagementApi->deleteGroupChannelAlias: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group_channel_alias_get_request** | [**\NexConnServerSdkPhp\Model\GroupChannelAliasGetRequest**](../Model/GroupChannelAliasGetRequest.md)|  | |


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

## `dismissGroupChannel()`

```php
dismissGroupChannel($group_channel_dismiss_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Dismiss a group

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\GroupChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$group_channel_dismiss_request = new \NexConnServerSdkPhp\Model\GroupChannelDismissRequest(); // \NexConnServerSdkPhp\Model\GroupChannelDismissRequest

try {
    $result = $apiInstance->dismissGroupChannel($group_channel_dismiss_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupChannelManagementApi->dismissGroupChannel: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group_channel_dismiss_request** | [**\NexConnServerSdkPhp\Model\GroupChannelDismissRequest**](../Model/GroupChannelDismissRequest.md)|  | |


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

## `getGroupChannelAlias()`

```php
getGroupChannelAlias($group_channel_alias_get_request): \NexConnServerSdkPhp\Model\GroupChannelAliasGetResponse
```

Get group alias

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\GroupChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$group_channel_alias_get_request = new \NexConnServerSdkPhp\Model\GroupChannelAliasGetRequest(); // \NexConnServerSdkPhp\Model\GroupChannelAliasGetRequest

try {
    $result = $apiInstance->getGroupChannelAlias($group_channel_alias_get_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupChannelManagementApi->getGroupChannelAlias: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group_channel_alias_get_request** | [**\NexConnServerSdkPhp\Model\GroupChannelAliasGetRequest**](../Model/GroupChannelAliasGetRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\GroupChannelAliasGetResponse**](../Model/GroupChannelAliasGetResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `joinGroupChannel()`

```php
joinGroupChannel($group_channel_join_request): \NexConnServerSdkPhp\Model\GroupChannelJoinResponse
```

Join a group

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\GroupChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$group_channel_join_request = new \NexConnServerSdkPhp\Model\GroupChannelJoinRequest(); // \NexConnServerSdkPhp\Model\GroupChannelJoinRequest

try {
    $result = $apiInstance->joinGroupChannel($group_channel_join_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupChannelManagementApi->joinGroupChannel: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group_channel_join_request** | [**\NexConnServerSdkPhp\Model\GroupChannelJoinRequest**](../Model/GroupChannelJoinRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\GroupChannelJoinResponse**](../Model/GroupChannelJoinResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `kickUserFromAllGroupChannels()`

```php
kickUserFromAllGroupChannels($group_channel_kick_user_from_all_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Remove a user from all groups

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\GroupChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$group_channel_kick_user_from_all_request = new \NexConnServerSdkPhp\Model\GroupChannelKickUserFromAllRequest(); // \NexConnServerSdkPhp\Model\GroupChannelKickUserFromAllRequest

try {
    $result = $apiInstance->kickUserFromAllGroupChannels($group_channel_kick_user_from_all_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupChannelManagementApi->kickUserFromAllGroupChannels: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group_channel_kick_user_from_all_request** | [**\NexConnServerSdkPhp\Model\GroupChannelKickUserFromAllRequest**](../Model/GroupChannelKickUserFromAllRequest.md)|  | |


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

## `listGroupChannelMemberFavorites()`

```php
listGroupChannelMemberFavorites($group_channel_member_favorites_list_request): \NexConnServerSdkPhp\Model\GroupChannelMemberFavoritesListResponse
```

List favorite group members

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\GroupChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$group_channel_member_favorites_list_request = new \NexConnServerSdkPhp\Model\GroupChannelMemberFavoritesListRequest(); // \NexConnServerSdkPhp\Model\GroupChannelMemberFavoritesListRequest

try {
    $result = $apiInstance->listGroupChannelMemberFavorites($group_channel_member_favorites_list_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupChannelManagementApi->listGroupChannelMemberFavorites: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group_channel_member_favorites_list_request** | [**\NexConnServerSdkPhp\Model\GroupChannelMemberFavoritesListRequest**](../Model/GroupChannelMemberFavoritesListRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\GroupChannelMemberFavoritesListResponse**](../Model/GroupChannelMemberFavoritesListResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listGroupChannelMembers()`

```php
listGroupChannelMembers($group_channel_member_list_request): \NexConnServerSdkPhp\Model\GroupChannelMemberListResponse
```

Query group members

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\GroupChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$group_channel_member_list_request = new \NexConnServerSdkPhp\Model\GroupChannelMemberListRequest(); // \NexConnServerSdkPhp\Model\GroupChannelMemberListRequest

try {
    $result = $apiInstance->listGroupChannelMembers($group_channel_member_list_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupChannelManagementApi->listGroupChannelMembers: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group_channel_member_list_request** | [**\NexConnServerSdkPhp\Model\GroupChannelMemberListRequest**](../Model/GroupChannelMemberListRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\GroupChannelMemberListResponse**](../Model/GroupChannelMemberListResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listGroupChannels()`

```php
listGroupChannels($group_channel_list_request): \NexConnServerSdkPhp\Model\GroupChannelListResponse
```

List group channels

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\GroupChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$group_channel_list_request = new \NexConnServerSdkPhp\Model\GroupChannelListRequest(); // \NexConnServerSdkPhp\Model\GroupChannelListRequest

try {
    $result = $apiInstance->listGroupChannels($group_channel_list_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupChannelManagementApi->listGroupChannels: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group_channel_list_request** | [**\NexConnServerSdkPhp\Model\GroupChannelListRequest**](../Model/GroupChannelListRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\GroupChannelListResponse**](../Model/GroupChannelListResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listUserJoinedGroupChannels()`

```php
listUserJoinedGroupChannels($group_channel_joined_list_request): \NexConnServerSdkPhp\Model\GroupChannelJoinedListResponse
```

Query user's groups

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\GroupChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$group_channel_joined_list_request = new \NexConnServerSdkPhp\Model\GroupChannelJoinedListRequest(); // \NexConnServerSdkPhp\Model\GroupChannelJoinedListRequest

try {
    $result = $apiInstance->listUserJoinedGroupChannels($group_channel_joined_list_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupChannelManagementApi->listUserJoinedGroupChannels: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group_channel_joined_list_request** | [**\NexConnServerSdkPhp\Model\GroupChannelJoinedListRequest**](../Model/GroupChannelJoinedListRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\GroupChannelJoinedListResponse**](../Model/GroupChannelJoinedListResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `quitGroupChannel()`

```php
quitGroupChannel($group_channel_quit_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Leave a group

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\GroupChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$group_channel_quit_request = new \NexConnServerSdkPhp\Model\GroupChannelQuitRequest(); // \NexConnServerSdkPhp\Model\GroupChannelQuitRequest

try {
    $result = $apiInstance->quitGroupChannel($group_channel_quit_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupChannelManagementApi->quitGroupChannel: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group_channel_quit_request** | [**\NexConnServerSdkPhp\Model\GroupChannelQuitRequest**](../Model/GroupChannelQuitRequest.md)|  | |


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

## `removeGroupChannelAdmins()`

```php
removeGroupChannelAdmins($group_channel_admin_users_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Remove group admins

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\GroupChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$group_channel_admin_users_request = new \NexConnServerSdkPhp\Model\GroupChannelAdminUsersRequest(); // \NexConnServerSdkPhp\Model\GroupChannelAdminUsersRequest

try {
    $result = $apiInstance->removeGroupChannelAdmins($group_channel_admin_users_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupChannelManagementApi->removeGroupChannelAdmins: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group_channel_admin_users_request** | [**\NexConnServerSdkPhp\Model\GroupChannelAdminUsersRequest**](../Model/GroupChannelAdminUsersRequest.md)|  | |


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

## `removeGroupChannelMemberFavorites()`

```php
removeGroupChannelMemberFavorites($group_channel_member_favorites_update_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Remove favorite group members

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\GroupChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$group_channel_member_favorites_update_request = new \NexConnServerSdkPhp\Model\GroupChannelMemberFavoritesUpdateRequest(); // \NexConnServerSdkPhp\Model\GroupChannelMemberFavoritesUpdateRequest

try {
    $result = $apiInstance->removeGroupChannelMemberFavorites($group_channel_member_favorites_update_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupChannelManagementApi->removeGroupChannelMemberFavorites: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group_channel_member_favorites_update_request** | [**\NexConnServerSdkPhp\Model\GroupChannelMemberFavoritesUpdateRequest**](../Model/GroupChannelMemberFavoritesUpdateRequest.md)|  | |


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

## `setGroupChannelAlias()`

```php
setGroupChannelAlias($group_channel_alias_set_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Set group alias

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\GroupChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$group_channel_alias_set_request = new \NexConnServerSdkPhp\Model\GroupChannelAliasSetRequest(); // \NexConnServerSdkPhp\Model\GroupChannelAliasSetRequest

try {
    $result = $apiInstance->setGroupChannelAlias($group_channel_alias_set_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupChannelManagementApi->setGroupChannelAlias: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group_channel_alias_set_request** | [**\NexConnServerSdkPhp\Model\GroupChannelAliasSetRequest**](../Model/GroupChannelAliasSetRequest.md)|  | |


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

## `setGroupChannelMember()`

```php
setGroupChannelMember($group_channel_member_set_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Set group member profile

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\GroupChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$group_channel_member_set_request = new \NexConnServerSdkPhp\Model\GroupChannelMemberSetRequest(); // \NexConnServerSdkPhp\Model\GroupChannelMemberSetRequest

try {
    $result = $apiInstance->setGroupChannelMember($group_channel_member_set_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupChannelManagementApi->setGroupChannelMember: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group_channel_member_set_request** | [**\NexConnServerSdkPhp\Model\GroupChannelMemberSetRequest**](../Model/GroupChannelMemberSetRequest.md)|  | |


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

## `transferGroupChannelOwner()`

```php
transferGroupChannelOwner($group_channel_transfer_owner_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Transfer group ownership

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\GroupChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$group_channel_transfer_owner_request = new \NexConnServerSdkPhp\Model\GroupChannelTransferOwnerRequest(); // \NexConnServerSdkPhp\Model\GroupChannelTransferOwnerRequest

try {
    $result = $apiInstance->transferGroupChannelOwner($group_channel_transfer_owner_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupChannelManagementApi->transferGroupChannelOwner: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group_channel_transfer_owner_request** | [**\NexConnServerSdkPhp\Model\GroupChannelTransferOwnerRequest**](../Model/GroupChannelTransferOwnerRequest.md)|  | |


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

## `updateGroupChannelProfile()`

```php
updateGroupChannelProfile($group_channel_profile_update_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Update group info

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\GroupChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$group_channel_profile_update_request = new \NexConnServerSdkPhp\Model\GroupChannelProfileUpdateRequest(); // \NexConnServerSdkPhp\Model\GroupChannelProfileUpdateRequest

try {
    $result = $apiInstance->updateGroupChannelProfile($group_channel_profile_update_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupChannelManagementApi->updateGroupChannelProfile: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group_channel_profile_update_request** | [**\NexConnServerSdkPhp\Model\GroupChannelProfileUpdateRequest**](../Model/GroupChannelProfileUpdateRequest.md)|  | |


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

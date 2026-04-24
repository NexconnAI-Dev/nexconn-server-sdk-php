# NexConnServerSdkPhp\UserManagementApi

All requests use the primary/backup domains configured by the caller.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**banUsers()**](UserManagementApi.md#banUsers) | **POST** /v4/user/ban | Ban a user |
| [**batchGetUserTags()**](UserManagementApi.md#batchGetUserTags) | **POST** /v4/user/tag/batch/get | Get user tags |
| [**batchSetUserTags()**](UserManagementApi.md#batchSetUserTags) | **POST** /v4/user/tag/batch/set | Batch set user tags |
| [**expireAccessToken()**](UserManagementApi.md#expireAccessToken) | **POST** /v4/auth/access-token/expire | Expire an access token |
| [**getUser()**](UserManagementApi.md#getUser) | **POST** /v4/user/get | Get user info |
| [**getUserConnectionStatus()**](UserManagementApi.md#getUserConnectionStatus) | **POST** /v4/user/connection-status/get | Check user online status |
| [**issueAccessToken()**](UserManagementApi.md#issueAccessToken) | **POST** /v4/auth/access-token/issue | Register a user |
| [**listBannedUsers()**](UserManagementApi.md#listBannedUsers) | **POST** /v4/user/ban/list | List banned users |
| [**listChannelTypeMute()**](UserManagementApi.md#listChannelTypeMute) | **POST** /v4/channel-type/mute/list | List muted direct channel users |
| [**listSoftDeletedUsers()**](UserManagementApi.md#listSoftDeletedUsers) | **POST** /v4/user/soft-deleted/list | Query soft-deleted users |
| [**restoreUsers()**](UserManagementApi.md#restoreUsers) | **POST** /v4/user/restore | Restore a user |
| [**setChannelTypeMute()**](UserManagementApi.md#setChannelTypeMute) | **POST** /v4/channel-type/mute/set | Mute a user in direct channels |
| [**softDeleteUsers()**](UserManagementApi.md#softDeleteUsers) | **POST** /v4/user/soft-delete | Soft-delete a user |
| [**unbanUsers()**](UserManagementApi.md#unbanUsers) | **POST** /v4/user/unban | Unban a user |
| [**updateUser()**](UserManagementApi.md#updateUser) | **POST** /v4/user/update | Update user info |


## `banUsers()`

```php
banUsers($user_ban_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Ban a user

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\UserManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$user_ban_request = new \NexConnServerSdkPhp\Model\UserBanRequest(); // \NexConnServerSdkPhp\Model\UserBanRequest

try {
    $result = $apiInstance->banUsers($user_ban_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserManagementApi->banUsers: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **user_ban_request** | [**\NexConnServerSdkPhp\Model\UserBanRequest**](../Model/UserBanRequest.md)|  | |


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

## `batchGetUserTags()`

```php
batchGetUserTags($user_tag_batch_get_request): \NexConnServerSdkPhp\Model\UserTagBatchGetResponse
```

Get user tags

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\UserManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$user_tag_batch_get_request = new \NexConnServerSdkPhp\Model\UserTagBatchGetRequest(); // \NexConnServerSdkPhp\Model\UserTagBatchGetRequest

try {
    $result = $apiInstance->batchGetUserTags($user_tag_batch_get_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserManagementApi->batchGetUserTags: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **user_tag_batch_get_request** | [**\NexConnServerSdkPhp\Model\UserTagBatchGetRequest**](../Model/UserTagBatchGetRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\UserTagBatchGetResponse**](../Model/UserTagBatchGetResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `batchSetUserTags()`

```php
batchSetUserTags($user_tag_batch_set_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Batch set user tags

Rate limit: 10/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\UserManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$user_tag_batch_set_request = new \NexConnServerSdkPhp\Model\UserTagBatchSetRequest(); // \NexConnServerSdkPhp\Model\UserTagBatchSetRequest

try {
    $result = $apiInstance->batchSetUserTags($user_tag_batch_set_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserManagementApi->batchSetUserTags: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **user_tag_batch_set_request** | [**\NexConnServerSdkPhp\Model\UserTagBatchSetRequest**](../Model/UserTagBatchSetRequest.md)|  | |


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

## `expireAccessToken()`

```php
expireAccessToken($access_token_expire_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Expire an access token

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\UserManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$access_token_expire_request = new \NexConnServerSdkPhp\Model\AccessTokenExpireRequest(); // \NexConnServerSdkPhp\Model\AccessTokenExpireRequest

try {
    $result = $apiInstance->expireAccessToken($access_token_expire_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserManagementApi->expireAccessToken: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **access_token_expire_request** | [**\NexConnServerSdkPhp\Model\AccessTokenExpireRequest**](../Model/AccessTokenExpireRequest.md)|  | |


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

## `getUser()`

```php
getUser($user_get_request): \NexConnServerSdkPhp\Model\UserGetResponse
```

Get user info

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\UserManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$user_get_request = new \NexConnServerSdkPhp\Model\UserGetRequest(); // \NexConnServerSdkPhp\Model\UserGetRequest

try {
    $result = $apiInstance->getUser($user_get_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserManagementApi->getUser: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **user_get_request** | [**\NexConnServerSdkPhp\Model\UserGetRequest**](../Model/UserGetRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\UserGetResponse**](../Model/UserGetResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getUserConnectionStatus()`

```php
getUserConnectionStatus($user_connection_status_request): \NexConnServerSdkPhp\Model\UserConnectionStatusResponse
```

Check user online status

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\UserManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$user_connection_status_request = new \NexConnServerSdkPhp\Model\UserConnectionStatusRequest(); // \NexConnServerSdkPhp\Model\UserConnectionStatusRequest

try {
    $result = $apiInstance->getUserConnectionStatus($user_connection_status_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserManagementApi->getUserConnectionStatus: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **user_connection_status_request** | [**\NexConnServerSdkPhp\Model\UserConnectionStatusRequest**](../Model/UserConnectionStatusRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\UserConnectionStatusResponse**](../Model/UserConnectionStatusResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `issueAccessToken()`

```php
issueAccessToken($access_token_issue_request): \NexConnServerSdkPhp\Model\AccessTokenIssueResponse
```

Register a user

Rate limit: 200/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\UserManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$access_token_issue_request = new \NexConnServerSdkPhp\Model\AccessTokenIssueRequest(); // \NexConnServerSdkPhp\Model\AccessTokenIssueRequest

try {
    $result = $apiInstance->issueAccessToken($access_token_issue_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserManagementApi->issueAccessToken: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **access_token_issue_request** | [**\NexConnServerSdkPhp\Model\AccessTokenIssueRequest**](../Model/AccessTokenIssueRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\AccessTokenIssueResponse**](../Model/AccessTokenIssueResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listBannedUsers()`

```php
listBannedUsers($user_ban_list_request): \NexConnServerSdkPhp\Model\UserBanListResponse
```

List banned users

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\UserManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$user_ban_list_request = new \NexConnServerSdkPhp\Model\UserBanListRequest(); // \NexConnServerSdkPhp\Model\UserBanListRequest

try {
    $result = $apiInstance->listBannedUsers($user_ban_list_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserManagementApi->listBannedUsers: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **user_ban_list_request** | [**\NexConnServerSdkPhp\Model\UserBanListRequest**](../Model/UserBanListRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\UserBanListResponse**](../Model/UserBanListResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listChannelTypeMute()`

```php
listChannelTypeMute($channel_type_mute_list_request): \NexConnServerSdkPhp\Model\ChannelTypeMuteListResponse
```

List muted direct channel users

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\UserManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$channel_type_mute_list_request = new \NexConnServerSdkPhp\Model\ChannelTypeMuteListRequest(); // \NexConnServerSdkPhp\Model\ChannelTypeMuteListRequest

try {
    $result = $apiInstance->listChannelTypeMute($channel_type_mute_list_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserManagementApi->listChannelTypeMute: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **channel_type_mute_list_request** | [**\NexConnServerSdkPhp\Model\ChannelTypeMuteListRequest**](../Model/ChannelTypeMuteListRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\ChannelTypeMuteListResponse**](../Model/ChannelTypeMuteListResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listSoftDeletedUsers()`

```php
listSoftDeletedUsers($user_soft_deleted_list_request): \NexConnServerSdkPhp\Model\UserSoftDeletedListResponse
```

Query soft-deleted users

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\UserManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$user_soft_deleted_list_request = new \NexConnServerSdkPhp\Model\UserSoftDeletedListRequest(); // \NexConnServerSdkPhp\Model\UserSoftDeletedListRequest

try {
    $result = $apiInstance->listSoftDeletedUsers($user_soft_deleted_list_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserManagementApi->listSoftDeletedUsers: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **user_soft_deleted_list_request** | [**\NexConnServerSdkPhp\Model\UserSoftDeletedListRequest**](../Model/UserSoftDeletedListRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\UserSoftDeletedListResponse**](../Model/UserSoftDeletedListResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `restoreUsers()`

```php
restoreUsers($user_ids_max100_request): \NexConnServerSdkPhp\Model\UserOperationResponse
```

Restore a user

Rate limit: 100 users/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\UserManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$user_ids_max100_request = new \NexConnServerSdkPhp\Model\UserIdsMax100Request(); // \NexConnServerSdkPhp\Model\UserIdsMax100Request

try {
    $result = $apiInstance->restoreUsers($user_ids_max100_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserManagementApi->restoreUsers: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **user_ids_max100_request** | [**\NexConnServerSdkPhp\Model\UserIdsMax100Request**](../Model/UserIdsMax100Request.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\UserOperationResponse**](../Model/UserOperationResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `setChannelTypeMute()`

```php
setChannelTypeMute($channel_type_mute_set_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Mute a user in direct channels

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\UserManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$channel_type_mute_set_request = new \NexConnServerSdkPhp\Model\ChannelTypeMuteSetRequest(); // \NexConnServerSdkPhp\Model\ChannelTypeMuteSetRequest

try {
    $result = $apiInstance->setChannelTypeMute($channel_type_mute_set_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserManagementApi->setChannelTypeMute: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **channel_type_mute_set_request** | [**\NexConnServerSdkPhp\Model\ChannelTypeMuteSetRequest**](../Model/ChannelTypeMuteSetRequest.md)|  | |


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

## `softDeleteUsers()`

```php
softDeleteUsers($user_ids_max100_request): \NexConnServerSdkPhp\Model\UserOperationResponse
```

Soft-delete a user

Rate limit: 100 users/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\UserManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$user_ids_max100_request = new \NexConnServerSdkPhp\Model\UserIdsMax100Request(); // \NexConnServerSdkPhp\Model\UserIdsMax100Request

try {
    $result = $apiInstance->softDeleteUsers($user_ids_max100_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserManagementApi->softDeleteUsers: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **user_ids_max100_request** | [**\NexConnServerSdkPhp\Model\UserIdsMax100Request**](../Model/UserIdsMax100Request.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\UserOperationResponse**](../Model/UserOperationResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `unbanUsers()`

```php
unbanUsers($user_ids_max20_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Unban a user

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\UserManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$user_ids_max20_request = new \NexConnServerSdkPhp\Model\UserIdsMax20Request(); // \NexConnServerSdkPhp\Model\UserIdsMax20Request

try {
    $result = $apiInstance->unbanUsers($user_ids_max20_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserManagementApi->unbanUsers: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **user_ids_max20_request** | [**\NexConnServerSdkPhp\Model\UserIdsMax20Request**](../Model/UserIdsMax20Request.md)|  | |


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

## `updateUser()`

```php
updateUser($user_update_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Update user info

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\UserManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$user_update_request = new \NexConnServerSdkPhp\Model\UserUpdateRequest(); // \NexConnServerSdkPhp\Model\UserUpdateRequest

try {
    $result = $apiInstance->updateUser($user_update_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserManagementApi->updateUser: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **user_update_request** | [**\NexConnServerSdkPhp\Model\UserUpdateRequest**](../Model/UserUpdateRequest.md)|  | |


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

# NexConnServerSdkPhp\GroupChannelModerationApi

All requests use the primary/backup domains configured by the caller.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**addGroupChannelAllowedSenderList()**](GroupChannelModerationApi.md#addGroupChannelAllowedSenderList) | **POST** /v4/group-channel/allowed-sender-list/add | Add to allowed senders list |
| [**addGroupChannelFreezeList()**](GroupChannelModerationApi.md#addGroupChannelFreezeList) | **POST** /v4/group-channel/freeze-list/add | Freeze a group |
| [**addGroupChannelUserMuteList()**](GroupChannelModerationApi.md#addGroupChannelUserMuteList) | **POST** /v4/group-channel/user/mute-list/add | Mute a group member |
| [**getGroupChannelAllowedSenderList()**](GroupChannelModerationApi.md#getGroupChannelAllowedSenderList) | **POST** /v4/group-channel/allowed-sender-list/get | Query allowed senders list |
| [**getGroupChannelFreezeList()**](GroupChannelModerationApi.md#getGroupChannelFreezeList) | **POST** /v4/group-channel/freeze-list/get | Query group freeze status |
| [**getGroupChannelUserMuteList()**](GroupChannelModerationApi.md#getGroupChannelUserMuteList) | **POST** /v4/group-channel/user/mute-list/get | List muted group members |
| [**removeGroupChannelAllowedSenderList()**](GroupChannelModerationApi.md#removeGroupChannelAllowedSenderList) | **POST** /v4/group-channel/allowed-sender-list/remove | Remove from allowed senders list |
| [**removeGroupChannelFreezeList()**](GroupChannelModerationApi.md#removeGroupChannelFreezeList) | **POST** /v4/group-channel/freeze-list/remove | Unfreeze a group |
| [**removeGroupChannelUserMuteList()**](GroupChannelModerationApi.md#removeGroupChannelUserMuteList) | **POST** /v4/group-channel/user/mute-list/remove | Unmute a group member |


## `addGroupChannelAllowedSenderList()`

```php
addGroupChannelAllowedSenderList($group_channel_allowed_sender_list_update_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Add to allowed senders list

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\GroupChannelModerationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$group_channel_allowed_sender_list_update_request = new \NexConnServerSdkPhp\Model\GroupChannelAllowedSenderListUpdateRequest(); // \NexConnServerSdkPhp\Model\GroupChannelAllowedSenderListUpdateRequest

try {
    $result = $apiInstance->addGroupChannelAllowedSenderList($group_channel_allowed_sender_list_update_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupChannelModerationApi->addGroupChannelAllowedSenderList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group_channel_allowed_sender_list_update_request** | [**\NexConnServerSdkPhp\Model\GroupChannelAllowedSenderListUpdateRequest**](../Model/GroupChannelAllowedSenderListUpdateRequest.md)|  | |


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

## `addGroupChannelFreezeList()`

```php
addGroupChannelFreezeList($group_channel_freeze_list_update_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Freeze a group

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\GroupChannelModerationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$group_channel_freeze_list_update_request = new \NexConnServerSdkPhp\Model\GroupChannelFreezeListUpdateRequest(); // \NexConnServerSdkPhp\Model\GroupChannelFreezeListUpdateRequest

try {
    $result = $apiInstance->addGroupChannelFreezeList($group_channel_freeze_list_update_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupChannelModerationApi->addGroupChannelFreezeList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group_channel_freeze_list_update_request** | [**\NexConnServerSdkPhp\Model\GroupChannelFreezeListUpdateRequest**](../Model/GroupChannelFreezeListUpdateRequest.md)|  | |


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

## `addGroupChannelUserMuteList()`

```php
addGroupChannelUserMuteList($group_channel_user_mute_list_add_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Mute a group member

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\GroupChannelModerationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$group_channel_user_mute_list_add_request = new \NexConnServerSdkPhp\Model\GroupChannelUserMuteListAddRequest(); // \NexConnServerSdkPhp\Model\GroupChannelUserMuteListAddRequest

try {
    $result = $apiInstance->addGroupChannelUserMuteList($group_channel_user_mute_list_add_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupChannelModerationApi->addGroupChannelUserMuteList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group_channel_user_mute_list_add_request** | [**\NexConnServerSdkPhp\Model\GroupChannelUserMuteListAddRequest**](../Model/GroupChannelUserMuteListAddRequest.md)|  | |


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

## `getGroupChannelAllowedSenderList()`

```php
getGroupChannelAllowedSenderList($group_channel_allowed_sender_list_get_request): \NexConnServerSdkPhp\Model\GroupChannelAllowedSenderListGetResponse
```

Query allowed senders list

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\GroupChannelModerationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$group_channel_allowed_sender_list_get_request = new \NexConnServerSdkPhp\Model\GroupChannelAllowedSenderListGetRequest(); // \NexConnServerSdkPhp\Model\GroupChannelAllowedSenderListGetRequest

try {
    $result = $apiInstance->getGroupChannelAllowedSenderList($group_channel_allowed_sender_list_get_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupChannelModerationApi->getGroupChannelAllowedSenderList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group_channel_allowed_sender_list_get_request** | [**\NexConnServerSdkPhp\Model\GroupChannelAllowedSenderListGetRequest**](../Model/GroupChannelAllowedSenderListGetRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\GroupChannelAllowedSenderListGetResponse**](../Model/GroupChannelAllowedSenderListGetResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getGroupChannelFreezeList()`

```php
getGroupChannelFreezeList($group_channel_freeze_list_get_request): \NexConnServerSdkPhp\Model\GroupChannelFreezeListGetResponse
```

Query group freeze status

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\GroupChannelModerationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$group_channel_freeze_list_get_request = new \NexConnServerSdkPhp\Model\GroupChannelFreezeListGetRequest(); // \NexConnServerSdkPhp\Model\GroupChannelFreezeListGetRequest

try {
    $result = $apiInstance->getGroupChannelFreezeList($group_channel_freeze_list_get_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupChannelModerationApi->getGroupChannelFreezeList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group_channel_freeze_list_get_request** | [**\NexConnServerSdkPhp\Model\GroupChannelFreezeListGetRequest**](../Model/GroupChannelFreezeListGetRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\GroupChannelFreezeListGetResponse**](../Model/GroupChannelFreezeListGetResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getGroupChannelUserMuteList()`

```php
getGroupChannelUserMuteList($group_channel_user_mute_list_get_request): \NexConnServerSdkPhp\Model\GroupChannelUserMuteListGetResponse
```

List muted group members

Rate limit: 100/sec. The public endpoint list currently publishes this capability as `/v4/group-channel/user/mute-list-get`.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\GroupChannelModerationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$group_channel_user_mute_list_get_request = new \NexConnServerSdkPhp\Model\GroupChannelUserMuteListGetRequest(); // \NexConnServerSdkPhp\Model\GroupChannelUserMuteListGetRequest

try {
    $result = $apiInstance->getGroupChannelUserMuteList($group_channel_user_mute_list_get_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupChannelModerationApi->getGroupChannelUserMuteList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group_channel_user_mute_list_get_request** | [**\NexConnServerSdkPhp\Model\GroupChannelUserMuteListGetRequest**](../Model/GroupChannelUserMuteListGetRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\GroupChannelUserMuteListGetResponse**](../Model/GroupChannelUserMuteListGetResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `removeGroupChannelAllowedSenderList()`

```php
removeGroupChannelAllowedSenderList($group_channel_allowed_sender_list_update_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Remove from allowed senders list

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\GroupChannelModerationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$group_channel_allowed_sender_list_update_request = new \NexConnServerSdkPhp\Model\GroupChannelAllowedSenderListUpdateRequest(); // \NexConnServerSdkPhp\Model\GroupChannelAllowedSenderListUpdateRequest

try {
    $result = $apiInstance->removeGroupChannelAllowedSenderList($group_channel_allowed_sender_list_update_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupChannelModerationApi->removeGroupChannelAllowedSenderList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group_channel_allowed_sender_list_update_request** | [**\NexConnServerSdkPhp\Model\GroupChannelAllowedSenderListUpdateRequest**](../Model/GroupChannelAllowedSenderListUpdateRequest.md)|  | |


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

## `removeGroupChannelFreezeList()`

```php
removeGroupChannelFreezeList($group_channel_freeze_list_update_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Unfreeze a group

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\GroupChannelModerationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$group_channel_freeze_list_update_request = new \NexConnServerSdkPhp\Model\GroupChannelFreezeListUpdateRequest(); // \NexConnServerSdkPhp\Model\GroupChannelFreezeListUpdateRequest

try {
    $result = $apiInstance->removeGroupChannelFreezeList($group_channel_freeze_list_update_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupChannelModerationApi->removeGroupChannelFreezeList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group_channel_freeze_list_update_request** | [**\NexConnServerSdkPhp\Model\GroupChannelFreezeListUpdateRequest**](../Model/GroupChannelFreezeListUpdateRequest.md)|  | |


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

## `removeGroupChannelUserMuteList()`

```php
removeGroupChannelUserMuteList($group_channel_user_mute_list_remove_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Unmute a group member

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\GroupChannelModerationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$group_channel_user_mute_list_remove_request = new \NexConnServerSdkPhp\Model\GroupChannelUserMuteListRemoveRequest(); // \NexConnServerSdkPhp\Model\GroupChannelUserMuteListRemoveRequest

try {
    $result = $apiInstance->removeGroupChannelUserMuteList($group_channel_user_mute_list_remove_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupChannelModerationApi->removeGroupChannelUserMuteList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group_channel_user_mute_list_remove_request** | [**\NexConnServerSdkPhp\Model\GroupChannelUserMuteListRemoveRequest**](../Model/GroupChannelUserMuteListRemoveRequest.md)|  | |


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

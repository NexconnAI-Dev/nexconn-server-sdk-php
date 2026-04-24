# NexConnServerSdkPhp\CommunityChannelModerationApi

All requests use the primary/backup domains configured by the caller.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**addCommunityChannelAllowedSenderList()**](CommunityChannelModerationApi.md#addCommunityChannelAllowedSenderList) | **POST** /v4/community-channel/allowed-sender-list/add | Add community channel allowed sender list |
| [**addCommunityChannelMutedUsers()**](CommunityChannelModerationApi.md#addCommunityChannelMutedUsers) | **POST** /v4/community-channel/mute-list/add | Add community-channel muted users |
| [**getCommunityChannelFreezeList()**](CommunityChannelModerationApi.md#getCommunityChannelFreezeList) | **POST** /v4/community-channel/freeze-list/get | Get community channel freeze status |
| [**listCommunityChannelAllowedSenderList()**](CommunityChannelModerationApi.md#listCommunityChannelAllowedSenderList) | **POST** /v4/community-channel/allowed-sender-list/get | List community channel allowed sender list |
| [**listCommunityChannelMutedUsers()**](CommunityChannelModerationApi.md#listCommunityChannelMutedUsers) | **POST** /v4/community-channel/mute-list/get | List community-channel muted users |
| [**removeCommunityChannelAllowedSenderList()**](CommunityChannelModerationApi.md#removeCommunityChannelAllowedSenderList) | **POST** /v4/community-channel/allowed-sender-list/remove | Remove community channel allowed sender list |
| [**removeCommunityChannelMutedUsers()**](CommunityChannelModerationApi.md#removeCommunityChannelMutedUsers) | **POST** /v4/community-channel/mute-list/remove | Remove community-channel muted users |
| [**setCommunityChannelFreezeList()**](CommunityChannelModerationApi.md#setCommunityChannelFreezeList) | **POST** /v4/community-channel/freeze-list/set | Set community channel freeze list |


## `addCommunityChannelAllowedSenderList()`

```php
addCommunityChannelAllowedSenderList($community_channel_allowed_sender_list_update_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Add community channel allowed sender list

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\CommunityChannelModerationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$community_channel_allowed_sender_list_update_request = new \NexConnServerSdkPhp\Model\CommunityChannelAllowedSenderListUpdateRequest(); // \NexConnServerSdkPhp\Model\CommunityChannelAllowedSenderListUpdateRequest

try {
    $result = $apiInstance->addCommunityChannelAllowedSenderList($community_channel_allowed_sender_list_update_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CommunityChannelModerationApi->addCommunityChannelAllowedSenderList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **community_channel_allowed_sender_list_update_request** | [**\NexConnServerSdkPhp\Model\CommunityChannelAllowedSenderListUpdateRequest**](../Model/CommunityChannelAllowedSenderListUpdateRequest.md)|  | |


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

## `addCommunityChannelMutedUsers()`

```php
addCommunityChannelMutedUsers($community_channel_mute_list_add_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Add community-channel muted users

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\CommunityChannelModerationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$community_channel_mute_list_add_request = new \NexConnServerSdkPhp\Model\CommunityChannelMuteListAddRequest(); // \NexConnServerSdkPhp\Model\CommunityChannelMuteListAddRequest

try {
    $result = $apiInstance->addCommunityChannelMutedUsers($community_channel_mute_list_add_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CommunityChannelModerationApi->addCommunityChannelMutedUsers: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **community_channel_mute_list_add_request** | [**\NexConnServerSdkPhp\Model\CommunityChannelMuteListAddRequest**](../Model/CommunityChannelMuteListAddRequest.md)|  | |


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

## `getCommunityChannelFreezeList()`

```php
getCommunityChannelFreezeList($community_channel_freeze_list_get_request): \NexConnServerSdkPhp\Model\CommunityChannelFreezeListGetResponse
```

Get community channel freeze status

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\CommunityChannelModerationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$community_channel_freeze_list_get_request = new \NexConnServerSdkPhp\Model\CommunityChannelFreezeListGetRequest(); // \NexConnServerSdkPhp\Model\CommunityChannelFreezeListGetRequest

try {
    $result = $apiInstance->getCommunityChannelFreezeList($community_channel_freeze_list_get_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CommunityChannelModerationApi->getCommunityChannelFreezeList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **community_channel_freeze_list_get_request** | [**\NexConnServerSdkPhp\Model\CommunityChannelFreezeListGetRequest**](../Model/CommunityChannelFreezeListGetRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\CommunityChannelFreezeListGetResponse**](../Model/CommunityChannelFreezeListGetResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listCommunityChannelAllowedSenderList()`

```php
listCommunityChannelAllowedSenderList($community_channel_allowed_sender_list_get_request): \NexConnServerSdkPhp\Model\CommunityChannelAllowedSenderListGetResponse
```

List community channel allowed sender list

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\CommunityChannelModerationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$community_channel_allowed_sender_list_get_request = new \NexConnServerSdkPhp\Model\CommunityChannelAllowedSenderListGetRequest(); // \NexConnServerSdkPhp\Model\CommunityChannelAllowedSenderListGetRequest

try {
    $result = $apiInstance->listCommunityChannelAllowedSenderList($community_channel_allowed_sender_list_get_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CommunityChannelModerationApi->listCommunityChannelAllowedSenderList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **community_channel_allowed_sender_list_get_request** | [**\NexConnServerSdkPhp\Model\CommunityChannelAllowedSenderListGetRequest**](../Model/CommunityChannelAllowedSenderListGetRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\CommunityChannelAllowedSenderListGetResponse**](../Model/CommunityChannelAllowedSenderListGetResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listCommunityChannelMutedUsers()`

```php
listCommunityChannelMutedUsers($community_channel_mute_list_get_request): \NexConnServerSdkPhp\Model\CommunityChannelMuteListGetResponse
```

List community-channel muted users

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\CommunityChannelModerationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$community_channel_mute_list_get_request = new \NexConnServerSdkPhp\Model\CommunityChannelMuteListGetRequest(); // \NexConnServerSdkPhp\Model\CommunityChannelMuteListGetRequest

try {
    $result = $apiInstance->listCommunityChannelMutedUsers($community_channel_mute_list_get_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CommunityChannelModerationApi->listCommunityChannelMutedUsers: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **community_channel_mute_list_get_request** | [**\NexConnServerSdkPhp\Model\CommunityChannelMuteListGetRequest**](../Model/CommunityChannelMuteListGetRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\CommunityChannelMuteListGetResponse**](../Model/CommunityChannelMuteListGetResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `removeCommunityChannelAllowedSenderList()`

```php
removeCommunityChannelAllowedSenderList($community_channel_allowed_sender_list_update_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Remove community channel allowed sender list

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\CommunityChannelModerationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$community_channel_allowed_sender_list_update_request = new \NexConnServerSdkPhp\Model\CommunityChannelAllowedSenderListUpdateRequest(); // \NexConnServerSdkPhp\Model\CommunityChannelAllowedSenderListUpdateRequest

try {
    $result = $apiInstance->removeCommunityChannelAllowedSenderList($community_channel_allowed_sender_list_update_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CommunityChannelModerationApi->removeCommunityChannelAllowedSenderList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **community_channel_allowed_sender_list_update_request** | [**\NexConnServerSdkPhp\Model\CommunityChannelAllowedSenderListUpdateRequest**](../Model/CommunityChannelAllowedSenderListUpdateRequest.md)|  | |


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

## `removeCommunityChannelMutedUsers()`

```php
removeCommunityChannelMutedUsers($community_channel_mute_list_remove_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Remove community-channel muted users

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\CommunityChannelModerationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$community_channel_mute_list_remove_request = new \NexConnServerSdkPhp\Model\CommunityChannelMuteListRemoveRequest(); // \NexConnServerSdkPhp\Model\CommunityChannelMuteListRemoveRequest

try {
    $result = $apiInstance->removeCommunityChannelMutedUsers($community_channel_mute_list_remove_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CommunityChannelModerationApi->removeCommunityChannelMutedUsers: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **community_channel_mute_list_remove_request** | [**\NexConnServerSdkPhp\Model\CommunityChannelMuteListRemoveRequest**](../Model/CommunityChannelMuteListRemoveRequest.md)|  | |


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

## `setCommunityChannelFreezeList()`

```php
setCommunityChannelFreezeList($community_channel_freeze_list_set_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Set community channel freeze list

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\CommunityChannelModerationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$community_channel_freeze_list_set_request = new \NexConnServerSdkPhp\Model\CommunityChannelFreezeListSetRequest(); // \NexConnServerSdkPhp\Model\CommunityChannelFreezeListSetRequest

try {
    $result = $apiInstance->setCommunityChannelFreezeList($community_channel_freeze_list_set_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CommunityChannelModerationApi->setCommunityChannelFreezeList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **community_channel_freeze_list_set_request** | [**\NexConnServerSdkPhp\Model\CommunityChannelFreezeListSetRequest**](../Model/CommunityChannelFreezeListSetRequest.md)|  | |


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

# NexConnServerSdkPhp\SystemMessagesApi

All requests use the primary/backup domains configured by the caller.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**broadcastMessageOnline()**](SystemMessagesApi.md#broadcastMessageOnline) | **POST** /v4/system-channel/message/broadcast-online | Broadcast to online users |
| [**broadcastSystemChannelMessage()**](SystemMessagesApi.md#broadcastSystemChannelMessage) | **POST** /v4/system-channel/message/broadcast-all | Broadcast to all users (persistent) |
| [**deleteBroadcastMessage()**](SystemMessagesApi.md#deleteBroadcastMessage) | **POST** /v4/system-channel/message/broadcast/delete | Recall broadcast to all users |
| [**sendSystemChannelMessage()**](SystemMessagesApi.md#sendSystemChannelMessage) | **POST** /v4/system-channel/message/send | Send a system message |
| [**sendSystemChannelPushByPackage()**](SystemMessagesApi.md#sendSystemChannelPushByPackage) | **POST** /v4/system-channel/app-package-users/send | Push by app package name |
| [**sendSystemChannelPushByTag()**](SystemMessagesApi.md#sendSystemChannelPushByTag) | **POST** /v4/system-channel/tagged-users/send | Push to tagged users |


## `broadcastMessageOnline()`

```php
broadcastMessageOnline($system_channel_broadcast_online_request): \NexConnServerSdkPhp\Model\SingleMessageIdResponse
```

Broadcast to online users

Rate limit: 60/min.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\SystemMessagesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$system_channel_broadcast_online_request = new \NexConnServerSdkPhp\Model\SystemChannelBroadcastOnlineRequest(); // \NexConnServerSdkPhp\Model\SystemChannelBroadcastOnlineRequest

try {
    $result = $apiInstance->broadcastMessageOnline($system_channel_broadcast_online_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SystemMessagesApi->broadcastMessageOnline: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **system_channel_broadcast_online_request** | [**\NexConnServerSdkPhp\Model\SystemChannelBroadcastOnlineRequest**](../Model/SystemChannelBroadcastOnlineRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\SingleMessageIdResponse**](../Model/SingleMessageIdResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `broadcastSystemChannelMessage()`

```php
broadcastSystemChannelMessage($system_channel_broadcast_all_request): \NexConnServerSdkPhp\Model\SingleMessageIdResponse
```

Broadcast to all users (persistent)

Rate limit: 2/hour, 3/day.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\SystemMessagesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$system_channel_broadcast_all_request = new \NexConnServerSdkPhp\Model\SystemChannelBroadcastAllRequest(); // \NexConnServerSdkPhp\Model\SystemChannelBroadcastAllRequest

try {
    $result = $apiInstance->broadcastSystemChannelMessage($system_channel_broadcast_all_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SystemMessagesApi->broadcastSystemChannelMessage: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **system_channel_broadcast_all_request** | [**\NexConnServerSdkPhp\Model\SystemChannelBroadcastAllRequest**](../Model/SystemChannelBroadcastAllRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\SingleMessageIdResponse**](../Model/SingleMessageIdResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteBroadcastMessage()`

```php
deleteBroadcastMessage($system_channel_broadcast_delete_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Recall broadcast to all users

Rate limit: 2/hour, 3/day.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\SystemMessagesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$system_channel_broadcast_delete_request = new \NexConnServerSdkPhp\Model\SystemChannelBroadcastDeleteRequest(); // \NexConnServerSdkPhp\Model\SystemChannelBroadcastDeleteRequest

try {
    $result = $apiInstance->deleteBroadcastMessage($system_channel_broadcast_delete_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SystemMessagesApi->deleteBroadcastMessage: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **system_channel_broadcast_delete_request** | [**\NexConnServerSdkPhp\Model\SystemChannelBroadcastDeleteRequest**](../Model/SystemChannelBroadcastDeleteRequest.md)|  | |


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

## `sendSystemChannelMessage()`

```php
sendSystemChannelMessage($system_channel_message_send_request): \NexConnServerSdkPhp\Model\UserMessageSendResponse
```

Send a system message

Rate limit: 100 msgs/sec (by recipient count).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\SystemMessagesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$system_channel_message_send_request = new \NexConnServerSdkPhp\Model\SystemChannelMessageSendRequest(); // \NexConnServerSdkPhp\Model\SystemChannelMessageSendRequest

try {
    $result = $apiInstance->sendSystemChannelMessage($system_channel_message_send_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SystemMessagesApi->sendSystemChannelMessage: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **system_channel_message_send_request** | [**\NexConnServerSdkPhp\Model\SystemChannelMessageSendRequest**](../Model/SystemChannelMessageSendRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\UserMessageSendResponse**](../Model/UserMessageSendResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `sendSystemChannelPushByPackage()`

```php
sendSystemChannelPushByPackage($system_channel_push_request): \NexConnServerSdkPhp\Model\SystemChannelPushResponse
```

Push by app package name

Rate limit: 2/hour, 3/day (shared).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\SystemMessagesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$system_channel_push_request = new \NexConnServerSdkPhp\Model\SystemChannelPushRequest(); // \NexConnServerSdkPhp\Model\SystemChannelPushRequest

try {
    $result = $apiInstance->sendSystemChannelPushByPackage($system_channel_push_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SystemMessagesApi->sendSystemChannelPushByPackage: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **system_channel_push_request** | [**\NexConnServerSdkPhp\Model\SystemChannelPushRequest**](../Model/SystemChannelPushRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\SystemChannelPushResponse**](../Model/SystemChannelPushResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `sendSystemChannelPushByTag()`

```php
sendSystemChannelPushByTag($system_channel_push_request): \NexConnServerSdkPhp\Model\SystemChannelPushResponse
```

Push to tagged users

Rate limit: 2/hour, 3/day (shared).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\SystemMessagesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$system_channel_push_request = new \NexConnServerSdkPhp\Model\SystemChannelPushRequest(); // \NexConnServerSdkPhp\Model\SystemChannelPushRequest

try {
    $result = $apiInstance->sendSystemChannelPushByTag($system_channel_push_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SystemMessagesApi->sendSystemChannelPushByTag: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **system_channel_push_request** | [**\NexConnServerSdkPhp\Model\SystemChannelPushRequest**](../Model/SystemChannelPushRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\SystemChannelPushResponse**](../Model/SystemChannelPushResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

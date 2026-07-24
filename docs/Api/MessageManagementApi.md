# NexConnServerSdkPhp\MessageManagementApi

All requests use the primary/backup domains configured by the caller.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**broadcastOpenChannelMessage()**](MessageManagementApi.md#broadcastOpenChannelMessage) | **POST** /v4/open-channel/message/broadcast | Broadcast to all open channels |
| [**deleteChannelMessageHistory()**](MessageManagementApi.md#deleteChannelMessageHistory) | **POST** /v4/channel/message/history/delete | Delete server-side channel message history |
| [**deleteChannelTypeMessageMetadata()**](MessageManagementApi.md#deleteChannelTypeMessageMetadata) | **POST** /v4/channel-type/message/metadata/delete | Delete message metadata |
| [**deleteCommunityChannelMessageMetadata()**](MessageManagementApi.md#deleteCommunityChannelMessageMetadata) | **POST** /v4/community-channel/message/metadata/delete | Delete community-channel message metadata keys |
| [**deleteMessage()**](MessageManagementApi.md#deleteMessage) | **POST** /v4/message/delete | Delete a message (recall) |
| [**listChannelTypeMessageMetadata()**](MessageManagementApi.md#listChannelTypeMessageMetadata) | **POST** /v4/channel-type/message/metadata/list | Get message metadata |
| [**listCommunityChannelMessageMetadata()**](MessageManagementApi.md#listCommunityChannelMessageMetadata) | **POST** /v4/community-channel/message/metadata/list | List community-channel message metadata |
| [**sendCommunityChannelMessage()**](MessageManagementApi.md#sendCommunityChannelMessage) | **POST** /v4/community-channel/message/send | Send a community channel message |
| [**sendDirectChannelMessage()**](MessageManagementApi.md#sendDirectChannelMessage) | **POST** /v4/direct-channel/message/send | Send a direct message |
| [**sendDirectChannelStreamMessage()**](MessageManagementApi.md#sendDirectChannelStreamMessage) | **POST** /v4/direct-channel/message/stream/send | Send a direct channel stream message |
| [**sendGroupChannelMessage()**](MessageManagementApi.md#sendGroupChannelMessage) | **POST** /v4/group-channel/message/send | Send a group message |
| [**sendGroupChannelStreamMessage()**](MessageManagementApi.md#sendGroupChannelStreamMessage) | **POST** /v4/group-channel/message/stream/send | Send a group channel stream message |
| [**sendOpenChannelMessage()**](MessageManagementApi.md#sendOpenChannelMessage) | **POST** /v4/open-channel/message/send | Send an open channel message |
| [**setChannelTypeMessageMetadata()**](MessageManagementApi.md#setChannelTypeMessageMetadata) | **POST** /v4/channel-type/message/metadata/set | Set message metadata |
| [**setCommunityChannelMessageMetadata()**](MessageManagementApi.md#setCommunityChannelMessageMetadata) | **POST** /v4/community-channel/message/metadata/set | Set community-channel message metadata |
| [**updateCommunityChannelMessage()**](MessageManagementApi.md#updateCommunityChannelMessage) | **POST** /v4/community-channel/message/update | Update community-channel message |
| [**updateDirectChannelMessage()**](MessageManagementApi.md#updateDirectChannelMessage) | **POST** /v4/direct-channel/message/update | Update direct-channel message |
| [**updateGroupChannelMessage()**](MessageManagementApi.md#updateGroupChannelMessage) | **POST** /v4/group-channel/message/update | Update group-channel message |


## `broadcastOpenChannelMessage()`

```php
broadcastOpenChannelMessage($open_channel_broadcast_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Broadcast to all open channels

Rate limit: 1/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\MessageManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$open_channel_broadcast_request = new \NexConnServerSdkPhp\Model\OpenChannelBroadcastRequest(); // \NexConnServerSdkPhp\Model\OpenChannelBroadcastRequest

try {
    $result = $apiInstance->broadcastOpenChannelMessage($open_channel_broadcast_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessageManagementApi->broadcastOpenChannelMessage: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **open_channel_broadcast_request** | [**\NexConnServerSdkPhp\Model\OpenChannelBroadcastRequest**](../Model/OpenChannelBroadcastRequest.md)|  | |


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

## `deleteChannelMessageHistory()`

```php
deleteChannelMessageHistory($channel_message_history_delete_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Delete server-side channel message history

Rate limit: 100/sec. Server path `/v4/channel/message/history/delete` (`HistoryCleanInput`).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\MessageManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$channel_message_history_delete_request = new \NexConnServerSdkPhp\Model\ChannelMessageHistoryDeleteRequest(); // \NexConnServerSdkPhp\Model\ChannelMessageHistoryDeleteRequest

try {
    $result = $apiInstance->deleteChannelMessageHistory($channel_message_history_delete_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessageManagementApi->deleteChannelMessageHistory: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **channel_message_history_delete_request** | [**\NexConnServerSdkPhp\Model\ChannelMessageHistoryDeleteRequest**](../Model/ChannelMessageHistoryDeleteRequest.md)|  | |


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

## `deleteChannelTypeMessageMetadata()`

```php
deleteChannelTypeMessageMetadata($channel_type_message_metadata_delete_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Delete message metadata

Rate limit: 100/sec (max 20 for group messages).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\MessageManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$channel_type_message_metadata_delete_request = new \NexConnServerSdkPhp\Model\ChannelTypeMessageMetadataDeleteRequest(); // \NexConnServerSdkPhp\Model\ChannelTypeMessageMetadataDeleteRequest

try {
    $result = $apiInstance->deleteChannelTypeMessageMetadata($channel_type_message_metadata_delete_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessageManagementApi->deleteChannelTypeMessageMetadata: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **channel_type_message_metadata_delete_request** | [**\NexConnServerSdkPhp\Model\ChannelTypeMessageMetadataDeleteRequest**](../Model/ChannelTypeMessageMetadataDeleteRequest.md)|  | |


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

## `deleteCommunityChannelMessageMetadata()`

```php
deleteCommunityChannelMessageMetadata($community_channel_message_metadata_delete_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Delete community-channel message metadata keys

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\MessageManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$community_channel_message_metadata_delete_request = new \NexConnServerSdkPhp\Model\CommunityChannelMessageMetadataDeleteRequest(); // \NexConnServerSdkPhp\Model\CommunityChannelMessageMetadataDeleteRequest

try {
    $result = $apiInstance->deleteCommunityChannelMessageMetadata($community_channel_message_metadata_delete_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessageManagementApi->deleteCommunityChannelMessageMetadata: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **community_channel_message_metadata_delete_request** | [**\NexConnServerSdkPhp\Model\CommunityChannelMessageMetadataDeleteRequest**](../Model/CommunityChannelMessageMetadataDeleteRequest.md)|  | |


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

## `deleteMessage()`

```php
deleteMessage($message_delete_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Delete a message (recall)

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\MessageManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$message_delete_request = new \NexConnServerSdkPhp\Model\MessageDeleteRequest(); // \NexConnServerSdkPhp\Model\MessageDeleteRequest

try {
    $result = $apiInstance->deleteMessage($message_delete_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessageManagementApi->deleteMessage: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **message_delete_request** | [**\NexConnServerSdkPhp\Model\MessageDeleteRequest**](../Model/MessageDeleteRequest.md)|  | |


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

## `listChannelTypeMessageMetadata()`

```php
listChannelTypeMessageMetadata($channel_type_message_metadata_list_request): \NexConnServerSdkPhp\Model\ChannelTypeMessageMetadataListResponse
```

Get message metadata

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\MessageManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$channel_type_message_metadata_list_request = new \NexConnServerSdkPhp\Model\ChannelTypeMessageMetadataListRequest(); // \NexConnServerSdkPhp\Model\ChannelTypeMessageMetadataListRequest

try {
    $result = $apiInstance->listChannelTypeMessageMetadata($channel_type_message_metadata_list_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessageManagementApi->listChannelTypeMessageMetadata: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **channel_type_message_metadata_list_request** | [**\NexConnServerSdkPhp\Model\ChannelTypeMessageMetadataListRequest**](../Model/ChannelTypeMessageMetadataListRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\ChannelTypeMessageMetadataListResponse**](../Model/ChannelTypeMessageMetadataListResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listCommunityChannelMessageMetadata()`

```php
listCommunityChannelMessageMetadata($community_channel_message_metadata_list_request): \NexConnServerSdkPhp\Model\CommunityChannelMessageMetadataListResponse
```

List community-channel message metadata

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\MessageManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$community_channel_message_metadata_list_request = new \NexConnServerSdkPhp\Model\CommunityChannelMessageMetadataListRequest(); // \NexConnServerSdkPhp\Model\CommunityChannelMessageMetadataListRequest

try {
    $result = $apiInstance->listCommunityChannelMessageMetadata($community_channel_message_metadata_list_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessageManagementApi->listCommunityChannelMessageMetadata: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **community_channel_message_metadata_list_request** | [**\NexConnServerSdkPhp\Model\CommunityChannelMessageMetadataListRequest**](../Model/CommunityChannelMessageMetadataListRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\CommunityChannelMessageMetadataListResponse**](../Model/CommunityChannelMessageMetadataListResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `sendCommunityChannelMessage()`

```php
sendCommunityChannelMessage($community_channel_message_send_request): \NexConnServerSdkPhp\Model\ChannelMessageSendResponse
```

Send a community channel message

Rate limit: 100/sec (by target group count); 20/sec per channel.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\MessageManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$community_channel_message_send_request = new \NexConnServerSdkPhp\Model\CommunityChannelMessageSendRequest(); // \NexConnServerSdkPhp\Model\CommunityChannelMessageSendRequest

try {
    $result = $apiInstance->sendCommunityChannelMessage($community_channel_message_send_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessageManagementApi->sendCommunityChannelMessage: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **community_channel_message_send_request** | [**\NexConnServerSdkPhp\Model\CommunityChannelMessageSendRequest**](../Model/CommunityChannelMessageSendRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\ChannelMessageSendResponse**](../Model/ChannelMessageSendResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `sendDirectChannelMessage()`

```php
sendDirectChannelMessage($direct_channel_message_send_request): \NexConnServerSdkPhp\Model\UserMessageSendResponse
```

Send a direct message

Rate limit: 6,000 msgs/min (by recipient count).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\MessageManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$direct_channel_message_send_request = new \NexConnServerSdkPhp\Model\DirectChannelMessageSendRequest(); // \NexConnServerSdkPhp\Model\DirectChannelMessageSendRequest

try {
    $result = $apiInstance->sendDirectChannelMessage($direct_channel_message_send_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessageManagementApi->sendDirectChannelMessage: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **direct_channel_message_send_request** | [**\NexConnServerSdkPhp\Model\DirectChannelMessageSendRequest**](../Model/DirectChannelMessageSendRequest.md)|  | |


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

## `sendDirectChannelStreamMessage()`

```php
sendDirectChannelStreamMessage($direct_channel_stream_message_send_request): \NexConnServerSdkPhp\Model\StreamMessageSendResponse
```

Send a direct channel stream message

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\MessageManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$direct_channel_stream_message_send_request = new \NexConnServerSdkPhp\Model\DirectChannelStreamMessageSendRequest(); // \NexConnServerSdkPhp\Model\DirectChannelStreamMessageSendRequest

try {
    $result = $apiInstance->sendDirectChannelStreamMessage($direct_channel_stream_message_send_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessageManagementApi->sendDirectChannelStreamMessage: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **direct_channel_stream_message_send_request** | [**\NexConnServerSdkPhp\Model\DirectChannelStreamMessageSendRequest**](../Model/DirectChannelStreamMessageSendRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\StreamMessageSendResponse**](../Model/StreamMessageSendResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `sendGroupChannelMessage()`

```php
sendGroupChannelMessage($group_channel_message_send_request): \NexConnServerSdkPhp\Model\ChannelMessageSendResponse
```

Send a group message

Rate limit: 20/sec (by target group count).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\MessageManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$group_channel_message_send_request = new \NexConnServerSdkPhp\Model\GroupChannelMessageSendRequest(); // \NexConnServerSdkPhp\Model\GroupChannelMessageSendRequest

try {
    $result = $apiInstance->sendGroupChannelMessage($group_channel_message_send_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessageManagementApi->sendGroupChannelMessage: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group_channel_message_send_request** | [**\NexConnServerSdkPhp\Model\GroupChannelMessageSendRequest**](../Model/GroupChannelMessageSendRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\ChannelMessageSendResponse**](../Model/ChannelMessageSendResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `sendGroupChannelStreamMessage()`

```php
sendGroupChannelStreamMessage($group_channel_stream_message_send_request): \NexConnServerSdkPhp\Model\StreamMessageSendResponse
```

Send a group channel stream message

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\MessageManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$group_channel_stream_message_send_request = new \NexConnServerSdkPhp\Model\GroupChannelStreamMessageSendRequest(); // \NexConnServerSdkPhp\Model\GroupChannelStreamMessageSendRequest

try {
    $result = $apiInstance->sendGroupChannelStreamMessage($group_channel_stream_message_send_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessageManagementApi->sendGroupChannelStreamMessage: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group_channel_stream_message_send_request** | [**\NexConnServerSdkPhp\Model\GroupChannelStreamMessageSendRequest**](../Model/GroupChannelStreamMessageSendRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\StreamMessageSendResponse**](../Model/StreamMessageSendResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `sendOpenChannelMessage()`

```php
sendOpenChannelMessage($open_channel_message_send_request): \NexConnServerSdkPhp\Model\ChannelMessageSendResponse
```

Send an open channel message

Rate limit: 100/sec (by target open channel count).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\MessageManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$open_channel_message_send_request = new \NexConnServerSdkPhp\Model\OpenChannelMessageSendRequest(); // \NexConnServerSdkPhp\Model\OpenChannelMessageSendRequest

try {
    $result = $apiInstance->sendOpenChannelMessage($open_channel_message_send_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessageManagementApi->sendOpenChannelMessage: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **open_channel_message_send_request** | [**\NexConnServerSdkPhp\Model\OpenChannelMessageSendRequest**](../Model/OpenChannelMessageSendRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\ChannelMessageSendResponse**](../Model/ChannelMessageSendResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `setChannelTypeMessageMetadata()`

```php
setChannelTypeMessageMetadata($message_metadata_set_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Set message metadata

Rate limit: 100/sec (max 20 for group messages).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\MessageManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$message_metadata_set_request = new \NexConnServerSdkPhp\Model\MessageMetadataSetRequest(); // \NexConnServerSdkPhp\Model\MessageMetadataSetRequest

try {
    $result = $apiInstance->setChannelTypeMessageMetadata($message_metadata_set_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessageManagementApi->setChannelTypeMessageMetadata: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **message_metadata_set_request** | [**\NexConnServerSdkPhp\Model\MessageMetadataSetRequest**](../Model/MessageMetadataSetRequest.md)|  | |


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

## `setCommunityChannelMessageMetadata()`

```php
setCommunityChannelMessageMetadata($community_channel_message_metadata_set_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Set community-channel message metadata

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\MessageManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$community_channel_message_metadata_set_request = new \NexConnServerSdkPhp\Model\CommunityChannelMessageMetadataSetRequest(); // \NexConnServerSdkPhp\Model\CommunityChannelMessageMetadataSetRequest

try {
    $result = $apiInstance->setCommunityChannelMessageMetadata($community_channel_message_metadata_set_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessageManagementApi->setCommunityChannelMessageMetadata: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **community_channel_message_metadata_set_request** | [**\NexConnServerSdkPhp\Model\CommunityChannelMessageMetadataSetRequest**](../Model/CommunityChannelMessageMetadataSetRequest.md)|  | |


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

## `updateCommunityChannelMessage()`

```php
updateCommunityChannelMessage($community_channel_message_update_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Update community-channel message

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\MessageManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$community_channel_message_update_request = new \NexConnServerSdkPhp\Model\CommunityChannelMessageUpdateRequest(); // \NexConnServerSdkPhp\Model\CommunityChannelMessageUpdateRequest

try {
    $result = $apiInstance->updateCommunityChannelMessage($community_channel_message_update_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessageManagementApi->updateCommunityChannelMessage: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **community_channel_message_update_request** | [**\NexConnServerSdkPhp\Model\CommunityChannelMessageUpdateRequest**](../Model/CommunityChannelMessageUpdateRequest.md)|  | |


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

## `updateDirectChannelMessage()`

```php
updateDirectChannelMessage($direct_channel_message_update_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Update direct-channel message

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\MessageManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$direct_channel_message_update_request = new \NexConnServerSdkPhp\Model\DirectChannelMessageUpdateRequest(); // \NexConnServerSdkPhp\Model\DirectChannelMessageUpdateRequest

try {
    $result = $apiInstance->updateDirectChannelMessage($direct_channel_message_update_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessageManagementApi->updateDirectChannelMessage: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **direct_channel_message_update_request** | [**\NexConnServerSdkPhp\Model\DirectChannelMessageUpdateRequest**](../Model/DirectChannelMessageUpdateRequest.md)|  | |


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

## `updateGroupChannelMessage()`

```php
updateGroupChannelMessage($group_channel_message_update_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Update group-channel message

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\MessageManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$group_channel_message_update_request = new \NexConnServerSdkPhp\Model\GroupChannelMessageUpdateRequest(); // \NexConnServerSdkPhp\Model\GroupChannelMessageUpdateRequest

try {
    $result = $apiInstance->updateGroupChannelMessage($group_channel_message_update_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessageManagementApi->updateGroupChannelMessage: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group_channel_message_update_request** | [**\NexConnServerSdkPhp\Model\GroupChannelMessageUpdateRequest**](../Model/GroupChannelMessageUpdateRequest.md)|  | |


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

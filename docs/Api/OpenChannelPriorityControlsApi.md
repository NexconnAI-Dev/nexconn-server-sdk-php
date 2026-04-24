# NexConnServerSdkPhp\OpenChannelPriorityControlsApi

All requests use the primary/backup domains configured by the caller.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**addOpenChannelPriorityMessageTypeList()**](OpenChannelPriorityControlsApi.md#addOpenChannelPriorityMessageTypeList) | **POST** /v4/open-channel/priority-message-type-list/add | Add priority message types |
| [**addOpenChannelPrioritySenderList()**](OpenChannelPriorityControlsApi.md#addOpenChannelPrioritySenderList) | **POST** /v4/open-channel/priority-sender-list/add | Add priority senders |
| [**getOpenChannelPriorityMessageTypeList()**](OpenChannelPriorityControlsApi.md#getOpenChannelPriorityMessageTypeList) | **POST** /v4/open-channel/priority-message-type-list/get | Query priority message types |
| [**getOpenChannelPrioritySenderList()**](OpenChannelPriorityControlsApi.md#getOpenChannelPrioritySenderList) | **POST** /v4/open-channel/priority-sender-list/get | Query priority senders |
| [**removeOpenChannelPriorityMessageTypeList()**](OpenChannelPriorityControlsApi.md#removeOpenChannelPriorityMessageTypeList) | **POST** /v4/open-channel/priority-message-type-list/remove | Remove priority message types |
| [**removeOpenChannelPrioritySenderList()**](OpenChannelPriorityControlsApi.md#removeOpenChannelPrioritySenderList) | **POST** /v4/open-channel/priority-sender-list/remove | Remove priority senders |


## `addOpenChannelPriorityMessageTypeList()`

```php
addOpenChannelPriorityMessageTypeList($open_channel_priority_message_type_list_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Add priority message types

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\OpenChannelPriorityControlsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$open_channel_priority_message_type_list_request = new \NexConnServerSdkPhp\Model\OpenChannelPriorityMessageTypeListRequest(); // \NexConnServerSdkPhp\Model\OpenChannelPriorityMessageTypeListRequest

try {
    $result = $apiInstance->addOpenChannelPriorityMessageTypeList($open_channel_priority_message_type_list_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OpenChannelPriorityControlsApi->addOpenChannelPriorityMessageTypeList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **open_channel_priority_message_type_list_request** | [**\NexConnServerSdkPhp\Model\OpenChannelPriorityMessageTypeListRequest**](../Model/OpenChannelPriorityMessageTypeListRequest.md)|  | |


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

## `addOpenChannelPrioritySenderList()`

```php
addOpenChannelPrioritySenderList($open_channel_participant_ids_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Add priority senders

Rate limit: 100/sec. The public endpoint list currently publishes this capability as `/v4/open-channel/participant/priority-sender-list/add`.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\OpenChannelPriorityControlsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$open_channel_participant_ids_request = new \NexConnServerSdkPhp\Model\OpenChannelParticipantIdsRequest(); // \NexConnServerSdkPhp\Model\OpenChannelParticipantIdsRequest

try {
    $result = $apiInstance->addOpenChannelPrioritySenderList($open_channel_participant_ids_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OpenChannelPriorityControlsApi->addOpenChannelPrioritySenderList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **open_channel_participant_ids_request** | [**\NexConnServerSdkPhp\Model\OpenChannelParticipantIdsRequest**](../Model/OpenChannelParticipantIdsRequest.md)|  | |


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

## `getOpenChannelPriorityMessageTypeList()`

```php
getOpenChannelPriorityMessageTypeList(): \NexConnServerSdkPhp\Model\OpenChannelMessageTypeListResponse
```

Query priority message types

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\OpenChannelPriorityControlsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getOpenChannelPriorityMessageTypeList();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OpenChannelPriorityControlsApi->getOpenChannelPriorityMessageTypeList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not require a request body.


### Return type

[**\NexConnServerSdkPhp\Model\OpenChannelMessageTypeListResponse**](../Model/OpenChannelMessageTypeListResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getOpenChannelPrioritySenderList()`

```php
getOpenChannelPrioritySenderList($open_channel_participant_list_by_channel_request): \NexConnServerSdkPhp\Model\OpenChannelParticipantIdsResponse
```

Query priority senders

Rate limit: 100/sec. The public endpoint list currently publishes this capability as `/v4/open-channel/participant/priority-sender-list/get`.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\OpenChannelPriorityControlsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$open_channel_participant_list_by_channel_request = new \NexConnServerSdkPhp\Model\OpenChannelParticipantListByChannelRequest(); // \NexConnServerSdkPhp\Model\OpenChannelParticipantListByChannelRequest

try {
    $result = $apiInstance->getOpenChannelPrioritySenderList($open_channel_participant_list_by_channel_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OpenChannelPriorityControlsApi->getOpenChannelPrioritySenderList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **open_channel_participant_list_by_channel_request** | [**\NexConnServerSdkPhp\Model\OpenChannelParticipantListByChannelRequest**](../Model/OpenChannelParticipantListByChannelRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\OpenChannelParticipantIdsResponse**](../Model/OpenChannelParticipantIdsResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `removeOpenChannelPriorityMessageTypeList()`

```php
removeOpenChannelPriorityMessageTypeList($open_channel_priority_message_type_list_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Remove priority message types

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\OpenChannelPriorityControlsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$open_channel_priority_message_type_list_request = new \NexConnServerSdkPhp\Model\OpenChannelPriorityMessageTypeListRequest(); // \NexConnServerSdkPhp\Model\OpenChannelPriorityMessageTypeListRequest

try {
    $result = $apiInstance->removeOpenChannelPriorityMessageTypeList($open_channel_priority_message_type_list_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OpenChannelPriorityControlsApi->removeOpenChannelPriorityMessageTypeList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **open_channel_priority_message_type_list_request** | [**\NexConnServerSdkPhp\Model\OpenChannelPriorityMessageTypeListRequest**](../Model/OpenChannelPriorityMessageTypeListRequest.md)|  | |


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

## `removeOpenChannelPrioritySenderList()`

```php
removeOpenChannelPrioritySenderList($open_channel_participant_ids_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Remove priority senders

Rate limit: 100/sec. The public endpoint list currently publishes this capability as `/v4/open-channel/participant/priority-sender-list/remove`.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\OpenChannelPriorityControlsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$open_channel_participant_ids_request = new \NexConnServerSdkPhp\Model\OpenChannelParticipantIdsRequest(); // \NexConnServerSdkPhp\Model\OpenChannelParticipantIdsRequest

try {
    $result = $apiInstance->removeOpenChannelPrioritySenderList($open_channel_participant_ids_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OpenChannelPriorityControlsApi->removeOpenChannelPrioritySenderList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **open_channel_participant_ids_request** | [**\NexConnServerSdkPhp\Model\OpenChannelParticipantIdsRequest**](../Model/OpenChannelParticipantIdsRequest.md)|  | |


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

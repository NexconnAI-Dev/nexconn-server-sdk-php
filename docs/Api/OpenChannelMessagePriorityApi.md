# NexConnServerSdkPhp\OpenChannelMessagePriorityApi

All requests use the primary/backup domains configured by the caller.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**addOpenChannelLowPriorityMessageTypeList()**](OpenChannelMessagePriorityApi.md#addOpenChannelLowPriorityMessageTypeList) | **POST** /v4/open-channel/low-priority-message-type-list/add | Add low-priority message types |
| [**getOpenChannelLowPriorityMessageTypeList()**](OpenChannelMessagePriorityApi.md#getOpenChannelLowPriorityMessageTypeList) | **POST** /v4/open-channel/low-priority-message-type-list/get | Query low-priority message types |
| [**removeOpenChannelLowPriorityMessageTypeList()**](OpenChannelMessagePriorityApi.md#removeOpenChannelLowPriorityMessageTypeList) | **POST** /v4/open-channel/low-priority-message-type-list/remove | Remove low-priority message types |


## `addOpenChannelLowPriorityMessageTypeList()`

```php
addOpenChannelLowPriorityMessageTypeList($open_channel_low_priority_message_type_list_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Add low-priority message types

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\OpenChannelMessagePriorityApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$open_channel_low_priority_message_type_list_request = new \NexConnServerSdkPhp\Model\OpenChannelLowPriorityMessageTypeListRequest(); // \NexConnServerSdkPhp\Model\OpenChannelLowPriorityMessageTypeListRequest

try {
    $result = $apiInstance->addOpenChannelLowPriorityMessageTypeList($open_channel_low_priority_message_type_list_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OpenChannelMessagePriorityApi->addOpenChannelLowPriorityMessageTypeList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **open_channel_low_priority_message_type_list_request** | [**\NexConnServerSdkPhp\Model\OpenChannelLowPriorityMessageTypeListRequest**](../Model/OpenChannelLowPriorityMessageTypeListRequest.md)|  | |


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

## `getOpenChannelLowPriorityMessageTypeList()`

```php
getOpenChannelLowPriorityMessageTypeList(): \NexConnServerSdkPhp\Model\OpenChannelMessageTypeListResponse
```

Query low-priority message types

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\OpenChannelMessagePriorityApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getOpenChannelLowPriorityMessageTypeList();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OpenChannelMessagePriorityApi->getOpenChannelLowPriorityMessageTypeList: ', $e->getMessage(), PHP_EOL;
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

## `removeOpenChannelLowPriorityMessageTypeList()`

```php
removeOpenChannelLowPriorityMessageTypeList($open_channel_low_priority_message_type_list_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Remove low-priority message types

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\OpenChannelMessagePriorityApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$open_channel_low_priority_message_type_list_request = new \NexConnServerSdkPhp\Model\OpenChannelLowPriorityMessageTypeListRequest(); // \NexConnServerSdkPhp\Model\OpenChannelLowPriorityMessageTypeListRequest

try {
    $result = $apiInstance->removeOpenChannelLowPriorityMessageTypeList($open_channel_low_priority_message_type_list_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OpenChannelMessagePriorityApi->removeOpenChannelLowPriorityMessageTypeList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **open_channel_low_priority_message_type_list_request** | [**\NexConnServerSdkPhp\Model\OpenChannelLowPriorityMessageTypeListRequest**](../Model/OpenChannelLowPriorityMessageTypeListRequest.md)|  | |


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

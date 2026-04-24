# NexConnServerSdkPhp\OpenChannelManagementApi

All requests use the primary/backup domains configured by the caller.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createOpenChannel()**](OpenChannelManagementApi.md#createOpenChannel) | **POST** /v4/open-channel/create | Create an open channel |
| [**destroyOpenChannels()**](OpenChannelManagementApi.md#destroyOpenChannels) | **POST** /v4/open-channel/destroy | Destroy an open channel |
| [**getOpenChannel()**](OpenChannelManagementApi.md#getOpenChannel) | **POST** /v4/open-channel/get | Get open channel info |
| [**setOpenChannelDestroyType()**](OpenChannelManagementApi.md#setOpenChannelDestroyType) | **POST** /v4/open-channel/destroy-type/set | Set auto-destroy type |


## `createOpenChannel()`

```php
createOpenChannel($open_channel_create_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Create an open channel

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\OpenChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$open_channel_create_request = new \NexConnServerSdkPhp\Model\OpenChannelCreateRequest(); // \NexConnServerSdkPhp\Model\OpenChannelCreateRequest

try {
    $result = $apiInstance->createOpenChannel($open_channel_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OpenChannelManagementApi->createOpenChannel: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **open_channel_create_request** | [**\NexConnServerSdkPhp\Model\OpenChannelCreateRequest**](../Model/OpenChannelCreateRequest.md)|  | |


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

## `destroyOpenChannels()`

```php
destroyOpenChannels($open_channel_destroy_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Destroy an open channel

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\OpenChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$open_channel_destroy_request = new \NexConnServerSdkPhp\Model\OpenChannelDestroyRequest(); // \NexConnServerSdkPhp\Model\OpenChannelDestroyRequest

try {
    $result = $apiInstance->destroyOpenChannels($open_channel_destroy_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OpenChannelManagementApi->destroyOpenChannels: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **open_channel_destroy_request** | [**\NexConnServerSdkPhp\Model\OpenChannelDestroyRequest**](../Model/OpenChannelDestroyRequest.md)|  | |


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

## `getOpenChannel()`

```php
getOpenChannel($open_channel_get_request): \NexConnServerSdkPhp\Model\OpenChannelGetResponse
```

Get open channel info

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\OpenChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$open_channel_get_request = new \NexConnServerSdkPhp\Model\OpenChannelGetRequest(); // \NexConnServerSdkPhp\Model\OpenChannelGetRequest

try {
    $result = $apiInstance->getOpenChannel($open_channel_get_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OpenChannelManagementApi->getOpenChannel: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **open_channel_get_request** | [**\NexConnServerSdkPhp\Model\OpenChannelGetRequest**](../Model/OpenChannelGetRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\OpenChannelGetResponse**](../Model/OpenChannelGetResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `setOpenChannelDestroyType()`

```php
setOpenChannelDestroyType($open_channel_destroy_type_set_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Set auto-destroy type

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\OpenChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$open_channel_destroy_type_set_request = new \NexConnServerSdkPhp\Model\OpenChannelDestroyTypeSetRequest(); // \NexConnServerSdkPhp\Model\OpenChannelDestroyTypeSetRequest

try {
    $result = $apiInstance->setOpenChannelDestroyType($open_channel_destroy_type_set_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OpenChannelManagementApi->setOpenChannelDestroyType: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **open_channel_destroy_type_set_request** | [**\NexConnServerSdkPhp\Model\OpenChannelDestroyTypeSetRequest**](../Model/OpenChannelDestroyTypeSetRequest.md)|  | |


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

# NexConnServerSdkPhp\OpenChannelMetadataApi

All requests use the primary/backup domains configured by the caller.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**batchGetOpenChannelMetadata()**](OpenChannelMetadataApi.md#batchGetOpenChannelMetadata) | **POST** /v4/open-channel/metadata/batch/get | Query metadata |
| [**batchRemoveOpenChannelMetadata()**](OpenChannelMetadataApi.md#batchRemoveOpenChannelMetadata) | **POST** /v4/open-channel/metadata/batch/remove | Batch delete metadata |
| [**batchSetOpenChannelMetadata()**](OpenChannelMetadataApi.md#batchSetOpenChannelMetadata) | **POST** /v4/open-channel/metadata/batch/set | Batch set metadata |


## `batchGetOpenChannelMetadata()`

```php
batchGetOpenChannelMetadata($open_channel_metadata_batch_get_request): \NexConnServerSdkPhp\Model\OpenChannelMetadataBatchGetResponse
```

Query metadata

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\OpenChannelMetadataApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$open_channel_metadata_batch_get_request = new \NexConnServerSdkPhp\Model\OpenChannelMetadataBatchGetRequest(); // \NexConnServerSdkPhp\Model\OpenChannelMetadataBatchGetRequest

try {
    $result = $apiInstance->batchGetOpenChannelMetadata($open_channel_metadata_batch_get_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OpenChannelMetadataApi->batchGetOpenChannelMetadata: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **open_channel_metadata_batch_get_request** | [**\NexConnServerSdkPhp\Model\OpenChannelMetadataBatchGetRequest**](../Model/OpenChannelMetadataBatchGetRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\OpenChannelMetadataBatchGetResponse**](../Model/OpenChannelMetadataBatchGetResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `batchRemoveOpenChannelMetadata()`

```php
batchRemoveOpenChannelMetadata($open_channel_metadata_batch_remove_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Batch delete metadata

Rate limit: 100 attrs/sec (shared).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\OpenChannelMetadataApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$open_channel_metadata_batch_remove_request = new \NexConnServerSdkPhp\Model\OpenChannelMetadataBatchRemoveRequest(); // \NexConnServerSdkPhp\Model\OpenChannelMetadataBatchRemoveRequest

try {
    $result = $apiInstance->batchRemoveOpenChannelMetadata($open_channel_metadata_batch_remove_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OpenChannelMetadataApi->batchRemoveOpenChannelMetadata: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **open_channel_metadata_batch_remove_request** | [**\NexConnServerSdkPhp\Model\OpenChannelMetadataBatchRemoveRequest**](../Model/OpenChannelMetadataBatchRemoveRequest.md)|  | |


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

## `batchSetOpenChannelMetadata()`

```php
batchSetOpenChannelMetadata($open_channel_metadata_batch_set_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Batch set metadata

Rate limit: 100 attrs/sec (shared).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\OpenChannelMetadataApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$open_channel_metadata_batch_set_request = new \NexConnServerSdkPhp\Model\OpenChannelMetadataBatchSetRequest(); // \NexConnServerSdkPhp\Model\OpenChannelMetadataBatchSetRequest

try {
    $result = $apiInstance->batchSetOpenChannelMetadata($open_channel_metadata_batch_set_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OpenChannelMetadataApi->batchSetOpenChannelMetadata: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **open_channel_metadata_batch_set_request** | [**\NexConnServerSdkPhp\Model\OpenChannelMetadataBatchSetRequest**](../Model/OpenChannelMetadataBatchSetRequest.md)|  | |


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

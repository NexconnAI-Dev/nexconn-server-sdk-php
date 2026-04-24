# NexConnServerSdkPhp\ModerationApi

All requests use the primary/backup domains configured by the caller.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**batchAddProfanityWords()**](ModerationApi.md#batchAddProfanityWords) | **POST** /v4/profanity-word/batch/add | Batch add profanity words |
| [**batchRemoveProfanityWords()**](ModerationApi.md#batchRemoveProfanityWords) | **POST** /v4/profanity-word/batch/remove | Batch delete profanity words |
| [**listProfanityWords()**](ModerationApi.md#listProfanityWords) | **POST** /v4/profanity-word/list | List profanity words |
| [**removeProfanityWord()**](ModerationApi.md#removeProfanityWord) | **POST** /v4/profanity-word/remove | Delete profanity word |


## `batchAddProfanityWords()`

```php
batchAddProfanityWords($profanity_word_batch_add_request): \NexConnServerSdkPhp\Model\ProfanityWordBatchAddResponse
```

Batch add profanity words

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\ModerationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$profanity_word_batch_add_request = new \NexConnServerSdkPhp\Model\ProfanityWordBatchAddRequest(); // \NexConnServerSdkPhp\Model\ProfanityWordBatchAddRequest

try {
    $result = $apiInstance->batchAddProfanityWords($profanity_word_batch_add_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ModerationApi->batchAddProfanityWords: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **profanity_word_batch_add_request** | [**\NexConnServerSdkPhp\Model\ProfanityWordBatchAddRequest**](../Model/ProfanityWordBatchAddRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\ProfanityWordBatchAddResponse**](../Model/ProfanityWordBatchAddResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `batchRemoveProfanityWords()`

```php
batchRemoveProfanityWords($profanity_word_batch_delete_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Batch delete profanity words

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\ModerationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$profanity_word_batch_delete_request = new \NexConnServerSdkPhp\Model\ProfanityWordBatchDeleteRequest(); // \NexConnServerSdkPhp\Model\ProfanityWordBatchDeleteRequest

try {
    $result = $apiInstance->batchRemoveProfanityWords($profanity_word_batch_delete_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ModerationApi->batchRemoveProfanityWords: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **profanity_word_batch_delete_request** | [**\NexConnServerSdkPhp\Model\ProfanityWordBatchDeleteRequest**](../Model/ProfanityWordBatchDeleteRequest.md)|  | |


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

## `listProfanityWords()`

```php
listProfanityWords($profanity_word_list_request): \NexConnServerSdkPhp\Model\ProfanityWordListResponse
```

List profanity words

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\ModerationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$profanity_word_list_request = new \NexConnServerSdkPhp\Model\ProfanityWordListRequest(); // \NexConnServerSdkPhp\Model\ProfanityWordListRequest

try {
    $result = $apiInstance->listProfanityWords($profanity_word_list_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ModerationApi->listProfanityWords: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **profanity_word_list_request** | [**\NexConnServerSdkPhp\Model\ProfanityWordListRequest**](../Model/ProfanityWordListRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\ProfanityWordListResponse**](../Model/ProfanityWordListResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `removeProfanityWord()`

```php
removeProfanityWord($profanity_word_delete_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Delete profanity word

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\ModerationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$profanity_word_delete_request = new \NexConnServerSdkPhp\Model\ProfanityWordDeleteRequest(); // \NexConnServerSdkPhp\Model\ProfanityWordDeleteRequest

try {
    $result = $apiInstance->removeProfanityWord($profanity_word_delete_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ModerationApi->removeProfanityWord: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **profanity_word_delete_request** | [**\NexConnServerSdkPhp\Model\ProfanityWordDeleteRequest**](../Model/ProfanityWordDeleteRequest.md)|  | |


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

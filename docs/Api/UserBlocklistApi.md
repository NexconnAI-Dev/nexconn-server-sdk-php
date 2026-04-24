# NexConnServerSdkPhp\UserBlocklistApi

All requests use the primary/backup domains configured by the caller.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**addUserBlocklist()**](UserBlocklistApi.md#addUserBlocklist) | **POST** /v4/user/blocklist/add | Add to blocklist |
| [**getUserBlocklist()**](UserBlocklistApi.md#getUserBlocklist) | **POST** /v4/user/blocklist/get | Get blocklist |
| [**removeUserBlocklist()**](UserBlocklistApi.md#removeUserBlocklist) | **POST** /v4/user/blocklist/remove | Remove from blocklist |


## `addUserBlocklist()`

```php
addUserBlocklist($user_blocklist_add_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Add to blocklist

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\UserBlocklistApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$user_blocklist_add_request = new \NexConnServerSdkPhp\Model\UserBlocklistAddRequest(); // \NexConnServerSdkPhp\Model\UserBlocklistAddRequest

try {
    $result = $apiInstance->addUserBlocklist($user_blocklist_add_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserBlocklistApi->addUserBlocklist: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **user_blocklist_add_request** | [**\NexConnServerSdkPhp\Model\UserBlocklistAddRequest**](../Model/UserBlocklistAddRequest.md)|  | |


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

## `getUserBlocklist()`

```php
getUserBlocklist($user_blocklist_get_request): \NexConnServerSdkPhp\Model\UserBlocklistGetResponse
```

Get blocklist

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\UserBlocklistApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$user_blocklist_get_request = new \NexConnServerSdkPhp\Model\UserBlocklistGetRequest(); // \NexConnServerSdkPhp\Model\UserBlocklistGetRequest

try {
    $result = $apiInstance->getUserBlocklist($user_blocklist_get_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserBlocklistApi->getUserBlocklist: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **user_blocklist_get_request** | [**\NexConnServerSdkPhp\Model\UserBlocklistGetRequest**](../Model/UserBlocklistGetRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\UserBlocklistGetResponse**](../Model/UserBlocklistGetResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `removeUserBlocklist()`

```php
removeUserBlocklist($user_blocklist_remove_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Remove from blocklist

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\UserBlocklistApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$user_blocklist_remove_request = new \NexConnServerSdkPhp\Model\UserBlocklistRemoveRequest(); // \NexConnServerSdkPhp\Model\UserBlocklistRemoveRequest

try {
    $result = $apiInstance->removeUserBlocklist($user_blocklist_remove_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserBlocklistApi->removeUserBlocklist: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **user_blocklist_remove_request** | [**\NexConnServerSdkPhp\Model\UserBlocklistRemoveRequest**](../Model/UserBlocklistRemoveRequest.md)|  | |


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

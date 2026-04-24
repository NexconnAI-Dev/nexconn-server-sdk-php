# NexConnServerSdkPhp\UserProfileHostingApi

All requests use the primary/backup domains configured by the caller.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**batchGetUserProfiles()**](UserProfileHostingApi.md#batchGetUserProfiles) | **POST** /v4/user/profile/batch/get | Batch get user profiles |
| [**deleteUserProfiles()**](UserProfileHostingApi.md#deleteUserProfiles) | **POST** /v4/user/profile/delete | Clear user profiles |
| [**listUserProfiles()**](UserProfileHostingApi.md#listUserProfiles) | **POST** /v4/user/profile/list | List user profiles |
| [**setUserProfile()**](UserProfileHostingApi.md#setUserProfile) | **POST** /v4/user/profile/set | Set user profile |


## `batchGetUserProfiles()`

```php
batchGetUserProfiles($user_ids_max20_request): \NexConnServerSdkPhp\Model\UserProfileBatchGetResponse
```

Batch get user profiles

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\UserProfileHostingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$user_ids_max20_request = new \NexConnServerSdkPhp\Model\UserIdsMax20Request(); // \NexConnServerSdkPhp\Model\UserIdsMax20Request

try {
    $result = $apiInstance->batchGetUserProfiles($user_ids_max20_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserProfileHostingApi->batchGetUserProfiles: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **user_ids_max20_request** | [**\NexConnServerSdkPhp\Model\UserIdsMax20Request**](../Model/UserIdsMax20Request.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\UserProfileBatchGetResponse**](../Model/UserProfileBatchGetResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteUserProfiles()`

```php
deleteUserProfiles($user_ids_max20_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Clear user profiles

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\UserProfileHostingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$user_ids_max20_request = new \NexConnServerSdkPhp\Model\UserIdsMax20Request(); // \NexConnServerSdkPhp\Model\UserIdsMax20Request

try {
    $result = $apiInstance->deleteUserProfiles($user_ids_max20_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserProfileHostingApi->deleteUserProfiles: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **user_ids_max20_request** | [**\NexConnServerSdkPhp\Model\UserIdsMax20Request**](../Model/UserIdsMax20Request.md)|  | |


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

## `listUserProfiles()`

```php
listUserProfiles($user_profile_list_request): \NexConnServerSdkPhp\Model\UserProfileListResponse
```

List user profiles

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\UserProfileHostingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$user_profile_list_request = new \NexConnServerSdkPhp\Model\UserProfileListRequest(); // \NexConnServerSdkPhp\Model\UserProfileListRequest

try {
    $result = $apiInstance->listUserProfiles($user_profile_list_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserProfileHostingApi->listUserProfiles: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **user_profile_list_request** | [**\NexConnServerSdkPhp\Model\UserProfileListRequest**](../Model/UserProfileListRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\UserProfileListResponse**](../Model/UserProfileListResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `setUserProfile()`

```php
setUserProfile($user_profile_set_request): \NexConnServerSdkPhp\Model\UserProfileSetResponse
```

Set user profile

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\UserProfileHostingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$user_profile_set_request = new \NexConnServerSdkPhp\Model\UserProfileSetRequest(); // \NexConnServerSdkPhp\Model\UserProfileSetRequest

try {
    $result = $apiInstance->setUserProfile($user_profile_set_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserProfileHostingApi->setUserProfile: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **user_profile_set_request** | [**\NexConnServerSdkPhp\Model\UserProfileSetRequest**](../Model/UserProfileSetRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\UserProfileSetResponse**](../Model/UserProfileSetResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

# NexConnServerSdkPhp\FriendshipApi

All requests use the primary/backup domains configured by the caller.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**addFriend()**](FriendshipApi.md#addFriend) | **POST** /v4/friend/add | Add friend |
| [**getFriendPermission()**](FriendshipApi.md#getFriendPermission) | **POST** /v4/friend/permission/get | Get friend permission |
| [**getFriendRelationships()**](FriendshipApi.md#getFriendRelationships) | **POST** /v4/friend/relationship/get | Get friend relationships |
| [**listFriends()**](FriendshipApi.md#listFriends) | **POST** /v4/friend/list | List friends |
| [**removeAllFriends()**](FriendshipApi.md#removeAllFriends) | **POST** /v4/friend/remove-all | Clean all friends |
| [**removeFriends()**](FriendshipApi.md#removeFriends) | **POST** /v4/friend/remove | Delete friends |
| [**setFriendPermission()**](FriendshipApi.md#setFriendPermission) | **POST** /v4/friend/permission/set | Set friend permission |
| [**setFriendProfile()**](FriendshipApi.md#setFriendProfile) | **POST** /v4/friend/profile/set | Set friend profile |


## `addFriend()`

```php
addFriend($friend_add_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Add friend

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\FriendshipApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$friend_add_request = new \NexConnServerSdkPhp\Model\FriendAddRequest(); // \NexConnServerSdkPhp\Model\FriendAddRequest

try {
    $result = $apiInstance->addFriend($friend_add_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FriendshipApi->addFriend: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **friend_add_request** | [**\NexConnServerSdkPhp\Model\FriendAddRequest**](../Model/FriendAddRequest.md)|  | |


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

## `getFriendPermission()`

```php
getFriendPermission($friend_permission_get_request): \NexConnServerSdkPhp\Model\FriendPermissionGetResponse
```

Get friend permission

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\FriendshipApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$friend_permission_get_request = new \NexConnServerSdkPhp\Model\FriendPermissionGetRequest(); // \NexConnServerSdkPhp\Model\FriendPermissionGetRequest

try {
    $result = $apiInstance->getFriendPermission($friend_permission_get_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FriendshipApi->getFriendPermission: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **friend_permission_get_request** | [**\NexConnServerSdkPhp\Model\FriendPermissionGetRequest**](../Model/FriendPermissionGetRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\FriendPermissionGetResponse**](../Model/FriendPermissionGetResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getFriendRelationships()`

```php
getFriendRelationships($friend_relationship_get_request): \NexConnServerSdkPhp\Model\FriendRelationshipGetResponse
```

Get friend relationships

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\FriendshipApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$friend_relationship_get_request = new \NexConnServerSdkPhp\Model\FriendRelationshipGetRequest(); // \NexConnServerSdkPhp\Model\FriendRelationshipGetRequest

try {
    $result = $apiInstance->getFriendRelationships($friend_relationship_get_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FriendshipApi->getFriendRelationships: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **friend_relationship_get_request** | [**\NexConnServerSdkPhp\Model\FriendRelationshipGetRequest**](../Model/FriendRelationshipGetRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\FriendRelationshipGetResponse**](../Model/FriendRelationshipGetResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listFriends()`

```php
listFriends($friend_list_request): \NexConnServerSdkPhp\Model\FriendListResponse
```

List friends

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\FriendshipApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$friend_list_request = new \NexConnServerSdkPhp\Model\FriendListRequest(); // \NexConnServerSdkPhp\Model\FriendListRequest

try {
    $result = $apiInstance->listFriends($friend_list_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FriendshipApi->listFriends: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **friend_list_request** | [**\NexConnServerSdkPhp\Model\FriendListRequest**](../Model/FriendListRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\FriendListResponse**](../Model/FriendListResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `removeAllFriends()`

```php
removeAllFriends($friend_clean_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Clean all friends

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\FriendshipApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$friend_clean_request = new \NexConnServerSdkPhp\Model\FriendCleanRequest(); // \NexConnServerSdkPhp\Model\FriendCleanRequest

try {
    $result = $apiInstance->removeAllFriends($friend_clean_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FriendshipApi->removeAllFriends: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **friend_clean_request** | [**\NexConnServerSdkPhp\Model\FriendCleanRequest**](../Model/FriendCleanRequest.md)|  | |


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

## `removeFriends()`

```php
removeFriends($friend_delete_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Delete friends

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\FriendshipApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$friend_delete_request = new \NexConnServerSdkPhp\Model\FriendDeleteRequest(); // \NexConnServerSdkPhp\Model\FriendDeleteRequest

try {
    $result = $apiInstance->removeFriends($friend_delete_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FriendshipApi->removeFriends: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **friend_delete_request** | [**\NexConnServerSdkPhp\Model\FriendDeleteRequest**](../Model/FriendDeleteRequest.md)|  | |


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

## `setFriendPermission()`

```php
setFriendPermission($friend_permission_set_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Set friend permission

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\FriendshipApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$friend_permission_set_request = new \NexConnServerSdkPhp\Model\FriendPermissionSetRequest(); // \NexConnServerSdkPhp\Model\FriendPermissionSetRequest

try {
    $result = $apiInstance->setFriendPermission($friend_permission_set_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FriendshipApi->setFriendPermission: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **friend_permission_set_request** | [**\NexConnServerSdkPhp\Model\FriendPermissionSetRequest**](../Model/FriendPermissionSetRequest.md)|  | |


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

## `setFriendProfile()`

```php
setFriendProfile($friend_profile_set_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Set friend profile

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\FriendshipApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$friend_profile_set_request = new \NexConnServerSdkPhp\Model\FriendProfileSetRequest(); // \NexConnServerSdkPhp\Model\FriendProfileSetRequest

try {
    $result = $apiInstance->setFriendProfile($friend_profile_set_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FriendshipApi->setFriendProfile: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **friend_profile_set_request** | [**\NexConnServerSdkPhp\Model\FriendProfileSetRequest**](../Model/FriendProfileSetRequest.md)|  | |


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

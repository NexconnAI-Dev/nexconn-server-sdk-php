# NexConnServerSdkPhp\ChannelManagementApi

All requests use the primary/backup domains configured by the caller.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**addTagToChannels()**](ChannelManagementApi.md#addTagToChannels) | **POST** /v4/channel/tag/add | Add tag to channel |
| [**addUserChannelTags()**](ChannelManagementApi.md#addUserChannelTags) | **POST** /v4/user/channel/tag/add | Add user channel tag |
| [**getChannelAttribute()**](ChannelManagementApi.md#getChannelAttribute) | **POST** /v4/channel/attribute/get | Get channel attributes |
| [**getChannelPushNotification()**](ChannelManagementApi.md#getChannelPushNotification) | **POST** /v4/channel/push/get | Get channel DND |
| [**getChannelTypeNotification()**](ChannelManagementApi.md#getChannelTypeNotification) | **POST** /v4/channel-type/push/get | Get DND by channel type |
| [**listChannelsByTag()**](ChannelManagementApi.md#listChannelsByTag) | **POST** /v4/channel/tag/list | Get channels by tag |
| [**listUserChannelTags()**](ChannelManagementApi.md#listUserChannelTags) | **POST** /v4/user/channel/tag/list | List user channel tags |
| [**removeTagFromChannels()**](ChannelManagementApi.md#removeTagFromChannels) | **POST** /v4/channel/tag/delete | Remove tag from channel |
| [**removeUserChannelTags()**](ChannelManagementApi.md#removeUserChannelTags) | **POST** /v4/user/channel/tag/remove | Remove user channel tag |
| [**setChannelPin()**](ChannelManagementApi.md#setChannelPin) | **POST** /v4/channel/pin/set | Pin a channel |
| [**setChannelPushNotification()**](ChannelManagementApi.md#setChannelPushNotification) | **POST** /v4/channel/push/set | Set channel DND |
| [**setChannelTypeNotification()**](ChannelManagementApi.md#setChannelTypeNotification) | **POST** /v4/channel-type/push/set | Set DND by channel type |


## `addTagToChannels()`

```php
addTagToChannels($channel_tag_add_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Add tag to channel

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\ChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$channel_tag_add_request = new \NexConnServerSdkPhp\Model\ChannelTagAddRequest(); // \NexConnServerSdkPhp\Model\ChannelTagAddRequest

try {
    $result = $apiInstance->addTagToChannels($channel_tag_add_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChannelManagementApi->addTagToChannels: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **channel_tag_add_request** | [**\NexConnServerSdkPhp\Model\ChannelTagAddRequest**](../Model/ChannelTagAddRequest.md)|  | |


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

## `addUserChannelTags()`

```php
addUserChannelTags($user_channel_tag_add_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Add user channel tag

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\ChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$user_channel_tag_add_request = new \NexConnServerSdkPhp\Model\UserChannelTagAddRequest(); // \NexConnServerSdkPhp\Model\UserChannelTagAddRequest

try {
    $result = $apiInstance->addUserChannelTags($user_channel_tag_add_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChannelManagementApi->addUserChannelTags: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **user_channel_tag_add_request** | [**\NexConnServerSdkPhp\Model\UserChannelTagAddRequest**](../Model/UserChannelTagAddRequest.md)|  | |


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

## `getChannelAttribute()`

```php
getChannelAttribute($channel_attribute_get_request): \NexConnServerSdkPhp\Model\ChannelAttributeGetResponse
```

Get channel attributes

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\ChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$channel_attribute_get_request = new \NexConnServerSdkPhp\Model\ChannelAttributeGetRequest(); // \NexConnServerSdkPhp\Model\ChannelAttributeGetRequest

try {
    $result = $apiInstance->getChannelAttribute($channel_attribute_get_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChannelManagementApi->getChannelAttribute: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **channel_attribute_get_request** | [**\NexConnServerSdkPhp\Model\ChannelAttributeGetRequest**](../Model/ChannelAttributeGetRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\ChannelAttributeGetResponse**](../Model/ChannelAttributeGetResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getChannelPushNotification()`

```php
getChannelPushNotification($channel_push_get_request): \NexConnServerSdkPhp\Model\ChannelPushGetResponse
```

Get channel DND

Rate limit: 100/sec. The public endpoint list currently publishes this capability as `/v4/channel/notification/get`.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\ChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$channel_push_get_request = new \NexConnServerSdkPhp\Model\ChannelPushGetRequest(); // \NexConnServerSdkPhp\Model\ChannelPushGetRequest

try {
    $result = $apiInstance->getChannelPushNotification($channel_push_get_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChannelManagementApi->getChannelPushNotification: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **channel_push_get_request** | [**\NexConnServerSdkPhp\Model\ChannelPushGetRequest**](../Model/ChannelPushGetRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\ChannelPushGetResponse**](../Model/ChannelPushGetResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getChannelTypeNotification()`

```php
getChannelTypeNotification($channel_type_notification_get_request): \NexConnServerSdkPhp\Model\ChannelTypeNotificationGetResponse
```

Get DND by channel type

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\ChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$channel_type_notification_get_request = new \NexConnServerSdkPhp\Model\ChannelTypeNotificationGetRequest(); // \NexConnServerSdkPhp\Model\ChannelTypeNotificationGetRequest

try {
    $result = $apiInstance->getChannelTypeNotification($channel_type_notification_get_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChannelManagementApi->getChannelTypeNotification: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **channel_type_notification_get_request** | [**\NexConnServerSdkPhp\Model\ChannelTypeNotificationGetRequest**](../Model/ChannelTypeNotificationGetRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\ChannelTypeNotificationGetResponse**](../Model/ChannelTypeNotificationGetResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listChannelsByTag()`

```php
listChannelsByTag($channel_tag_list_request): \NexConnServerSdkPhp\Model\ChannelTagListResponse
```

Get channels by tag

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\ChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$channel_tag_list_request = new \NexConnServerSdkPhp\Model\ChannelTagListRequest(); // \NexConnServerSdkPhp\Model\ChannelTagListRequest

try {
    $result = $apiInstance->listChannelsByTag($channel_tag_list_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChannelManagementApi->listChannelsByTag: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **channel_tag_list_request** | [**\NexConnServerSdkPhp\Model\ChannelTagListRequest**](../Model/ChannelTagListRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\ChannelTagListResponse**](../Model/ChannelTagListResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listUserChannelTags()`

```php
listUserChannelTags($user_channel_tag_list_request): \NexConnServerSdkPhp\Model\UserChannelTagListResponse
```

List user channel tags

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\ChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$user_channel_tag_list_request = new \NexConnServerSdkPhp\Model\UserChannelTagListRequest(); // \NexConnServerSdkPhp\Model\UserChannelTagListRequest

try {
    $result = $apiInstance->listUserChannelTags($user_channel_tag_list_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChannelManagementApi->listUserChannelTags: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **user_channel_tag_list_request** | [**\NexConnServerSdkPhp\Model\UserChannelTagListRequest**](../Model/UserChannelTagListRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\UserChannelTagListResponse**](../Model/UserChannelTagListResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `removeTagFromChannels()`

```php
removeTagFromChannels($channel_tag_remove_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Remove tag from channel

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\ChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$channel_tag_remove_request = new \NexConnServerSdkPhp\Model\ChannelTagRemoveRequest(); // \NexConnServerSdkPhp\Model\ChannelTagRemoveRequest

try {
    $result = $apiInstance->removeTagFromChannels($channel_tag_remove_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChannelManagementApi->removeTagFromChannels: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **channel_tag_remove_request** | [**\NexConnServerSdkPhp\Model\ChannelTagRemoveRequest**](../Model/ChannelTagRemoveRequest.md)|  | |


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

## `removeUserChannelTags()`

```php
removeUserChannelTags($user_channel_tag_remove_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Remove user channel tag

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\ChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$user_channel_tag_remove_request = new \NexConnServerSdkPhp\Model\UserChannelTagRemoveRequest(); // \NexConnServerSdkPhp\Model\UserChannelTagRemoveRequest

try {
    $result = $apiInstance->removeUserChannelTags($user_channel_tag_remove_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChannelManagementApi->removeUserChannelTags: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **user_channel_tag_remove_request** | [**\NexConnServerSdkPhp\Model\UserChannelTagRemoveRequest**](../Model/UserChannelTagRemoveRequest.md)|  | |


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

## `setChannelPin()`

```php
setChannelPin($channel_pin_set_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Pin a channel

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\ChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$channel_pin_set_request = new \NexConnServerSdkPhp\Model\ChannelPinSetRequest(); // \NexConnServerSdkPhp\Model\ChannelPinSetRequest

try {
    $result = $apiInstance->setChannelPin($channel_pin_set_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChannelManagementApi->setChannelPin: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **channel_pin_set_request** | [**\NexConnServerSdkPhp\Model\ChannelPinSetRequest**](../Model/ChannelPinSetRequest.md)|  | |


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

## `setChannelPushNotification()`

```php
setChannelPushNotification($channel_push_set_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Set channel DND

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\ChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$channel_push_set_request = new \NexConnServerSdkPhp\Model\ChannelPushSetRequest(); // \NexConnServerSdkPhp\Model\ChannelPushSetRequest

try {
    $result = $apiInstance->setChannelPushNotification($channel_push_set_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChannelManagementApi->setChannelPushNotification: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **channel_push_set_request** | [**\NexConnServerSdkPhp\Model\ChannelPushSetRequest**](../Model/ChannelPushSetRequest.md)|  | |


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

## `setChannelTypeNotification()`

```php
setChannelTypeNotification($channel_type_notification_set_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Set DND by channel type

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\ChannelManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$channel_type_notification_set_request = new \NexConnServerSdkPhp\Model\ChannelTypeNotificationSetRequest(); // \NexConnServerSdkPhp\Model\ChannelTypeNotificationSetRequest

try {
    $result = $apiInstance->setChannelTypeNotification($channel_type_notification_set_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChannelManagementApi->setChannelTypeNotification: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **channel_type_notification_set_request** | [**\NexConnServerSdkPhp\Model\ChannelTypeNotificationSetRequest**](../Model/ChannelTypeNotificationSetRequest.md)|  | |


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

# NexConnServerSdkPhp\OpenChannelParticipantsModerationApi

All requests use the primary/backup domains configured by the caller.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**addOpenChannelFreezeList()**](OpenChannelParticipantsModerationApi.md#addOpenChannelFreezeList) | **POST** /v4/open-channel/freeze-list/add | Freeze an open channel |
| [**addOpenChannelGlobalMuteList()**](OpenChannelParticipantsModerationApi.md#addOpenChannelGlobalMuteList) | **POST** /v4/open-channel/global-mute-list/add | Mute a user globally |
| [**addOpenChannelParticipantAllowedSenderList()**](OpenChannelParticipantsModerationApi.md#addOpenChannelParticipantAllowedSenderList) | **POST** /v4/open-channel/participant/allowed-sender-list/add | Add to allowed senders list |
| [**addOpenChannelParticipantBanList()**](OpenChannelParticipantsModerationApi.md#addOpenChannelParticipantBanList) | **POST** /v4/open-channel/participant/ban-list/add | Ban a participant |
| [**addOpenChannelParticipantMuteList()**](OpenChannelParticipantsModerationApi.md#addOpenChannelParticipantMuteList) | **POST** /v4/open-channel/participant/mute-list/add | Mute a participant |
| [**checkOpenChannelFreeze()**](OpenChannelParticipantsModerationApi.md#checkOpenChannelFreeze) | **POST** /v4/open-channel/freeze/check | Check open channel freeze status |
| [**checkOpenChannelParticipantsExist()**](OpenChannelParticipantsModerationApi.md#checkOpenChannelParticipantsExist) | **POST** /v4/open-channel/participant/exist | Batch check participants |
| [**getOpenChannelGlobalMuteList()**](OpenChannelParticipantsModerationApi.md#getOpenChannelGlobalMuteList) | **POST** /v4/open-channel/global-mute-list/get | List globally muted users |
| [**getOpenChannelParticipantAllowedSenderList()**](OpenChannelParticipantsModerationApi.md#getOpenChannelParticipantAllowedSenderList) | **POST** /v4/open-channel/participant/allowed-sender-list/get | Query allowed senders list |
| [**getOpenChannelParticipantBanList()**](OpenChannelParticipantsModerationApi.md#getOpenChannelParticipantBanList) | **POST** /v4/open-channel/participant/ban-list/get | List banned participants |
| [**getOpenChannelParticipantMuteList()**](OpenChannelParticipantsModerationApi.md#getOpenChannelParticipantMuteList) | **POST** /v4/open-channel/participant/mute-list/get | List muted participants |
| [**listFrozenOpenChannels()**](OpenChannelParticipantsModerationApi.md#listFrozenOpenChannels) | **POST** /v4/open-channel/freeze-list/get | List frozen open channels |
| [**listOpenChannelParticipants()**](OpenChannelParticipantsModerationApi.md#listOpenChannelParticipants) | **POST** /v4/open-channel/participant/list | List participants |
| [**removeOpenChannelFreezeList()**](OpenChannelParticipantsModerationApi.md#removeOpenChannelFreezeList) | **POST** /v4/open-channel/freeze-list/remove | Unfreeze an open channel |
| [**removeOpenChannelGlobalMuteList()**](OpenChannelParticipantsModerationApi.md#removeOpenChannelGlobalMuteList) | **POST** /v4/open-channel/global-mute-list/remove | Unmute a user globally |
| [**removeOpenChannelParticipantAllowedSenderList()**](OpenChannelParticipantsModerationApi.md#removeOpenChannelParticipantAllowedSenderList) | **POST** /v4/open-channel/participant/allowed-sender-list/remove | Remove from allowed senders list |
| [**removeOpenChannelParticipantBanList()**](OpenChannelParticipantsModerationApi.md#removeOpenChannelParticipantBanList) | **POST** /v4/open-channel/participant/ban-list/remove | Unban a participant |
| [**removeOpenChannelParticipantMuteList()**](OpenChannelParticipantsModerationApi.md#removeOpenChannelParticipantMuteList) | **POST** /v4/open-channel/participant/mute-list/remove | Unmute a participant |


## `addOpenChannelFreezeList()`

```php
addOpenChannelFreezeList($open_channel_freeze_list_update_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Freeze an open channel

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\OpenChannelParticipantsModerationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$open_channel_freeze_list_update_request = new \NexConnServerSdkPhp\Model\OpenChannelFreezeListUpdateRequest(); // \NexConnServerSdkPhp\Model\OpenChannelFreezeListUpdateRequest

try {
    $result = $apiInstance->addOpenChannelFreezeList($open_channel_freeze_list_update_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OpenChannelParticipantsModerationApi->addOpenChannelFreezeList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **open_channel_freeze_list_update_request** | [**\NexConnServerSdkPhp\Model\OpenChannelFreezeListUpdateRequest**](../Model/OpenChannelFreezeListUpdateRequest.md)|  | |


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

## `addOpenChannelGlobalMuteList()`

```php
addOpenChannelGlobalMuteList($open_channel_global_mute_list_add_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Mute a user globally

Rate limit: 100/sec. The public endpoint list currently publishes this capability as `/v4/open-channel/participant/global-mute-list/add`.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\OpenChannelParticipantsModerationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$open_channel_global_mute_list_add_request = new \NexConnServerSdkPhp\Model\OpenChannelGlobalMuteListAddRequest(); // \NexConnServerSdkPhp\Model\OpenChannelGlobalMuteListAddRequest

try {
    $result = $apiInstance->addOpenChannelGlobalMuteList($open_channel_global_mute_list_add_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OpenChannelParticipantsModerationApi->addOpenChannelGlobalMuteList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **open_channel_global_mute_list_add_request** | [**\NexConnServerSdkPhp\Model\OpenChannelGlobalMuteListAddRequest**](../Model/OpenChannelGlobalMuteListAddRequest.md)|  | |


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

## `addOpenChannelParticipantAllowedSenderList()`

```php
addOpenChannelParticipantAllowedSenderList($open_channel_allowed_sender_list_update_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Add to allowed senders list

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\OpenChannelParticipantsModerationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$open_channel_allowed_sender_list_update_request = new \NexConnServerSdkPhp\Model\OpenChannelAllowedSenderListUpdateRequest(); // \NexConnServerSdkPhp\Model\OpenChannelAllowedSenderListUpdateRequest

try {
    $result = $apiInstance->addOpenChannelParticipantAllowedSenderList($open_channel_allowed_sender_list_update_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OpenChannelParticipantsModerationApi->addOpenChannelParticipantAllowedSenderList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **open_channel_allowed_sender_list_update_request** | [**\NexConnServerSdkPhp\Model\OpenChannelAllowedSenderListUpdateRequest**](../Model/OpenChannelAllowedSenderListUpdateRequest.md)|  | |


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

## `addOpenChannelParticipantBanList()`

```php
addOpenChannelParticipantBanList($open_channel_participant_mute_list_add_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Ban a participant

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\OpenChannelParticipantsModerationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$open_channel_participant_mute_list_add_request = new \NexConnServerSdkPhp\Model\OpenChannelParticipantMuteListAddRequest(); // \NexConnServerSdkPhp\Model\OpenChannelParticipantMuteListAddRequest

try {
    $result = $apiInstance->addOpenChannelParticipantBanList($open_channel_participant_mute_list_add_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OpenChannelParticipantsModerationApi->addOpenChannelParticipantBanList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **open_channel_participant_mute_list_add_request** | [**\NexConnServerSdkPhp\Model\OpenChannelParticipantMuteListAddRequest**](../Model/OpenChannelParticipantMuteListAddRequest.md)|  | |


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

## `addOpenChannelParticipantMuteList()`

```php
addOpenChannelParticipantMuteList($open_channel_participant_mute_list_add_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Mute a participant

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\OpenChannelParticipantsModerationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$open_channel_participant_mute_list_add_request = new \NexConnServerSdkPhp\Model\OpenChannelParticipantMuteListAddRequest(); // \NexConnServerSdkPhp\Model\OpenChannelParticipantMuteListAddRequest

try {
    $result = $apiInstance->addOpenChannelParticipantMuteList($open_channel_participant_mute_list_add_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OpenChannelParticipantsModerationApi->addOpenChannelParticipantMuteList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **open_channel_participant_mute_list_add_request** | [**\NexConnServerSdkPhp\Model\OpenChannelParticipantMuteListAddRequest**](../Model/OpenChannelParticipantMuteListAddRequest.md)|  | |


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

## `checkOpenChannelFreeze()`

```php
checkOpenChannelFreeze($open_channel_freeze_check_request): \NexConnServerSdkPhp\Model\OpenChannelFreezeCheckResponse
```

Check open channel freeze status

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\OpenChannelParticipantsModerationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$open_channel_freeze_check_request = new \NexConnServerSdkPhp\Model\OpenChannelFreezeCheckRequest(); // \NexConnServerSdkPhp\Model\OpenChannelFreezeCheckRequest

try {
    $result = $apiInstance->checkOpenChannelFreeze($open_channel_freeze_check_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OpenChannelParticipantsModerationApi->checkOpenChannelFreeze: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **open_channel_freeze_check_request** | [**\NexConnServerSdkPhp\Model\OpenChannelFreezeCheckRequest**](../Model/OpenChannelFreezeCheckRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\OpenChannelFreezeCheckResponse**](../Model/OpenChannelFreezeCheckResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `checkOpenChannelParticipantsExist()`

```php
checkOpenChannelParticipantsExist($open_channel_participant_exist_request): \NexConnServerSdkPhp\Model\OpenChannelParticipantExistResponse
```

Batch check participants

Rate limit: 100/sec. The same endpoint is also documented for single-user participant checks.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\OpenChannelParticipantsModerationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$open_channel_participant_exist_request = new \NexConnServerSdkPhp\Model\OpenChannelParticipantExistRequest(); // \NexConnServerSdkPhp\Model\OpenChannelParticipantExistRequest

try {
    $result = $apiInstance->checkOpenChannelParticipantsExist($open_channel_participant_exist_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OpenChannelParticipantsModerationApi->checkOpenChannelParticipantsExist: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **open_channel_participant_exist_request** | [**\NexConnServerSdkPhp\Model\OpenChannelParticipantExistRequest**](../Model/OpenChannelParticipantExistRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\OpenChannelParticipantExistResponse**](../Model/OpenChannelParticipantExistResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getOpenChannelGlobalMuteList()`

```php
getOpenChannelGlobalMuteList(): \NexConnServerSdkPhp\Model\OpenChannelParticipantMuteListGetResponse
```

List globally muted users

Rate limit: 100/sec. The public endpoint list currently publishes this capability as `/v4/open-channel/participant/global-mute-list/get`.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\OpenChannelParticipantsModerationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getOpenChannelGlobalMuteList();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OpenChannelParticipantsModerationApi->getOpenChannelGlobalMuteList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not require a request body.


### Return type

[**\NexConnServerSdkPhp\Model\OpenChannelParticipantMuteListGetResponse**](../Model/OpenChannelParticipantMuteListGetResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getOpenChannelParticipantAllowedSenderList()`

```php
getOpenChannelParticipantAllowedSenderList($open_channel_participant_list_by_channel_request): \NexConnServerSdkPhp\Model\OpenChannelAllowedSenderListGetResponse
```

Query allowed senders list

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\OpenChannelParticipantsModerationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$open_channel_participant_list_by_channel_request = new \NexConnServerSdkPhp\Model\OpenChannelParticipantListByChannelRequest(); // \NexConnServerSdkPhp\Model\OpenChannelParticipantListByChannelRequest

try {
    $result = $apiInstance->getOpenChannelParticipantAllowedSenderList($open_channel_participant_list_by_channel_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OpenChannelParticipantsModerationApi->getOpenChannelParticipantAllowedSenderList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **open_channel_participant_list_by_channel_request** | [**\NexConnServerSdkPhp\Model\OpenChannelParticipantListByChannelRequest**](../Model/OpenChannelParticipantListByChannelRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\OpenChannelAllowedSenderListGetResponse**](../Model/OpenChannelAllowedSenderListGetResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getOpenChannelParticipantBanList()`

```php
getOpenChannelParticipantBanList($open_channel_participant_list_by_channel_request): \NexConnServerSdkPhp\Model\OpenChannelParticipantBanListGetResponse
```

List banned participants

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\OpenChannelParticipantsModerationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$open_channel_participant_list_by_channel_request = new \NexConnServerSdkPhp\Model\OpenChannelParticipantListByChannelRequest(); // \NexConnServerSdkPhp\Model\OpenChannelParticipantListByChannelRequest

try {
    $result = $apiInstance->getOpenChannelParticipantBanList($open_channel_participant_list_by_channel_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OpenChannelParticipantsModerationApi->getOpenChannelParticipantBanList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **open_channel_participant_list_by_channel_request** | [**\NexConnServerSdkPhp\Model\OpenChannelParticipantListByChannelRequest**](../Model/OpenChannelParticipantListByChannelRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\OpenChannelParticipantBanListGetResponse**](../Model/OpenChannelParticipantBanListGetResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getOpenChannelParticipantMuteList()`

```php
getOpenChannelParticipantMuteList($open_channel_participant_list_by_channel_request): \NexConnServerSdkPhp\Model\OpenChannelParticipantMuteListGetResponse
```

List muted participants

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\OpenChannelParticipantsModerationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$open_channel_participant_list_by_channel_request = new \NexConnServerSdkPhp\Model\OpenChannelParticipantListByChannelRequest(); // \NexConnServerSdkPhp\Model\OpenChannelParticipantListByChannelRequest

try {
    $result = $apiInstance->getOpenChannelParticipantMuteList($open_channel_participant_list_by_channel_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OpenChannelParticipantsModerationApi->getOpenChannelParticipantMuteList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **open_channel_participant_list_by_channel_request** | [**\NexConnServerSdkPhp\Model\OpenChannelParticipantListByChannelRequest**](../Model/OpenChannelParticipantListByChannelRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\OpenChannelParticipantMuteListGetResponse**](../Model/OpenChannelParticipantMuteListGetResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listFrozenOpenChannels()`

```php
listFrozenOpenChannels($open_channel_freeze_list_get_request): \NexConnServerSdkPhp\Model\OpenChannelFreezeListGetResponse
```

List frozen open channels

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\OpenChannelParticipantsModerationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$open_channel_freeze_list_get_request = new \NexConnServerSdkPhp\Model\OpenChannelFreezeListGetRequest(); // \NexConnServerSdkPhp\Model\OpenChannelFreezeListGetRequest

try {
    $result = $apiInstance->listFrozenOpenChannels($open_channel_freeze_list_get_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OpenChannelParticipantsModerationApi->listFrozenOpenChannels: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **open_channel_freeze_list_get_request** | [**\NexConnServerSdkPhp\Model\OpenChannelFreezeListGetRequest**](../Model/OpenChannelFreezeListGetRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\OpenChannelFreezeListGetResponse**](../Model/OpenChannelFreezeListGetResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listOpenChannelParticipants()`

```php
listOpenChannelParticipants($open_channel_participant_list_request): \NexConnServerSdkPhp\Model\OpenChannelParticipantListResponse
```

List participants

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\OpenChannelParticipantsModerationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$open_channel_participant_list_request = new \NexConnServerSdkPhp\Model\OpenChannelParticipantListRequest(); // \NexConnServerSdkPhp\Model\OpenChannelParticipantListRequest

try {
    $result = $apiInstance->listOpenChannelParticipants($open_channel_participant_list_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OpenChannelParticipantsModerationApi->listOpenChannelParticipants: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **open_channel_participant_list_request** | [**\NexConnServerSdkPhp\Model\OpenChannelParticipantListRequest**](../Model/OpenChannelParticipantListRequest.md)|  | |


### Return type

[**\NexConnServerSdkPhp\Model\OpenChannelParticipantListResponse**](../Model/OpenChannelParticipantListResponse.md)

### Authorization

[NexconnSignature](../../README.md#NexconnSignature)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `removeOpenChannelFreezeList()`

```php
removeOpenChannelFreezeList($open_channel_freeze_list_update_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Unfreeze an open channel

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\OpenChannelParticipantsModerationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$open_channel_freeze_list_update_request = new \NexConnServerSdkPhp\Model\OpenChannelFreezeListUpdateRequest(); // \NexConnServerSdkPhp\Model\OpenChannelFreezeListUpdateRequest

try {
    $result = $apiInstance->removeOpenChannelFreezeList($open_channel_freeze_list_update_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OpenChannelParticipantsModerationApi->removeOpenChannelFreezeList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **open_channel_freeze_list_update_request** | [**\NexConnServerSdkPhp\Model\OpenChannelFreezeListUpdateRequest**](../Model/OpenChannelFreezeListUpdateRequest.md)|  | |


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

## `removeOpenChannelGlobalMuteList()`

```php
removeOpenChannelGlobalMuteList($open_channel_global_mute_list_remove_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Unmute a user globally

Rate limit: 100/sec. The public endpoint list currently publishes this capability as `/v4/open-channel/participant/global-mute-list/remove`.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\OpenChannelParticipantsModerationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$open_channel_global_mute_list_remove_request = new \NexConnServerSdkPhp\Model\OpenChannelGlobalMuteListRemoveRequest(); // \NexConnServerSdkPhp\Model\OpenChannelGlobalMuteListRemoveRequest

try {
    $result = $apiInstance->removeOpenChannelGlobalMuteList($open_channel_global_mute_list_remove_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OpenChannelParticipantsModerationApi->removeOpenChannelGlobalMuteList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **open_channel_global_mute_list_remove_request** | [**\NexConnServerSdkPhp\Model\OpenChannelGlobalMuteListRemoveRequest**](../Model/OpenChannelGlobalMuteListRemoveRequest.md)|  | |


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

## `removeOpenChannelParticipantAllowedSenderList()`

```php
removeOpenChannelParticipantAllowedSenderList($open_channel_allowed_sender_list_update_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Remove from allowed senders list

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\OpenChannelParticipantsModerationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$open_channel_allowed_sender_list_update_request = new \NexConnServerSdkPhp\Model\OpenChannelAllowedSenderListUpdateRequest(); // \NexConnServerSdkPhp\Model\OpenChannelAllowedSenderListUpdateRequest

try {
    $result = $apiInstance->removeOpenChannelParticipantAllowedSenderList($open_channel_allowed_sender_list_update_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OpenChannelParticipantsModerationApi->removeOpenChannelParticipantAllowedSenderList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **open_channel_allowed_sender_list_update_request** | [**\NexConnServerSdkPhp\Model\OpenChannelAllowedSenderListUpdateRequest**](../Model/OpenChannelAllowedSenderListUpdateRequest.md)|  | |


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

## `removeOpenChannelParticipantBanList()`

```php
removeOpenChannelParticipantBanList($open_channel_participant_mute_list_remove_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Unban a participant

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\OpenChannelParticipantsModerationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$open_channel_participant_mute_list_remove_request = new \NexConnServerSdkPhp\Model\OpenChannelParticipantMuteListRemoveRequest(); // \NexConnServerSdkPhp\Model\OpenChannelParticipantMuteListRemoveRequest

try {
    $result = $apiInstance->removeOpenChannelParticipantBanList($open_channel_participant_mute_list_remove_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OpenChannelParticipantsModerationApi->removeOpenChannelParticipantBanList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **open_channel_participant_mute_list_remove_request** | [**\NexConnServerSdkPhp\Model\OpenChannelParticipantMuteListRemoveRequest**](../Model/OpenChannelParticipantMuteListRemoveRequest.md)|  | |


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

## `removeOpenChannelParticipantMuteList()`

```php
removeOpenChannelParticipantMuteList($open_channel_participant_mute_list_remove_request): \NexConnServerSdkPhp\Model\CodeOnlyResponse
```

Unmute a participant

Rate limit: 100/sec.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: NexconnSignature
$config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKey('App-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = NexConnServerSdkPhp\Configuration::getDefaultConfiguration()->setApiKeyPrefix('App-Key', 'Bearer');


$apiInstance = new NexConnServerSdkPhp\Api\OpenChannelParticipantsModerationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

$open_channel_participant_mute_list_remove_request = new \NexConnServerSdkPhp\Model\OpenChannelParticipantMuteListRemoveRequest(); // \NexConnServerSdkPhp\Model\OpenChannelParticipantMuteListRemoveRequest

try {
    $result = $apiInstance->removeOpenChannelParticipantMuteList($open_channel_participant_mute_list_remove_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OpenChannelParticipantsModerationApi->removeOpenChannelParticipantMuteList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **open_channel_participant_mute_list_remove_request** | [**\NexConnServerSdkPhp\Model\OpenChannelParticipantMuteListRemoveRequest**](../Model/OpenChannelParticipantMuteListRemoveRequest.md)|  | |


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

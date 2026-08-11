# InvoicePDFs\ApiKeysApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createApiKey()**](ApiKeysApi.md#createApiKey) | **POST** /api/v1/api-keys | Create Api Key |
| [**getApiKey()**](ApiKeysApi.md#getApiKey) | **GET** /api/v1/api-keys/{api_key_id} | Get Api Key |
| [**listApiKeys()**](ApiKeysApi.md#listApiKeys) | **GET** /api/v1/api-keys | List Api Keys |
| [**revokeApiKey()**](ApiKeysApi.md#revokeApiKey) | **DELETE** /api/v1/api-keys/{api_key_id} | Revoke Api Key |
| [**rotateApiKey()**](ApiKeysApi.md#rotateApiKey) | **POST** /api/v1/api-keys/{api_key_id}/rotate | Rotate Api Key |
| [**updateApiKey()**](ApiKeysApi.md#updateApiKey) | **PATCH** /api/v1/api-keys/{api_key_id} | Update Api Key |


## `createApiKey()`

```php
createApiKey($api_key_create_request): \InvoicePDFs\Model\ApiKeyCreateResponse
```

Create Api Key

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\ApiKeysApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$api_key_create_request = new \InvoicePDFs\Model\ApiKeyCreateRequest(); // \InvoicePDFs\Model\ApiKeyCreateRequest

try {
    $result = $apiInstance->createApiKey($api_key_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ApiKeysApi->createApiKey: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **api_key_create_request** | [**\InvoicePDFs\Model\ApiKeyCreateRequest**](../Model/ApiKeyCreateRequest.md)|  | |

### Return type

[**\InvoicePDFs\Model\ApiKeyCreateResponse**](../Model/ApiKeyCreateResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getApiKey()`

```php
getApiKey($api_key_id): \InvoicePDFs\Model\ApiKeyDetailResponse
```

Get Api Key

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\ApiKeysApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$api_key_id = 'api_key_id_example'; // string

try {
    $result = $apiInstance->getApiKey($api_key_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ApiKeysApi->getApiKey: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **api_key_id** | **string**|  | |

### Return type

[**\InvoicePDFs\Model\ApiKeyDetailResponse**](../Model/ApiKeyDetailResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listApiKeys()`

```php
listApiKeys(): \InvoicePDFs\Model\ApiKeyListResponse
```

List Api Keys

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\ApiKeysApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->listApiKeys();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ApiKeysApi->listApiKeys: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\InvoicePDFs\Model\ApiKeyListResponse**](../Model/ApiKeyListResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `revokeApiKey()`

```php
revokeApiKey($api_key_id): \InvoicePDFs\Model\ApiKeyRevokeResponse
```

Revoke Api Key

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\ApiKeysApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$api_key_id = 'api_key_id_example'; // string

try {
    $result = $apiInstance->revokeApiKey($api_key_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ApiKeysApi->revokeApiKey: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **api_key_id** | **string**|  | |

### Return type

[**\InvoicePDFs\Model\ApiKeyRevokeResponse**](../Model/ApiKeyRevokeResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `rotateApiKey()`

```php
rotateApiKey($api_key_id): \InvoicePDFs\Model\ApiKeyRotateResponse
```

Rotate Api Key

Revoke the existing key and create a new one with the same name.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\ApiKeysApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$api_key_id = 'api_key_id_example'; // string

try {
    $result = $apiInstance->rotateApiKey($api_key_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ApiKeysApi->rotateApiKey: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **api_key_id** | **string**|  | |

### Return type

[**\InvoicePDFs\Model\ApiKeyRotateResponse**](../Model/ApiKeyRotateResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateApiKey()`

```php
updateApiKey($api_key_id, $api_key_patch_request): \InvoicePDFs\Model\ApiKeyDetailResponse
```

Update Api Key

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\ApiKeysApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$api_key_id = 'api_key_id_example'; // string
$api_key_patch_request = new \InvoicePDFs\Model\ApiKeyPatchRequest(); // \InvoicePDFs\Model\ApiKeyPatchRequest

try {
    $result = $apiInstance->updateApiKey($api_key_id, $api_key_patch_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ApiKeysApi->updateApiKey: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **api_key_id** | **string**|  | |
| **api_key_patch_request** | [**\InvoicePDFs\Model\ApiKeyPatchRequest**](../Model/ApiKeyPatchRequest.md)|  | |

### Return type

[**\InvoicePDFs\Model\ApiKeyDetailResponse**](../Model/ApiKeyDetailResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

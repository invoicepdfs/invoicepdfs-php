# OpenAPI\Client\ApiKeysApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createApiKeyApiV1ApiKeysPost()**](ApiKeysApi.md#createApiKeyApiV1ApiKeysPost) | **POST** /api/v1/api-keys | Create Api Key |
| [**getApiKeyApiV1ApiKeysApiKeyIdGet()**](ApiKeysApi.md#getApiKeyApiV1ApiKeysApiKeyIdGet) | **GET** /api/v1/api-keys/{api_key_id} | Get Api Key |
| [**listApiKeysApiV1ApiKeysGet()**](ApiKeysApi.md#listApiKeysApiV1ApiKeysGet) | **GET** /api/v1/api-keys | List Api Keys |
| [**patchApiKeyApiV1ApiKeysApiKeyIdPatch()**](ApiKeysApi.md#patchApiKeyApiV1ApiKeysApiKeyIdPatch) | **PATCH** /api/v1/api-keys/{api_key_id} | Patch Api Key |
| [**revokeApiKeyApiV1ApiKeysApiKeyIdDelete()**](ApiKeysApi.md#revokeApiKeyApiV1ApiKeysApiKeyIdDelete) | **DELETE** /api/v1/api-keys/{api_key_id} | Revoke Api Key |
| [**rotateApiKeyApiV1ApiKeysApiKeyIdRotatePost()**](ApiKeysApi.md#rotateApiKeyApiV1ApiKeysApiKeyIdRotatePost) | **POST** /api/v1/api-keys/{api_key_id}/rotate | Rotate Api Key |


## `createApiKeyApiV1ApiKeysPost()`

```php
createApiKeyApiV1ApiKeysPost($api_key_create_request): \OpenAPI\Client\Model\ApiKeyCreateResponse
```

Create Api Key

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ApiKeysApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$api_key_create_request = new \OpenAPI\Client\Model\ApiKeyCreateRequest(); // \OpenAPI\Client\Model\ApiKeyCreateRequest

try {
    $result = $apiInstance->createApiKeyApiV1ApiKeysPost($api_key_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ApiKeysApi->createApiKeyApiV1ApiKeysPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **api_key_create_request** | [**\OpenAPI\Client\Model\ApiKeyCreateRequest**](../Model/ApiKeyCreateRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\ApiKeyCreateResponse**](../Model/ApiKeyCreateResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getApiKeyApiV1ApiKeysApiKeyIdGet()`

```php
getApiKeyApiV1ApiKeysApiKeyIdGet($api_key_id): \OpenAPI\Client\Model\ApiKeyDetailResponse
```

Get Api Key

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ApiKeysApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$api_key_id = 'api_key_id_example'; // string

try {
    $result = $apiInstance->getApiKeyApiV1ApiKeysApiKeyIdGet($api_key_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ApiKeysApi->getApiKeyApiV1ApiKeysApiKeyIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **api_key_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\ApiKeyDetailResponse**](../Model/ApiKeyDetailResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listApiKeysApiV1ApiKeysGet()`

```php
listApiKeysApiV1ApiKeysGet(): \OpenAPI\Client\Model\ApiKeyListResponse
```

List Api Keys

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ApiKeysApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->listApiKeysApiV1ApiKeysGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ApiKeysApi->listApiKeysApiV1ApiKeysGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\ApiKeyListResponse**](../Model/ApiKeyListResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `patchApiKeyApiV1ApiKeysApiKeyIdPatch()`

```php
patchApiKeyApiV1ApiKeysApiKeyIdPatch($api_key_id, $api_key_patch_request): \OpenAPI\Client\Model\ApiKeyDetailResponse
```

Patch Api Key

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ApiKeysApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$api_key_id = 'api_key_id_example'; // string
$api_key_patch_request = new \OpenAPI\Client\Model\ApiKeyPatchRequest(); // \OpenAPI\Client\Model\ApiKeyPatchRequest

try {
    $result = $apiInstance->patchApiKeyApiV1ApiKeysApiKeyIdPatch($api_key_id, $api_key_patch_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ApiKeysApi->patchApiKeyApiV1ApiKeysApiKeyIdPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **api_key_id** | **string**|  | |
| **api_key_patch_request** | [**\OpenAPI\Client\Model\ApiKeyPatchRequest**](../Model/ApiKeyPatchRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\ApiKeyDetailResponse**](../Model/ApiKeyDetailResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `revokeApiKeyApiV1ApiKeysApiKeyIdDelete()`

```php
revokeApiKeyApiV1ApiKeysApiKeyIdDelete($api_key_id): \OpenAPI\Client\Model\ApiKeyRevokeResponse
```

Revoke Api Key

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ApiKeysApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$api_key_id = 'api_key_id_example'; // string

try {
    $result = $apiInstance->revokeApiKeyApiV1ApiKeysApiKeyIdDelete($api_key_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ApiKeysApi->revokeApiKeyApiV1ApiKeysApiKeyIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **api_key_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\ApiKeyRevokeResponse**](../Model/ApiKeyRevokeResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `rotateApiKeyApiV1ApiKeysApiKeyIdRotatePost()`

```php
rotateApiKeyApiV1ApiKeysApiKeyIdRotatePost($api_key_id): \OpenAPI\Client\Model\ApiKeyRotateResponse
```

Rotate Api Key

Revoke the existing key and create a new one with the same name.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ApiKeysApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$api_key_id = 'api_key_id_example'; // string

try {
    $result = $apiInstance->rotateApiKeyApiV1ApiKeysApiKeyIdRotatePost($api_key_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ApiKeysApi->rotateApiKeyApiV1ApiKeysApiKeyIdRotatePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **api_key_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\ApiKeyRotateResponse**](../Model/ApiKeyRotateResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

# OpenAPI\Client\ImportsApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**cancelImportApiV1ImportsImportIdCancelPost()**](ImportsApi.md#cancelImportApiV1ImportsImportIdCancelPost) | **POST** /api/v1/imports/{import_id}/cancel | Cancel Import |
| [**confirmImportApiV1ImportsImportIdConfirmPost()**](ImportsApi.md#confirmImportApiV1ImportsImportIdConfirmPost) | **POST** /api/v1/imports/{import_id}/confirm | Confirm Import |
| [**createImportApiV1ImportsPost()**](ImportsApi.md#createImportApiV1ImportsPost) | **POST** /api/v1/imports | Create Import |
| [**getImportApiV1ImportsImportIdGet()**](ImportsApi.md#getImportApiV1ImportsImportIdGet) | **GET** /api/v1/imports/{import_id} | Get Import |


## `cancelImportApiV1ImportsImportIdCancelPost()`

```php
cancelImportApiV1ImportsImportIdCancelPost($import_id): \OpenAPI\Client\Model\ImportResponse
```

Cancel Import

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ImportsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$import_id = 'import_id_example'; // string

try {
    $result = $apiInstance->cancelImportApiV1ImportsImportIdCancelPost($import_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ImportsApi->cancelImportApiV1ImportsImportIdCancelPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **import_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\ImportResponse**](../Model/ImportResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `confirmImportApiV1ImportsImportIdConfirmPost()`

```php
confirmImportApiV1ImportsImportIdConfirmPost($import_id): \OpenAPI\Client\Model\ImportResponse
```

Confirm Import

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ImportsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$import_id = 'import_id_example'; // string

try {
    $result = $apiInstance->confirmImportApiV1ImportsImportIdConfirmPost($import_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ImportsApi->confirmImportApiV1ImportsImportIdConfirmPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **import_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\ImportResponse**](../Model/ImportResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createImportApiV1ImportsPost()`

```php
createImportApiV1ImportsPost($import_create_request): \OpenAPI\Client\Model\ImportResponse
```

Create Import

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ImportsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$import_create_request = new \OpenAPI\Client\Model\ImportCreateRequest(); // \OpenAPI\Client\Model\ImportCreateRequest

try {
    $result = $apiInstance->createImportApiV1ImportsPost($import_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ImportsApi->createImportApiV1ImportsPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **import_create_request** | [**\OpenAPI\Client\Model\ImportCreateRequest**](../Model/ImportCreateRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\ImportResponse**](../Model/ImportResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getImportApiV1ImportsImportIdGet()`

```php
getImportApiV1ImportsImportIdGet($import_id): \OpenAPI\Client\Model\ImportResponse
```

Get Import

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ImportsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$import_id = 'import_id_example'; // string

try {
    $result = $apiInstance->getImportApiV1ImportsImportIdGet($import_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ImportsApi->getImportApiV1ImportsImportIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **import_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\ImportResponse**](../Model/ImportResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

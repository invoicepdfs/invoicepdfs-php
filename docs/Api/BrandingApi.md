# OpenAPI\Client\BrandingApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**deleteLogoApiV1BrandingLogoDelete()**](BrandingApi.md#deleteLogoApiV1BrandingLogoDelete) | **DELETE** /api/v1/branding/logo | Delete Logo |
| [**getBrandingApiV1BrandingGet()**](BrandingApi.md#getBrandingApiV1BrandingGet) | **GET** /api/v1/branding | Get Branding |
| [**updateBrandingApiV1BrandingPut()**](BrandingApi.md#updateBrandingApiV1BrandingPut) | **PUT** /api/v1/branding | Update Branding |
| [**uploadLogoApiV1BrandingLogoPost()**](BrandingApi.md#uploadLogoApiV1BrandingLogoPost) | **POST** /api/v1/branding/logo | Upload Logo |


## `deleteLogoApiV1BrandingLogoDelete()`

```php
deleteLogoApiV1BrandingLogoDelete(): \OpenAPI\Client\Model\SimpleBoolResponse
```

Delete Logo

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BrandingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->deleteLogoApiV1BrandingLogoDelete();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BrandingApi->deleteLogoApiV1BrandingLogoDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\SimpleBoolResponse**](../Model/SimpleBoolResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getBrandingApiV1BrandingGet()`

```php
getBrandingApiV1BrandingGet(): \OpenAPI\Client\Model\BrandingResponse
```

Get Branding

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BrandingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getBrandingApiV1BrandingGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BrandingApi->getBrandingApiV1BrandingGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\BrandingResponse**](../Model/BrandingResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateBrandingApiV1BrandingPut()`

```php
updateBrandingApiV1BrandingPut($branding_update_request): \OpenAPI\Client\Model\BrandingResponse
```

Update Branding

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BrandingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$branding_update_request = new \OpenAPI\Client\Model\BrandingUpdateRequest(); // \OpenAPI\Client\Model\BrandingUpdateRequest

try {
    $result = $apiInstance->updateBrandingApiV1BrandingPut($branding_update_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BrandingApi->updateBrandingApiV1BrandingPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **branding_update_request** | [**\OpenAPI\Client\Model\BrandingUpdateRequest**](../Model/BrandingUpdateRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\BrandingResponse**](../Model/BrandingResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `uploadLogoApiV1BrandingLogoPost()`

```php
uploadLogoApiV1BrandingLogoPost($file): \OpenAPI\Client\Model\BrandingResponse
```

Upload Logo

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BrandingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$file = "/path/to/file.txt"; // \SplFileObject

try {
    $result = $apiInstance->uploadLogoApiV1BrandingLogoPost($file);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BrandingApi->uploadLogoApiV1BrandingLogoPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **file** | **\SplFileObject****\SplFileObject**|  | |

### Return type

[**\OpenAPI\Client\Model\BrandingResponse**](../Model/BrandingResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `multipart/form-data`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

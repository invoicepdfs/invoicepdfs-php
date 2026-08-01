# OpenAPI\Client\RendersApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**downloadRenderApiV1RendersRenderIdDownloadGet()**](RendersApi.md#downloadRenderApiV1RendersRenderIdDownloadGet) | **GET** /api/v1/renders/{render_id}/download | Download Render |
| [**getRenderApiV1RendersRenderIdGet()**](RendersApi.md#getRenderApiV1RendersRenderIdGet) | **GET** /api/v1/renders/{render_id} | Get Render |


## `downloadRenderApiV1RendersRenderIdDownloadGet()`

```php
downloadRenderApiV1RendersRenderIdDownloadGet($render_id): \SplFileObject
```

Download Render

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\RendersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$render_id = 'render_id_example'; // string

try {
    $result = $apiInstance->downloadRenderApiV1RendersRenderIdDownloadGet($render_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RendersApi->downloadRenderApiV1RendersRenderIdDownloadGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **render_id** | **string**|  | |

### Return type

**\SplFileObject**

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/pdf`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getRenderApiV1RendersRenderIdGet()`

```php
getRenderApiV1RendersRenderIdGet($render_id): array<string,mixed>
```

Get Render

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\RendersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$render_id = 'render_id_example'; // string

try {
    $result = $apiInstance->getRenderApiV1RendersRenderIdGet($render_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RendersApi->getRenderApiV1RendersRenderIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **render_id** | **string**|  | |

### Return type

**array<string,mixed>**

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

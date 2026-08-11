# InvoicePDFs\RendersApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**downloadRender()**](RendersApi.md#downloadRender) | **GET** /api/v1/renders/{render_id}/download | Download Render |
| [**getRender()**](RendersApi.md#getRender) | **GET** /api/v1/renders/{render_id} | Get Render |


## `downloadRender()`

```php
downloadRender($render_id): \SplFileObject
```

Download Render

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\RendersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$render_id = 'render_id_example'; // string

try {
    $result = $apiInstance->downloadRender($render_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RendersApi->downloadRender: ', $e->getMessage(), PHP_EOL;
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

## `getRender()`

```php
getRender($render_id): array<string,mixed>
```

Get Render

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\RendersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$render_id = 'render_id_example'; // string

try {
    $result = $apiInstance->getRender($render_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RendersApi->getRender: ', $e->getMessage(), PHP_EOL;
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

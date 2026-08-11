# InvoicePDFs\HealthApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getHealth()**](HealthApi.md#getHealth) | **GET** /health | Get Health |
| [**getReadiness()**](HealthApi.md#getReadiness) | **GET** /ready | Get Readiness |
| [**getVersion()**](HealthApi.md#getVersion) | **GET** /version | Get Version |


## `getHealth()`

```php
getHealth(): \InvoicePDFs\Model\HealthResponse
```

Get Health

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new InvoicePDFs\Api\HealthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->getHealth();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling HealthApi->getHealth: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\InvoicePDFs\Model\HealthResponse**](../Model/HealthResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getReadiness()`

```php
getReadiness(): \InvoicePDFs\Model\ReadyResponse
```

Get Readiness

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new InvoicePDFs\Api\HealthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->getReadiness();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling HealthApi->getReadiness: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\InvoicePDFs\Model\ReadyResponse**](../Model/ReadyResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getVersion()`

```php
getVersion(): \InvoicePDFs\Model\VersionResponse
```

Get Version

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new InvoicePDFs\Api\HealthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->getVersion();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling HealthApi->getVersion: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\InvoicePDFs\Model\VersionResponse**](../Model/VersionResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

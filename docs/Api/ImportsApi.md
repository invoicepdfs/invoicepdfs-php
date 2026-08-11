# InvoicePDFs\ImportsApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**cancelImport()**](ImportsApi.md#cancelImport) | **POST** /api/v1/imports/{import_id}/cancel | Cancel Import |
| [**confirmImport()**](ImportsApi.md#confirmImport) | **POST** /api/v1/imports/{import_id}/confirm | Confirm Import |
| [**createImport()**](ImportsApi.md#createImport) | **POST** /api/v1/imports | Create Import |
| [**getImport()**](ImportsApi.md#getImport) | **GET** /api/v1/imports/{import_id} | Get Import |


## `cancelImport()`

```php
cancelImport($import_id): \InvoicePDFs\Model\ImportResponse
```

Cancel Import

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\ImportsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$import_id = 'import_id_example'; // string

try {
    $result = $apiInstance->cancelImport($import_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ImportsApi->cancelImport: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **import_id** | **string**|  | |

### Return type

[**\InvoicePDFs\Model\ImportResponse**](../Model/ImportResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `confirmImport()`

```php
confirmImport($import_id): \InvoicePDFs\Model\ImportResponse
```

Confirm Import

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\ImportsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$import_id = 'import_id_example'; // string

try {
    $result = $apiInstance->confirmImport($import_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ImportsApi->confirmImport: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **import_id** | **string**|  | |

### Return type

[**\InvoicePDFs\Model\ImportResponse**](../Model/ImportResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createImport()`

```php
createImport($import_create_request): \InvoicePDFs\Model\ImportResponse
```

Create Import

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\ImportsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$import_create_request = new \InvoicePDFs\Model\ImportCreateRequest(); // \InvoicePDFs\Model\ImportCreateRequest

try {
    $result = $apiInstance->createImport($import_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ImportsApi->createImport: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **import_create_request** | [**\InvoicePDFs\Model\ImportCreateRequest**](../Model/ImportCreateRequest.md)|  | |

### Return type

[**\InvoicePDFs\Model\ImportResponse**](../Model/ImportResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getImport()`

```php
getImport($import_id): \InvoicePDFs\Model\ImportResponse
```

Get Import

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\ImportsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$import_id = 'import_id_example'; // string

try {
    $result = $apiInstance->getImport($import_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ImportsApi->getImport: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **import_id** | **string**|  | |

### Return type

[**\InvoicePDFs\Model\ImportResponse**](../Model/ImportResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

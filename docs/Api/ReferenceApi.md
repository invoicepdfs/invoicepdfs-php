# OpenAPI\Client\ReferenceApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**listCountriesApiV1ReferenceCountriesGet()**](ReferenceApi.md#listCountriesApiV1ReferenceCountriesGet) | **GET** /api/v1/reference/countries | List Countries |
| [**listCurrenciesApiV1ReferenceCurrenciesGet()**](ReferenceApi.md#listCurrenciesApiV1ReferenceCurrenciesGet) | **GET** /api/v1/reference/currencies | List Currencies |
| [**listDocumentTypesApiV1ReferenceDocumentTypesGet()**](ReferenceApi.md#listDocumentTypesApiV1ReferenceDocumentTypesGet) | **GET** /api/v1/reference/document-types | List Document Types |
| [**listLocalesApiV1ReferenceLocalesGet()**](ReferenceApi.md#listLocalesApiV1ReferenceLocalesGet) | **GET** /api/v1/reference/locales | List Locales |
| [**listPageSizesApiV1ReferencePageSizesGet()**](ReferenceApi.md#listPageSizesApiV1ReferencePageSizesGet) | **GET** /api/v1/reference/page-sizes | List Page Sizes |
| [**listTimezonesApiV1ReferenceTimezonesGet()**](ReferenceApi.md#listTimezonesApiV1ReferenceTimezonesGet) | **GET** /api/v1/reference/timezones | List Timezones |


## `listCountriesApiV1ReferenceCountriesGet()`

```php
listCountriesApiV1ReferenceCountriesGet(): array<string,mixed>
```

List Countries

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ReferenceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->listCountriesApiV1ReferenceCountriesGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReferenceApi->listCountriesApiV1ReferenceCountriesGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

**array<string,mixed>**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listCurrenciesApiV1ReferenceCurrenciesGet()`

```php
listCurrenciesApiV1ReferenceCurrenciesGet(): array<string,mixed>
```

List Currencies

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ReferenceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->listCurrenciesApiV1ReferenceCurrenciesGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReferenceApi->listCurrenciesApiV1ReferenceCurrenciesGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

**array<string,mixed>**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listDocumentTypesApiV1ReferenceDocumentTypesGet()`

```php
listDocumentTypesApiV1ReferenceDocumentTypesGet(): array<string,mixed>
```

List Document Types

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ReferenceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->listDocumentTypesApiV1ReferenceDocumentTypesGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReferenceApi->listDocumentTypesApiV1ReferenceDocumentTypesGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

**array<string,mixed>**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listLocalesApiV1ReferenceLocalesGet()`

```php
listLocalesApiV1ReferenceLocalesGet(): array<string,mixed>
```

List Locales

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ReferenceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->listLocalesApiV1ReferenceLocalesGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReferenceApi->listLocalesApiV1ReferenceLocalesGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

**array<string,mixed>**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listPageSizesApiV1ReferencePageSizesGet()`

```php
listPageSizesApiV1ReferencePageSizesGet(): array<string,mixed>
```

List Page Sizes

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ReferenceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->listPageSizesApiV1ReferencePageSizesGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReferenceApi->listPageSizesApiV1ReferencePageSizesGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

**array<string,mixed>**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listTimezonesApiV1ReferenceTimezonesGet()`

```php
listTimezonesApiV1ReferenceTimezonesGet(): array<string,mixed>
```

List Timezones

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ReferenceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->listTimezonesApiV1ReferenceTimezonesGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReferenceApi->listTimezonesApiV1ReferenceTimezonesGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

**array<string,mixed>**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

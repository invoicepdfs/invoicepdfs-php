# InvoicePDFs\ReferenceApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**listCountries()**](ReferenceApi.md#listCountries) | **GET** /api/v1/reference/countries | List Countries |
| [**listCurrencies()**](ReferenceApi.md#listCurrencies) | **GET** /api/v1/reference/currencies | List Currencies |
| [**listDocumentTypes()**](ReferenceApi.md#listDocumentTypes) | **GET** /api/v1/reference/document-types | List Document Types |
| [**listLocales()**](ReferenceApi.md#listLocales) | **GET** /api/v1/reference/locales | List Locales |
| [**listPageSizes()**](ReferenceApi.md#listPageSizes) | **GET** /api/v1/reference/page-sizes | List Page Sizes |
| [**listTimezones()**](ReferenceApi.md#listTimezones) | **GET** /api/v1/reference/timezones | List Timezones |


## `listCountries()`

```php
listCountries(): array<string,mixed>
```

List Countries

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new InvoicePDFs\Api\ReferenceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->listCountries();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReferenceApi->listCountries: ', $e->getMessage(), PHP_EOL;
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

## `listCurrencies()`

```php
listCurrencies(): array<string,mixed>
```

List Currencies

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new InvoicePDFs\Api\ReferenceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->listCurrencies();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReferenceApi->listCurrencies: ', $e->getMessage(), PHP_EOL;
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

## `listDocumentTypes()`

```php
listDocumentTypes(): array<string,mixed>
```

List Document Types

List every supported document type with the metadata a client needs to build a type-aware create form: the number prefix, whether it is payable / takes a source document / supports a reason, which line-item shape it uses (``standard`` = priced, ``shipped`` = quantities only), and the lifecycle actions available to it.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new InvoicePDFs\Api\ReferenceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->listDocumentTypes();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReferenceApi->listDocumentTypes: ', $e->getMessage(), PHP_EOL;
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

## `listLocales()`

```php
listLocales(): array<string,mixed>
```

List Locales

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new InvoicePDFs\Api\ReferenceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->listLocales();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReferenceApi->listLocales: ', $e->getMessage(), PHP_EOL;
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

## `listPageSizes()`

```php
listPageSizes(): array<string,mixed>
```

List Page Sizes

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new InvoicePDFs\Api\ReferenceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->listPageSizes();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReferenceApi->listPageSizes: ', $e->getMessage(), PHP_EOL;
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

## `listTimezones()`

```php
listTimezones(): array<string,mixed>
```

List Timezones

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new InvoicePDFs\Api\ReferenceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->listTimezones();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReferenceApi->listTimezones: ', $e->getMessage(), PHP_EOL;
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

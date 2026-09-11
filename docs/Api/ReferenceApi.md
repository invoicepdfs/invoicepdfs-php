# InvoicePDFs\ReferenceApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**listCountries()**](ReferenceApi.md#listCountries) | **GET** /api/v1/reference/countries | List Countries |
| [**listCurrencies()**](ReferenceApi.md#listCurrencies) | **GET** /api/v1/reference/currencies | List Currencies |
| [**listDocumentTypes()**](ReferenceApi.md#listDocumentTypes) | **GET** /api/v1/reference/document-types | List Document Types |
| [**listLocales()**](ReferenceApi.md#listLocales) | **GET** /api/v1/reference/locales | List Locales |
| [**listPageSizes()**](ReferenceApi.md#listPageSizes) | **GET** /api/v1/reference/page-sizes | List Page Sizes |
| [**listTaxCategories()**](ReferenceApi.md#listTaxCategories) | **GET** /api/v1/reference/tax-categories | List Tax Categories |
| [**listTaxSchemes()**](ReferenceApi.md#listTaxSchemes) | **GET** /api/v1/reference/tax-schemes | List Tax Schemes |
| [**listTimezones()**](ReferenceApi.md#listTimezones) | **GET** /api/v1/reference/timezones | List Timezones |
| [**listUnitCodes()**](ReferenceApi.md#listUnitCodes) | **GET** /api/v1/reference/unit-codes | List Unit Codes |


## `listCountries()`

```php
listCountries(): \InvoicePDFs\Model\CountriesListResponse
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

[**\InvoicePDFs\Model\CountriesListResponse**](../Model/CountriesListResponse.md)

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
listCurrencies(): \InvoicePDFs\Model\CurrenciesListResponse
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

[**\InvoicePDFs\Model\CurrenciesListResponse**](../Model/CurrenciesListResponse.md)

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
listDocumentTypes(): \InvoicePDFs\Model\DocumentTypesListResponse
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

[**\InvoicePDFs\Model\DocumentTypesListResponse**](../Model/DocumentTypesListResponse.md)

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
listLocales(): \InvoicePDFs\Model\LocalesListResponse
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

[**\InvoicePDFs\Model\LocalesListResponse**](../Model/LocalesListResponse.md)

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
listPageSizes(): \InvoicePDFs\Model\PageSizesListResponse
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

[**\InvoicePDFs\Model\PageSizesListResponse**](../Model/PageSizesListResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listTaxCategories()`

```php
listTaxCategories(): \InvoicePDFs\Model\CodeListResponse
```

List Tax Categories

UNCL5305, in full — the VAT treatment of a line, which its rate does not say.  Two lines at 0% may be zero-rated, exempt, reverse-charge or outside scope, and EN 16931 puts them in separate VAT breakdown groups with different mandatory fields. Exhaustive: a category outside this list is wrong.

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
    $result = $apiInstance->listTaxCategories();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReferenceApi->listTaxCategories: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\InvoicePDFs\Model\CodeListResponse**](../Model/CodeListResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listTaxSchemes()`

```php
listTaxSchemes(): \InvoicePDFs\Model\CodeListResponse
```

List Tax Schemes

UNCL5153 — which tax regime a document is issued under, one per document.  `VAT` is the only member an e-invoice can carry; the others exist so a caller can state that their tax is *not* VAT and be told so, rather than have VAT assumed on their behalf. There is no default: a PDF does not need a scheme, and guessing one puts a claim in a document a tax authority reads that the caller never made.

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
    $result = $apiInstance->listTaxSchemes();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReferenceApi->listTaxSchemes: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\InvoicePDFs\Model\CodeListResponse**](../Model/CodeListResponse.md)

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
listTimezones(): \InvoicePDFs\Model\TimezonesListResponse
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

[**\InvoicePDFs\Model\TimezonesListResponse**](../Model/TimezonesListResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listUnitCodes()`

```php
listUnitCodes(): \InvoicePDFs\Model\CodeListResponse
```

List Unit Codes

UN/ECE Recommendation 20 — the unit a line item is measured in.  A **shortlist**: twenty-one of hundreds, ordered by how often an invoice needs them. `exhaustive` is false, and it means it — `unit_code` accepts any value, nothing validates against this list, and an uncommon code is still correct. Offered because the field takes a code rather than the printed label: mapping \"hrs\" to HUR is an inference that is right until it silently is not, and the audience for the result is a tax authority.

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
    $result = $apiInstance->listUnitCodes();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReferenceApi->listUnitCodes: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\InvoicePDFs\Model\CodeListResponse**](../Model/CodeListResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

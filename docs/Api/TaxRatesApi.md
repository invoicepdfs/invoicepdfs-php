# InvoicePDFs\TaxRatesApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createTaxRate()**](TaxRatesApi.md#createTaxRate) | **POST** /api/v1/tax-rates | Create Tax Rate |
| [**deleteTaxRate()**](TaxRatesApi.md#deleteTaxRate) | **DELETE** /api/v1/tax-rates/{tax_rate_id} | Delete Tax Rate |
| [**getTaxRate()**](TaxRatesApi.md#getTaxRate) | **GET** /api/v1/tax-rates/{tax_rate_id} | Get Tax Rate |
| [**listTaxRates()**](TaxRatesApi.md#listTaxRates) | **GET** /api/v1/tax-rates | List Tax Rates |
| [**updateTaxRate()**](TaxRatesApi.md#updateTaxRate) | **PATCH** /api/v1/tax-rates/{tax_rate_id} | Update Tax Rate |


## `createTaxRate()`

```php
createTaxRate($tax_rate_create_request): \InvoicePDFs\Model\TaxRateResponse
```

Create Tax Rate

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\TaxRatesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tax_rate_create_request = new \InvoicePDFs\Model\TaxRateCreateRequest(); // \InvoicePDFs\Model\TaxRateCreateRequest

try {
    $result = $apiInstance->createTaxRate($tax_rate_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TaxRatesApi->createTaxRate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tax_rate_create_request** | [**\InvoicePDFs\Model\TaxRateCreateRequest**](../Model/TaxRateCreateRequest.md)|  | |

### Return type

[**\InvoicePDFs\Model\TaxRateResponse**](../Model/TaxRateResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteTaxRate()`

```php
deleteTaxRate($tax_rate_id): \InvoicePDFs\Model\SimpleBoolResponse
```

Delete Tax Rate

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\TaxRatesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tax_rate_id = 'tax_rate_id_example'; // string

try {
    $result = $apiInstance->deleteTaxRate($tax_rate_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TaxRatesApi->deleteTaxRate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tax_rate_id** | **string**|  | |

### Return type

[**\InvoicePDFs\Model\SimpleBoolResponse**](../Model/SimpleBoolResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getTaxRate()`

```php
getTaxRate($tax_rate_id): \InvoicePDFs\Model\TaxRateResponse
```

Get Tax Rate

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\TaxRatesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tax_rate_id = 'tax_rate_id_example'; // string

try {
    $result = $apiInstance->getTaxRate($tax_rate_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TaxRatesApi->getTaxRate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tax_rate_id** | **string**|  | |

### Return type

[**\InvoicePDFs\Model\TaxRateResponse**](../Model/TaxRateResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listTaxRates()`

```php
listTaxRates($limit, $cursor): \InvoicePDFs\Model\TaxRatesListResponse
```

List Tax Rates

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\TaxRatesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$limit = 50; // int
$cursor = 'cursor_example'; // string

try {
    $result = $apiInstance->listTaxRates($limit, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TaxRatesApi->listTaxRates: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **limit** | **int**|  | [optional] [default to 50] |
| **cursor** | **string**|  | [optional] |

### Return type

[**\InvoicePDFs\Model\TaxRatesListResponse**](../Model/TaxRatesListResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateTaxRate()`

```php
updateTaxRate($tax_rate_id, $tax_rate_patch_request): \InvoicePDFs\Model\TaxRateResponse
```

Update Tax Rate

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\TaxRatesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tax_rate_id = 'tax_rate_id_example'; // string
$tax_rate_patch_request = new \InvoicePDFs\Model\TaxRatePatchRequest(); // \InvoicePDFs\Model\TaxRatePatchRequest

try {
    $result = $apiInstance->updateTaxRate($tax_rate_id, $tax_rate_patch_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TaxRatesApi->updateTaxRate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tax_rate_id** | **string**|  | |
| **tax_rate_patch_request** | [**\InvoicePDFs\Model\TaxRatePatchRequest**](../Model/TaxRatePatchRequest.md)|  | |

### Return type

[**\InvoicePDFs\Model\TaxRateResponse**](../Model/TaxRateResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

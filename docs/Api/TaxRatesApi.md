# InvoicePDFs\TaxRatesApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createTaxRateApiV1TaxRatesPost()**](TaxRatesApi.md#createTaxRateApiV1TaxRatesPost) | **POST** /api/v1/tax-rates | Create Tax Rate |
| [**deleteTaxRateApiV1TaxRatesTaxRateIdDelete()**](TaxRatesApi.md#deleteTaxRateApiV1TaxRatesTaxRateIdDelete) | **DELETE** /api/v1/tax-rates/{tax_rate_id} | Delete Tax Rate |
| [**getTaxRateApiV1TaxRatesTaxRateIdGet()**](TaxRatesApi.md#getTaxRateApiV1TaxRatesTaxRateIdGet) | **GET** /api/v1/tax-rates/{tax_rate_id} | Get Tax Rate |
| [**listTaxRatesApiV1TaxRatesGet()**](TaxRatesApi.md#listTaxRatesApiV1TaxRatesGet) | **GET** /api/v1/tax-rates | List Tax Rates |
| [**updateTaxRateApiV1TaxRatesTaxRateIdPatch()**](TaxRatesApi.md#updateTaxRateApiV1TaxRatesTaxRateIdPatch) | **PATCH** /api/v1/tax-rates/{tax_rate_id} | Update Tax Rate |


## `createTaxRateApiV1TaxRatesPost()`

```php
createTaxRateApiV1TaxRatesPost($tax_rate_create_request): \InvoicePDFs\Model\TaxRateResponse
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
    $result = $apiInstance->createTaxRateApiV1TaxRatesPost($tax_rate_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TaxRatesApi->createTaxRateApiV1TaxRatesPost: ', $e->getMessage(), PHP_EOL;
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

## `deleteTaxRateApiV1TaxRatesTaxRateIdDelete()`

```php
deleteTaxRateApiV1TaxRatesTaxRateIdDelete($tax_rate_id): \InvoicePDFs\Model\SimpleBoolResponse
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
    $result = $apiInstance->deleteTaxRateApiV1TaxRatesTaxRateIdDelete($tax_rate_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TaxRatesApi->deleteTaxRateApiV1TaxRatesTaxRateIdDelete: ', $e->getMessage(), PHP_EOL;
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

## `getTaxRateApiV1TaxRatesTaxRateIdGet()`

```php
getTaxRateApiV1TaxRatesTaxRateIdGet($tax_rate_id): \InvoicePDFs\Model\TaxRateResponse
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
    $result = $apiInstance->getTaxRateApiV1TaxRatesTaxRateIdGet($tax_rate_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TaxRatesApi->getTaxRateApiV1TaxRatesTaxRateIdGet: ', $e->getMessage(), PHP_EOL;
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

## `listTaxRatesApiV1TaxRatesGet()`

```php
listTaxRatesApiV1TaxRatesGet($limit, $cursor): \InvoicePDFs\Model\TaxRatesListResponse
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
    $result = $apiInstance->listTaxRatesApiV1TaxRatesGet($limit, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TaxRatesApi->listTaxRatesApiV1TaxRatesGet: ', $e->getMessage(), PHP_EOL;
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

## `updateTaxRateApiV1TaxRatesTaxRateIdPatch()`

```php
updateTaxRateApiV1TaxRatesTaxRateIdPatch($tax_rate_id, $tax_rate_patch_request): \InvoicePDFs\Model\TaxRateResponse
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
    $result = $apiInstance->updateTaxRateApiV1TaxRatesTaxRateIdPatch($tax_rate_id, $tax_rate_patch_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TaxRatesApi->updateTaxRateApiV1TaxRatesTaxRateIdPatch: ', $e->getMessage(), PHP_EOL;
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

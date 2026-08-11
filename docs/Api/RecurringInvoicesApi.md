# InvoicePDFs\RecurringInvoicesApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**cancelRecurringInvoice()**](RecurringInvoicesApi.md#cancelRecurringInvoice) | **DELETE** /api/v1/recurring-invoices/{recurring_id} | Cancel Recurring Invoice |
| [**createRecurringInvoice()**](RecurringInvoicesApi.md#createRecurringInvoice) | **POST** /api/v1/recurring-invoices | Create Recurring Invoice |
| [**getRecurringInvoice()**](RecurringInvoicesApi.md#getRecurringInvoice) | **GET** /api/v1/recurring-invoices/{recurring_id} | Get Recurring Invoice |
| [**listGeneratedInvoices()**](RecurringInvoicesApi.md#listGeneratedInvoices) | **GET** /api/v1/recurring-invoices/{recurring_id}/invoices | List Generated Invoices |
| [**listRecurringInvoices()**](RecurringInvoicesApi.md#listRecurringInvoices) | **GET** /api/v1/recurring-invoices | List Recurring Invoices |
| [**pauseRecurringInvoice()**](RecurringInvoicesApi.md#pauseRecurringInvoice) | **POST** /api/v1/recurring-invoices/{recurring_id}/pause | Pause Recurring Invoice |
| [**resumeRecurringInvoice()**](RecurringInvoicesApi.md#resumeRecurringInvoice) | **POST** /api/v1/recurring-invoices/{recurring_id}/resume | Resume Recurring Invoice |
| [**updateRecurringInvoice()**](RecurringInvoicesApi.md#updateRecurringInvoice) | **PATCH** /api/v1/recurring-invoices/{recurring_id} | Update Recurring Invoice |


## `cancelRecurringInvoice()`

```php
cancelRecurringInvoice($recurring_id): \InvoicePDFs\Model\RecurringInvoiceResponse
```

Cancel Recurring Invoice

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\RecurringInvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$recurring_id = 'recurring_id_example'; // string

try {
    $result = $apiInstance->cancelRecurringInvoice($recurring_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RecurringInvoicesApi->cancelRecurringInvoice: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **recurring_id** | **string**|  | |

### Return type

[**\InvoicePDFs\Model\RecurringInvoiceResponse**](../Model/RecurringInvoiceResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createRecurringInvoice()`

```php
createRecurringInvoice($recurring_invoice_create_request): \InvoicePDFs\Model\RecurringInvoiceResponse
```

Create Recurring Invoice

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\RecurringInvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$recurring_invoice_create_request = new \InvoicePDFs\Model\RecurringInvoiceCreateRequest(); // \InvoicePDFs\Model\RecurringInvoiceCreateRequest

try {
    $result = $apiInstance->createRecurringInvoice($recurring_invoice_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RecurringInvoicesApi->createRecurringInvoice: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **recurring_invoice_create_request** | [**\InvoicePDFs\Model\RecurringInvoiceCreateRequest**](../Model/RecurringInvoiceCreateRequest.md)|  | |

### Return type

[**\InvoicePDFs\Model\RecurringInvoiceResponse**](../Model/RecurringInvoiceResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getRecurringInvoice()`

```php
getRecurringInvoice($recurring_id): \InvoicePDFs\Model\RecurringInvoiceResponse
```

Get Recurring Invoice

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\RecurringInvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$recurring_id = 'recurring_id_example'; // string

try {
    $result = $apiInstance->getRecurringInvoice($recurring_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RecurringInvoicesApi->getRecurringInvoice: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **recurring_id** | **string**|  | |

### Return type

[**\InvoicePDFs\Model\RecurringInvoiceResponse**](../Model/RecurringInvoiceResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listGeneratedInvoices()`

```php
listGeneratedInvoices($recurring_id, $limit, $cursor): \InvoicePDFs\Model\InvoicesListResponse
```

List Generated Invoices

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\RecurringInvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$recurring_id = 'recurring_id_example'; // string
$limit = 50; // int
$cursor = 'cursor_example'; // string

try {
    $result = $apiInstance->listGeneratedInvoices($recurring_id, $limit, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RecurringInvoicesApi->listGeneratedInvoices: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **recurring_id** | **string**|  | |
| **limit** | **int**|  | [optional] [default to 50] |
| **cursor** | **string**|  | [optional] |

### Return type

[**\InvoicePDFs\Model\InvoicesListResponse**](../Model/InvoicesListResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listRecurringInvoices()`

```php
listRecurringInvoices($limit, $cursor, $status): \InvoicePDFs\Model\RecurringInvoicesListResponse
```

List Recurring Invoices

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\RecurringInvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$limit = 50; // int
$cursor = 'cursor_example'; // string
$status = 'status_example'; // string

try {
    $result = $apiInstance->listRecurringInvoices($limit, $cursor, $status);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RecurringInvoicesApi->listRecurringInvoices: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **limit** | **int**|  | [optional] [default to 50] |
| **cursor** | **string**|  | [optional] |
| **status** | **string**|  | [optional] |

### Return type

[**\InvoicePDFs\Model\RecurringInvoicesListResponse**](../Model/RecurringInvoicesListResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `pauseRecurringInvoice()`

```php
pauseRecurringInvoice($recurring_id): \InvoicePDFs\Model\RecurringInvoiceResponse
```

Pause Recurring Invoice

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\RecurringInvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$recurring_id = 'recurring_id_example'; // string

try {
    $result = $apiInstance->pauseRecurringInvoice($recurring_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RecurringInvoicesApi->pauseRecurringInvoice: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **recurring_id** | **string**|  | |

### Return type

[**\InvoicePDFs\Model\RecurringInvoiceResponse**](../Model/RecurringInvoiceResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `resumeRecurringInvoice()`

```php
resumeRecurringInvoice($recurring_id): \InvoicePDFs\Model\RecurringInvoiceResponse
```

Resume Recurring Invoice

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\RecurringInvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$recurring_id = 'recurring_id_example'; // string

try {
    $result = $apiInstance->resumeRecurringInvoice($recurring_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RecurringInvoicesApi->resumeRecurringInvoice: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **recurring_id** | **string**|  | |

### Return type

[**\InvoicePDFs\Model\RecurringInvoiceResponse**](../Model/RecurringInvoiceResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateRecurringInvoice()`

```php
updateRecurringInvoice($recurring_id, $recurring_invoice_patch_request): \InvoicePDFs\Model\RecurringInvoiceResponse
```

Update Recurring Invoice

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\RecurringInvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$recurring_id = 'recurring_id_example'; // string
$recurring_invoice_patch_request = new \InvoicePDFs\Model\RecurringInvoicePatchRequest(); // \InvoicePDFs\Model\RecurringInvoicePatchRequest

try {
    $result = $apiInstance->updateRecurringInvoice($recurring_id, $recurring_invoice_patch_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RecurringInvoicesApi->updateRecurringInvoice: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **recurring_id** | **string**|  | |
| **recurring_invoice_patch_request** | [**\InvoicePDFs\Model\RecurringInvoicePatchRequest**](../Model/RecurringInvoicePatchRequest.md)|  | |

### Return type

[**\InvoicePDFs\Model\RecurringInvoiceResponse**](../Model/RecurringInvoiceResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

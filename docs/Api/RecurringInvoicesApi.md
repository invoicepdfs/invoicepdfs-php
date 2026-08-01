# InvoicePDFs\RecurringInvoicesApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**cancelRecurringInvoiceApiV1RecurringInvoicesRecurringIdDelete()**](RecurringInvoicesApi.md#cancelRecurringInvoiceApiV1RecurringInvoicesRecurringIdDelete) | **DELETE** /api/v1/recurring-invoices/{recurring_id} | Cancel Recurring Invoice |
| [**createRecurringInvoiceApiV1RecurringInvoicesPost()**](RecurringInvoicesApi.md#createRecurringInvoiceApiV1RecurringInvoicesPost) | **POST** /api/v1/recurring-invoices | Create Recurring Invoice |
| [**getRecurringInvoiceApiV1RecurringInvoicesRecurringIdGet()**](RecurringInvoicesApi.md#getRecurringInvoiceApiV1RecurringInvoicesRecurringIdGet) | **GET** /api/v1/recurring-invoices/{recurring_id} | Get Recurring Invoice |
| [**listGeneratedInvoicesApiV1RecurringInvoicesRecurringIdInvoicesGet()**](RecurringInvoicesApi.md#listGeneratedInvoicesApiV1RecurringInvoicesRecurringIdInvoicesGet) | **GET** /api/v1/recurring-invoices/{recurring_id}/invoices | List Generated Invoices |
| [**listRecurringInvoicesApiV1RecurringInvoicesGet()**](RecurringInvoicesApi.md#listRecurringInvoicesApiV1RecurringInvoicesGet) | **GET** /api/v1/recurring-invoices | List Recurring Invoices |
| [**patchRecurringInvoiceApiV1RecurringInvoicesRecurringIdPatch()**](RecurringInvoicesApi.md#patchRecurringInvoiceApiV1RecurringInvoicesRecurringIdPatch) | **PATCH** /api/v1/recurring-invoices/{recurring_id} | Patch Recurring Invoice |
| [**pauseRecurringInvoiceApiV1RecurringInvoicesRecurringIdPausePost()**](RecurringInvoicesApi.md#pauseRecurringInvoiceApiV1RecurringInvoicesRecurringIdPausePost) | **POST** /api/v1/recurring-invoices/{recurring_id}/pause | Pause Recurring Invoice |
| [**resumeRecurringInvoiceApiV1RecurringInvoicesRecurringIdResumePost()**](RecurringInvoicesApi.md#resumeRecurringInvoiceApiV1RecurringInvoicesRecurringIdResumePost) | **POST** /api/v1/recurring-invoices/{recurring_id}/resume | Resume Recurring Invoice |


## `cancelRecurringInvoiceApiV1RecurringInvoicesRecurringIdDelete()`

```php
cancelRecurringInvoiceApiV1RecurringInvoicesRecurringIdDelete($recurring_id): \InvoicePDFs\Model\RecurringInvoiceResponse
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
    $result = $apiInstance->cancelRecurringInvoiceApiV1RecurringInvoicesRecurringIdDelete($recurring_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RecurringInvoicesApi->cancelRecurringInvoiceApiV1RecurringInvoicesRecurringIdDelete: ', $e->getMessage(), PHP_EOL;
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

## `createRecurringInvoiceApiV1RecurringInvoicesPost()`

```php
createRecurringInvoiceApiV1RecurringInvoicesPost($recurring_invoice_create_request): \InvoicePDFs\Model\RecurringInvoiceResponse
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
    $result = $apiInstance->createRecurringInvoiceApiV1RecurringInvoicesPost($recurring_invoice_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RecurringInvoicesApi->createRecurringInvoiceApiV1RecurringInvoicesPost: ', $e->getMessage(), PHP_EOL;
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

## `getRecurringInvoiceApiV1RecurringInvoicesRecurringIdGet()`

```php
getRecurringInvoiceApiV1RecurringInvoicesRecurringIdGet($recurring_id): \InvoicePDFs\Model\RecurringInvoiceResponse
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
    $result = $apiInstance->getRecurringInvoiceApiV1RecurringInvoicesRecurringIdGet($recurring_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RecurringInvoicesApi->getRecurringInvoiceApiV1RecurringInvoicesRecurringIdGet: ', $e->getMessage(), PHP_EOL;
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

## `listGeneratedInvoicesApiV1RecurringInvoicesRecurringIdInvoicesGet()`

```php
listGeneratedInvoicesApiV1RecurringInvoicesRecurringIdInvoicesGet($recurring_id, $limit, $cursor): \InvoicePDFs\Model\InvoicesListResponse
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
    $result = $apiInstance->listGeneratedInvoicesApiV1RecurringInvoicesRecurringIdInvoicesGet($recurring_id, $limit, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RecurringInvoicesApi->listGeneratedInvoicesApiV1RecurringInvoicesRecurringIdInvoicesGet: ', $e->getMessage(), PHP_EOL;
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

## `listRecurringInvoicesApiV1RecurringInvoicesGet()`

```php
listRecurringInvoicesApiV1RecurringInvoicesGet($limit, $cursor, $status): \InvoicePDFs\Model\RecurringInvoicesListResponse
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
    $result = $apiInstance->listRecurringInvoicesApiV1RecurringInvoicesGet($limit, $cursor, $status);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RecurringInvoicesApi->listRecurringInvoicesApiV1RecurringInvoicesGet: ', $e->getMessage(), PHP_EOL;
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

## `patchRecurringInvoiceApiV1RecurringInvoicesRecurringIdPatch()`

```php
patchRecurringInvoiceApiV1RecurringInvoicesRecurringIdPatch($recurring_id, $recurring_invoice_patch_request): \InvoicePDFs\Model\RecurringInvoiceResponse
```

Patch Recurring Invoice

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
    $result = $apiInstance->patchRecurringInvoiceApiV1RecurringInvoicesRecurringIdPatch($recurring_id, $recurring_invoice_patch_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RecurringInvoicesApi->patchRecurringInvoiceApiV1RecurringInvoicesRecurringIdPatch: ', $e->getMessage(), PHP_EOL;
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

## `pauseRecurringInvoiceApiV1RecurringInvoicesRecurringIdPausePost()`

```php
pauseRecurringInvoiceApiV1RecurringInvoicesRecurringIdPausePost($recurring_id): \InvoicePDFs\Model\RecurringInvoiceResponse
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
    $result = $apiInstance->pauseRecurringInvoiceApiV1RecurringInvoicesRecurringIdPausePost($recurring_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RecurringInvoicesApi->pauseRecurringInvoiceApiV1RecurringInvoicesRecurringIdPausePost: ', $e->getMessage(), PHP_EOL;
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

## `resumeRecurringInvoiceApiV1RecurringInvoicesRecurringIdResumePost()`

```php
resumeRecurringInvoiceApiV1RecurringInvoicesRecurringIdResumePost($recurring_id): \InvoicePDFs\Model\RecurringInvoiceResponse
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
    $result = $apiInstance->resumeRecurringInvoiceApiV1RecurringInvoicesRecurringIdResumePost($recurring_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RecurringInvoicesApi->resumeRecurringInvoiceApiV1RecurringInvoicesRecurringIdResumePost: ', $e->getMessage(), PHP_EOL;
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

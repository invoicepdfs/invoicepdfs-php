# OpenAPI\Client\InvoicesApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**archiveInvoiceApiV1InvoicesInvoiceIdArchivePost()**](InvoicesApi.md#archiveInvoiceApiV1InvoicesInvoiceIdArchivePost) | **POST** /api/v1/invoices/{invoice_id}/archive | Archive Invoice |
| [**calculateInvoiceApiV1InvoicesCalculatePost()**](InvoicesApi.md#calculateInvoiceApiV1InvoicesCalculatePost) | **POST** /api/v1/invoices/calculate | Calculate Invoice |
| [**createInvoiceApiV1InvoicesPost()**](InvoicesApi.md#createInvoiceApiV1InvoicesPost) | **POST** /api/v1/invoices | Create Invoice |
| [**deleteInvoiceApiV1InvoicesInvoiceIdDelete()**](InvoicesApi.md#deleteInvoiceApiV1InvoicesInvoiceIdDelete) | **DELETE** /api/v1/invoices/{invoice_id} | Delete Invoice |
| [**duplicateInvoiceApiV1InvoicesInvoiceIdDuplicatePost()**](InvoicesApi.md#duplicateInvoiceApiV1InvoicesInvoiceIdDuplicatePost) | **POST** /api/v1/invoices/{invoice_id}/duplicate | Duplicate Invoice |
| [**finalizeInvoiceApiV1InvoicesInvoiceIdFinalizePost()**](InvoicesApi.md#finalizeInvoiceApiV1InvoicesInvoiceIdFinalizePost) | **POST** /api/v1/invoices/{invoice_id}/finalize | Finalize Invoice |
| [**getInvoiceApiV1InvoicesInvoiceIdGet()**](InvoicesApi.md#getInvoiceApiV1InvoicesInvoiceIdGet) | **GET** /api/v1/invoices/{invoice_id} | Get Invoice |
| [**listInvoiceDeliveriesApiV1InvoicesInvoiceIdDeliveriesGet()**](InvoicesApi.md#listInvoiceDeliveriesApiV1InvoicesInvoiceIdDeliveriesGet) | **GET** /api/v1/invoices/{invoice_id}/deliveries | List Invoice Deliveries |
| [**listInvoicesApiV1InvoicesGet()**](InvoicesApi.md#listInvoicesApiV1InvoicesGet) | **GET** /api/v1/invoices | List Invoices |
| [**markPaidApiV1InvoicesInvoiceIdMarkPaidPost()**](InvoicesApi.md#markPaidApiV1InvoicesInvoiceIdMarkPaidPost) | **POST** /api/v1/invoices/{invoice_id}/mark-paid | Mark Paid |
| [**markSentApiV1InvoicesInvoiceIdMarkSentPost()**](InvoicesApi.md#markSentApiV1InvoicesInvoiceIdMarkSentPost) | **POST** /api/v1/invoices/{invoice_id}/mark-sent | Mark Sent |
| [**markUnpaidApiV1InvoicesInvoiceIdMarkUnpaidPost()**](InvoicesApi.md#markUnpaidApiV1InvoicesInvoiceIdMarkUnpaidPost) | **POST** /api/v1/invoices/{invoice_id}/mark-unpaid | Mark Unpaid |
| [**patchInvoiceApiV1InvoicesInvoiceIdPatch()**](InvoicesApi.md#patchInvoiceApiV1InvoicesInvoiceIdPatch) | **PATCH** /api/v1/invoices/{invoice_id} | Patch Invoice |
| [**previewInvoiceApiV1InvoicesPreviewPost()**](InvoicesApi.md#previewInvoiceApiV1InvoicesPreviewPost) | **POST** /api/v1/invoices/preview | Preview Invoice |
| [**renderInvoiceApiV1InvoicesInvoiceIdRendersPost()**](InvoicesApi.md#renderInvoiceApiV1InvoicesInvoiceIdRendersPost) | **POST** /api/v1/invoices/{invoice_id}/renders | Render Invoice |
| [**replaceInvoiceApiV1InvoicesInvoiceIdPut()**](InvoicesApi.md#replaceInvoiceApiV1InvoicesInvoiceIdPut) | **PUT** /api/v1/invoices/{invoice_id} | Replace Invoice |
| [**restoreInvoiceApiV1InvoicesInvoiceIdRestorePost()**](InvoicesApi.md#restoreInvoiceApiV1InvoicesInvoiceIdRestorePost) | **POST** /api/v1/invoices/{invoice_id}/restore | Restore Invoice |
| [**sendInvoiceApiV1InvoicesInvoiceIdSendPost()**](InvoicesApi.md#sendInvoiceApiV1InvoicesInvoiceIdSendPost) | **POST** /api/v1/invoices/{invoice_id}/send | Send Invoice |
| [**validateInvoiceApiV1InvoicesValidatePost()**](InvoicesApi.md#validateInvoiceApiV1InvoicesValidatePost) | **POST** /api/v1/invoices/validate | Validate Invoice |
| [**voidInvoiceApiV1InvoicesInvoiceIdVoidPost()**](InvoicesApi.md#voidInvoiceApiV1InvoicesInvoiceIdVoidPost) | **POST** /api/v1/invoices/{invoice_id}/void | Void Invoice |


## `archiveInvoiceApiV1InvoicesInvoiceIdArchivePost()`

```php
archiveInvoiceApiV1InvoicesInvoiceIdArchivePost($invoice_id): \OpenAPI\Client\Model\InvoiceResponse
```

Archive Invoice

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\InvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$invoice_id = 'invoice_id_example'; // string

try {
    $result = $apiInstance->archiveInvoiceApiV1InvoicesInvoiceIdArchivePost($invoice_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InvoicesApi->archiveInvoiceApiV1InvoicesInvoiceIdArchivePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invoice_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\InvoiceResponse**](../Model/InvoiceResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `calculateInvoiceApiV1InvoicesCalculatePost()`

```php
calculateInvoiceApiV1InvoicesCalculatePost($invoice_draft_request): array<string,mixed>
```

Calculate Invoice

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\InvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$invoice_draft_request = new \OpenAPI\Client\Model\InvoiceDraftRequest(); // \OpenAPI\Client\Model\InvoiceDraftRequest

try {
    $result = $apiInstance->calculateInvoiceApiV1InvoicesCalculatePost($invoice_draft_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InvoicesApi->calculateInvoiceApiV1InvoicesCalculatePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invoice_draft_request** | [**\OpenAPI\Client\Model\InvoiceDraftRequest**](../Model/InvoiceDraftRequest.md)|  | |

### Return type

**array<string,mixed>**

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createInvoiceApiV1InvoicesPost()`

```php
createInvoiceApiV1InvoicesPost($invoice_create_request, $idempotency_key): \OpenAPI\Client\Model\InvoiceResponse
```

Create Invoice

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\InvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$invoice_create_request = new \OpenAPI\Client\Model\InvoiceCreateRequest(); // \OpenAPI\Client\Model\InvoiceCreateRequest
$idempotency_key = 'idempotency_key_example'; // string

try {
    $result = $apiInstance->createInvoiceApiV1InvoicesPost($invoice_create_request, $idempotency_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InvoicesApi->createInvoiceApiV1InvoicesPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invoice_create_request** | [**\OpenAPI\Client\Model\InvoiceCreateRequest**](../Model/InvoiceCreateRequest.md)|  | |
| **idempotency_key** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\InvoiceResponse**](../Model/InvoiceResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteInvoiceApiV1InvoicesInvoiceIdDelete()`

```php
deleteInvoiceApiV1InvoicesInvoiceIdDelete($invoice_id): \OpenAPI\Client\Model\SimpleBoolResponse
```

Delete Invoice

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\InvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$invoice_id = 'invoice_id_example'; // string

try {
    $result = $apiInstance->deleteInvoiceApiV1InvoicesInvoiceIdDelete($invoice_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InvoicesApi->deleteInvoiceApiV1InvoicesInvoiceIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invoice_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\SimpleBoolResponse**](../Model/SimpleBoolResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `duplicateInvoiceApiV1InvoicesInvoiceIdDuplicatePost()`

```php
duplicateInvoiceApiV1InvoicesInvoiceIdDuplicatePost($invoice_id): \OpenAPI\Client\Model\InvoiceResponse
```

Duplicate Invoice

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\InvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$invoice_id = 'invoice_id_example'; // string

try {
    $result = $apiInstance->duplicateInvoiceApiV1InvoicesInvoiceIdDuplicatePost($invoice_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InvoicesApi->duplicateInvoiceApiV1InvoicesInvoiceIdDuplicatePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invoice_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\InvoiceResponse**](../Model/InvoiceResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `finalizeInvoiceApiV1InvoicesInvoiceIdFinalizePost()`

```php
finalizeInvoiceApiV1InvoicesInvoiceIdFinalizePost($invoice_id, $idempotency_key): array<string,mixed>
```

Finalize Invoice

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\InvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$invoice_id = 'invoice_id_example'; // string
$idempotency_key = 'idempotency_key_example'; // string

try {
    $result = $apiInstance->finalizeInvoiceApiV1InvoicesInvoiceIdFinalizePost($invoice_id, $idempotency_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InvoicesApi->finalizeInvoiceApiV1InvoicesInvoiceIdFinalizePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invoice_id** | **string**|  | |
| **idempotency_key** | **string**|  | [optional] |

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

## `getInvoiceApiV1InvoicesInvoiceIdGet()`

```php
getInvoiceApiV1InvoicesInvoiceIdGet($invoice_id): \OpenAPI\Client\Model\InvoiceResponse
```

Get Invoice

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\InvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$invoice_id = 'invoice_id_example'; // string

try {
    $result = $apiInstance->getInvoiceApiV1InvoicesInvoiceIdGet($invoice_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InvoicesApi->getInvoiceApiV1InvoicesInvoiceIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invoice_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\InvoiceResponse**](../Model/InvoiceResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listInvoiceDeliveriesApiV1InvoicesInvoiceIdDeliveriesGet()`

```php
listInvoiceDeliveriesApiV1InvoicesInvoiceIdDeliveriesGet($invoice_id, $limit, $cursor): \OpenAPI\Client\Model\DeliveriesListResponse
```

List Invoice Deliveries

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\InvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$invoice_id = 'invoice_id_example'; // string
$limit = 50; // int
$cursor = 'cursor_example'; // string

try {
    $result = $apiInstance->listInvoiceDeliveriesApiV1InvoicesInvoiceIdDeliveriesGet($invoice_id, $limit, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InvoicesApi->listInvoiceDeliveriesApiV1InvoicesInvoiceIdDeliveriesGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invoice_id** | **string**|  | |
| **limit** | **int**|  | [optional] [default to 50] |
| **cursor** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\DeliveriesListResponse**](../Model/DeliveriesListResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listInvoicesApiV1InvoicesGet()`

```php
listInvoicesApiV1InvoicesGet($limit, $cursor, $status): \OpenAPI\Client\Model\InvoicesListResponse
```

List Invoices

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\InvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$limit = 50; // int
$cursor = 'cursor_example'; // string
$status = 'status_example'; // string

try {
    $result = $apiInstance->listInvoicesApiV1InvoicesGet($limit, $cursor, $status);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InvoicesApi->listInvoicesApiV1InvoicesGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **limit** | **int**|  | [optional] [default to 50] |
| **cursor** | **string**|  | [optional] |
| **status** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\InvoicesListResponse**](../Model/InvoicesListResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `markPaidApiV1InvoicesInvoiceIdMarkPaidPost()`

```php
markPaidApiV1InvoicesInvoiceIdMarkPaidPost($invoice_id): \OpenAPI\Client\Model\InvoiceResponse
```

Mark Paid

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\InvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$invoice_id = 'invoice_id_example'; // string

try {
    $result = $apiInstance->markPaidApiV1InvoicesInvoiceIdMarkPaidPost($invoice_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InvoicesApi->markPaidApiV1InvoicesInvoiceIdMarkPaidPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invoice_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\InvoiceResponse**](../Model/InvoiceResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `markSentApiV1InvoicesInvoiceIdMarkSentPost()`

```php
markSentApiV1InvoicesInvoiceIdMarkSentPost($invoice_id): \OpenAPI\Client\Model\InvoiceResponse
```

Mark Sent

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\InvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$invoice_id = 'invoice_id_example'; // string

try {
    $result = $apiInstance->markSentApiV1InvoicesInvoiceIdMarkSentPost($invoice_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InvoicesApi->markSentApiV1InvoicesInvoiceIdMarkSentPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invoice_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\InvoiceResponse**](../Model/InvoiceResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `markUnpaidApiV1InvoicesInvoiceIdMarkUnpaidPost()`

```php
markUnpaidApiV1InvoicesInvoiceIdMarkUnpaidPost($invoice_id): \OpenAPI\Client\Model\InvoiceResponse
```

Mark Unpaid

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\InvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$invoice_id = 'invoice_id_example'; // string

try {
    $result = $apiInstance->markUnpaidApiV1InvoicesInvoiceIdMarkUnpaidPost($invoice_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InvoicesApi->markUnpaidApiV1InvoicesInvoiceIdMarkUnpaidPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invoice_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\InvoiceResponse**](../Model/InvoiceResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `patchInvoiceApiV1InvoicesInvoiceIdPatch()`

```php
patchInvoiceApiV1InvoicesInvoiceIdPatch($invoice_id, $invoice_patch_request, $idempotency_key): \OpenAPI\Client\Model\InvoiceResponse
```

Patch Invoice

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\InvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$invoice_id = 'invoice_id_example'; // string
$invoice_patch_request = new \OpenAPI\Client\Model\InvoicePatchRequest(); // \OpenAPI\Client\Model\InvoicePatchRequest
$idempotency_key = 'idempotency_key_example'; // string

try {
    $result = $apiInstance->patchInvoiceApiV1InvoicesInvoiceIdPatch($invoice_id, $invoice_patch_request, $idempotency_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InvoicesApi->patchInvoiceApiV1InvoicesInvoiceIdPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invoice_id** | **string**|  | |
| **invoice_patch_request** | [**\OpenAPI\Client\Model\InvoicePatchRequest**](../Model/InvoicePatchRequest.md)|  | |
| **idempotency_key** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\InvoiceResponse**](../Model/InvoiceResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `previewInvoiceApiV1InvoicesPreviewPost()`

```php
previewInvoiceApiV1InvoicesPreviewPost($invoice_preview_request): mixed
```

Preview Invoice

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\InvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$invoice_preview_request = new \OpenAPI\Client\Model\InvoicePreviewRequest(); // \OpenAPI\Client\Model\InvoicePreviewRequest

try {
    $result = $apiInstance->previewInvoiceApiV1InvoicesPreviewPost($invoice_preview_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InvoicesApi->previewInvoiceApiV1InvoicesPreviewPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invoice_preview_request** | [**\OpenAPI\Client\Model\InvoicePreviewRequest**](../Model/InvoicePreviewRequest.md)|  | |

### Return type

**mixed**

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `renderInvoiceApiV1InvoicesInvoiceIdRendersPost()`

```php
renderInvoiceApiV1InvoicesInvoiceIdRendersPost($invoice_id, $invoice_render_request, $idempotency_key): mixed
```

Render Invoice

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\InvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$invoice_id = 'invoice_id_example'; // string
$invoice_render_request = new \OpenAPI\Client\Model\InvoiceRenderRequest(); // \OpenAPI\Client\Model\InvoiceRenderRequest
$idempotency_key = 'idempotency_key_example'; // string

try {
    $result = $apiInstance->renderInvoiceApiV1InvoicesInvoiceIdRendersPost($invoice_id, $invoice_render_request, $idempotency_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InvoicesApi->renderInvoiceApiV1InvoicesInvoiceIdRendersPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invoice_id** | **string**|  | |
| **invoice_render_request** | [**\OpenAPI\Client\Model\InvoiceRenderRequest**](../Model/InvoiceRenderRequest.md)|  | |
| **idempotency_key** | **string**|  | [optional] |

### Return type

**mixed**

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `replaceInvoiceApiV1InvoicesInvoiceIdPut()`

```php
replaceInvoiceApiV1InvoicesInvoiceIdPut($invoice_id, $invoice_create_request, $idempotency_key): \OpenAPI\Client\Model\InvoiceResponse
```

Replace Invoice

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\InvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$invoice_id = 'invoice_id_example'; // string
$invoice_create_request = new \OpenAPI\Client\Model\InvoiceCreateRequest(); // \OpenAPI\Client\Model\InvoiceCreateRequest
$idempotency_key = 'idempotency_key_example'; // string

try {
    $result = $apiInstance->replaceInvoiceApiV1InvoicesInvoiceIdPut($invoice_id, $invoice_create_request, $idempotency_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InvoicesApi->replaceInvoiceApiV1InvoicesInvoiceIdPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invoice_id** | **string**|  | |
| **invoice_create_request** | [**\OpenAPI\Client\Model\InvoiceCreateRequest**](../Model/InvoiceCreateRequest.md)|  | |
| **idempotency_key** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\InvoiceResponse**](../Model/InvoiceResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `restoreInvoiceApiV1InvoicesInvoiceIdRestorePost()`

```php
restoreInvoiceApiV1InvoicesInvoiceIdRestorePost($invoice_id): \OpenAPI\Client\Model\InvoiceResponse
```

Restore Invoice

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\InvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$invoice_id = 'invoice_id_example'; // string

try {
    $result = $apiInstance->restoreInvoiceApiV1InvoicesInvoiceIdRestorePost($invoice_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InvoicesApi->restoreInvoiceApiV1InvoicesInvoiceIdRestorePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invoice_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\InvoiceResponse**](../Model/InvoiceResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `sendInvoiceApiV1InvoicesInvoiceIdSendPost()`

```php
sendInvoiceApiV1InvoicesInvoiceIdSendPost($invoice_id, $delivery_send_request): \OpenAPI\Client\Model\DeliveryResponse
```

Send Invoice

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\InvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$invoice_id = 'invoice_id_example'; // string
$delivery_send_request = new \OpenAPI\Client\Model\DeliverySendRequest(); // \OpenAPI\Client\Model\DeliverySendRequest

try {
    $result = $apiInstance->sendInvoiceApiV1InvoicesInvoiceIdSendPost($invoice_id, $delivery_send_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InvoicesApi->sendInvoiceApiV1InvoicesInvoiceIdSendPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invoice_id** | **string**|  | |
| **delivery_send_request** | [**\OpenAPI\Client\Model\DeliverySendRequest**](../Model/DeliverySendRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\DeliveryResponse**](../Model/DeliveryResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `validateInvoiceApiV1InvoicesValidatePost()`

```php
validateInvoiceApiV1InvoicesValidatePost($invoice_draft_request): array<string,mixed>
```

Validate Invoice

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\InvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$invoice_draft_request = new \OpenAPI\Client\Model\InvoiceDraftRequest(); // \OpenAPI\Client\Model\InvoiceDraftRequest

try {
    $result = $apiInstance->validateInvoiceApiV1InvoicesValidatePost($invoice_draft_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InvoicesApi->validateInvoiceApiV1InvoicesValidatePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invoice_draft_request** | [**\OpenAPI\Client\Model\InvoiceDraftRequest**](../Model/InvoiceDraftRequest.md)|  | |

### Return type

**array<string,mixed>**

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `voidInvoiceApiV1InvoicesInvoiceIdVoidPost()`

```php
voidInvoiceApiV1InvoicesInvoiceIdVoidPost($invoice_id): \OpenAPI\Client\Model\InvoiceResponse
```

Void Invoice

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\InvoicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$invoice_id = 'invoice_id_example'; // string

try {
    $result = $apiInstance->voidInvoiceApiV1InvoicesInvoiceIdVoidPost($invoice_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InvoicesApi->voidInvoiceApiV1InvoicesInvoiceIdVoidPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invoice_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\InvoiceResponse**](../Model/InvoiceResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

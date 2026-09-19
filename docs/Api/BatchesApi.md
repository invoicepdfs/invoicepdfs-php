# InvoicePDFs\BatchesApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**cancelBatch()**](BatchesApi.md#cancelBatch) | **POST** /api/v1/batches/{batch_id}/cancel | Cancel Batch |
| [**createBatch()**](BatchesApi.md#createBatch) | **POST** /api/v1/batches | Create Batch |
| [**downloadBatch()**](BatchesApi.md#downloadBatch) | **GET** /api/v1/batches/{batch_id}/download | Download Batch |
| [**getBatch()**](BatchesApi.md#getBatch) | **GET** /api/v1/batches/{batch_id} | Get Batch |
| [**listBatchItems()**](BatchesApi.md#listBatchItems) | **GET** /api/v1/batches/{batch_id}/items | List Batch Items |
| [**listBatches()**](BatchesApi.md#listBatches) | **GET** /api/v1/batches | List Batches |


## `cancelBatch()`

```php
cancelBatch($batch_id): \InvoicePDFs\Model\BatchResponse
```

Cancel Batch

Stop a batch that has not finished.  Items not yet started are cancelled. An item already rendering completes — the work is done and cancelling it would waste it.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\BatchesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$batch_id = 'batch_id_example'; // string

try {
    $result = $apiInstance->cancelBatch($batch_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BatchesApi->cancelBatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **batch_id** | **string**|  | |

### Return type

[**\InvoicePDFs\Model\BatchResponse**](../Model/BatchResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createBatch()`

```php
createBatch($batch_create_request): \InvoicePDFs\Model\BatchResponse
```

Create Batch

Queue many documents to be rendered at once.  Returns `202` — the batch is recorded and a worker renders it; nothing is rendered inside this request. Poll `get_batch` for progress, then `download_batch` for the results.  The whole batch is refused if it would exceed the monthly quota, rather than rendering part of it.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\BatchesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$batch_create_request = new \InvoicePDFs\Model\BatchCreateRequest(); // \InvoicePDFs\Model\BatchCreateRequest

try {
    $result = $apiInstance->createBatch($batch_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BatchesApi->createBatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **batch_create_request** | [**\InvoicePDFs\Model\BatchCreateRequest**](../Model/BatchCreateRequest.md)|  | |

### Return type

[**\InvoicePDFs\Model\BatchResponse**](../Model/BatchResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `downloadBatch()`

```php
downloadBatch($batch_id): \SplFileObject
```

Download Batch

Every completed render in the batch, as a ZIP.  `409` until the batch is `completed`. Items that failed are simply absent, so check `failed_items` rather than counting files.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\BatchesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$batch_id = 'batch_id_example'; // string

try {
    $result = $apiInstance->downloadBatch($batch_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BatchesApi->downloadBatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **batch_id** | **string**|  | |

### Return type

**\SplFileObject**

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/zip`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getBatch()`

```php
getBatch($batch_id): \InvoicePDFs\Model\BatchResponse
```

Get Batch

A batch's status and its per-item counts.  The poll surface: `total_items`, `completed_items` and `failed_items` say how far it has got without listing every item.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\BatchesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$batch_id = 'batch_id_example'; // string

try {
    $result = $apiInstance->getBatch($batch_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BatchesApi->getBatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **batch_id** | **string**|  | |

### Return type

[**\InvoicePDFs\Model\BatchResponse**](../Model/BatchResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listBatchItems()`

```php
listBatchItems($batch_id, $limit, $cursor): \InvoicePDFs\Model\BatchItemsListResponse
```

List Batch Items

Every item in a batch with its own status, newest first.  Where to look when `failed_items` is not zero: each row carries its error and, once rendered, its `render_id`.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\BatchesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$batch_id = 'batch_id_example'; // string
$limit = 50; // int
$cursor = 'cursor_example'; // string

try {
    $result = $apiInstance->listBatchItems($batch_id, $limit, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BatchesApi->listBatchItems: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **batch_id** | **string**|  | |
| **limit** | **int**|  | [optional] [default to 50] |
| **cursor** | **string**|  | [optional] |

### Return type

[**\InvoicePDFs\Model\BatchItemsListResponse**](../Model/BatchItemsListResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listBatches()`

```php
listBatches($limit, $cursor): \InvoicePDFs\Model\BatchesListResponse
```

List Batches

Batch jobs on this account, newest first.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\BatchesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$limit = 50; // int
$cursor = 'cursor_example'; // string

try {
    $result = $apiInstance->listBatches($limit, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BatchesApi->listBatches: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **limit** | **int**|  | [optional] [default to 50] |
| **cursor** | **string**|  | [optional] |

### Return type

[**\InvoicePDFs\Model\BatchesListResponse**](../Model/BatchesListResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

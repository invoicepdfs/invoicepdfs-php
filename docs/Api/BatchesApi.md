# InvoicePDFs\BatchesApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**cancelBatchApiV1BatchesBatchIdCancelPost()**](BatchesApi.md#cancelBatchApiV1BatchesBatchIdCancelPost) | **POST** /api/v1/batches/{batch_id}/cancel | Cancel Batch |
| [**createBatchApiV1BatchesPost()**](BatchesApi.md#createBatchApiV1BatchesPost) | **POST** /api/v1/batches | Create Batch |
| [**downloadBatchApiV1BatchesBatchIdDownloadGet()**](BatchesApi.md#downloadBatchApiV1BatchesBatchIdDownloadGet) | **GET** /api/v1/batches/{batch_id}/download | Download Batch |
| [**getBatchApiV1BatchesBatchIdGet()**](BatchesApi.md#getBatchApiV1BatchesBatchIdGet) | **GET** /api/v1/batches/{batch_id} | Get Batch |
| [**listBatchItemsApiV1BatchesBatchIdItemsGet()**](BatchesApi.md#listBatchItemsApiV1BatchesBatchIdItemsGet) | **GET** /api/v1/batches/{batch_id}/items | List Batch Items |
| [**listBatchesApiV1BatchesGet()**](BatchesApi.md#listBatchesApiV1BatchesGet) | **GET** /api/v1/batches | List Batches |


## `cancelBatchApiV1BatchesBatchIdCancelPost()`

```php
cancelBatchApiV1BatchesBatchIdCancelPost($batch_id): \InvoicePDFs\Model\BatchResponse
```

Cancel Batch

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
    $result = $apiInstance->cancelBatchApiV1BatchesBatchIdCancelPost($batch_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BatchesApi->cancelBatchApiV1BatchesBatchIdCancelPost: ', $e->getMessage(), PHP_EOL;
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

## `createBatchApiV1BatchesPost()`

```php
createBatchApiV1BatchesPost($batch_create_request): \InvoicePDFs\Model\BatchResponse
```

Create Batch

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
    $result = $apiInstance->createBatchApiV1BatchesPost($batch_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BatchesApi->createBatchApiV1BatchesPost: ', $e->getMessage(), PHP_EOL;
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

## `downloadBatchApiV1BatchesBatchIdDownloadGet()`

```php
downloadBatchApiV1BatchesBatchIdDownloadGet($batch_id): mixed
```

Download Batch

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
    $result = $apiInstance->downloadBatchApiV1BatchesBatchIdDownloadGet($batch_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BatchesApi->downloadBatchApiV1BatchesBatchIdDownloadGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **batch_id** | **string**|  | |

### Return type

**mixed**

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getBatchApiV1BatchesBatchIdGet()`

```php
getBatchApiV1BatchesBatchIdGet($batch_id): \InvoicePDFs\Model\BatchResponse
```

Get Batch

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
    $result = $apiInstance->getBatchApiV1BatchesBatchIdGet($batch_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BatchesApi->getBatchApiV1BatchesBatchIdGet: ', $e->getMessage(), PHP_EOL;
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

## `listBatchItemsApiV1BatchesBatchIdItemsGet()`

```php
listBatchItemsApiV1BatchesBatchIdItemsGet($batch_id, $limit, $cursor): \InvoicePDFs\Model\BatchItemsListResponse
```

List Batch Items

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
    $result = $apiInstance->listBatchItemsApiV1BatchesBatchIdItemsGet($batch_id, $limit, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BatchesApi->listBatchItemsApiV1BatchesBatchIdItemsGet: ', $e->getMessage(), PHP_EOL;
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

## `listBatchesApiV1BatchesGet()`

```php
listBatchesApiV1BatchesGet($limit, $cursor): \InvoicePDFs\Model\BatchesListResponse
```

List Batches

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
    $result = $apiInstance->listBatchesApiV1BatchesGet($limit, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BatchesApi->listBatchesApiV1BatchesGet: ', $e->getMessage(), PHP_EOL;
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

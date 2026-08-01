# InvoicePDFs\JobsApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**cancelJobApiV1JobsJobIdCancelPost()**](JobsApi.md#cancelJobApiV1JobsJobIdCancelPost) | **POST** /api/v1/jobs/{job_id}/cancel | Cancel Job |
| [**getJobApiV1JobsJobIdGet()**](JobsApi.md#getJobApiV1JobsJobIdGet) | **GET** /api/v1/jobs/{job_id} | Get Job |
| [**retryJobApiV1JobsJobIdRetryPost()**](JobsApi.md#retryJobApiV1JobsJobIdRetryPost) | **POST** /api/v1/jobs/{job_id}/retry | Retry Job |


## `cancelJobApiV1JobsJobIdCancelPost()`

```php
cancelJobApiV1JobsJobIdCancelPost($job_id): \InvoicePDFs\Model\JobResponse
```

Cancel Job

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\JobsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$job_id = 'job_id_example'; // string

try {
    $result = $apiInstance->cancelJobApiV1JobsJobIdCancelPost($job_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling JobsApi->cancelJobApiV1JobsJobIdCancelPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **job_id** | **string**|  | |

### Return type

[**\InvoicePDFs\Model\JobResponse**](../Model/JobResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getJobApiV1JobsJobIdGet()`

```php
getJobApiV1JobsJobIdGet($job_id): \InvoicePDFs\Model\JobResponse
```

Get Job

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\JobsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$job_id = 'job_id_example'; // string

try {
    $result = $apiInstance->getJobApiV1JobsJobIdGet($job_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling JobsApi->getJobApiV1JobsJobIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **job_id** | **string**|  | |

### Return type

[**\InvoicePDFs\Model\JobResponse**](../Model/JobResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `retryJobApiV1JobsJobIdRetryPost()`

```php
retryJobApiV1JobsJobIdRetryPost($job_id): \InvoicePDFs\Model\JobResponse
```

Retry Job

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\JobsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$job_id = 'job_id_example'; // string

try {
    $result = $apiInstance->retryJobApiV1JobsJobIdRetryPost($job_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling JobsApi->retryJobApiV1JobsJobIdRetryPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **job_id** | **string**|  | |

### Return type

[**\InvoicePDFs\Model\JobResponse**](../Model/JobResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

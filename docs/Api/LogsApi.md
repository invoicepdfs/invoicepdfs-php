# InvoicePDFs\LogsApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**listLogsApiV1LogsGet()**](LogsApi.md#listLogsApiV1LogsGet) | **GET** /api/v1/logs | List Logs |


## `listLogsApiV1LogsGet()`

```php
listLogsApiV1LogsGet($status, $limit): \InvoicePDFs\Model\ApiRequestLogsListResponse
```

List Logs

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\LogsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$status = ''; // string
$limit = 100; // int

try {
    $result = $apiInstance->listLogsApiV1LogsGet($status, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LogsApi->listLogsApiV1LogsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **status** | **string**|  | [optional] [default to &#39;&#39;] |
| **limit** | **int**|  | [optional] [default to 100] |

### Return type

[**\InvoicePDFs\Model\ApiRequestLogsListResponse**](../Model/ApiRequestLogsListResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

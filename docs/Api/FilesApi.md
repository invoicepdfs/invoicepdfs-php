# OpenAPI\Client\FilesApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**deleteFileApiV1FilesFileIdDelete()**](FilesApi.md#deleteFileApiV1FilesFileIdDelete) | **DELETE** /api/v1/files/{file_id} | Delete File |
| [**getFileApiV1FilesFileIdGet()**](FilesApi.md#getFileApiV1FilesFileIdGet) | **GET** /api/v1/files/{file_id} | Get File |
| [**uploadFileApiV1FilesPost()**](FilesApi.md#uploadFileApiV1FilesPost) | **POST** /api/v1/files | Upload File |


## `deleteFileApiV1FilesFileIdDelete()`

```php
deleteFileApiV1FilesFileIdDelete($file_id): \OpenAPI\Client\Model\SimpleBoolResponse
```

Delete File

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\FilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$file_id = 'file_id_example'; // string

try {
    $result = $apiInstance->deleteFileApiV1FilesFileIdDelete($file_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FilesApi->deleteFileApiV1FilesFileIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **file_id** | **string**|  | |

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

## `getFileApiV1FilesFileIdGet()`

```php
getFileApiV1FilesFileIdGet($file_id): \OpenAPI\Client\Model\FileResponse
```

Get File

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\FilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$file_id = 'file_id_example'; // string

try {
    $result = $apiInstance->getFileApiV1FilesFileIdGet($file_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FilesApi->getFileApiV1FilesFileIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **file_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\FileResponse**](../Model/FileResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `uploadFileApiV1FilesPost()`

```php
uploadFileApiV1FilesPost($file, $idempotency_key): \OpenAPI\Client\Model\FileResponse
```

Upload File

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\FilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$file = "/path/to/file.txt"; // \SplFileObject
$idempotency_key = 'idempotency_key_example'; // string

try {
    $result = $apiInstance->uploadFileApiV1FilesPost($file, $idempotency_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FilesApi->uploadFileApiV1FilesPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **file** | **\SplFileObject****\SplFileObject**|  | |
| **idempotency_key** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\FileResponse**](../Model/FileResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `multipart/form-data`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

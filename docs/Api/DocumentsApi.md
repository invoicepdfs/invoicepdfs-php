# OpenAPI\Client\DocumentsApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**calculateDocumentApiV1DocumentsCalculatePost()**](DocumentsApi.md#calculateDocumentApiV1DocumentsCalculatePost) | **POST** /api/v1/documents/calculate | Calculate Document |
| [**renderDocumentApiV1DocumentsRenderPost()**](DocumentsApi.md#renderDocumentApiV1DocumentsRenderPost) | **POST** /api/v1/documents/render | Render Document |
| [**validateDocumentApiV1DocumentsValidatePost()**](DocumentsApi.md#validateDocumentApiV1DocumentsValidatePost) | **POST** /api/v1/documents/validate | Validate Document |


## `calculateDocumentApiV1DocumentsCalculatePost()`

```php
calculateDocumentApiV1DocumentsCalculatePost($document_calculate_request): \OpenAPI\Client\Model\DocumentCalculateResponse
```

Calculate Document

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\DocumentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$document_calculate_request = new \OpenAPI\Client\Model\DocumentCalculateRequest(); // \OpenAPI\Client\Model\DocumentCalculateRequest

try {
    $result = $apiInstance->calculateDocumentApiV1DocumentsCalculatePost($document_calculate_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentsApi->calculateDocumentApiV1DocumentsCalculatePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **document_calculate_request** | [**\OpenAPI\Client\Model\DocumentCalculateRequest**](../Model/DocumentCalculateRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\DocumentCalculateResponse**](../Model/DocumentCalculateResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `renderDocumentApiV1DocumentsRenderPost()`

```php
renderDocumentApiV1DocumentsRenderPost($document_render_request, $idempotency_key): mixed
```

Render Document

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\DocumentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$document_render_request = new \OpenAPI\Client\Model\DocumentRenderRequest(); // \OpenAPI\Client\Model\DocumentRenderRequest
$idempotency_key = 'idempotency_key_example'; // string

try {
    $result = $apiInstance->renderDocumentApiV1DocumentsRenderPost($document_render_request, $idempotency_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentsApi->renderDocumentApiV1DocumentsRenderPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **document_render_request** | [**\OpenAPI\Client\Model\DocumentRenderRequest**](../Model/DocumentRenderRequest.md)|  | |
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

## `validateDocumentApiV1DocumentsValidatePost()`

```php
validateDocumentApiV1DocumentsValidatePost($document_validate_request): \OpenAPI\Client\Model\DocumentValidateResponse
```

Validate Document

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\DocumentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$document_validate_request = new \OpenAPI\Client\Model\DocumentValidateRequest(); // \OpenAPI\Client\Model\DocumentValidateRequest

try {
    $result = $apiInstance->validateDocumentApiV1DocumentsValidatePost($document_validate_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentsApi->validateDocumentApiV1DocumentsValidatePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **document_validate_request** | [**\OpenAPI\Client\Model\DocumentValidateRequest**](../Model/DocumentValidateRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\DocumentValidateResponse**](../Model/DocumentValidateResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

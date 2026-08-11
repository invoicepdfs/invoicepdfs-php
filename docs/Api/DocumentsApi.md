# InvoicePDFs\DocumentsApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**archiveDocument()**](DocumentsApi.md#archiveDocument) | **POST** /api/v1/documents/{document_id}/archive | Archive Document |
| [**calculateDocument()**](DocumentsApi.md#calculateDocument) | **POST** /api/v1/documents/calculate | Calculate Document |
| [**createDocument()**](DocumentsApi.md#createDocument) | **POST** /api/v1/documents | Create Document |
| [**createDocumentRender()**](DocumentsApi.md#createDocumentRender) | **POST** /api/v1/documents/{document_id}/renders | Create Document Render |
| [**deleteDocument()**](DocumentsApi.md#deleteDocument) | **DELETE** /api/v1/documents/{document_id} | Delete Document |
| [**duplicateDocument()**](DocumentsApi.md#duplicateDocument) | **POST** /api/v1/documents/{document_id}/duplicate | Duplicate Document |
| [**finalizeDocument()**](DocumentsApi.md#finalizeDocument) | **POST** /api/v1/documents/{document_id}/finalize | Finalize Document |
| [**getDocument()**](DocumentsApi.md#getDocument) | **GET** /api/v1/documents/{document_id} | Get Document |
| [**listDocumentDeliveries()**](DocumentsApi.md#listDocumentDeliveries) | **GET** /api/v1/documents/{document_id}/deliveries | List Document Deliveries |
| [**listDocuments()**](DocumentsApi.md#listDocuments) | **GET** /api/v1/documents | List Documents |
| [**markPaid()**](DocumentsApi.md#markPaid) | **POST** /api/v1/documents/{document_id}/mark-paid | Mark Paid |
| [**markSent()**](DocumentsApi.md#markSent) | **POST** /api/v1/documents/{document_id}/mark-sent | Mark Sent |
| [**markUnpaid()**](DocumentsApi.md#markUnpaid) | **POST** /api/v1/documents/{document_id}/mark-unpaid | Mark Unpaid |
| [**renderDocument()**](DocumentsApi.md#renderDocument) | **POST** /api/v1/documents/render | Render Document |
| [**restoreDocument()**](DocumentsApi.md#restoreDocument) | **POST** /api/v1/documents/{document_id}/restore | Restore Document |
| [**sendDocument()**](DocumentsApi.md#sendDocument) | **POST** /api/v1/documents/{document_id}/send | Send Document |
| [**updateDocument()**](DocumentsApi.md#updateDocument) | **PATCH** /api/v1/documents/{document_id} | Update Document |
| [**validateDocument()**](DocumentsApi.md#validateDocument) | **POST** /api/v1/documents/validate | Validate Document |
| [**voidDocument()**](DocumentsApi.md#voidDocument) | **POST** /api/v1/documents/{document_id}/void | Void Document |


## `archiveDocument()`

```php
archiveDocument($document_id): \InvoicePDFs\Model\DocumentResponse
```

Archive Document

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\DocumentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$document_id = 'document_id_example'; // string

try {
    $result = $apiInstance->archiveDocument($document_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentsApi->archiveDocument: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **document_id** | **string**|  | |

### Return type

[**\InvoicePDFs\Model\DocumentResponse**](../Model/DocumentResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `calculateDocument()`

```php
calculateDocument($document_calculate_request): \InvoicePDFs\Model\DocumentCalculateResponse
```

Calculate Document

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\DocumentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$document_calculate_request = new \InvoicePDFs\Model\DocumentCalculateRequest(); // \InvoicePDFs\Model\DocumentCalculateRequest

try {
    $result = $apiInstance->calculateDocument($document_calculate_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentsApi->calculateDocument: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **document_calculate_request** | [**\InvoicePDFs\Model\DocumentCalculateRequest**](../Model/DocumentCalculateRequest.md)|  | |

### Return type

[**\InvoicePDFs\Model\DocumentCalculateResponse**](../Model/DocumentCalculateResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createDocument()`

```php
createDocument($document_create_request, $idempotency_key): \InvoicePDFs\Model\DocumentResponse
```

Create Document

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\DocumentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$document_create_request = new \InvoicePDFs\Model\DocumentCreateRequest(); // \InvoicePDFs\Model\DocumentCreateRequest
$idempotency_key = 'idempotency_key_example'; // string

try {
    $result = $apiInstance->createDocument($document_create_request, $idempotency_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentsApi->createDocument: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **document_create_request** | [**\InvoicePDFs\Model\DocumentCreateRequest**](../Model/DocumentCreateRequest.md)|  | |
| **idempotency_key** | **string**|  | [optional] |

### Return type

[**\InvoicePDFs\Model\DocumentResponse**](../Model/DocumentResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createDocumentRender()`

```php
createDocumentRender($document_id, $document_render_options, $idempotency_key): mixed
```

Create Document Render

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\DocumentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$document_id = 'document_id_example'; // string
$document_render_options = new \InvoicePDFs\Model\DocumentRenderOptions(); // \InvoicePDFs\Model\DocumentRenderOptions
$idempotency_key = 'idempotency_key_example'; // string

try {
    $result = $apiInstance->createDocumentRender($document_id, $document_render_options, $idempotency_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentsApi->createDocumentRender: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **document_id** | **string**|  | |
| **document_render_options** | [**\InvoicePDFs\Model\DocumentRenderOptions**](../Model/DocumentRenderOptions.md)|  | |
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

## `deleteDocument()`

```php
deleteDocument($document_id): \InvoicePDFs\Model\SimpleBoolResponse
```

Delete Document

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\DocumentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$document_id = 'document_id_example'; // string

try {
    $result = $apiInstance->deleteDocument($document_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentsApi->deleteDocument: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **document_id** | **string**|  | |

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

## `duplicateDocument()`

```php
duplicateDocument($document_id): \InvoicePDFs\Model\DocumentResponse
```

Duplicate Document

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\DocumentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$document_id = 'document_id_example'; // string

try {
    $result = $apiInstance->duplicateDocument($document_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentsApi->duplicateDocument: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **document_id** | **string**|  | |

### Return type

[**\InvoicePDFs\Model\DocumentResponse**](../Model/DocumentResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `finalizeDocument()`

```php
finalizeDocument($document_id): \InvoicePDFs\Model\DocumentResponse
```

Finalize Document

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\DocumentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$document_id = 'document_id_example'; // string

try {
    $result = $apiInstance->finalizeDocument($document_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentsApi->finalizeDocument: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **document_id** | **string**|  | |

### Return type

[**\InvoicePDFs\Model\DocumentResponse**](../Model/DocumentResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getDocument()`

```php
getDocument($document_id): \InvoicePDFs\Model\DocumentResponse
```

Get Document

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\DocumentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$document_id = 'document_id_example'; // string

try {
    $result = $apiInstance->getDocument($document_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentsApi->getDocument: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **document_id** | **string**|  | |

### Return type

[**\InvoicePDFs\Model\DocumentResponse**](../Model/DocumentResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listDocumentDeliveries()`

```php
listDocumentDeliveries($document_id, $limit, $cursor): \InvoicePDFs\Model\DeliveriesListResponse
```

List Document Deliveries

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\DocumentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$document_id = 'document_id_example'; // string
$limit = 50; // int
$cursor = 'cursor_example'; // string

try {
    $result = $apiInstance->listDocumentDeliveries($document_id, $limit, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentsApi->listDocumentDeliveries: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **document_id** | **string**|  | |
| **limit** | **int**|  | [optional] [default to 50] |
| **cursor** | **string**|  | [optional] |

### Return type

[**\InvoicePDFs\Model\DeliveriesListResponse**](../Model/DeliveriesListResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listDocuments()`

```php
listDocuments($limit, $cursor, $document_type, $status): \InvoicePDFs\Model\DocumentsListResponse
```

List Documents

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\DocumentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$limit = 50; // int
$cursor = 'cursor_example'; // string
$document_type = 'document_type_example'; // string
$status = 'status_example'; // string

try {
    $result = $apiInstance->listDocuments($limit, $cursor, $document_type, $status);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentsApi->listDocuments: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **limit** | **int**|  | [optional] [default to 50] |
| **cursor** | **string**|  | [optional] |
| **document_type** | **string**|  | [optional] |
| **status** | **string**|  | [optional] |

### Return type

[**\InvoicePDFs\Model\DocumentsListResponse**](../Model/DocumentsListResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `markPaid()`

```php
markPaid($document_id): \InvoicePDFs\Model\DocumentResponse
```

Mark Paid

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\DocumentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$document_id = 'document_id_example'; // string

try {
    $result = $apiInstance->markPaid($document_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentsApi->markPaid: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **document_id** | **string**|  | |

### Return type

[**\InvoicePDFs\Model\DocumentResponse**](../Model/DocumentResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `markSent()`

```php
markSent($document_id): \InvoicePDFs\Model\DocumentResponse
```

Mark Sent

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\DocumentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$document_id = 'document_id_example'; // string

try {
    $result = $apiInstance->markSent($document_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentsApi->markSent: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **document_id** | **string**|  | |

### Return type

[**\InvoicePDFs\Model\DocumentResponse**](../Model/DocumentResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `markUnpaid()`

```php
markUnpaid($document_id): \InvoicePDFs\Model\DocumentResponse
```

Mark Unpaid

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\DocumentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$document_id = 'document_id_example'; // string

try {
    $result = $apiInstance->markUnpaid($document_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentsApi->markUnpaid: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **document_id** | **string**|  | |

### Return type

[**\InvoicePDFs\Model\DocumentResponse**](../Model/DocumentResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `renderDocument()`

```php
renderDocument($document_render_request, $idempotency_key): mixed
```

Render Document

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\DocumentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$document_render_request = new \InvoicePDFs\Model\DocumentRenderRequest(); // \InvoicePDFs\Model\DocumentRenderRequest
$idempotency_key = 'idempotency_key_example'; // string

try {
    $result = $apiInstance->renderDocument($document_render_request, $idempotency_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentsApi->renderDocument: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **document_render_request** | [**\InvoicePDFs\Model\DocumentRenderRequest**](../Model/DocumentRenderRequest.md)|  | |
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

## `restoreDocument()`

```php
restoreDocument($document_id): \InvoicePDFs\Model\DocumentResponse
```

Restore Document

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\DocumentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$document_id = 'document_id_example'; // string

try {
    $result = $apiInstance->restoreDocument($document_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentsApi->restoreDocument: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **document_id** | **string**|  | |

### Return type

[**\InvoicePDFs\Model\DocumentResponse**](../Model/DocumentResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `sendDocument()`

```php
sendDocument($document_id, $delivery_send_request): \InvoicePDFs\Model\DeliveryResponse
```

Send Document

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\DocumentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$document_id = 'document_id_example'; // string
$delivery_send_request = new \InvoicePDFs\Model\DeliverySendRequest(); // \InvoicePDFs\Model\DeliverySendRequest

try {
    $result = $apiInstance->sendDocument($document_id, $delivery_send_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentsApi->sendDocument: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **document_id** | **string**|  | |
| **delivery_send_request** | [**\InvoicePDFs\Model\DeliverySendRequest**](../Model/DeliverySendRequest.md)|  | |

### Return type

[**\InvoicePDFs\Model\DeliveryResponse**](../Model/DeliveryResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateDocument()`

```php
updateDocument($document_id, $document_patch_request): \InvoicePDFs\Model\DocumentResponse
```

Update Document

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\DocumentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$document_id = 'document_id_example'; // string
$document_patch_request = new \InvoicePDFs\Model\DocumentPatchRequest(); // \InvoicePDFs\Model\DocumentPatchRequest

try {
    $result = $apiInstance->updateDocument($document_id, $document_patch_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentsApi->updateDocument: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **document_id** | **string**|  | |
| **document_patch_request** | [**\InvoicePDFs\Model\DocumentPatchRequest**](../Model/DocumentPatchRequest.md)|  | |

### Return type

[**\InvoicePDFs\Model\DocumentResponse**](../Model/DocumentResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `validateDocument()`

```php
validateDocument($document_validate_request): \InvoicePDFs\Model\DocumentValidateResponse
```

Validate Document

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\DocumentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$document_validate_request = new \InvoicePDFs\Model\DocumentValidateRequest(); // \InvoicePDFs\Model\DocumentValidateRequest

try {
    $result = $apiInstance->validateDocument($document_validate_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentsApi->validateDocument: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **document_validate_request** | [**\InvoicePDFs\Model\DocumentValidateRequest**](../Model/DocumentValidateRequest.md)|  | |

### Return type

[**\InvoicePDFs\Model\DocumentValidateResponse**](../Model/DocumentValidateResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `voidDocument()`

```php
voidDocument($document_id): \InvoicePDFs\Model\DocumentResponse
```

Void Document

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\DocumentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$document_id = 'document_id_example'; // string

try {
    $result = $apiInstance->voidDocument($document_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentsApi->voidDocument: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **document_id** | **string**|  | |

### Return type

[**\InvoicePDFs\Model\DocumentResponse**](../Model/DocumentResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

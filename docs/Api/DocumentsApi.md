# InvoicePDFs\DocumentsApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**archiveDocumentApiV1DocumentsDocumentIdArchivePost()**](DocumentsApi.md#archiveDocumentApiV1DocumentsDocumentIdArchivePost) | **POST** /api/v1/documents/{document_id}/archive | Archive Document |
| [**calculateDocumentApiV1DocumentsCalculatePost()**](DocumentsApi.md#calculateDocumentApiV1DocumentsCalculatePost) | **POST** /api/v1/documents/calculate | Calculate Document |
| [**createDocumentApiV1DocumentsPost()**](DocumentsApi.md#createDocumentApiV1DocumentsPost) | **POST** /api/v1/documents | Create Document |
| [**deleteDocumentApiV1DocumentsDocumentIdDelete()**](DocumentsApi.md#deleteDocumentApiV1DocumentsDocumentIdDelete) | **DELETE** /api/v1/documents/{document_id} | Delete Document |
| [**duplicateDocumentApiV1DocumentsDocumentIdDuplicatePost()**](DocumentsApi.md#duplicateDocumentApiV1DocumentsDocumentIdDuplicatePost) | **POST** /api/v1/documents/{document_id}/duplicate | Duplicate Document |
| [**finalizeDocumentApiV1DocumentsDocumentIdFinalizePost()**](DocumentsApi.md#finalizeDocumentApiV1DocumentsDocumentIdFinalizePost) | **POST** /api/v1/documents/{document_id}/finalize | Finalize Document |
| [**getDocumentApiV1DocumentsDocumentIdGet()**](DocumentsApi.md#getDocumentApiV1DocumentsDocumentIdGet) | **GET** /api/v1/documents/{document_id} | Get Document |
| [**listDocumentDeliveriesApiV1DocumentsDocumentIdDeliveriesGet()**](DocumentsApi.md#listDocumentDeliveriesApiV1DocumentsDocumentIdDeliveriesGet) | **GET** /api/v1/documents/{document_id}/deliveries | List Document Deliveries |
| [**listDocumentsApiV1DocumentsGet()**](DocumentsApi.md#listDocumentsApiV1DocumentsGet) | **GET** /api/v1/documents | List Documents |
| [**markPaidApiV1DocumentsDocumentIdMarkPaidPost()**](DocumentsApi.md#markPaidApiV1DocumentsDocumentIdMarkPaidPost) | **POST** /api/v1/documents/{document_id}/mark-paid | Mark Paid |
| [**markSentApiV1DocumentsDocumentIdMarkSentPost()**](DocumentsApi.md#markSentApiV1DocumentsDocumentIdMarkSentPost) | **POST** /api/v1/documents/{document_id}/mark-sent | Mark Sent |
| [**markUnpaidApiV1DocumentsDocumentIdMarkUnpaidPost()**](DocumentsApi.md#markUnpaidApiV1DocumentsDocumentIdMarkUnpaidPost) | **POST** /api/v1/documents/{document_id}/mark-unpaid | Mark Unpaid |
| [**patchDocumentApiV1DocumentsDocumentIdPatch()**](DocumentsApi.md#patchDocumentApiV1DocumentsDocumentIdPatch) | **PATCH** /api/v1/documents/{document_id} | Patch Document |
| [**renderDocumentApiV1DocumentsDocumentIdRendersPost()**](DocumentsApi.md#renderDocumentApiV1DocumentsDocumentIdRendersPost) | **POST** /api/v1/documents/{document_id}/renders | Render Document |
| [**renderDocumentApiV1DocumentsRenderPost()**](DocumentsApi.md#renderDocumentApiV1DocumentsRenderPost) | **POST** /api/v1/documents/render | Render Document |
| [**restoreDocumentApiV1DocumentsDocumentIdRestorePost()**](DocumentsApi.md#restoreDocumentApiV1DocumentsDocumentIdRestorePost) | **POST** /api/v1/documents/{document_id}/restore | Restore Document |
| [**sendDocumentApiV1DocumentsDocumentIdSendPost()**](DocumentsApi.md#sendDocumentApiV1DocumentsDocumentIdSendPost) | **POST** /api/v1/documents/{document_id}/send | Send Document |
| [**validateDocumentApiV1DocumentsValidatePost()**](DocumentsApi.md#validateDocumentApiV1DocumentsValidatePost) | **POST** /api/v1/documents/validate | Validate Document |
| [**voidDocumentApiV1DocumentsDocumentIdVoidPost()**](DocumentsApi.md#voidDocumentApiV1DocumentsDocumentIdVoidPost) | **POST** /api/v1/documents/{document_id}/void | Void Document |


## `archiveDocumentApiV1DocumentsDocumentIdArchivePost()`

```php
archiveDocumentApiV1DocumentsDocumentIdArchivePost($document_id): \InvoicePDFs\Model\DocumentResponse
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
    $result = $apiInstance->archiveDocumentApiV1DocumentsDocumentIdArchivePost($document_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentsApi->archiveDocumentApiV1DocumentsDocumentIdArchivePost: ', $e->getMessage(), PHP_EOL;
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

## `calculateDocumentApiV1DocumentsCalculatePost()`

```php
calculateDocumentApiV1DocumentsCalculatePost($document_calculate_request): \InvoicePDFs\Model\DocumentCalculateResponse
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
    $result = $apiInstance->calculateDocumentApiV1DocumentsCalculatePost($document_calculate_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentsApi->calculateDocumentApiV1DocumentsCalculatePost: ', $e->getMessage(), PHP_EOL;
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

## `createDocumentApiV1DocumentsPost()`

```php
createDocumentApiV1DocumentsPost($document_create_request, $idempotency_key): \InvoicePDFs\Model\DocumentResponse
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
    $result = $apiInstance->createDocumentApiV1DocumentsPost($document_create_request, $idempotency_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentsApi->createDocumentApiV1DocumentsPost: ', $e->getMessage(), PHP_EOL;
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

## `deleteDocumentApiV1DocumentsDocumentIdDelete()`

```php
deleteDocumentApiV1DocumentsDocumentIdDelete($document_id): \InvoicePDFs\Model\SimpleBoolResponse
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
    $result = $apiInstance->deleteDocumentApiV1DocumentsDocumentIdDelete($document_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentsApi->deleteDocumentApiV1DocumentsDocumentIdDelete: ', $e->getMessage(), PHP_EOL;
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

## `duplicateDocumentApiV1DocumentsDocumentIdDuplicatePost()`

```php
duplicateDocumentApiV1DocumentsDocumentIdDuplicatePost($document_id): \InvoicePDFs\Model\DocumentResponse
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
    $result = $apiInstance->duplicateDocumentApiV1DocumentsDocumentIdDuplicatePost($document_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentsApi->duplicateDocumentApiV1DocumentsDocumentIdDuplicatePost: ', $e->getMessage(), PHP_EOL;
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

## `finalizeDocumentApiV1DocumentsDocumentIdFinalizePost()`

```php
finalizeDocumentApiV1DocumentsDocumentIdFinalizePost($document_id): \InvoicePDFs\Model\DocumentResponse
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
    $result = $apiInstance->finalizeDocumentApiV1DocumentsDocumentIdFinalizePost($document_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentsApi->finalizeDocumentApiV1DocumentsDocumentIdFinalizePost: ', $e->getMessage(), PHP_EOL;
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

## `getDocumentApiV1DocumentsDocumentIdGet()`

```php
getDocumentApiV1DocumentsDocumentIdGet($document_id): \InvoicePDFs\Model\DocumentResponse
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
    $result = $apiInstance->getDocumentApiV1DocumentsDocumentIdGet($document_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentsApi->getDocumentApiV1DocumentsDocumentIdGet: ', $e->getMessage(), PHP_EOL;
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

## `listDocumentDeliveriesApiV1DocumentsDocumentIdDeliveriesGet()`

```php
listDocumentDeliveriesApiV1DocumentsDocumentIdDeliveriesGet($document_id, $limit, $cursor): \InvoicePDFs\Model\DeliveriesListResponse
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
    $result = $apiInstance->listDocumentDeliveriesApiV1DocumentsDocumentIdDeliveriesGet($document_id, $limit, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentsApi->listDocumentDeliveriesApiV1DocumentsDocumentIdDeliveriesGet: ', $e->getMessage(), PHP_EOL;
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

## `listDocumentsApiV1DocumentsGet()`

```php
listDocumentsApiV1DocumentsGet($limit, $cursor, $document_type, $status): \InvoicePDFs\Model\DocumentsListResponse
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
    $result = $apiInstance->listDocumentsApiV1DocumentsGet($limit, $cursor, $document_type, $status);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentsApi->listDocumentsApiV1DocumentsGet: ', $e->getMessage(), PHP_EOL;
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

## `markPaidApiV1DocumentsDocumentIdMarkPaidPost()`

```php
markPaidApiV1DocumentsDocumentIdMarkPaidPost($document_id): \InvoicePDFs\Model\DocumentResponse
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
    $result = $apiInstance->markPaidApiV1DocumentsDocumentIdMarkPaidPost($document_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentsApi->markPaidApiV1DocumentsDocumentIdMarkPaidPost: ', $e->getMessage(), PHP_EOL;
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

## `markSentApiV1DocumentsDocumentIdMarkSentPost()`

```php
markSentApiV1DocumentsDocumentIdMarkSentPost($document_id): \InvoicePDFs\Model\DocumentResponse
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
    $result = $apiInstance->markSentApiV1DocumentsDocumentIdMarkSentPost($document_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentsApi->markSentApiV1DocumentsDocumentIdMarkSentPost: ', $e->getMessage(), PHP_EOL;
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

## `markUnpaidApiV1DocumentsDocumentIdMarkUnpaidPost()`

```php
markUnpaidApiV1DocumentsDocumentIdMarkUnpaidPost($document_id): \InvoicePDFs\Model\DocumentResponse
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
    $result = $apiInstance->markUnpaidApiV1DocumentsDocumentIdMarkUnpaidPost($document_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentsApi->markUnpaidApiV1DocumentsDocumentIdMarkUnpaidPost: ', $e->getMessage(), PHP_EOL;
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

## `patchDocumentApiV1DocumentsDocumentIdPatch()`

```php
patchDocumentApiV1DocumentsDocumentIdPatch($document_id, $document_patch_request): \InvoicePDFs\Model\DocumentResponse
```

Patch Document

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
    $result = $apiInstance->patchDocumentApiV1DocumentsDocumentIdPatch($document_id, $document_patch_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentsApi->patchDocumentApiV1DocumentsDocumentIdPatch: ', $e->getMessage(), PHP_EOL;
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

## `renderDocumentApiV1DocumentsDocumentIdRendersPost()`

```php
renderDocumentApiV1DocumentsDocumentIdRendersPost($document_id, $app_documents_schemas_document_render_request, $idempotency_key): mixed
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
$document_id = 'document_id_example'; // string
$app_documents_schemas_document_render_request = new \InvoicePDFs\Model\AppDocumentsSchemasDocumentRenderRequest(); // \InvoicePDFs\Model\AppDocumentsSchemasDocumentRenderRequest
$idempotency_key = 'idempotency_key_example'; // string

try {
    $result = $apiInstance->renderDocumentApiV1DocumentsDocumentIdRendersPost($document_id, $app_documents_schemas_document_render_request, $idempotency_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentsApi->renderDocumentApiV1DocumentsDocumentIdRendersPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **document_id** | **string**|  | |
| **app_documents_schemas_document_render_request** | [**\InvoicePDFs\Model\AppDocumentsSchemasDocumentRenderRequest**](../Model/AppDocumentsSchemasDocumentRenderRequest.md)|  | |
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

## `renderDocumentApiV1DocumentsRenderPost()`

```php
renderDocumentApiV1DocumentsRenderPost($app_schemas_v1_document_render_request, $idempotency_key): mixed
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
$app_schemas_v1_document_render_request = new \InvoicePDFs\Model\AppSchemasV1DocumentRenderRequest(); // \InvoicePDFs\Model\AppSchemasV1DocumentRenderRequest
$idempotency_key = 'idempotency_key_example'; // string

try {
    $result = $apiInstance->renderDocumentApiV1DocumentsRenderPost($app_schemas_v1_document_render_request, $idempotency_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentsApi->renderDocumentApiV1DocumentsRenderPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **app_schemas_v1_document_render_request** | [**\InvoicePDFs\Model\AppSchemasV1DocumentRenderRequest**](../Model/AppSchemasV1DocumentRenderRequest.md)|  | |
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

## `restoreDocumentApiV1DocumentsDocumentIdRestorePost()`

```php
restoreDocumentApiV1DocumentsDocumentIdRestorePost($document_id): \InvoicePDFs\Model\DocumentResponse
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
    $result = $apiInstance->restoreDocumentApiV1DocumentsDocumentIdRestorePost($document_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentsApi->restoreDocumentApiV1DocumentsDocumentIdRestorePost: ', $e->getMessage(), PHP_EOL;
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

## `sendDocumentApiV1DocumentsDocumentIdSendPost()`

```php
sendDocumentApiV1DocumentsDocumentIdSendPost($document_id, $delivery_send_request): \InvoicePDFs\Model\DeliveryResponse
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
    $result = $apiInstance->sendDocumentApiV1DocumentsDocumentIdSendPost($document_id, $delivery_send_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentsApi->sendDocumentApiV1DocumentsDocumentIdSendPost: ', $e->getMessage(), PHP_EOL;
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

## `validateDocumentApiV1DocumentsValidatePost()`

```php
validateDocumentApiV1DocumentsValidatePost($document_validate_request): \InvoicePDFs\Model\DocumentValidateResponse
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
    $result = $apiInstance->validateDocumentApiV1DocumentsValidatePost($document_validate_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentsApi->validateDocumentApiV1DocumentsValidatePost: ', $e->getMessage(), PHP_EOL;
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

## `voidDocumentApiV1DocumentsDocumentIdVoidPost()`

```php
voidDocumentApiV1DocumentsDocumentIdVoidPost($document_id): \InvoicePDFs\Model\DocumentResponse
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
    $result = $apiInstance->voidDocumentApiV1DocumentsDocumentIdVoidPost($document_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentsApi->voidDocumentApiV1DocumentsDocumentIdVoidPost: ', $e->getMessage(), PHP_EOL;
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

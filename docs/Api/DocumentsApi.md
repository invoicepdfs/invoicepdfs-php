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

Move a document out of the active list.  Archiving hides a document from the default listing without destroying it; `restore_document` brings it back. Drafts are deleted rather than archived.

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

Compute the totals for a document without storing or rendering it.  Returns the same breakdown — subtotal, discounts, tax, shipping, total — that a render would print, so a checkout page can show a figure before committing to one.

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

Create a document in `draft`.  Totals are computed and stored at creation, so the figures you read back are the ones that were issued rather than a recalculation. Nothing is rendered — use `create_document_render` once the document is final.

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
createDocumentRender($document_id, $document_render_options, $idempotency_key): \InvoicePDFs\Model\RenderResponse
```

Create Document Render

Render a stored document to a PDF.  Use this when the document lives here. To render one you hold yourself, without storing it, use `render_document`.  The response carries a signed `download_url` that needs no API key, valid until `expires_at`.

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

[**\InvoicePDFs\Model\RenderResponse**](../Model/RenderResponse.md)

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

Permanently remove a `draft`.  `409` if anything still points at it — a render, a delivery or a payment — naming what does. Finalized documents are voided or archived, not deleted.

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

Copy a document into a new `draft`.  The copy gets the next available number rather than the original's, so it can be finalized without colliding with the document it came from.

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

Issue a `draft`: fix its number and totals.  From here the document is a record. It can be sent, marked paid, voided or archived, but not edited — `update_document` returns `409` afterwards.

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

One document, with the totals stored when it was created.

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

Every email delivery attempted for this document.  One row per attempt, newest first, including the ones that failed — which is where to look when a customer says the invoice never arrived.

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

Every document on the account, newest first.  Cursor-paginated: pass the `next_cursor` from a response to fetch the page after it. Filter by `document_type` or `status` to narrow the list.

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

Record that the document was paid in full.

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

Record that the document reached the customer.  **This does not send anything** — it only moves the status, for when the document was delivered by some means of your own. Use `send_document` to have us email it.

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

Undo `mark_paid`, returning the document to `sent`.  For a payment that was recorded in error or later reversed.

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
renderDocument($document_render_request, $idempotency_key): \InvoicePDFs\Model\RenderResponse
```

Render Document

Render a document supplied inline, storing nothing but the PDF.  The stateless path: pass the whole document in the body and get a PDF back, with no customer, business profile or stored document required. To render a document that already lives here, use `create_document_render`.  Returns JSON with a signed `download_url` by default. Ask for the bytes directly with `output.delivery: \"binary\"` or `Accept: application/pdf`.

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

[**\InvoicePDFs\Model\RenderResponse**](../Model/RenderResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`, `application/pdf`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `restoreDocument()`

```php
restoreDocument($document_id): \InvoicePDFs\Model\DocumentResponse
```

Restore Document

Bring an archived document back to `finalized`.

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

Queue the document to be emailed.  Returns 202 with the delivery in `queued`. The mail is sent in the background and retried on transient failure; poll `GET /deliveries/{id}` for the outcome.

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

Change a document that is still a `draft`.  A finalized document is a record of what was issued and cannot be edited; `409` if it has moved past `draft`. Only the fields you send are changed — omit one to leave it alone, and send `null` to clear it.

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

Check that a document body is well-formed, without pricing it.  The cheapest of the three stateless operations: no totals are computed and no PDF is produced. Use `calculate_document` for the money and `render_document` for the document.

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

Cancel a document that was issued.  Voiding is how a finalized document is withdrawn, since it cannot be deleted. The PDF renders with a `VOID` mark from then on, so a copy already sent is distinguishable from the live one.

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

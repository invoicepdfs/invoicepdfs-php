# InvoicePDFs\DocumentAttachmentsApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createDocumentAttachment()**](DocumentAttachmentsApi.md#createDocumentAttachment) | **POST** /api/v1/documents/{document_id}/attachments | Create Document Attachment |
| [**deleteDocumentAttachment()**](DocumentAttachmentsApi.md#deleteDocumentAttachment) | **DELETE** /api/v1/documents/{document_id}/attachments/{attachment_id} | Delete Document Attachment |
| [**listDocumentAttachments()**](DocumentAttachmentsApi.md#listDocumentAttachments) | **GET** /api/v1/documents/{document_id}/attachments | List Document Attachments |


## `createDocumentAttachment()`

```php
createDocumentAttachment($document_id, $invoice_attachment_create_request): \InvoicePDFs\Model\InvoiceAttachmentResponse
```

Create Document Attachment

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\DocumentAttachmentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$document_id = 'document_id_example'; // string
$invoice_attachment_create_request = new \InvoicePDFs\Model\InvoiceAttachmentCreateRequest(); // \InvoicePDFs\Model\InvoiceAttachmentCreateRequest

try {
    $result = $apiInstance->createDocumentAttachment($document_id, $invoice_attachment_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentAttachmentsApi->createDocumentAttachment: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **document_id** | **string**|  | |
| **invoice_attachment_create_request** | [**\InvoicePDFs\Model\InvoiceAttachmentCreateRequest**](../Model/InvoiceAttachmentCreateRequest.md)|  | |

### Return type

[**\InvoicePDFs\Model\InvoiceAttachmentResponse**](../Model/InvoiceAttachmentResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteDocumentAttachment()`

```php
deleteDocumentAttachment($document_id, $attachment_id): \InvoicePDFs\Model\SimpleBoolResponse
```

Delete Document Attachment

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\DocumentAttachmentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$document_id = 'document_id_example'; // string
$attachment_id = 'attachment_id_example'; // string

try {
    $result = $apiInstance->deleteDocumentAttachment($document_id, $attachment_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentAttachmentsApi->deleteDocumentAttachment: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **document_id** | **string**|  | |
| **attachment_id** | **string**|  | |

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

## `listDocumentAttachments()`

```php
listDocumentAttachments($document_id): \InvoicePDFs\Model\InvoiceAttachmentsListResponse
```

List Document Attachments

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\DocumentAttachmentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$document_id = 'document_id_example'; // string

try {
    $result = $apiInstance->listDocumentAttachments($document_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentAttachmentsApi->listDocumentAttachments: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **document_id** | **string**|  | |

### Return type

[**\InvoicePDFs\Model\InvoiceAttachmentsListResponse**](../Model/InvoiceAttachmentsListResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

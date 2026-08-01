# InvoicePDFs\InvoiceAttachmentsApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createAttachmentApiV1DocumentsInvoiceIdAttachmentsPost()**](InvoiceAttachmentsApi.md#createAttachmentApiV1DocumentsInvoiceIdAttachmentsPost) | **POST** /api/v1/documents/{invoice_id}/attachments | Create Attachment |
| [**deleteAttachmentApiV1DocumentsInvoiceIdAttachmentsAttachmentIdDelete()**](InvoiceAttachmentsApi.md#deleteAttachmentApiV1DocumentsInvoiceIdAttachmentsAttachmentIdDelete) | **DELETE** /api/v1/documents/{invoice_id}/attachments/{attachment_id} | Delete Attachment |
| [**listAttachmentsApiV1DocumentsInvoiceIdAttachmentsGet()**](InvoiceAttachmentsApi.md#listAttachmentsApiV1DocumentsInvoiceIdAttachmentsGet) | **GET** /api/v1/documents/{invoice_id}/attachments | List Attachments |


## `createAttachmentApiV1DocumentsInvoiceIdAttachmentsPost()`

```php
createAttachmentApiV1DocumentsInvoiceIdAttachmentsPost($invoice_id, $invoice_attachment_create_request): \InvoicePDFs\Model\InvoiceAttachmentResponse
```

Create Attachment

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\InvoiceAttachmentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$invoice_id = 'invoice_id_example'; // string
$invoice_attachment_create_request = new \InvoicePDFs\Model\InvoiceAttachmentCreateRequest(); // \InvoicePDFs\Model\InvoiceAttachmentCreateRequest

try {
    $result = $apiInstance->createAttachmentApiV1DocumentsInvoiceIdAttachmentsPost($invoice_id, $invoice_attachment_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InvoiceAttachmentsApi->createAttachmentApiV1DocumentsInvoiceIdAttachmentsPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invoice_id** | **string**|  | |
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

## `deleteAttachmentApiV1DocumentsInvoiceIdAttachmentsAttachmentIdDelete()`

```php
deleteAttachmentApiV1DocumentsInvoiceIdAttachmentsAttachmentIdDelete($invoice_id, $attachment_id): \InvoicePDFs\Model\SimpleBoolResponse
```

Delete Attachment

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\InvoiceAttachmentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$invoice_id = 'invoice_id_example'; // string
$attachment_id = 'attachment_id_example'; // string

try {
    $result = $apiInstance->deleteAttachmentApiV1DocumentsInvoiceIdAttachmentsAttachmentIdDelete($invoice_id, $attachment_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InvoiceAttachmentsApi->deleteAttachmentApiV1DocumentsInvoiceIdAttachmentsAttachmentIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invoice_id** | **string**|  | |
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

## `listAttachmentsApiV1DocumentsInvoiceIdAttachmentsGet()`

```php
listAttachmentsApiV1DocumentsInvoiceIdAttachmentsGet($invoice_id): \InvoicePDFs\Model\InvoiceAttachmentsListResponse
```

List Attachments

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\InvoiceAttachmentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$invoice_id = 'invoice_id_example'; // string

try {
    $result = $apiInstance->listAttachmentsApiV1DocumentsInvoiceIdAttachmentsGet($invoice_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InvoiceAttachmentsApi->listAttachmentsApiV1DocumentsInvoiceIdAttachmentsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invoice_id** | **string**|  | |

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

# OpenAPI\Client\InvoiceAttachmentsApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createAttachmentApiV1InvoicesInvoiceIdAttachmentsPost()**](InvoiceAttachmentsApi.md#createAttachmentApiV1InvoicesInvoiceIdAttachmentsPost) | **POST** /api/v1/invoices/{invoice_id}/attachments | Create Attachment |
| [**deleteAttachmentApiV1InvoicesInvoiceIdAttachmentsAttachmentIdDelete()**](InvoiceAttachmentsApi.md#deleteAttachmentApiV1InvoicesInvoiceIdAttachmentsAttachmentIdDelete) | **DELETE** /api/v1/invoices/{invoice_id}/attachments/{attachment_id} | Delete Attachment |
| [**listAttachmentsApiV1InvoicesInvoiceIdAttachmentsGet()**](InvoiceAttachmentsApi.md#listAttachmentsApiV1InvoicesInvoiceIdAttachmentsGet) | **GET** /api/v1/invoices/{invoice_id}/attachments | List Attachments |


## `createAttachmentApiV1InvoicesInvoiceIdAttachmentsPost()`

```php
createAttachmentApiV1InvoicesInvoiceIdAttachmentsPost($invoice_id, $invoice_attachment_create_request): \OpenAPI\Client\Model\InvoiceAttachmentResponse
```

Create Attachment

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\InvoiceAttachmentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$invoice_id = 'invoice_id_example'; // string
$invoice_attachment_create_request = new \OpenAPI\Client\Model\InvoiceAttachmentCreateRequest(); // \OpenAPI\Client\Model\InvoiceAttachmentCreateRequest

try {
    $result = $apiInstance->createAttachmentApiV1InvoicesInvoiceIdAttachmentsPost($invoice_id, $invoice_attachment_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InvoiceAttachmentsApi->createAttachmentApiV1InvoicesInvoiceIdAttachmentsPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invoice_id** | **string**|  | |
| **invoice_attachment_create_request** | [**\OpenAPI\Client\Model\InvoiceAttachmentCreateRequest**](../Model/InvoiceAttachmentCreateRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\InvoiceAttachmentResponse**](../Model/InvoiceAttachmentResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteAttachmentApiV1InvoicesInvoiceIdAttachmentsAttachmentIdDelete()`

```php
deleteAttachmentApiV1InvoicesInvoiceIdAttachmentsAttachmentIdDelete($invoice_id, $attachment_id): \OpenAPI\Client\Model\SimpleBoolResponse
```

Delete Attachment

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\InvoiceAttachmentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$invoice_id = 'invoice_id_example'; // string
$attachment_id = 'attachment_id_example'; // string

try {
    $result = $apiInstance->deleteAttachmentApiV1InvoicesInvoiceIdAttachmentsAttachmentIdDelete($invoice_id, $attachment_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InvoiceAttachmentsApi->deleteAttachmentApiV1InvoicesInvoiceIdAttachmentsAttachmentIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invoice_id** | **string**|  | |
| **attachment_id** | **string**|  | |

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

## `listAttachmentsApiV1InvoicesInvoiceIdAttachmentsGet()`

```php
listAttachmentsApiV1InvoicesInvoiceIdAttachmentsGet($invoice_id): \OpenAPI\Client\Model\InvoiceAttachmentsListResponse
```

List Attachments

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\InvoiceAttachmentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$invoice_id = 'invoice_id_example'; // string

try {
    $result = $apiInstance->listAttachmentsApiV1InvoicesInvoiceIdAttachmentsGet($invoice_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InvoiceAttachmentsApi->listAttachmentsApiV1InvoicesInvoiceIdAttachmentsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invoice_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\InvoiceAttachmentsListResponse**](../Model/InvoiceAttachmentsListResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

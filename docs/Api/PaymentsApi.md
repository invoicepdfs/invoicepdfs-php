# InvoicePDFs\PaymentsApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createDocumentPayment()**](PaymentsApi.md#createDocumentPayment) | **POST** /api/v1/documents/{document_id}/payments | Create Document Payment |
| [**deletePayment()**](PaymentsApi.md#deletePayment) | **DELETE** /api/v1/payments/{payment_id} | Delete Payment |
| [**getPayment()**](PaymentsApi.md#getPayment) | **GET** /api/v1/payments/{payment_id} | Get Payment |
| [**listDocumentPayments()**](PaymentsApi.md#listDocumentPayments) | **GET** /api/v1/documents/{document_id}/payments | List Document Payments |
| [**updatePayment()**](PaymentsApi.md#updatePayment) | **PATCH** /api/v1/payments/{payment_id} | Update Payment |


## `createDocumentPayment()`

```php
createDocumentPayment($document_id, $payment_create_request): \InvoicePDFs\Model\PaymentResponse
```

Create Document Payment

Record a payment received against an invoice.  The currency is taken from the invoice rather than from the request, so a payment can never disagree with what was billed.  Refused with 409 while the invoice is still a draft. Recording a payment does not move the invoice to `paid` — use `mark_paid` for that.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\PaymentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$document_id = 'document_id_example'; // string
$payment_create_request = new \InvoicePDFs\Model\PaymentCreateRequest(); // \InvoicePDFs\Model\PaymentCreateRequest

try {
    $result = $apiInstance->createDocumentPayment($document_id, $payment_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PaymentsApi->createDocumentPayment: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **document_id** | **string**|  | |
| **payment_create_request** | [**\InvoicePDFs\Model\PaymentCreateRequest**](../Model/PaymentCreateRequest.md)|  | |

### Return type

[**\InvoicePDFs\Model\PaymentResponse**](../Model/PaymentResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deletePayment()`

```php
deletePayment($payment_id): \InvoicePDFs\Model\SimpleBoolResponse
```

Delete Payment

Remove a recorded payment.  The payment is deleted outright rather than reversed, and the invoice's status is left alone. The deletion is kept in the audit log.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\PaymentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$payment_id = 'payment_id_example'; // string

try {
    $result = $apiInstance->deletePayment($payment_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PaymentsApi->deletePayment: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **payment_id** | **string**|  | |

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

## `getPayment()`

```php
getPayment($payment_id): \InvoicePDFs\Model\PaymentResponse
```

Get Payment

One recorded payment by id.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\PaymentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$payment_id = 'payment_id_example'; // string

try {
    $result = $apiInstance->getPayment($payment_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PaymentsApi->getPayment: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **payment_id** | **string**|  | |

### Return type

[**\InvoicePDFs\Model\PaymentResponse**](../Model/PaymentResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listDocumentPayments()`

```php
listDocumentPayments($document_id, $limit, $cursor): \InvoicePDFs\Model\PaymentsListResponse
```

List Document Payments

Payments recorded against one document, newest first.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\PaymentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$document_id = 'document_id_example'; // string
$limit = 50; // int
$cursor = 'cursor_example'; // string

try {
    $result = $apiInstance->listDocumentPayments($document_id, $limit, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PaymentsApi->listDocumentPayments: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **document_id** | **string**|  | |
| **limit** | **int**|  | [optional] [default to 50] |
| **cursor** | **string**|  | [optional] |

### Return type

[**\InvoicePDFs\Model\PaymentsListResponse**](../Model/PaymentsListResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updatePayment()`

```php
updatePayment($payment_id, $payment_patch_request): \InvoicePDFs\Model\PaymentResponse
```

Update Payment

Correct a payment that was already recorded.  Only the fields you send are changed. The invoice's status and totals are left alone.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\PaymentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$payment_id = 'payment_id_example'; // string
$payment_patch_request = new \InvoicePDFs\Model\PaymentPatchRequest(); // \InvoicePDFs\Model\PaymentPatchRequest

try {
    $result = $apiInstance->updatePayment($payment_id, $payment_patch_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PaymentsApi->updatePayment: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **payment_id** | **string**|  | |
| **payment_patch_request** | [**\InvoicePDFs\Model\PaymentPatchRequest**](../Model/PaymentPatchRequest.md)|  | |

### Return type

[**\InvoicePDFs\Model\PaymentResponse**](../Model/PaymentResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

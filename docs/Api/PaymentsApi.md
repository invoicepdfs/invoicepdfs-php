# OpenAPI\Client\PaymentsApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createPaymentApiV1InvoicesInvoiceIdPaymentsPost()**](PaymentsApi.md#createPaymentApiV1InvoicesInvoiceIdPaymentsPost) | **POST** /api/v1/invoices/{invoice_id}/payments | Create Payment |
| [**deletePaymentApiV1PaymentsPaymentIdDelete()**](PaymentsApi.md#deletePaymentApiV1PaymentsPaymentIdDelete) | **DELETE** /api/v1/payments/{payment_id} | Delete Payment |
| [**getPaymentApiV1PaymentsPaymentIdGet()**](PaymentsApi.md#getPaymentApiV1PaymentsPaymentIdGet) | **GET** /api/v1/payments/{payment_id} | Get Payment |
| [**listInvoicePaymentsApiV1InvoicesInvoiceIdPaymentsGet()**](PaymentsApi.md#listInvoicePaymentsApiV1InvoicesInvoiceIdPaymentsGet) | **GET** /api/v1/invoices/{invoice_id}/payments | List Invoice Payments |
| [**updatePaymentApiV1PaymentsPaymentIdPatch()**](PaymentsApi.md#updatePaymentApiV1PaymentsPaymentIdPatch) | **PATCH** /api/v1/payments/{payment_id} | Update Payment |


## `createPaymentApiV1InvoicesInvoiceIdPaymentsPost()`

```php
createPaymentApiV1InvoicesInvoiceIdPaymentsPost($invoice_id, $payment_create_request): \OpenAPI\Client\Model\PaymentResponse
```

Create Payment

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PaymentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$invoice_id = 'invoice_id_example'; // string
$payment_create_request = new \OpenAPI\Client\Model\PaymentCreateRequest(); // \OpenAPI\Client\Model\PaymentCreateRequest

try {
    $result = $apiInstance->createPaymentApiV1InvoicesInvoiceIdPaymentsPost($invoice_id, $payment_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PaymentsApi->createPaymentApiV1InvoicesInvoiceIdPaymentsPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invoice_id** | **string**|  | |
| **payment_create_request** | [**\OpenAPI\Client\Model\PaymentCreateRequest**](../Model/PaymentCreateRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\PaymentResponse**](../Model/PaymentResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deletePaymentApiV1PaymentsPaymentIdDelete()`

```php
deletePaymentApiV1PaymentsPaymentIdDelete($payment_id): \OpenAPI\Client\Model\SimpleBoolResponse
```

Delete Payment

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PaymentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$payment_id = 'payment_id_example'; // string

try {
    $result = $apiInstance->deletePaymentApiV1PaymentsPaymentIdDelete($payment_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PaymentsApi->deletePaymentApiV1PaymentsPaymentIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **payment_id** | **string**|  | |

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

## `getPaymentApiV1PaymentsPaymentIdGet()`

```php
getPaymentApiV1PaymentsPaymentIdGet($payment_id): \OpenAPI\Client\Model\PaymentResponse
```

Get Payment

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PaymentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$payment_id = 'payment_id_example'; // string

try {
    $result = $apiInstance->getPaymentApiV1PaymentsPaymentIdGet($payment_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PaymentsApi->getPaymentApiV1PaymentsPaymentIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **payment_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\PaymentResponse**](../Model/PaymentResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listInvoicePaymentsApiV1InvoicesInvoiceIdPaymentsGet()`

```php
listInvoicePaymentsApiV1InvoicesInvoiceIdPaymentsGet($invoice_id, $limit, $cursor): \OpenAPI\Client\Model\PaymentsListResponse
```

List Invoice Payments

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PaymentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$invoice_id = 'invoice_id_example'; // string
$limit = 50; // int
$cursor = 'cursor_example'; // string

try {
    $result = $apiInstance->listInvoicePaymentsApiV1InvoicesInvoiceIdPaymentsGet($invoice_id, $limit, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PaymentsApi->listInvoicePaymentsApiV1InvoicesInvoiceIdPaymentsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invoice_id** | **string**|  | |
| **limit** | **int**|  | [optional] [default to 50] |
| **cursor** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\PaymentsListResponse**](../Model/PaymentsListResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updatePaymentApiV1PaymentsPaymentIdPatch()`

```php
updatePaymentApiV1PaymentsPaymentIdPatch($payment_id, $payment_patch_request): \OpenAPI\Client\Model\PaymentResponse
```

Update Payment

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PaymentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$payment_id = 'payment_id_example'; // string
$payment_patch_request = new \OpenAPI\Client\Model\PaymentPatchRequest(); // \OpenAPI\Client\Model\PaymentPatchRequest

try {
    $result = $apiInstance->updatePaymentApiV1PaymentsPaymentIdPatch($payment_id, $payment_patch_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PaymentsApi->updatePaymentApiV1PaymentsPaymentIdPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **payment_id** | **string**|  | |
| **payment_patch_request** | [**\OpenAPI\Client\Model\PaymentPatchRequest**](../Model/PaymentPatchRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\PaymentResponse**](../Model/PaymentResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

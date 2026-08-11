# InvoicePDFs\CustomersApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createCustomer()**](CustomersApi.md#createCustomer) | **POST** /api/v1/customers | Create Customer |
| [**deleteCustomer()**](CustomersApi.md#deleteCustomer) | **DELETE** /api/v1/customers/{customer_id} | Delete Customer |
| [**getCustomer()**](CustomersApi.md#getCustomer) | **GET** /api/v1/customers/{customer_id} | Get Customer |
| [**listCustomers()**](CustomersApi.md#listCustomers) | **GET** /api/v1/customers | List Customers |
| [**updateCustomer()**](CustomersApi.md#updateCustomer) | **PATCH** /api/v1/customers/{customer_id} | Update Customer |


## `createCustomer()`

```php
createCustomer($customer_create, $idempotency_key): \InvoicePDFs\Model\CustomerResponse
```

Create Customer

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\CustomersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$customer_create = new \InvoicePDFs\Model\CustomerCreate(); // \InvoicePDFs\Model\CustomerCreate
$idempotency_key = 'idempotency_key_example'; // string

try {
    $result = $apiInstance->createCustomer($customer_create, $idempotency_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomersApi->createCustomer: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **customer_create** | [**\InvoicePDFs\Model\CustomerCreate**](../Model/CustomerCreate.md)|  | |
| **idempotency_key** | **string**|  | [optional] |

### Return type

[**\InvoicePDFs\Model\CustomerResponse**](../Model/CustomerResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteCustomer()`

```php
deleteCustomer($customer_id): \InvoicePDFs\Model\SimpleBoolResponse
```

Delete Customer

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\CustomersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$customer_id = 'customer_id_example'; // string

try {
    $result = $apiInstance->deleteCustomer($customer_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomersApi->deleteCustomer: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **customer_id** | **string**|  | |

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

## `getCustomer()`

```php
getCustomer($customer_id): \InvoicePDFs\Model\CustomerResponse
```

Get Customer

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\CustomersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$customer_id = 'customer_id_example'; // string

try {
    $result = $apiInstance->getCustomer($customer_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomersApi->getCustomer: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **customer_id** | **string**|  | |

### Return type

[**\InvoicePDFs\Model\CustomerResponse**](../Model/CustomerResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listCustomers()`

```php
listCustomers($limit, $cursor): \InvoicePDFs\Model\CustomersListResponse
```

List Customers

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\CustomersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$limit = 50; // int
$cursor = 'cursor_example'; // string

try {
    $result = $apiInstance->listCustomers($limit, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomersApi->listCustomers: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **limit** | **int**|  | [optional] [default to 50] |
| **cursor** | **string**|  | [optional] |

### Return type

[**\InvoicePDFs\Model\CustomersListResponse**](../Model/CustomersListResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateCustomer()`

```php
updateCustomer($customer_id, $customer_patch, $idempotency_key): \InvoicePDFs\Model\CustomerResponse
```

Update Customer

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\CustomersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$customer_id = 'customer_id_example'; // string
$customer_patch = new \InvoicePDFs\Model\CustomerPatch(); // \InvoicePDFs\Model\CustomerPatch
$idempotency_key = 'idempotency_key_example'; // string

try {
    $result = $apiInstance->updateCustomer($customer_id, $customer_patch, $idempotency_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomersApi->updateCustomer: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **customer_id** | **string**|  | |
| **customer_patch** | [**\InvoicePDFs\Model\CustomerPatch**](../Model/CustomerPatch.md)|  | |
| **idempotency_key** | **string**|  | [optional] |

### Return type

[**\InvoicePDFs\Model\CustomerResponse**](../Model/CustomerResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

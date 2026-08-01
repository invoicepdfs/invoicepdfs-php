# InvoicePDFs\CustomersApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createCustomerApiV1CustomersPost()**](CustomersApi.md#createCustomerApiV1CustomersPost) | **POST** /api/v1/customers | Create Customer |
| [**deleteCustomerApiV1CustomersCustomerIdDelete()**](CustomersApi.md#deleteCustomerApiV1CustomersCustomerIdDelete) | **DELETE** /api/v1/customers/{customer_id} | Delete Customer |
| [**getCustomerApiV1CustomersCustomerIdGet()**](CustomersApi.md#getCustomerApiV1CustomersCustomerIdGet) | **GET** /api/v1/customers/{customer_id} | Get Customer |
| [**listCustomersApiV1CustomersGet()**](CustomersApi.md#listCustomersApiV1CustomersGet) | **GET** /api/v1/customers | List Customers |
| [**patchCustomerApiV1CustomersCustomerIdPatch()**](CustomersApi.md#patchCustomerApiV1CustomersCustomerIdPatch) | **PATCH** /api/v1/customers/{customer_id} | Patch Customer |


## `createCustomerApiV1CustomersPost()`

```php
createCustomerApiV1CustomersPost($customer_create, $idempotency_key): \InvoicePDFs\Model\CustomerResponse
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
    $result = $apiInstance->createCustomerApiV1CustomersPost($customer_create, $idempotency_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomersApi->createCustomerApiV1CustomersPost: ', $e->getMessage(), PHP_EOL;
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

## `deleteCustomerApiV1CustomersCustomerIdDelete()`

```php
deleteCustomerApiV1CustomersCustomerIdDelete($customer_id): \InvoicePDFs\Model\SimpleBoolResponse
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
    $result = $apiInstance->deleteCustomerApiV1CustomersCustomerIdDelete($customer_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomersApi->deleteCustomerApiV1CustomersCustomerIdDelete: ', $e->getMessage(), PHP_EOL;
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

## `getCustomerApiV1CustomersCustomerIdGet()`

```php
getCustomerApiV1CustomersCustomerIdGet($customer_id): \InvoicePDFs\Model\CustomerResponse
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
    $result = $apiInstance->getCustomerApiV1CustomersCustomerIdGet($customer_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomersApi->getCustomerApiV1CustomersCustomerIdGet: ', $e->getMessage(), PHP_EOL;
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

## `listCustomersApiV1CustomersGet()`

```php
listCustomersApiV1CustomersGet($limit, $cursor): \InvoicePDFs\Model\CustomersListResponse
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
    $result = $apiInstance->listCustomersApiV1CustomersGet($limit, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomersApi->listCustomersApiV1CustomersGet: ', $e->getMessage(), PHP_EOL;
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

## `patchCustomerApiV1CustomersCustomerIdPatch()`

```php
patchCustomerApiV1CustomersCustomerIdPatch($customer_id, $customer_patch, $idempotency_key): \InvoicePDFs\Model\CustomerResponse
```

Patch Customer

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
    $result = $apiInstance->patchCustomerApiV1CustomersCustomerIdPatch($customer_id, $customer_patch, $idempotency_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomersApi->patchCustomerApiV1CustomersCustomerIdPatch: ', $e->getMessage(), PHP_EOL;
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

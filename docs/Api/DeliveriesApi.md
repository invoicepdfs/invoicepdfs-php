# InvoicePDFs\DeliveriesApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getDelivery()**](DeliveriesApi.md#getDelivery) | **GET** /api/v1/deliveries/{delivery_id} | Get Delivery |
| [**retryDelivery()**](DeliveriesApi.md#retryDelivery) | **POST** /api/v1/deliveries/{delivery_id}/retry | Retry Delivery |


## `getDelivery()`

```php
getDelivery($delivery_id): \InvoicePDFs\Model\DeliveryResponse
```

Get Delivery

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\DeliveriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$delivery_id = 'delivery_id_example'; // string

try {
    $result = $apiInstance->getDelivery($delivery_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeliveriesApi->getDelivery: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **delivery_id** | **string**|  | |

### Return type

[**\InvoicePDFs\Model\DeliveryResponse**](../Model/DeliveryResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `retryDelivery()`

```php
retryDelivery($delivery_id): \InvoicePDFs\Model\DeliveryResponse
```

Retry Delivery

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\DeliveriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$delivery_id = 'delivery_id_example'; // string

try {
    $result = $apiInstance->retryDelivery($delivery_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeliveriesApi->retryDelivery: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **delivery_id** | **string**|  | |

### Return type

[**\InvoicePDFs\Model\DeliveryResponse**](../Model/DeliveryResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

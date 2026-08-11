# InvoicePDFs\WebhooksApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createWebhookEndpoint()**](WebhooksApi.md#createWebhookEndpoint) | **POST** /api/v1/webhook-endpoints | Create Webhook Endpoint |
| [**deleteWebhookEndpoint()**](WebhooksApi.md#deleteWebhookEndpoint) | **DELETE** /api/v1/webhook-endpoints/{endpoint_id} | Delete Webhook Endpoint |
| [**getWebhookDelivery()**](WebhooksApi.md#getWebhookDelivery) | **GET** /api/v1/webhook-deliveries/{delivery_id} | Get Webhook Delivery |
| [**getWebhookEndpoint()**](WebhooksApi.md#getWebhookEndpoint) | **GET** /api/v1/webhook-endpoints/{endpoint_id} | Get Webhook Endpoint |
| [**listWebhookDeliveries()**](WebhooksApi.md#listWebhookDeliveries) | **GET** /api/v1/webhook-deliveries | List Webhook Deliveries |
| [**listWebhookEndpoints()**](WebhooksApi.md#listWebhookEndpoints) | **GET** /api/v1/webhook-endpoints | List Webhook Endpoints |
| [**retryWebhookDelivery()**](WebhooksApi.md#retryWebhookDelivery) | **POST** /api/v1/webhook-deliveries/{delivery_id}/retry | Retry Webhook Delivery |
| [**rotateWebhookSecret()**](WebhooksApi.md#rotateWebhookSecret) | **POST** /api/v1/webhook-endpoints/{endpoint_id}/rotate-secret | Rotate Webhook Secret |
| [**testWebhookEndpoint()**](WebhooksApi.md#testWebhookEndpoint) | **POST** /api/v1/webhook-endpoints/{endpoint_id}/test | Test Webhook Endpoint |
| [**updateWebhookEndpoint()**](WebhooksApi.md#updateWebhookEndpoint) | **PATCH** /api/v1/webhook-endpoints/{endpoint_id} | Update Webhook Endpoint |


## `createWebhookEndpoint()`

```php
createWebhookEndpoint($webhook_endpoint_create_request): \InvoicePDFs\Model\WebhookEndpointResponse
```

Create Webhook Endpoint

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\WebhooksApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$webhook_endpoint_create_request = new \InvoicePDFs\Model\WebhookEndpointCreateRequest(); // \InvoicePDFs\Model\WebhookEndpointCreateRequest

try {
    $result = $apiInstance->createWebhookEndpoint($webhook_endpoint_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhooksApi->createWebhookEndpoint: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **webhook_endpoint_create_request** | [**\InvoicePDFs\Model\WebhookEndpointCreateRequest**](../Model/WebhookEndpointCreateRequest.md)|  | |

### Return type

[**\InvoicePDFs\Model\WebhookEndpointResponse**](../Model/WebhookEndpointResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteWebhookEndpoint()`

```php
deleteWebhookEndpoint($endpoint_id): \InvoicePDFs\Model\SimpleBoolResponse
```

Delete Webhook Endpoint

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\WebhooksApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$endpoint_id = 'endpoint_id_example'; // string

try {
    $result = $apiInstance->deleteWebhookEndpoint($endpoint_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhooksApi->deleteWebhookEndpoint: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **endpoint_id** | **string**|  | |

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

## `getWebhookDelivery()`

```php
getWebhookDelivery($delivery_id): \InvoicePDFs\Model\WebhookDeliveryResponse
```

Get Webhook Delivery

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\WebhooksApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$delivery_id = 'delivery_id_example'; // string

try {
    $result = $apiInstance->getWebhookDelivery($delivery_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhooksApi->getWebhookDelivery: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **delivery_id** | **string**|  | |

### Return type

[**\InvoicePDFs\Model\WebhookDeliveryResponse**](../Model/WebhookDeliveryResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getWebhookEndpoint()`

```php
getWebhookEndpoint($endpoint_id): \InvoicePDFs\Model\WebhookEndpointResponse
```

Get Webhook Endpoint

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\WebhooksApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$endpoint_id = 'endpoint_id_example'; // string

try {
    $result = $apiInstance->getWebhookEndpoint($endpoint_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhooksApi->getWebhookEndpoint: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **endpoint_id** | **string**|  | |

### Return type

[**\InvoicePDFs\Model\WebhookEndpointResponse**](../Model/WebhookEndpointResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listWebhookDeliveries()`

```php
listWebhookDeliveries($limit, $cursor): \InvoicePDFs\Model\WebhookDeliveriesListResponse
```

List Webhook Deliveries

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\WebhooksApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$limit = 50; // int
$cursor = 'cursor_example'; // string

try {
    $result = $apiInstance->listWebhookDeliveries($limit, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhooksApi->listWebhookDeliveries: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **limit** | **int**|  | [optional] [default to 50] |
| **cursor** | **string**|  | [optional] |

### Return type

[**\InvoicePDFs\Model\WebhookDeliveriesListResponse**](../Model/WebhookDeliveriesListResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listWebhookEndpoints()`

```php
listWebhookEndpoints($limit, $cursor): \InvoicePDFs\Model\WebhookEndpointsListResponse
```

List Webhook Endpoints

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\WebhooksApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$limit = 50; // int
$cursor = 'cursor_example'; // string

try {
    $result = $apiInstance->listWebhookEndpoints($limit, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhooksApi->listWebhookEndpoints: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **limit** | **int**|  | [optional] [default to 50] |
| **cursor** | **string**|  | [optional] |

### Return type

[**\InvoicePDFs\Model\WebhookEndpointsListResponse**](../Model/WebhookEndpointsListResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `retryWebhookDelivery()`

```php
retryWebhookDelivery($delivery_id): \InvoicePDFs\Model\WebhookDeliveryResponse
```

Retry Webhook Delivery

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\WebhooksApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$delivery_id = 'delivery_id_example'; // string

try {
    $result = $apiInstance->retryWebhookDelivery($delivery_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhooksApi->retryWebhookDelivery: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **delivery_id** | **string**|  | |

### Return type

[**\InvoicePDFs\Model\WebhookDeliveryResponse**](../Model/WebhookDeliveryResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `rotateWebhookSecret()`

```php
rotateWebhookSecret($endpoint_id): \InvoicePDFs\Model\WebhookSecretResponse
```

Rotate Webhook Secret

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\WebhooksApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$endpoint_id = 'endpoint_id_example'; // string

try {
    $result = $apiInstance->rotateWebhookSecret($endpoint_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhooksApi->rotateWebhookSecret: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **endpoint_id** | **string**|  | |

### Return type

[**\InvoicePDFs\Model\WebhookSecretResponse**](../Model/WebhookSecretResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `testWebhookEndpoint()`

```php
testWebhookEndpoint($endpoint_id): \InvoicePDFs\Model\WebhookDeliveryResponse
```

Test Webhook Endpoint

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\WebhooksApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$endpoint_id = 'endpoint_id_example'; // string

try {
    $result = $apiInstance->testWebhookEndpoint($endpoint_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhooksApi->testWebhookEndpoint: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **endpoint_id** | **string**|  | |

### Return type

[**\InvoicePDFs\Model\WebhookDeliveryResponse**](../Model/WebhookDeliveryResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateWebhookEndpoint()`

```php
updateWebhookEndpoint($endpoint_id, $webhook_endpoint_patch_request): \InvoicePDFs\Model\WebhookEndpointResponse
```

Update Webhook Endpoint

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\WebhooksApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$endpoint_id = 'endpoint_id_example'; // string
$webhook_endpoint_patch_request = new \InvoicePDFs\Model\WebhookEndpointPatchRequest(); // \InvoicePDFs\Model\WebhookEndpointPatchRequest

try {
    $result = $apiInstance->updateWebhookEndpoint($endpoint_id, $webhook_endpoint_patch_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhooksApi->updateWebhookEndpoint: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **endpoint_id** | **string**|  | |
| **webhook_endpoint_patch_request** | [**\InvoicePDFs\Model\WebhookEndpointPatchRequest**](../Model/WebhookEndpointPatchRequest.md)|  | |

### Return type

[**\InvoicePDFs\Model\WebhookEndpointResponse**](../Model/WebhookEndpointResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

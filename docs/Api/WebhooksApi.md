# InvoicePDFs\WebhooksApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createWebhookEndpointApiV1WebhookEndpointsPost()**](WebhooksApi.md#createWebhookEndpointApiV1WebhookEndpointsPost) | **POST** /api/v1/webhook-endpoints | Create Webhook Endpoint |
| [**deleteWebhookEndpointApiV1WebhookEndpointsEndpointIdDelete()**](WebhooksApi.md#deleteWebhookEndpointApiV1WebhookEndpointsEndpointIdDelete) | **DELETE** /api/v1/webhook-endpoints/{endpoint_id} | Delete Webhook Endpoint |
| [**getWebhookDeliveryApiV1WebhookDeliveriesDeliveryIdGet()**](WebhooksApi.md#getWebhookDeliveryApiV1WebhookDeliveriesDeliveryIdGet) | **GET** /api/v1/webhook-deliveries/{delivery_id} | Get Webhook Delivery |
| [**getWebhookEndpointApiV1WebhookEndpointsEndpointIdGet()**](WebhooksApi.md#getWebhookEndpointApiV1WebhookEndpointsEndpointIdGet) | **GET** /api/v1/webhook-endpoints/{endpoint_id} | Get Webhook Endpoint |
| [**listWebhookDeliveriesApiV1WebhookDeliveriesGet()**](WebhooksApi.md#listWebhookDeliveriesApiV1WebhookDeliveriesGet) | **GET** /api/v1/webhook-deliveries | List Webhook Deliveries |
| [**listWebhookEndpointsApiV1WebhookEndpointsGet()**](WebhooksApi.md#listWebhookEndpointsApiV1WebhookEndpointsGet) | **GET** /api/v1/webhook-endpoints | List Webhook Endpoints |
| [**retryWebhookDeliveryApiV1WebhookDeliveriesDeliveryIdRetryPost()**](WebhooksApi.md#retryWebhookDeliveryApiV1WebhookDeliveriesDeliveryIdRetryPost) | **POST** /api/v1/webhook-deliveries/{delivery_id}/retry | Retry Webhook Delivery |
| [**rotateWebhookSecretApiV1WebhookEndpointsEndpointIdRotateSecretPost()**](WebhooksApi.md#rotateWebhookSecretApiV1WebhookEndpointsEndpointIdRotateSecretPost) | **POST** /api/v1/webhook-endpoints/{endpoint_id}/rotate-secret | Rotate Webhook Secret |
| [**testWebhookEndpointApiV1WebhookEndpointsEndpointIdTestPost()**](WebhooksApi.md#testWebhookEndpointApiV1WebhookEndpointsEndpointIdTestPost) | **POST** /api/v1/webhook-endpoints/{endpoint_id}/test | Test Webhook Endpoint |
| [**updateWebhookEndpointApiV1WebhookEndpointsEndpointIdPatch()**](WebhooksApi.md#updateWebhookEndpointApiV1WebhookEndpointsEndpointIdPatch) | **PATCH** /api/v1/webhook-endpoints/{endpoint_id} | Update Webhook Endpoint |


## `createWebhookEndpointApiV1WebhookEndpointsPost()`

```php
createWebhookEndpointApiV1WebhookEndpointsPost($webhook_endpoint_create_request): \InvoicePDFs\Model\WebhookEndpointResponse
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
    $result = $apiInstance->createWebhookEndpointApiV1WebhookEndpointsPost($webhook_endpoint_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhooksApi->createWebhookEndpointApiV1WebhookEndpointsPost: ', $e->getMessage(), PHP_EOL;
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

## `deleteWebhookEndpointApiV1WebhookEndpointsEndpointIdDelete()`

```php
deleteWebhookEndpointApiV1WebhookEndpointsEndpointIdDelete($endpoint_id): \InvoicePDFs\Model\SimpleBoolResponse
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
    $result = $apiInstance->deleteWebhookEndpointApiV1WebhookEndpointsEndpointIdDelete($endpoint_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhooksApi->deleteWebhookEndpointApiV1WebhookEndpointsEndpointIdDelete: ', $e->getMessage(), PHP_EOL;
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

## `getWebhookDeliveryApiV1WebhookDeliveriesDeliveryIdGet()`

```php
getWebhookDeliveryApiV1WebhookDeliveriesDeliveryIdGet($delivery_id): \InvoicePDFs\Model\WebhookDeliveryResponse
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
    $result = $apiInstance->getWebhookDeliveryApiV1WebhookDeliveriesDeliveryIdGet($delivery_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhooksApi->getWebhookDeliveryApiV1WebhookDeliveriesDeliveryIdGet: ', $e->getMessage(), PHP_EOL;
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

## `getWebhookEndpointApiV1WebhookEndpointsEndpointIdGet()`

```php
getWebhookEndpointApiV1WebhookEndpointsEndpointIdGet($endpoint_id): \InvoicePDFs\Model\WebhookEndpointResponse
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
    $result = $apiInstance->getWebhookEndpointApiV1WebhookEndpointsEndpointIdGet($endpoint_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhooksApi->getWebhookEndpointApiV1WebhookEndpointsEndpointIdGet: ', $e->getMessage(), PHP_EOL;
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

## `listWebhookDeliveriesApiV1WebhookDeliveriesGet()`

```php
listWebhookDeliveriesApiV1WebhookDeliveriesGet($limit, $cursor): \InvoicePDFs\Model\WebhookDeliveriesListResponse
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
    $result = $apiInstance->listWebhookDeliveriesApiV1WebhookDeliveriesGet($limit, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhooksApi->listWebhookDeliveriesApiV1WebhookDeliveriesGet: ', $e->getMessage(), PHP_EOL;
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

## `listWebhookEndpointsApiV1WebhookEndpointsGet()`

```php
listWebhookEndpointsApiV1WebhookEndpointsGet($limit, $cursor): \InvoicePDFs\Model\WebhookEndpointsListResponse
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
    $result = $apiInstance->listWebhookEndpointsApiV1WebhookEndpointsGet($limit, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhooksApi->listWebhookEndpointsApiV1WebhookEndpointsGet: ', $e->getMessage(), PHP_EOL;
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

## `retryWebhookDeliveryApiV1WebhookDeliveriesDeliveryIdRetryPost()`

```php
retryWebhookDeliveryApiV1WebhookDeliveriesDeliveryIdRetryPost($delivery_id): \InvoicePDFs\Model\WebhookDeliveryResponse
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
    $result = $apiInstance->retryWebhookDeliveryApiV1WebhookDeliveriesDeliveryIdRetryPost($delivery_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhooksApi->retryWebhookDeliveryApiV1WebhookDeliveriesDeliveryIdRetryPost: ', $e->getMessage(), PHP_EOL;
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

## `rotateWebhookSecretApiV1WebhookEndpointsEndpointIdRotateSecretPost()`

```php
rotateWebhookSecretApiV1WebhookEndpointsEndpointIdRotateSecretPost($endpoint_id): \InvoicePDFs\Model\WebhookSecretResponse
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
    $result = $apiInstance->rotateWebhookSecretApiV1WebhookEndpointsEndpointIdRotateSecretPost($endpoint_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhooksApi->rotateWebhookSecretApiV1WebhookEndpointsEndpointIdRotateSecretPost: ', $e->getMessage(), PHP_EOL;
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

## `testWebhookEndpointApiV1WebhookEndpointsEndpointIdTestPost()`

```php
testWebhookEndpointApiV1WebhookEndpointsEndpointIdTestPost($endpoint_id): \InvoicePDFs\Model\WebhookDeliveryResponse
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
    $result = $apiInstance->testWebhookEndpointApiV1WebhookEndpointsEndpointIdTestPost($endpoint_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhooksApi->testWebhookEndpointApiV1WebhookEndpointsEndpointIdTestPost: ', $e->getMessage(), PHP_EOL;
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

## `updateWebhookEndpointApiV1WebhookEndpointsEndpointIdPatch()`

```php
updateWebhookEndpointApiV1WebhookEndpointsEndpointIdPatch($endpoint_id, $webhook_endpoint_patch_request): \InvoicePDFs\Model\WebhookEndpointResponse
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
    $result = $apiInstance->updateWebhookEndpointApiV1WebhookEndpointsEndpointIdPatch($endpoint_id, $webhook_endpoint_patch_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhooksApi->updateWebhookEndpointApiV1WebhookEndpointsEndpointIdPatch: ', $e->getMessage(), PHP_EOL;
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

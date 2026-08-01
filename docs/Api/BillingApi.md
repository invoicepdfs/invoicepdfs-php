# InvoicePDFs\BillingApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createCheckoutApiV1BillingCheckoutSessionPost()**](BillingApi.md#createCheckoutApiV1BillingCheckoutSessionPost) | **POST** /api/v1/billing/checkout-session | Create Checkout |
| [**createPortalApiV1BillingPortalSessionPost()**](BillingApi.md#createPortalApiV1BillingPortalSessionPost) | **POST** /api/v1/billing/portal-session | Create Portal |
| [**getSubscriptionApiV1BillingSubscriptionGet()**](BillingApi.md#getSubscriptionApiV1BillingSubscriptionGet) | **GET** /api/v1/billing/subscription | Get Subscription |


## `createCheckoutApiV1BillingCheckoutSessionPost()`

```php
createCheckoutApiV1BillingCheckoutSessionPost($billing_checkout_request): \InvoicePDFs\Model\BillingCheckoutResponse
```

Create Checkout

Create a Stripe Checkout session for a subscription.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\BillingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$billing_checkout_request = new \InvoicePDFs\Model\BillingCheckoutRequest(); // \InvoicePDFs\Model\BillingCheckoutRequest

try {
    $result = $apiInstance->createCheckoutApiV1BillingCheckoutSessionPost($billing_checkout_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BillingApi->createCheckoutApiV1BillingCheckoutSessionPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **billing_checkout_request** | [**\InvoicePDFs\Model\BillingCheckoutRequest**](../Model/BillingCheckoutRequest.md)|  | |

### Return type

[**\InvoicePDFs\Model\BillingCheckoutResponse**](../Model/BillingCheckoutResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createPortalApiV1BillingPortalSessionPost()`

```php
createPortalApiV1BillingPortalSessionPost(): \InvoicePDFs\Model\BillingPortalResponse
```

Create Portal

Create a Stripe Customer Portal session for self-service management.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\BillingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->createPortalApiV1BillingPortalSessionPost();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BillingApi->createPortalApiV1BillingPortalSessionPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\InvoicePDFs\Model\BillingPortalResponse**](../Model/BillingPortalResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getSubscriptionApiV1BillingSubscriptionGet()`

```php
getSubscriptionApiV1BillingSubscriptionGet(): \InvoicePDFs\Model\BillingSubscriptionResponse
```

Get Subscription

Get current subscription status (from DB, no Stripe API call).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\BillingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getSubscriptionApiV1BillingSubscriptionGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BillingApi->getSubscriptionApiV1BillingSubscriptionGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\InvoicePDFs\Model\BillingSubscriptionResponse**](../Model/BillingSubscriptionResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

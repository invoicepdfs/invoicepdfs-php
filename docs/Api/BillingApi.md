# InvoicePDFs\BillingApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createCheckoutSession()**](BillingApi.md#createCheckoutSession) | **POST** /api/v1/billing/checkout-session | Create Checkout Session |
| [**createPortalSession()**](BillingApi.md#createPortalSession) | **POST** /api/v1/billing/portal-session | Create Portal Session |
| [**getSubscription()**](BillingApi.md#getSubscription) | **GET** /api/v1/billing/subscription | Get Subscription |
| [**listPlans()**](BillingApi.md#listPlans) | **GET** /api/v1/billing/plans | List Plans |


## `createCheckoutSession()`

```php
createCheckoutSession($billing_checkout_request): \InvoicePDFs\Model\BillingCheckoutResponse
```

Create Checkout Session

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
    $result = $apiInstance->createCheckoutSession($billing_checkout_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BillingApi->createCheckoutSession: ', $e->getMessage(), PHP_EOL;
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

## `createPortalSession()`

```php
createPortalSession(): \InvoicePDFs\Model\BillingPortalResponse
```

Create Portal Session

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
    $result = $apiInstance->createPortalSession();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BillingApi->createPortalSession: ', $e->getMessage(), PHP_EOL;
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

## `getSubscription()`

```php
getSubscription(): \InvoicePDFs\Model\BillingSubscriptionResponse
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
    $result = $apiInstance->getSubscription();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BillingApi->getSubscription: ', $e->getMessage(), PHP_EOL;
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

## `listPlans()`

```php
listPlans(): \InvoicePDFs\Model\BillingPlansListResponse
```

List Plans

Purchasable plans — the ones wired to a Stripe price.

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
    $result = $apiInstance->listPlans();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BillingApi->listPlans: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\InvoicePDFs\Model\BillingPlansListResponse**](../Model/BillingPlansListResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

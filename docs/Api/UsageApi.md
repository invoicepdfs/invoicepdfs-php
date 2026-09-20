# InvoicePDFs\UsageApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getUsage()**](UsageApi.md#getUsage) | **GET** /api/v1/usage | Get Usage |
| [**getUsageLimits()**](UsageApi.md#getUsageLimits) | **GET** /api/v1/usage/limits | Get Usage Limits |
| [**listUsageEvents()**](UsageApi.md#listUsageEvents) | **GET** /api/v1/usage/events | List Usage Events |


## `getUsage()`

```php
getUsage(): \InvoicePDFs\Model\UsageResponse
```

Get Usage

Renders used this calendar month, against the plan's quota.  The period starts at midnight UTC on the first of the month.  For rate limits, log retention and overage, use `get_usage_limits`; for the individual renders behind the count, `list_usage_events`.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\UsageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getUsage();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsageApi->getUsage: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\InvoicePDFs\Model\UsageResponse**](../Model/UsageResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getUsageLimits()`

```php
getUsageLimits(): \InvoicePDFs\Model\UsageLimitsResponse
```

Get Usage Limits

Every ceiling on the account, and how close you are to each.  A superset of `get_usage`: the render quota and what is left of it, plus requests per second, how long API logs are kept, and overage — whether it is enabled and available on the plan, how many renders have gone over, and what they have cost so far.  The cost estimate is rounded up, so it is never lower than the invoice.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\UsageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getUsageLimits();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsageApi->getUsageLimits: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\InvoicePDFs\Model\UsageLimitsResponse**](../Model/UsageLimitsResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listUsageEvents()`

```php
listUsageEvents($limit, $cursor): \InvoicePDFs\Model\UsageEventsListResponse
```

List Usage Events

One row per metered render, newest first.  The detail behind the count `get_usage` returns, each row naming the render that produced it.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\UsageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$limit = 50; // int
$cursor = 'cursor_example'; // string

try {
    $result = $apiInstance->listUsageEvents($limit, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsageApi->listUsageEvents: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **limit** | **int**|  | [optional] [default to 50] |
| **cursor** | **string**|  | [optional] |

### Return type

[**\InvoicePDFs\Model\UsageEventsListResponse**](../Model/UsageEventsListResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

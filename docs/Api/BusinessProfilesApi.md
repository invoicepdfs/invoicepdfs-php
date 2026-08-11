# InvoicePDFs\BusinessProfilesApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createBusinessProfile()**](BusinessProfilesApi.md#createBusinessProfile) | **POST** /api/v1/business-profiles | Create Business Profile |
| [**deleteBusinessProfile()**](BusinessProfilesApi.md#deleteBusinessProfile) | **DELETE** /api/v1/business-profiles/{business_profile_id} | Delete Business Profile |
| [**getBusinessProfile()**](BusinessProfilesApi.md#getBusinessProfile) | **GET** /api/v1/business-profiles/{business_profile_id} | Get Business Profile |
| [**listBusinessProfiles()**](BusinessProfilesApi.md#listBusinessProfiles) | **GET** /api/v1/business-profiles | List Business Profiles |
| [**updateBusinessProfile()**](BusinessProfilesApi.md#updateBusinessProfile) | **PATCH** /api/v1/business-profiles/{business_profile_id} | Update Business Profile |


## `createBusinessProfile()`

```php
createBusinessProfile($business_profile_create, $idempotency_key): \InvoicePDFs\Model\BusinessProfileResponse
```

Create Business Profile

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\BusinessProfilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$business_profile_create = new \InvoicePDFs\Model\BusinessProfileCreate(); // \InvoicePDFs\Model\BusinessProfileCreate
$idempotency_key = 'idempotency_key_example'; // string

try {
    $result = $apiInstance->createBusinessProfile($business_profile_create, $idempotency_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BusinessProfilesApi->createBusinessProfile: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **business_profile_create** | [**\InvoicePDFs\Model\BusinessProfileCreate**](../Model/BusinessProfileCreate.md)|  | |
| **idempotency_key** | **string**|  | [optional] |

### Return type

[**\InvoicePDFs\Model\BusinessProfileResponse**](../Model/BusinessProfileResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteBusinessProfile()`

```php
deleteBusinessProfile($business_profile_id): \InvoicePDFs\Model\SimpleBoolResponse
```

Delete Business Profile

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\BusinessProfilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$business_profile_id = 'business_profile_id_example'; // string

try {
    $result = $apiInstance->deleteBusinessProfile($business_profile_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BusinessProfilesApi->deleteBusinessProfile: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **business_profile_id** | **string**|  | |

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

## `getBusinessProfile()`

```php
getBusinessProfile($business_profile_id): \InvoicePDFs\Model\BusinessProfileResponse
```

Get Business Profile

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\BusinessProfilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$business_profile_id = 'business_profile_id_example'; // string

try {
    $result = $apiInstance->getBusinessProfile($business_profile_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BusinessProfilesApi->getBusinessProfile: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **business_profile_id** | **string**|  | |

### Return type

[**\InvoicePDFs\Model\BusinessProfileResponse**](../Model/BusinessProfileResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listBusinessProfiles()`

```php
listBusinessProfiles($limit, $cursor): \InvoicePDFs\Model\BusinessProfilesListResponse
```

List Business Profiles

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\BusinessProfilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$limit = 50; // int
$cursor = 'cursor_example'; // string

try {
    $result = $apiInstance->listBusinessProfiles($limit, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BusinessProfilesApi->listBusinessProfiles: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **limit** | **int**|  | [optional] [default to 50] |
| **cursor** | **string**|  | [optional] |

### Return type

[**\InvoicePDFs\Model\BusinessProfilesListResponse**](../Model/BusinessProfilesListResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateBusinessProfile()`

```php
updateBusinessProfile($business_profile_id, $business_profile_patch, $idempotency_key): \InvoicePDFs\Model\BusinessProfileResponse
```

Update Business Profile

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\BusinessProfilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$business_profile_id = 'business_profile_id_example'; // string
$business_profile_patch = new \InvoicePDFs\Model\BusinessProfilePatch(); // \InvoicePDFs\Model\BusinessProfilePatch
$idempotency_key = 'idempotency_key_example'; // string

try {
    $result = $apiInstance->updateBusinessProfile($business_profile_id, $business_profile_patch, $idempotency_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BusinessProfilesApi->updateBusinessProfile: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **business_profile_id** | **string**|  | |
| **business_profile_patch** | [**\InvoicePDFs\Model\BusinessProfilePatch**](../Model/BusinessProfilePatch.md)|  | |
| **idempotency_key** | **string**|  | [optional] |

### Return type

[**\InvoicePDFs\Model\BusinessProfileResponse**](../Model/BusinessProfileResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

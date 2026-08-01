# OpenAPI\Client\BusinessProfilesApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createBusinessProfileApiV1BusinessProfilesPost()**](BusinessProfilesApi.md#createBusinessProfileApiV1BusinessProfilesPost) | **POST** /api/v1/business-profiles | Create Business Profile |
| [**deleteBusinessProfileApiV1BusinessProfilesBusinessProfileIdDelete()**](BusinessProfilesApi.md#deleteBusinessProfileApiV1BusinessProfilesBusinessProfileIdDelete) | **DELETE** /api/v1/business-profiles/{business_profile_id} | Delete Business Profile |
| [**getBusinessProfileApiV1BusinessProfilesBusinessProfileIdGet()**](BusinessProfilesApi.md#getBusinessProfileApiV1BusinessProfilesBusinessProfileIdGet) | **GET** /api/v1/business-profiles/{business_profile_id} | Get Business Profile |
| [**listBusinessProfilesApiV1BusinessProfilesGet()**](BusinessProfilesApi.md#listBusinessProfilesApiV1BusinessProfilesGet) | **GET** /api/v1/business-profiles | List Business Profiles |
| [**patchBusinessProfileApiV1BusinessProfilesBusinessProfileIdPatch()**](BusinessProfilesApi.md#patchBusinessProfileApiV1BusinessProfilesBusinessProfileIdPatch) | **PATCH** /api/v1/business-profiles/{business_profile_id} | Patch Business Profile |


## `createBusinessProfileApiV1BusinessProfilesPost()`

```php
createBusinessProfileApiV1BusinessProfilesPost($business_profile_create, $idempotency_key): \OpenAPI\Client\Model\BusinessProfileResponse
```

Create Business Profile

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BusinessProfilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$business_profile_create = new \OpenAPI\Client\Model\BusinessProfileCreate(); // \OpenAPI\Client\Model\BusinessProfileCreate
$idempotency_key = 'idempotency_key_example'; // string

try {
    $result = $apiInstance->createBusinessProfileApiV1BusinessProfilesPost($business_profile_create, $idempotency_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BusinessProfilesApi->createBusinessProfileApiV1BusinessProfilesPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **business_profile_create** | [**\OpenAPI\Client\Model\BusinessProfileCreate**](../Model/BusinessProfileCreate.md)|  | |
| **idempotency_key** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\BusinessProfileResponse**](../Model/BusinessProfileResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteBusinessProfileApiV1BusinessProfilesBusinessProfileIdDelete()`

```php
deleteBusinessProfileApiV1BusinessProfilesBusinessProfileIdDelete($business_profile_id): \OpenAPI\Client\Model\SimpleBoolResponse
```

Delete Business Profile

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BusinessProfilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$business_profile_id = 'business_profile_id_example'; // string

try {
    $result = $apiInstance->deleteBusinessProfileApiV1BusinessProfilesBusinessProfileIdDelete($business_profile_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BusinessProfilesApi->deleteBusinessProfileApiV1BusinessProfilesBusinessProfileIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **business_profile_id** | **string**|  | |

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

## `getBusinessProfileApiV1BusinessProfilesBusinessProfileIdGet()`

```php
getBusinessProfileApiV1BusinessProfilesBusinessProfileIdGet($business_profile_id): \OpenAPI\Client\Model\BusinessProfileResponse
```

Get Business Profile

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BusinessProfilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$business_profile_id = 'business_profile_id_example'; // string

try {
    $result = $apiInstance->getBusinessProfileApiV1BusinessProfilesBusinessProfileIdGet($business_profile_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BusinessProfilesApi->getBusinessProfileApiV1BusinessProfilesBusinessProfileIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **business_profile_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\BusinessProfileResponse**](../Model/BusinessProfileResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listBusinessProfilesApiV1BusinessProfilesGet()`

```php
listBusinessProfilesApiV1BusinessProfilesGet($limit, $cursor): \OpenAPI\Client\Model\BusinessProfilesListResponse
```

List Business Profiles

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BusinessProfilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$limit = 50; // int
$cursor = 'cursor_example'; // string

try {
    $result = $apiInstance->listBusinessProfilesApiV1BusinessProfilesGet($limit, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BusinessProfilesApi->listBusinessProfilesApiV1BusinessProfilesGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **limit** | **int**|  | [optional] [default to 50] |
| **cursor** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\BusinessProfilesListResponse**](../Model/BusinessProfilesListResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `patchBusinessProfileApiV1BusinessProfilesBusinessProfileIdPatch()`

```php
patchBusinessProfileApiV1BusinessProfilesBusinessProfileIdPatch($business_profile_id, $business_profile_patch, $idempotency_key): \OpenAPI\Client\Model\BusinessProfileResponse
```

Patch Business Profile

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BusinessProfilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$business_profile_id = 'business_profile_id_example'; // string
$business_profile_patch = new \OpenAPI\Client\Model\BusinessProfilePatch(); // \OpenAPI\Client\Model\BusinessProfilePatch
$idempotency_key = 'idempotency_key_example'; // string

try {
    $result = $apiInstance->patchBusinessProfileApiV1BusinessProfilesBusinessProfileIdPatch($business_profile_id, $business_profile_patch, $idempotency_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BusinessProfilesApi->patchBusinessProfileApiV1BusinessProfilesBusinessProfileIdPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **business_profile_id** | **string**|  | |
| **business_profile_patch** | [**\OpenAPI\Client\Model\BusinessProfilePatch**](../Model/BusinessProfilePatch.md)|  | |
| **idempotency_key** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\BusinessProfileResponse**](../Model/BusinessProfileResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

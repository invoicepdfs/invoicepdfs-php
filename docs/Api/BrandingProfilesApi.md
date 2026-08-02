# InvoicePDFs\BrandingProfilesApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createProfileApiV1BrandingProfilesPost()**](BrandingProfilesApi.md#createProfileApiV1BrandingProfilesPost) | **POST** /api/v1/branding-profiles | Create Profile |
| [**deleteLogoApiV1BrandingProfilesProfileIdLogoDelete()**](BrandingProfilesApi.md#deleteLogoApiV1BrandingProfilesProfileIdLogoDelete) | **DELETE** /api/v1/branding-profiles/{profile_id}/logo | Delete Logo |
| [**deleteProfileApiV1BrandingProfilesProfileIdDelete()**](BrandingProfilesApi.md#deleteProfileApiV1BrandingProfilesProfileIdDelete) | **DELETE** /api/v1/branding-profiles/{profile_id} | Delete Profile |
| [**getProfileApiV1BrandingProfilesProfileIdGet()**](BrandingProfilesApi.md#getProfileApiV1BrandingProfilesProfileIdGet) | **GET** /api/v1/branding-profiles/{profile_id} | Get Profile |
| [**listProfilesApiV1BrandingProfilesGet()**](BrandingProfilesApi.md#listProfilesApiV1BrandingProfilesGet) | **GET** /api/v1/branding-profiles | List Profiles |
| [**setDefaultApiV1BrandingProfilesProfileIdDefaultPost()**](BrandingProfilesApi.md#setDefaultApiV1BrandingProfilesProfileIdDefaultPost) | **POST** /api/v1/branding-profiles/{profile_id}/default | Set Default |
| [**updateProfileApiV1BrandingProfilesProfileIdPatch()**](BrandingProfilesApi.md#updateProfileApiV1BrandingProfilesProfileIdPatch) | **PATCH** /api/v1/branding-profiles/{profile_id} | Update Profile |
| [**uploadLogoApiV1BrandingProfilesProfileIdLogoPost()**](BrandingProfilesApi.md#uploadLogoApiV1BrandingProfilesProfileIdLogoPost) | **POST** /api/v1/branding-profiles/{profile_id}/logo | Upload Logo |


## `createProfileApiV1BrandingProfilesPost()`

```php
createProfileApiV1BrandingProfilesPost($branding_profile_create_request): \InvoicePDFs\Model\BrandingProfileResponse
```

Create Profile

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\BrandingProfilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$branding_profile_create_request = new \InvoicePDFs\Model\BrandingProfileCreateRequest(); // \InvoicePDFs\Model\BrandingProfileCreateRequest

try {
    $result = $apiInstance->createProfileApiV1BrandingProfilesPost($branding_profile_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BrandingProfilesApi->createProfileApiV1BrandingProfilesPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **branding_profile_create_request** | [**\InvoicePDFs\Model\BrandingProfileCreateRequest**](../Model/BrandingProfileCreateRequest.md)|  | |

### Return type

[**\InvoicePDFs\Model\BrandingProfileResponse**](../Model/BrandingProfileResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteLogoApiV1BrandingProfilesProfileIdLogoDelete()`

```php
deleteLogoApiV1BrandingProfilesProfileIdLogoDelete($profile_id): \InvoicePDFs\Model\SimpleBoolResponse
```

Delete Logo

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\BrandingProfilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$profile_id = 'profile_id_example'; // string

try {
    $result = $apiInstance->deleteLogoApiV1BrandingProfilesProfileIdLogoDelete($profile_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BrandingProfilesApi->deleteLogoApiV1BrandingProfilesProfileIdLogoDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **profile_id** | **string**|  | |

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

## `deleteProfileApiV1BrandingProfilesProfileIdDelete()`

```php
deleteProfileApiV1BrandingProfilesProfileIdDelete($profile_id): \InvoicePDFs\Model\SimpleBoolResponse
```

Delete Profile

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\BrandingProfilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$profile_id = 'profile_id_example'; // string

try {
    $result = $apiInstance->deleteProfileApiV1BrandingProfilesProfileIdDelete($profile_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BrandingProfilesApi->deleteProfileApiV1BrandingProfilesProfileIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **profile_id** | **string**|  | |

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

## `getProfileApiV1BrandingProfilesProfileIdGet()`

```php
getProfileApiV1BrandingProfilesProfileIdGet($profile_id): \InvoicePDFs\Model\BrandingProfileResponse
```

Get Profile

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\BrandingProfilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$profile_id = 'profile_id_example'; // string

try {
    $result = $apiInstance->getProfileApiV1BrandingProfilesProfileIdGet($profile_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BrandingProfilesApi->getProfileApiV1BrandingProfilesProfileIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **profile_id** | **string**|  | |

### Return type

[**\InvoicePDFs\Model\BrandingProfileResponse**](../Model/BrandingProfileResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listProfilesApiV1BrandingProfilesGet()`

```php
listProfilesApiV1BrandingProfilesGet(): \InvoicePDFs\Model\BrandingProfilesListResponse
```

List Profiles

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\BrandingProfilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->listProfilesApiV1BrandingProfilesGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BrandingProfilesApi->listProfilesApiV1BrandingProfilesGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\InvoicePDFs\Model\BrandingProfilesListResponse**](../Model/BrandingProfilesListResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `setDefaultApiV1BrandingProfilesProfileIdDefaultPost()`

```php
setDefaultApiV1BrandingProfilesProfileIdDefaultPost($profile_id): \InvoicePDFs\Model\BrandingProfileResponse
```

Set Default

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\BrandingProfilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$profile_id = 'profile_id_example'; // string

try {
    $result = $apiInstance->setDefaultApiV1BrandingProfilesProfileIdDefaultPost($profile_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BrandingProfilesApi->setDefaultApiV1BrandingProfilesProfileIdDefaultPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **profile_id** | **string**|  | |

### Return type

[**\InvoicePDFs\Model\BrandingProfileResponse**](../Model/BrandingProfileResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateProfileApiV1BrandingProfilesProfileIdPatch()`

```php
updateProfileApiV1BrandingProfilesProfileIdPatch($profile_id, $branding_profile_patch_request): \InvoicePDFs\Model\BrandingProfileResponse
```

Update Profile

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\BrandingProfilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$profile_id = 'profile_id_example'; // string
$branding_profile_patch_request = new \InvoicePDFs\Model\BrandingProfilePatchRequest(); // \InvoicePDFs\Model\BrandingProfilePatchRequest

try {
    $result = $apiInstance->updateProfileApiV1BrandingProfilesProfileIdPatch($profile_id, $branding_profile_patch_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BrandingProfilesApi->updateProfileApiV1BrandingProfilesProfileIdPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **profile_id** | **string**|  | |
| **branding_profile_patch_request** | [**\InvoicePDFs\Model\BrandingProfilePatchRequest**](../Model/BrandingProfilePatchRequest.md)|  | |

### Return type

[**\InvoicePDFs\Model\BrandingProfileResponse**](../Model/BrandingProfileResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `uploadLogoApiV1BrandingProfilesProfileIdLogoPost()`

```php
uploadLogoApiV1BrandingProfilesProfileIdLogoPost($profile_id, $file): \InvoicePDFs\Model\BrandingProfileResponse
```

Upload Logo

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\BrandingProfilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$profile_id = 'profile_id_example'; // string
$file = "/path/to/file.txt"; // \SplFileObject

try {
    $result = $apiInstance->uploadLogoApiV1BrandingProfilesProfileIdLogoPost($profile_id, $file);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BrandingProfilesApi->uploadLogoApiV1BrandingProfilesProfileIdLogoPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **profile_id** | **string**|  | |
| **file** | **\SplFileObject****\SplFileObject**|  | |

### Return type

[**\InvoicePDFs\Model\BrandingProfileResponse**](../Model/BrandingProfileResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `multipart/form-data`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

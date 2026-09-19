# InvoicePDFs\BrandingProfilesApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createBrandingProfile()**](BrandingProfilesApi.md#createBrandingProfile) | **POST** /api/v1/branding-profiles | Create Branding Profile |
| [**deleteBrandingLogo()**](BrandingProfilesApi.md#deleteBrandingLogo) | **DELETE** /api/v1/branding-profiles/{profile_id}/logo | Delete Branding Logo |
| [**deleteBrandingProfile()**](BrandingProfilesApi.md#deleteBrandingProfile) | **DELETE** /api/v1/branding-profiles/{profile_id} | Delete Branding Profile |
| [**getBrandingProfile()**](BrandingProfilesApi.md#getBrandingProfile) | **GET** /api/v1/branding-profiles/{profile_id} | Get Branding Profile |
| [**listBrandingProfiles()**](BrandingProfilesApi.md#listBrandingProfiles) | **GET** /api/v1/branding-profiles | List Branding Profiles |
| [**setDefaultBrandingProfile()**](BrandingProfilesApi.md#setDefaultBrandingProfile) | **POST** /api/v1/branding-profiles/{profile_id}/default | Set Default Branding Profile |
| [**updateBrandingProfile()**](BrandingProfilesApi.md#updateBrandingProfile) | **PATCH** /api/v1/branding-profiles/{profile_id} | Update Branding Profile |
| [**uploadBrandingLogo()**](BrandingProfilesApi.md#uploadBrandingLogo) | **POST** /api/v1/branding-profiles/{profile_id}/logo | Upload Branding Logo |


## `createBrandingProfile()`

```php
createBrandingProfile($branding_profile_create_request): \InvoicePDFs\Model\BrandingProfileResponse
```

Create Branding Profile

Create a look: colours, logo, fonts and footer.  Applies on top of whichever template a render names, so one template can serve several brands. Mark one as the default and documents that name no profile will use it.

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
    $result = $apiInstance->createBrandingProfile($branding_profile_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BrandingProfilesApi->createBrandingProfile: ', $e->getMessage(), PHP_EOL;
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

## `deleteBrandingLogo()`

```php
deleteBrandingLogo($profile_id): \InvoicePDFs\Model\SimpleBoolResponse
```

Delete Branding Logo

Remove this profile's logo, leaving its colours and text intact.

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
    $result = $apiInstance->deleteBrandingLogo($profile_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BrandingProfilesApi->deleteBrandingLogo: ', $e->getMessage(), PHP_EOL;
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

## `deleteBrandingProfile()`

```php
deleteBrandingProfile($profile_id): \InvoicePDFs\Model\SimpleBoolResponse
```

Delete Branding Profile

Remove a branding profile.  Deleting the default is allowed: the oldest remaining profile becomes the default in its place, so documents that name no profile keep rendering.

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
    $result = $apiInstance->deleteBrandingProfile($profile_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BrandingProfilesApi->deleteBrandingProfile: ', $e->getMessage(), PHP_EOL;
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

## `getBrandingProfile()`

```php
getBrandingProfile($profile_id): \InvoicePDFs\Model\BrandingProfileResponse
```

Get Branding Profile

One branding profile.

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
    $result = $apiInstance->getBrandingProfile($profile_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BrandingProfilesApi->getBrandingProfile: ', $e->getMessage(), PHP_EOL;
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

## `listBrandingProfiles()`

```php
listBrandingProfiles(): \InvoicePDFs\Model\BrandingProfilesListResponse
```

List Branding Profiles

The looks a document can be rendered in, newest first.  Colours, logo, fonts and footer text — how a document appears. Who it is issued by is a business profile, which is a different thing.

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
    $result = $apiInstance->listBrandingProfiles();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BrandingProfilesApi->listBrandingProfiles: ', $e->getMessage(), PHP_EOL;
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

## `setDefaultBrandingProfile()`

```php
setDefaultBrandingProfile($profile_id): \InvoicePDFs\Model\BrandingProfileResponse
```

Set Default Branding Profile

Make this the profile used when a document names none.  Exactly one profile is the default; setting a new one clears the previous.

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
    $result = $apiInstance->setDefaultBrandingProfile($profile_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BrandingProfilesApi->setDefaultBrandingProfile: ', $e->getMessage(), PHP_EOL;
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

## `updateBrandingProfile()`

```php
updateBrandingProfile($profile_id, $branding_profile_patch_request): \InvoicePDFs\Model\BrandingProfileResponse
```

Update Branding Profile

Change a branding profile.  Only the fields you send are changed. `hide_invoicepdfs_branding` is stored on any plan but only honoured on a plan that includes it — it is applied when a document renders, not validated here, so setting it on a plan without it is accepted and has no effect.

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
    $result = $apiInstance->updateBrandingProfile($profile_id, $branding_profile_patch_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BrandingProfilesApi->updateBrandingProfile: ', $e->getMessage(), PHP_EOL;
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

## `uploadBrandingLogo()`

```php
uploadBrandingLogo($profile_id, $file): \InvoicePDFs\Model\BrandingProfileResponse
```

Upload Branding Logo

Attach a logo image to this branding profile.  Replaces whatever logo the profile carried. The image is embedded when a document renders, so a later change applies to future renders and leaves PDFs already produced as they were.

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
    $result = $apiInstance->uploadBrandingLogo($profile_id, $file);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BrandingProfilesApi->uploadBrandingLogo: ', $e->getMessage(), PHP_EOL;
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

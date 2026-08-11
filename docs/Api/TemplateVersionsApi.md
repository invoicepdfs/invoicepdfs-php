# InvoicePDFs\TemplateVersionsApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createTemplateVersion()**](TemplateVersionsApi.md#createTemplateVersion) | **POST** /api/v1/templates/{template_id}/versions | Create Template Version |
| [**getTemplateVersion()**](TemplateVersionsApi.md#getTemplateVersion) | **GET** /api/v1/templates/{template_id}/versions/{version} | Get Template Version |
| [**listTemplateVersions()**](TemplateVersionsApi.md#listTemplateVersions) | **GET** /api/v1/templates/{template_id}/versions | List Template Versions |


## `createTemplateVersion()`

```php
createTemplateVersion($template_id, $template_version_create_request): \InvoicePDFs\Model\TemplateVersionResponse
```

Create Template Version

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\TemplateVersionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$template_id = 'template_id_example'; // string
$template_version_create_request = new \InvoicePDFs\Model\TemplateVersionCreateRequest(); // \InvoicePDFs\Model\TemplateVersionCreateRequest

try {
    $result = $apiInstance->createTemplateVersion($template_id, $template_version_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TemplateVersionsApi->createTemplateVersion: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **template_id** | **string**|  | |
| **template_version_create_request** | [**\InvoicePDFs\Model\TemplateVersionCreateRequest**](../Model/TemplateVersionCreateRequest.md)|  | |

### Return type

[**\InvoicePDFs\Model\TemplateVersionResponse**](../Model/TemplateVersionResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getTemplateVersion()`

```php
getTemplateVersion($template_id, $version): \InvoicePDFs\Model\TemplateVersionResponse
```

Get Template Version

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\TemplateVersionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$template_id = 'template_id_example'; // string
$version = 56; // int

try {
    $result = $apiInstance->getTemplateVersion($template_id, $version);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TemplateVersionsApi->getTemplateVersion: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **template_id** | **string**|  | |
| **version** | **int**|  | |

### Return type

[**\InvoicePDFs\Model\TemplateVersionResponse**](../Model/TemplateVersionResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listTemplateVersions()`

```php
listTemplateVersions($template_id): \InvoicePDFs\Model\TemplateVersionsListResponse
```

List Template Versions

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\TemplateVersionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$template_id = 'template_id_example'; // string

try {
    $result = $apiInstance->listTemplateVersions($template_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TemplateVersionsApi->listTemplateVersions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **template_id** | **string**|  | |

### Return type

[**\InvoicePDFs\Model\TemplateVersionsListResponse**](../Model/TemplateVersionsListResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

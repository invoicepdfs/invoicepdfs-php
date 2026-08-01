# OpenAPI\Client\TemplateVersionsApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createTemplateVersionApiV1TemplatesTemplateIdVersionsPost()**](TemplateVersionsApi.md#createTemplateVersionApiV1TemplatesTemplateIdVersionsPost) | **POST** /api/v1/templates/{template_id}/versions | Create Template Version |
| [**getTemplateVersionApiV1TemplatesTemplateIdVersionsVersionGet()**](TemplateVersionsApi.md#getTemplateVersionApiV1TemplatesTemplateIdVersionsVersionGet) | **GET** /api/v1/templates/{template_id}/versions/{version} | Get Template Version |
| [**listTemplateVersionsApiV1TemplatesTemplateIdVersionsGet()**](TemplateVersionsApi.md#listTemplateVersionsApiV1TemplatesTemplateIdVersionsGet) | **GET** /api/v1/templates/{template_id}/versions | List Template Versions |


## `createTemplateVersionApiV1TemplatesTemplateIdVersionsPost()`

```php
createTemplateVersionApiV1TemplatesTemplateIdVersionsPost($template_id, $template_version_create_request): \OpenAPI\Client\Model\TemplateVersionResponse
```

Create Template Version

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\TemplateVersionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$template_id = 'template_id_example'; // string
$template_version_create_request = new \OpenAPI\Client\Model\TemplateVersionCreateRequest(); // \OpenAPI\Client\Model\TemplateVersionCreateRequest

try {
    $result = $apiInstance->createTemplateVersionApiV1TemplatesTemplateIdVersionsPost($template_id, $template_version_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TemplateVersionsApi->createTemplateVersionApiV1TemplatesTemplateIdVersionsPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **template_id** | **string**|  | |
| **template_version_create_request** | [**\OpenAPI\Client\Model\TemplateVersionCreateRequest**](../Model/TemplateVersionCreateRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\TemplateVersionResponse**](../Model/TemplateVersionResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getTemplateVersionApiV1TemplatesTemplateIdVersionsVersionGet()`

```php
getTemplateVersionApiV1TemplatesTemplateIdVersionsVersionGet($template_id, $version): \OpenAPI\Client\Model\TemplateVersionResponse
```

Get Template Version

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\TemplateVersionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$template_id = 'template_id_example'; // string
$version = 56; // int

try {
    $result = $apiInstance->getTemplateVersionApiV1TemplatesTemplateIdVersionsVersionGet($template_id, $version);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TemplateVersionsApi->getTemplateVersionApiV1TemplatesTemplateIdVersionsVersionGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **template_id** | **string**|  | |
| **version** | **int**|  | |

### Return type

[**\OpenAPI\Client\Model\TemplateVersionResponse**](../Model/TemplateVersionResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listTemplateVersionsApiV1TemplatesTemplateIdVersionsGet()`

```php
listTemplateVersionsApiV1TemplatesTemplateIdVersionsGet($template_id): \OpenAPI\Client\Model\TemplateVersionsListResponse
```

List Template Versions

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\TemplateVersionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$template_id = 'template_id_example'; // string

try {
    $result = $apiInstance->listTemplateVersionsApiV1TemplatesTemplateIdVersionsGet($template_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TemplateVersionsApi->listTemplateVersionsApiV1TemplatesTemplateIdVersionsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **template_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\TemplateVersionsListResponse**](../Model/TemplateVersionsListResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

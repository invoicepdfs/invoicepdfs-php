# InvoicePDFs\TemplatesApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createTemplateApiV1TemplatesCustomPost()**](TemplatesApi.md#createTemplateApiV1TemplatesCustomPost) | **POST** /api/v1/templates/custom | Create Template |
| [**deleteTemplateApiV1TemplatesCustomTemplateIdDelete()**](TemplatesApi.md#deleteTemplateApiV1TemplatesCustomTemplateIdDelete) | **DELETE** /api/v1/templates/custom/{template_id} | Delete Template |
| [**duplicateTemplateApiV1TemplatesCustomTemplateIdDuplicatePost()**](TemplatesApi.md#duplicateTemplateApiV1TemplatesCustomTemplateIdDuplicatePost) | **POST** /api/v1/templates/custom/{template_id}/duplicate | Duplicate Template |
| [**getBuiltinTemplateApiV1TemplatesBuiltinTemplateIdGet()**](TemplatesApi.md#getBuiltinTemplateApiV1TemplatesBuiltinTemplateIdGet) | **GET** /api/v1/templates/builtin/{template_id} | Get Builtin Template |
| [**getCustomTemplateApiV1TemplatesCustomTemplateIdGet()**](TemplatesApi.md#getCustomTemplateApiV1TemplatesCustomTemplateIdGet) | **GET** /api/v1/templates/custom/{template_id} | Get Custom Template |
| [**getTemplateApiV1TemplatesTemplateIdGet()**](TemplatesApi.md#getTemplateApiV1TemplatesTemplateIdGet) | **GET** /api/v1/templates/{template_id} | Get Template |
| [**listCustomTemplatesApiV1TemplatesCustomGet()**](TemplatesApi.md#listCustomTemplatesApiV1TemplatesCustomGet) | **GET** /api/v1/templates/custom | List Custom Templates |
| [**patchTemplateApiV1TemplatesCustomTemplateIdPatch()**](TemplatesApi.md#patchTemplateApiV1TemplatesCustomTemplateIdPatch) | **PATCH** /api/v1/templates/custom/{template_id} | Patch Template |
| [**previewTemplateApiV1TemplatesTemplateIdPreviewPost()**](TemplatesApi.md#previewTemplateApiV1TemplatesTemplateIdPreviewPost) | **POST** /api/v1/templates/{template_id}/preview | Preview Template |
| [**publishTemplateApiV1TemplatesCustomTemplateIdPublishPost()**](TemplatesApi.md#publishTemplateApiV1TemplatesCustomTemplateIdPublishPost) | **POST** /api/v1/templates/custom/{template_id}/publish | Publish Template |
| [**templatesApiV1TemplatesGet()**](TemplatesApi.md#templatesApiV1TemplatesGet) | **GET** /api/v1/templates | Templates |


## `createTemplateApiV1TemplatesCustomPost()`

```php
createTemplateApiV1TemplatesCustomPost($template_create_request): \InvoicePDFs\Model\CustomTemplateResponse
```

Create Template

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\TemplatesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$template_create_request = new \InvoicePDFs\Model\TemplateCreateRequest(); // \InvoicePDFs\Model\TemplateCreateRequest

try {
    $result = $apiInstance->createTemplateApiV1TemplatesCustomPost($template_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TemplatesApi->createTemplateApiV1TemplatesCustomPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **template_create_request** | [**\InvoicePDFs\Model\TemplateCreateRequest**](../Model/TemplateCreateRequest.md)|  | |

### Return type

[**\InvoicePDFs\Model\CustomTemplateResponse**](../Model/CustomTemplateResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteTemplateApiV1TemplatesCustomTemplateIdDelete()`

```php
deleteTemplateApiV1TemplatesCustomTemplateIdDelete($template_id)
```

Delete Template

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\TemplatesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$template_id = 'template_id_example'; // string

try {
    $apiInstance->deleteTemplateApiV1TemplatesCustomTemplateIdDelete($template_id);
} catch (Exception $e) {
    echo 'Exception when calling TemplatesApi->deleteTemplateApiV1TemplatesCustomTemplateIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **template_id** | **string**|  | |

### Return type

void (empty response body)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `duplicateTemplateApiV1TemplatesCustomTemplateIdDuplicatePost()`

```php
duplicateTemplateApiV1TemplatesCustomTemplateIdDuplicatePost($template_id): \InvoicePDFs\Model\CustomTemplateResponse
```

Duplicate Template

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\TemplatesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$template_id = 'template_id_example'; // string

try {
    $result = $apiInstance->duplicateTemplateApiV1TemplatesCustomTemplateIdDuplicatePost($template_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TemplatesApi->duplicateTemplateApiV1TemplatesCustomTemplateIdDuplicatePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **template_id** | **string**|  | |

### Return type

[**\InvoicePDFs\Model\CustomTemplateResponse**](../Model/CustomTemplateResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getBuiltinTemplateApiV1TemplatesBuiltinTemplateIdGet()`

```php
getBuiltinTemplateApiV1TemplatesBuiltinTemplateIdGet($template_id): \InvoicePDFs\Model\TemplateDetailResponse
```

Get Builtin Template

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\TemplatesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$template_id = 'template_id_example'; // string

try {
    $result = $apiInstance->getBuiltinTemplateApiV1TemplatesBuiltinTemplateIdGet($template_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TemplatesApi->getBuiltinTemplateApiV1TemplatesBuiltinTemplateIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **template_id** | **string**|  | |

### Return type

[**\InvoicePDFs\Model\TemplateDetailResponse**](../Model/TemplateDetailResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getCustomTemplateApiV1TemplatesCustomTemplateIdGet()`

```php
getCustomTemplateApiV1TemplatesCustomTemplateIdGet($template_id): \InvoicePDFs\Model\CustomTemplateResponse
```

Get Custom Template

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\TemplatesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$template_id = 'template_id_example'; // string

try {
    $result = $apiInstance->getCustomTemplateApiV1TemplatesCustomTemplateIdGet($template_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TemplatesApi->getCustomTemplateApiV1TemplatesCustomTemplateIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **template_id** | **string**|  | |

### Return type

[**\InvoicePDFs\Model\CustomTemplateResponse**](../Model/CustomTemplateResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getTemplateApiV1TemplatesTemplateIdGet()`

```php
getTemplateApiV1TemplatesTemplateIdGet($template_id): \InvoicePDFs\Model\TemplateDetailResponse
```

Get Template

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\TemplatesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$template_id = 'template_id_example'; // string

try {
    $result = $apiInstance->getTemplateApiV1TemplatesTemplateIdGet($template_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TemplatesApi->getTemplateApiV1TemplatesTemplateIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **template_id** | **string**|  | |

### Return type

[**\InvoicePDFs\Model\TemplateDetailResponse**](../Model/TemplateDetailResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listCustomTemplatesApiV1TemplatesCustomGet()`

```php
listCustomTemplatesApiV1TemplatesCustomGet($limit, $cursor): \InvoicePDFs\Model\CustomTemplatesListResponse
```

List Custom Templates

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\TemplatesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$limit = 50; // int
$cursor = 'cursor_example'; // string

try {
    $result = $apiInstance->listCustomTemplatesApiV1TemplatesCustomGet($limit, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TemplatesApi->listCustomTemplatesApiV1TemplatesCustomGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **limit** | **int**|  | [optional] [default to 50] |
| **cursor** | **string**|  | [optional] |

### Return type

[**\InvoicePDFs\Model\CustomTemplatesListResponse**](../Model/CustomTemplatesListResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `patchTemplateApiV1TemplatesCustomTemplateIdPatch()`

```php
patchTemplateApiV1TemplatesCustomTemplateIdPatch($template_id, $template_patch_request): \InvoicePDFs\Model\CustomTemplateResponse
```

Patch Template

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\TemplatesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$template_id = 'template_id_example'; // string
$template_patch_request = new \InvoicePDFs\Model\TemplatePatchRequest(); // \InvoicePDFs\Model\TemplatePatchRequest

try {
    $result = $apiInstance->patchTemplateApiV1TemplatesCustomTemplateIdPatch($template_id, $template_patch_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TemplatesApi->patchTemplateApiV1TemplatesCustomTemplateIdPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **template_id** | **string**|  | |
| **template_patch_request** | [**\InvoicePDFs\Model\TemplatePatchRequest**](../Model/TemplatePatchRequest.md)|  | |

### Return type

[**\InvoicePDFs\Model\CustomTemplateResponse**](../Model/CustomTemplateResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `previewTemplateApiV1TemplatesTemplateIdPreviewPost()`

```php
previewTemplateApiV1TemplatesTemplateIdPreviewPost($template_id, $document_render_request, $idempotency_key): mixed
```

Preview Template

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\TemplatesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$template_id = 'template_id_example'; // string
$document_render_request = new \InvoicePDFs\Model\DocumentRenderRequest(); // \InvoicePDFs\Model\DocumentRenderRequest
$idempotency_key = 'idempotency_key_example'; // string

try {
    $result = $apiInstance->previewTemplateApiV1TemplatesTemplateIdPreviewPost($template_id, $document_render_request, $idempotency_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TemplatesApi->previewTemplateApiV1TemplatesTemplateIdPreviewPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **template_id** | **string**|  | |
| **document_render_request** | [**\InvoicePDFs\Model\DocumentRenderRequest**](../Model/DocumentRenderRequest.md)|  | |
| **idempotency_key** | **string**|  | [optional] |

### Return type

**mixed**

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `publishTemplateApiV1TemplatesCustomTemplateIdPublishPost()`

```php
publishTemplateApiV1TemplatesCustomTemplateIdPublishPost($template_id): \InvoicePDFs\Model\CustomTemplateResponse
```

Publish Template

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\TemplatesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$template_id = 'template_id_example'; // string

try {
    $result = $apiInstance->publishTemplateApiV1TemplatesCustomTemplateIdPublishPost($template_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TemplatesApi->publishTemplateApiV1TemplatesCustomTemplateIdPublishPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **template_id** | **string**|  | |

### Return type

[**\InvoicePDFs\Model\CustomTemplateResponse**](../Model/CustomTemplateResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `templatesApiV1TemplatesGet()`

```php
templatesApiV1TemplatesGet(): \InvoicePDFs\Model\TemplatesListResponse
```

Templates

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\TemplatesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->templatesApiV1TemplatesGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TemplatesApi->templatesApiV1TemplatesGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\InvoicePDFs\Model\TemplatesListResponse**](../Model/TemplatesListResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

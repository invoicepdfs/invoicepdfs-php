# InvoicePDFs\TemplatesApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createTemplate()**](TemplatesApi.md#createTemplate) | **POST** /api/v1/templates/custom | Create Template |
| [**deleteTemplate()**](TemplatesApi.md#deleteTemplate) | **DELETE** /api/v1/templates/custom/{template_id} | Delete Template |
| [**duplicateTemplate()**](TemplatesApi.md#duplicateTemplate) | **POST** /api/v1/templates/custom/{template_id}/duplicate | Duplicate Template |
| [**getBuiltinTemplate()**](TemplatesApi.md#getBuiltinTemplate) | **GET** /api/v1/templates/builtin/{template_id} | Get Builtin Template |
| [**getCustomTemplate()**](TemplatesApi.md#getCustomTemplate) | **GET** /api/v1/templates/custom/{template_id} | Get Custom Template |
| [**getTemplate()**](TemplatesApi.md#getTemplate) | **GET** /api/v1/templates/{template_id} | Get Template |
| [**listCustomTemplates()**](TemplatesApi.md#listCustomTemplates) | **GET** /api/v1/templates/custom | List Custom Templates |
| [**listTemplates()**](TemplatesApi.md#listTemplates) | **GET** /api/v1/templates | List Templates |
| [**previewTemplate()**](TemplatesApi.md#previewTemplate) | **POST** /api/v1/templates/{template_id}/preview | Preview Template |
| [**publishTemplate()**](TemplatesApi.md#publishTemplate) | **POST** /api/v1/templates/custom/{template_id}/publish | Publish Template |
| [**updateTemplate()**](TemplatesApi.md#updateTemplate) | **PATCH** /api/v1/templates/custom/{template_id} | Update Template |


## `createTemplate()`

```php
createTemplate($template_create_request): \InvoicePDFs\Model\CustomTemplateResponse
```

Create Template

Design a template of your own, starting as a `draft`.  A custom template is a built-in plus your own configuration — it does not replace the layout, it adjusts it. Drafts can be rendered while you iterate; publish it when you want a version pinned.

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
    $result = $apiInstance->createTemplate($template_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TemplatesApi->createTemplate: ', $e->getMessage(), PHP_EOL;
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

## `deleteTemplate()`

```php
deleteTemplate($template_id)
```

Delete Template

Remove a custom template.  `409` if a document or a recurring schedule still names it.

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
    $apiInstance->deleteTemplate($template_id);
} catch (Exception $e) {
    echo 'Exception when calling TemplatesApi->deleteTemplate: ', $e->getMessage(), PHP_EOL;
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

## `duplicateTemplate()`

```php
duplicateTemplate($template_id): \InvoicePDFs\Model\CustomTemplateResponse
```

Duplicate Template

Copy a custom template into a new `draft`, to change without affecting the original.

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
    $result = $apiInstance->duplicateTemplate($template_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TemplatesApi->duplicateTemplate: ', $e->getMessage(), PHP_EOL;
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

## `getBuiltinTemplate()`

```php
getBuiltinTemplate($template_id): \InvoicePDFs\Model\TemplateDetailResponse
```

Get Builtin Template

One built-in template: its id, name and the options it accepts.

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
    $result = $apiInstance->getBuiltinTemplate($template_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TemplatesApi->getBuiltinTemplate: ', $e->getMessage(), PHP_EOL;
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

## `getCustomTemplate()`

```php
getCustomTemplate($template_id): \InvoicePDFs\Model\CustomTemplateResponse
```

Get Custom Template

One of this account's templates.

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
    $result = $apiInstance->getCustomTemplate($template_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TemplatesApi->getCustomTemplate: ', $e->getMessage(), PHP_EOL;
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

## `getTemplate()`

```php
getTemplate($template_id): \InvoicePDFs\Model\TemplateDetailResponse
```

Get Template

One built-in template: its id, name and the options it accepts.

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
    $result = $apiInstance->getTemplate($template_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TemplatesApi->getTemplate: ', $e->getMessage(), PHP_EOL;
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

## `listCustomTemplates()`

```php
listCustomTemplates($limit, $cursor): \InvoicePDFs\Model\CustomTemplatesListResponse
```

List Custom Templates

Templates this account has designed, newest first. Cursor-paginated.

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
    $result = $apiInstance->listCustomTemplates($limit, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TemplatesApi->listCustomTemplates: ', $e->getMessage(), PHP_EOL;
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

## `listTemplates()`

```php
listTemplates(): \InvoicePDFs\Model\TemplatesListResponse
```

List Templates

The built-in templates every account can render with.  Your own designs are listed separately by `list_custom_templates`.

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
    $result = $apiInstance->listTemplates();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TemplatesApi->listTemplates: ', $e->getMessage(), PHP_EOL;
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

## `previewTemplate()`

```php
previewTemplate($template_id, $document_render_request, $version, $idempotency_key): \InvoicePDFs\Model\RenderResponse
```

Preview Template

Render a template against sample data to see how it looks.  **This is a real render**: it counts against the monthly quota and is metered like any other, because it does the same work. Use it to check a design, not as a way to render documents.

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
$version = 56; // int | Preview the config this version recorded rather than the template's current config. Only a custom (`ctpl_`) template has versions.
$idempotency_key = 'idempotency_key_example'; // string

try {
    $result = $apiInstance->previewTemplate($template_id, $document_render_request, $version, $idempotency_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TemplatesApi->previewTemplate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **template_id** | **string**|  | |
| **document_render_request** | [**\InvoicePDFs\Model\DocumentRenderRequest**](../Model/DocumentRenderRequest.md)|  | |
| **version** | **int**| Preview the config this version recorded rather than the template&#39;s current config. Only a custom (&#x60;ctpl_&#x60;) template has versions. | [optional] |
| **idempotency_key** | **string**|  | [optional] |

### Return type

[**\InvoicePDFs\Model\RenderResponse**](../Model/RenderResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`, `application/pdf`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `publishTemplate()`

```php
publishTemplate($template_id): \InvoicePDFs\Model\CustomTemplateResponse
```

Publish Template

Mark a custom template `published`.  `409` if it is published already. Publishing is what makes a version pinnable, so a document rendered months from now can still be reproduced.

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
    $result = $apiInstance->publishTemplate($template_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TemplatesApi->publishTemplate: ', $e->getMessage(), PHP_EOL;
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

## `updateTemplate()`

```php
updateTemplate($template_id, $template_patch_request): \InvoicePDFs\Model\CustomTemplateResponse
```

Update Template

Change a custom template. Only the fields you send are changed.

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
    $result = $apiInstance->updateTemplate($template_id, $template_patch_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TemplatesApi->updateTemplate: ', $e->getMessage(), PHP_EOL;
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

# InvoicePDFs\CreditNotesApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createCreditNoteApiV1CreditNotesPost()**](CreditNotesApi.md#createCreditNoteApiV1CreditNotesPost) | **POST** /api/v1/credit-notes | Create Credit Note |
| [**finalizeCreditNoteApiV1CreditNotesCreditNoteIdFinalizePost()**](CreditNotesApi.md#finalizeCreditNoteApiV1CreditNotesCreditNoteIdFinalizePost) | **POST** /api/v1/credit-notes/{credit_note_id}/finalize | Finalize Credit Note |
| [**getCreditNoteApiV1CreditNotesCreditNoteIdGet()**](CreditNotesApi.md#getCreditNoteApiV1CreditNotesCreditNoteIdGet) | **GET** /api/v1/credit-notes/{credit_note_id} | Get Credit Note |
| [**listCreditNotesApiV1CreditNotesGet()**](CreditNotesApi.md#listCreditNotesApiV1CreditNotesGet) | **GET** /api/v1/credit-notes | List Credit Notes |
| [**renderCreditNoteApiV1CreditNotesCreditNoteIdRendersPost()**](CreditNotesApi.md#renderCreditNoteApiV1CreditNotesCreditNoteIdRendersPost) | **POST** /api/v1/credit-notes/{credit_note_id}/renders | Render Credit Note |


## `createCreditNoteApiV1CreditNotesPost()`

```php
createCreditNoteApiV1CreditNotesPost($credit_note_create_request): \InvoicePDFs\Model\CreditNoteResponse
```

Create Credit Note

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\CreditNotesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$credit_note_create_request = new \InvoicePDFs\Model\CreditNoteCreateRequest(); // \InvoicePDFs\Model\CreditNoteCreateRequest

try {
    $result = $apiInstance->createCreditNoteApiV1CreditNotesPost($credit_note_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CreditNotesApi->createCreditNoteApiV1CreditNotesPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **credit_note_create_request** | [**\InvoicePDFs\Model\CreditNoteCreateRequest**](../Model/CreditNoteCreateRequest.md)|  | |

### Return type

[**\InvoicePDFs\Model\CreditNoteResponse**](../Model/CreditNoteResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `finalizeCreditNoteApiV1CreditNotesCreditNoteIdFinalizePost()`

```php
finalizeCreditNoteApiV1CreditNotesCreditNoteIdFinalizePost($credit_note_id): \InvoicePDFs\Model\CreditNoteResponse
```

Finalize Credit Note

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\CreditNotesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$credit_note_id = 'credit_note_id_example'; // string

try {
    $result = $apiInstance->finalizeCreditNoteApiV1CreditNotesCreditNoteIdFinalizePost($credit_note_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CreditNotesApi->finalizeCreditNoteApiV1CreditNotesCreditNoteIdFinalizePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **credit_note_id** | **string**|  | |

### Return type

[**\InvoicePDFs\Model\CreditNoteResponse**](../Model/CreditNoteResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getCreditNoteApiV1CreditNotesCreditNoteIdGet()`

```php
getCreditNoteApiV1CreditNotesCreditNoteIdGet($credit_note_id): \InvoicePDFs\Model\CreditNoteResponse
```

Get Credit Note

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\CreditNotesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$credit_note_id = 'credit_note_id_example'; // string

try {
    $result = $apiInstance->getCreditNoteApiV1CreditNotesCreditNoteIdGet($credit_note_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CreditNotesApi->getCreditNoteApiV1CreditNotesCreditNoteIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **credit_note_id** | **string**|  | |

### Return type

[**\InvoicePDFs\Model\CreditNoteResponse**](../Model/CreditNoteResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listCreditNotesApiV1CreditNotesGet()`

```php
listCreditNotesApiV1CreditNotesGet($limit, $cursor): \InvoicePDFs\Model\CreditNotesListResponse
```

List Credit Notes

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\CreditNotesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$limit = 50; // int
$cursor = 'cursor_example'; // string

try {
    $result = $apiInstance->listCreditNotesApiV1CreditNotesGet($limit, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CreditNotesApi->listCreditNotesApiV1CreditNotesGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **limit** | **int**|  | [optional] [default to 50] |
| **cursor** | **string**|  | [optional] |

### Return type

[**\InvoicePDFs\Model\CreditNotesListResponse**](../Model/CreditNotesListResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `renderCreditNoteApiV1CreditNotesCreditNoteIdRendersPost()`

```php
renderCreditNoteApiV1CreditNotesCreditNoteIdRendersPost($credit_note_id, $credit_note_render_request): mixed
```

Render Credit Note

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\CreditNotesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$credit_note_id = 'credit_note_id_example'; // string
$credit_note_render_request = new \InvoicePDFs\Model\CreditNoteRenderRequest(); // \InvoicePDFs\Model\CreditNoteRenderRequest

try {
    $result = $apiInstance->renderCreditNoteApiV1CreditNotesCreditNoteIdRendersPost($credit_note_id, $credit_note_render_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CreditNotesApi->renderCreditNoteApiV1CreditNotesCreditNoteIdRendersPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **credit_note_id** | **string**|  | |
| **credit_note_render_request** | [**\InvoicePDFs\Model\CreditNoteRenderRequest**](../Model/CreditNoteRenderRequest.md)|  | [optional] |

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

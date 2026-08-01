# InvoicePDFs\NumberingSequencesApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**consumeNextApiV1NumberingSequencesSequenceIdNextPost()**](NumberingSequencesApi.md#consumeNextApiV1NumberingSequencesSequenceIdNextPost) | **POST** /api/v1/numbering-sequences/{sequence_id}/next | Consume Next |
| [**createSequenceApiV1NumberingSequencesPost()**](NumberingSequencesApi.md#createSequenceApiV1NumberingSequencesPost) | **POST** /api/v1/numbering-sequences | Create Sequence |
| [**deleteSequenceApiV1NumberingSequencesSequenceIdDelete()**](NumberingSequencesApi.md#deleteSequenceApiV1NumberingSequencesSequenceIdDelete) | **DELETE** /api/v1/numbering-sequences/{sequence_id} | Delete Sequence |
| [**getSequenceApiV1NumberingSequencesSequenceIdGet()**](NumberingSequencesApi.md#getSequenceApiV1NumberingSequencesSequenceIdGet) | **GET** /api/v1/numbering-sequences/{sequence_id} | Get Sequence |
| [**listSequencesApiV1NumberingSequencesGet()**](NumberingSequencesApi.md#listSequencesApiV1NumberingSequencesGet) | **GET** /api/v1/numbering-sequences | List Sequences |
| [**previewSequenceApiV1NumberingSequencesSequenceIdPreviewPost()**](NumberingSequencesApi.md#previewSequenceApiV1NumberingSequencesSequenceIdPreviewPost) | **POST** /api/v1/numbering-sequences/{sequence_id}/preview | Preview Sequence |
| [**updateSequenceApiV1NumberingSequencesSequenceIdPatch()**](NumberingSequencesApi.md#updateSequenceApiV1NumberingSequencesSequenceIdPatch) | **PATCH** /api/v1/numbering-sequences/{sequence_id} | Update Sequence |


## `consumeNextApiV1NumberingSequencesSequenceIdNextPost()`

```php
consumeNextApiV1NumberingSequencesSequenceIdNextPost($sequence_id): \InvoicePDFs\Model\NumberingSequenceResponse
```

Consume Next

Consume and return the next number, incrementing the counter.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\NumberingSequencesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sequence_id = 'sequence_id_example'; // string

try {
    $result = $apiInstance->consumeNextApiV1NumberingSequencesSequenceIdNextPost($sequence_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NumberingSequencesApi->consumeNextApiV1NumberingSequencesSequenceIdNextPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sequence_id** | **string**|  | |

### Return type

[**\InvoicePDFs\Model\NumberingSequenceResponse**](../Model/NumberingSequenceResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createSequenceApiV1NumberingSequencesPost()`

```php
createSequenceApiV1NumberingSequencesPost($numbering_sequence_create_request): \InvoicePDFs\Model\NumberingSequenceResponse
```

Create Sequence

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\NumberingSequencesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$numbering_sequence_create_request = new \InvoicePDFs\Model\NumberingSequenceCreateRequest(); // \InvoicePDFs\Model\NumberingSequenceCreateRequest

try {
    $result = $apiInstance->createSequenceApiV1NumberingSequencesPost($numbering_sequence_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NumberingSequencesApi->createSequenceApiV1NumberingSequencesPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **numbering_sequence_create_request** | [**\InvoicePDFs\Model\NumberingSequenceCreateRequest**](../Model/NumberingSequenceCreateRequest.md)|  | |

### Return type

[**\InvoicePDFs\Model\NumberingSequenceResponse**](../Model/NumberingSequenceResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteSequenceApiV1NumberingSequencesSequenceIdDelete()`

```php
deleteSequenceApiV1NumberingSequencesSequenceIdDelete($sequence_id): \InvoicePDFs\Model\SimpleBoolResponse
```

Delete Sequence

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\NumberingSequencesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sequence_id = 'sequence_id_example'; // string

try {
    $result = $apiInstance->deleteSequenceApiV1NumberingSequencesSequenceIdDelete($sequence_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NumberingSequencesApi->deleteSequenceApiV1NumberingSequencesSequenceIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sequence_id** | **string**|  | |

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

## `getSequenceApiV1NumberingSequencesSequenceIdGet()`

```php
getSequenceApiV1NumberingSequencesSequenceIdGet($sequence_id): \InvoicePDFs\Model\NumberingSequenceResponse
```

Get Sequence

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\NumberingSequencesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sequence_id = 'sequence_id_example'; // string

try {
    $result = $apiInstance->getSequenceApiV1NumberingSequencesSequenceIdGet($sequence_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NumberingSequencesApi->getSequenceApiV1NumberingSequencesSequenceIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sequence_id** | **string**|  | |

### Return type

[**\InvoicePDFs\Model\NumberingSequenceResponse**](../Model/NumberingSequenceResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listSequencesApiV1NumberingSequencesGet()`

```php
listSequencesApiV1NumberingSequencesGet($limit, $cursor): \InvoicePDFs\Model\NumberingSequencesListResponse
```

List Sequences

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\NumberingSequencesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$limit = 50; // int
$cursor = 'cursor_example'; // string

try {
    $result = $apiInstance->listSequencesApiV1NumberingSequencesGet($limit, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NumberingSequencesApi->listSequencesApiV1NumberingSequencesGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **limit** | **int**|  | [optional] [default to 50] |
| **cursor** | **string**|  | [optional] |

### Return type

[**\InvoicePDFs\Model\NumberingSequencesListResponse**](../Model/NumberingSequencesListResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `previewSequenceApiV1NumberingSequencesSequenceIdPreviewPost()`

```php
previewSequenceApiV1NumberingSequencesSequenceIdPreviewPost($sequence_id): \InvoicePDFs\Model\NumberingSequencePreviewResponse
```

Preview Sequence

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\NumberingSequencesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sequence_id = 'sequence_id_example'; // string

try {
    $result = $apiInstance->previewSequenceApiV1NumberingSequencesSequenceIdPreviewPost($sequence_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NumberingSequencesApi->previewSequenceApiV1NumberingSequencesSequenceIdPreviewPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sequence_id** | **string**|  | |

### Return type

[**\InvoicePDFs\Model\NumberingSequencePreviewResponse**](../Model/NumberingSequencePreviewResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateSequenceApiV1NumberingSequencesSequenceIdPatch()`

```php
updateSequenceApiV1NumberingSequencesSequenceIdPatch($sequence_id, $numbering_sequence_patch_request): \InvoicePDFs\Model\NumberingSequenceResponse
```

Update Sequence

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\NumberingSequencesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sequence_id = 'sequence_id_example'; // string
$numbering_sequence_patch_request = new \InvoicePDFs\Model\NumberingSequencePatchRequest(); // \InvoicePDFs\Model\NumberingSequencePatchRequest

try {
    $result = $apiInstance->updateSequenceApiV1NumberingSequencesSequenceIdPatch($sequence_id, $numbering_sequence_patch_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NumberingSequencesApi->updateSequenceApiV1NumberingSequencesSequenceIdPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sequence_id** | **string**|  | |
| **numbering_sequence_patch_request** | [**\InvoicePDFs\Model\NumberingSequencePatchRequest**](../Model/NumberingSequencePatchRequest.md)|  | |

### Return type

[**\InvoicePDFs\Model\NumberingSequenceResponse**](../Model/NumberingSequenceResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

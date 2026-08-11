# InvoicePDFs\NumberingSequencesApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**consumeSequenceNumber()**](NumberingSequencesApi.md#consumeSequenceNumber) | **POST** /api/v1/numbering-sequences/{sequence_id}/next | Consume Sequence Number |
| [**createSequence()**](NumberingSequencesApi.md#createSequence) | **POST** /api/v1/numbering-sequences | Create Sequence |
| [**deleteSequence()**](NumberingSequencesApi.md#deleteSequence) | **DELETE** /api/v1/numbering-sequences/{sequence_id} | Delete Sequence |
| [**getSequence()**](NumberingSequencesApi.md#getSequence) | **GET** /api/v1/numbering-sequences/{sequence_id} | Get Sequence |
| [**listSequences()**](NumberingSequencesApi.md#listSequences) | **GET** /api/v1/numbering-sequences | List Sequences |
| [**previewSequence()**](NumberingSequencesApi.md#previewSequence) | **POST** /api/v1/numbering-sequences/{sequence_id}/preview | Preview Sequence |
| [**updateSequence()**](NumberingSequencesApi.md#updateSequence) | **PATCH** /api/v1/numbering-sequences/{sequence_id} | Update Sequence |


## `consumeSequenceNumber()`

```php
consumeSequenceNumber($sequence_id): \InvoicePDFs\Model\NumberingSequenceResponse
```

Consume Sequence Number

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
    $result = $apiInstance->consumeSequenceNumber($sequence_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NumberingSequencesApi->consumeSequenceNumber: ', $e->getMessage(), PHP_EOL;
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

## `createSequence()`

```php
createSequence($numbering_sequence_create_request): \InvoicePDFs\Model\NumberingSequenceResponse
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
    $result = $apiInstance->createSequence($numbering_sequence_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NumberingSequencesApi->createSequence: ', $e->getMessage(), PHP_EOL;
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

## `deleteSequence()`

```php
deleteSequence($sequence_id): \InvoicePDFs\Model\SimpleBoolResponse
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
    $result = $apiInstance->deleteSequence($sequence_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NumberingSequencesApi->deleteSequence: ', $e->getMessage(), PHP_EOL;
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

## `getSequence()`

```php
getSequence($sequence_id): \InvoicePDFs\Model\NumberingSequenceResponse
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
    $result = $apiInstance->getSequence($sequence_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NumberingSequencesApi->getSequence: ', $e->getMessage(), PHP_EOL;
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

## `listSequences()`

```php
listSequences($limit, $cursor): \InvoicePDFs\Model\NumberingSequencesListResponse
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
    $result = $apiInstance->listSequences($limit, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NumberingSequencesApi->listSequences: ', $e->getMessage(), PHP_EOL;
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

## `previewSequence()`

```php
previewSequence($sequence_id): \InvoicePDFs\Model\NumberingSequencePreviewResponse
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
    $result = $apiInstance->previewSequence($sequence_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NumberingSequencesApi->previewSequence: ', $e->getMessage(), PHP_EOL;
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

## `updateSequence()`

```php
updateSequence($sequence_id, $numbering_sequence_patch_request): \InvoicePDFs\Model\NumberingSequenceResponse
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
    $result = $apiInstance->updateSequence($sequence_id, $numbering_sequence_patch_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NumberingSequencesApi->updateSequence: ', $e->getMessage(), PHP_EOL;
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

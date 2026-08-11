# InvoicePDFs\AuditLogApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getAuditEvent()**](AuditLogApi.md#getAuditEvent) | **GET** /api/v1/audit-events/{audit_event_id} | Get Audit Event |
| [**listAuditEvents()**](AuditLogApi.md#listAuditEvents) | **GET** /api/v1/audit-events | List Audit Events |


## `getAuditEvent()`

```php
getAuditEvent($audit_event_id): \InvoicePDFs\Model\AuditEventResponse
```

Get Audit Event

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\AuditLogApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$audit_event_id = 'audit_event_id_example'; // string

try {
    $result = $apiInstance->getAuditEvent($audit_event_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuditLogApi->getAuditEvent: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **audit_event_id** | **string**|  | |

### Return type

[**\InvoicePDFs\Model\AuditEventResponse**](../Model/AuditEventResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listAuditEvents()`

```php
listAuditEvents($limit, $cursor, $action, $resource_type, $resource_id): \InvoicePDFs\Model\AuditEventsListResponse
```

List Audit Events

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\AuditLogApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$limit = 50; // int
$cursor = 'cursor_example'; // string
$action = 'action_example'; // string
$resource_type = 'resource_type_example'; // string
$resource_id = 'resource_id_example'; // string

try {
    $result = $apiInstance->listAuditEvents($limit, $cursor, $action, $resource_type, $resource_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuditLogApi->listAuditEvents: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **limit** | **int**|  | [optional] [default to 50] |
| **cursor** | **string**|  | [optional] |
| **action** | **string**|  | [optional] |
| **resource_type** | **string**|  | [optional] |
| **resource_id** | **string**|  | [optional] |

### Return type

[**\InvoicePDFs\Model\AuditEventsListResponse**](../Model/AuditEventsListResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

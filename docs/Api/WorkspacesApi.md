# InvoicePDFs\WorkspacesApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**addWorkspaceMember()**](WorkspacesApi.md#addWorkspaceMember) | **POST** /api/v1/workspaces/{workspace_id}/members | Add Workspace Member |
| [**createWorkspace()**](WorkspacesApi.md#createWorkspace) | **POST** /api/v1/workspaces | Create Workspace |
| [**deleteWorkspace()**](WorkspacesApi.md#deleteWorkspace) | **DELETE** /api/v1/workspaces/{workspace_id} | Delete Workspace |
| [**getWorkspace()**](WorkspacesApi.md#getWorkspace) | **GET** /api/v1/workspaces/{workspace_id} | Get Workspace |
| [**listWorkspaceMembers()**](WorkspacesApi.md#listWorkspaceMembers) | **GET** /api/v1/workspaces/{workspace_id}/members | List Workspace Members |
| [**listWorkspaces()**](WorkspacesApi.md#listWorkspaces) | **GET** /api/v1/workspaces | List Workspaces |
| [**removeWorkspaceMember()**](WorkspacesApi.md#removeWorkspaceMember) | **DELETE** /api/v1/workspaces/{workspace_id}/members/{member_id} | Remove Workspace Member |
| [**updateWorkspace()**](WorkspacesApi.md#updateWorkspace) | **PATCH** /api/v1/workspaces/{workspace_id} | Update Workspace |
| [**updateWorkspaceMember()**](WorkspacesApi.md#updateWorkspaceMember) | **PATCH** /api/v1/workspaces/{workspace_id}/members/{member_id} | Update Workspace Member |


## `addWorkspaceMember()`

```php
addWorkspaceMember($workspace_id, $workspace_member_create_request, $idempotency_key): \InvoicePDFs\Model\WorkspaceMembersListResponse
```

Add Workspace Member

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\WorkspacesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$workspace_id = 'workspace_id_example'; // string
$workspace_member_create_request = new \InvoicePDFs\Model\WorkspaceMemberCreateRequest(); // \InvoicePDFs\Model\WorkspaceMemberCreateRequest
$idempotency_key = 'idempotency_key_example'; // string

try {
    $result = $apiInstance->addWorkspaceMember($workspace_id, $workspace_member_create_request, $idempotency_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WorkspacesApi->addWorkspaceMember: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **workspace_id** | **string**|  | |
| **workspace_member_create_request** | [**\InvoicePDFs\Model\WorkspaceMemberCreateRequest**](../Model/WorkspaceMemberCreateRequest.md)|  | |
| **idempotency_key** | **string**|  | [optional] |

### Return type

[**\InvoicePDFs\Model\WorkspaceMembersListResponse**](../Model/WorkspaceMembersListResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createWorkspace()`

```php
createWorkspace($workspace_create_request, $idempotency_key): \InvoicePDFs\Model\WorkspaceResponse
```

Create Workspace

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\WorkspacesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$workspace_create_request = new \InvoicePDFs\Model\WorkspaceCreateRequest(); // \InvoicePDFs\Model\WorkspaceCreateRequest
$idempotency_key = 'idempotency_key_example'; // string

try {
    $result = $apiInstance->createWorkspace($workspace_create_request, $idempotency_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WorkspacesApi->createWorkspace: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **workspace_create_request** | [**\InvoicePDFs\Model\WorkspaceCreateRequest**](../Model/WorkspaceCreateRequest.md)|  | |
| **idempotency_key** | **string**|  | [optional] |

### Return type

[**\InvoicePDFs\Model\WorkspaceResponse**](../Model/WorkspaceResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteWorkspace()`

```php
deleteWorkspace($workspace_id): \InvoicePDFs\Model\SimpleBoolResponse
```

Delete Workspace

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\WorkspacesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$workspace_id = 'workspace_id_example'; // string

try {
    $result = $apiInstance->deleteWorkspace($workspace_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WorkspacesApi->deleteWorkspace: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **workspace_id** | **string**|  | |

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

## `getWorkspace()`

```php
getWorkspace($workspace_id): \InvoicePDFs\Model\WorkspaceResponse
```

Get Workspace

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\WorkspacesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$workspace_id = 'workspace_id_example'; // string

try {
    $result = $apiInstance->getWorkspace($workspace_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WorkspacesApi->getWorkspace: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **workspace_id** | **string**|  | |

### Return type

[**\InvoicePDFs\Model\WorkspaceResponse**](../Model/WorkspaceResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listWorkspaceMembers()`

```php
listWorkspaceMembers($workspace_id): \InvoicePDFs\Model\WorkspaceMembersListResponse
```

List Workspace Members

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\WorkspacesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$workspace_id = 'workspace_id_example'; // string

try {
    $result = $apiInstance->listWorkspaceMembers($workspace_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WorkspacesApi->listWorkspaceMembers: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **workspace_id** | **string**|  | |

### Return type

[**\InvoicePDFs\Model\WorkspaceMembersListResponse**](../Model/WorkspaceMembersListResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listWorkspaces()`

```php
listWorkspaces($limit, $cursor): \InvoicePDFs\Model\WorkspacesListResponse
```

List Workspaces

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\WorkspacesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$limit = 50; // int
$cursor = 'cursor_example'; // string

try {
    $result = $apiInstance->listWorkspaces($limit, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WorkspacesApi->listWorkspaces: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **limit** | **int**|  | [optional] [default to 50] |
| **cursor** | **string**|  | [optional] |

### Return type

[**\InvoicePDFs\Model\WorkspacesListResponse**](../Model/WorkspacesListResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `removeWorkspaceMember()`

```php
removeWorkspaceMember($workspace_id, $member_id): \InvoicePDFs\Model\SimpleBoolResponse
```

Remove Workspace Member

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\WorkspacesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$workspace_id = 'workspace_id_example'; // string
$member_id = 'member_id_example'; // string

try {
    $result = $apiInstance->removeWorkspaceMember($workspace_id, $member_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WorkspacesApi->removeWorkspaceMember: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **workspace_id** | **string**|  | |
| **member_id** | **string**|  | |

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

## `updateWorkspace()`

```php
updateWorkspace($workspace_id, $workspace_patch_request, $idempotency_key): \InvoicePDFs\Model\WorkspaceResponse
```

Update Workspace

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\WorkspacesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$workspace_id = 'workspace_id_example'; // string
$workspace_patch_request = new \InvoicePDFs\Model\WorkspacePatchRequest(); // \InvoicePDFs\Model\WorkspacePatchRequest
$idempotency_key = 'idempotency_key_example'; // string

try {
    $result = $apiInstance->updateWorkspace($workspace_id, $workspace_patch_request, $idempotency_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WorkspacesApi->updateWorkspace: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **workspace_id** | **string**|  | |
| **workspace_patch_request** | [**\InvoicePDFs\Model\WorkspacePatchRequest**](../Model/WorkspacePatchRequest.md)|  | |
| **idempotency_key** | **string**|  | [optional] |

### Return type

[**\InvoicePDFs\Model\WorkspaceResponse**](../Model/WorkspaceResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateWorkspaceMember()`

```php
updateWorkspaceMember($workspace_id, $member_id, $workspace_member_patch_request): \InvoicePDFs\Model\WorkspaceMemberOut
```

Update Workspace Member

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\WorkspacesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$workspace_id = 'workspace_id_example'; // string
$member_id = 'member_id_example'; // string
$workspace_member_patch_request = new \InvoicePDFs\Model\WorkspaceMemberPatchRequest(); // \InvoicePDFs\Model\WorkspaceMemberPatchRequest

try {
    $result = $apiInstance->updateWorkspaceMember($workspace_id, $member_id, $workspace_member_patch_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WorkspacesApi->updateWorkspaceMember: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **workspace_id** | **string**|  | |
| **member_id** | **string**|  | |
| **workspace_member_patch_request** | [**\InvoicePDFs\Model\WorkspaceMemberPatchRequest**](../Model/WorkspaceMemberPatchRequest.md)|  | |

### Return type

[**\InvoicePDFs\Model\WorkspaceMemberOut**](../Model/WorkspaceMemberOut.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

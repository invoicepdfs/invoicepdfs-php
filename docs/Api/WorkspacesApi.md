# OpenAPI\Client\WorkspacesApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createMemberApiV1WorkspacesWorkspaceIdMembersPost()**](WorkspacesApi.md#createMemberApiV1WorkspacesWorkspaceIdMembersPost) | **POST** /api/v1/workspaces/{workspace_id}/members | Create Member |
| [**createWorkspaceApiV1WorkspacesPost()**](WorkspacesApi.md#createWorkspaceApiV1WorkspacesPost) | **POST** /api/v1/workspaces | Create Workspace |
| [**deleteMemberApiV1WorkspacesWorkspaceIdMembersMemberIdDelete()**](WorkspacesApi.md#deleteMemberApiV1WorkspacesWorkspaceIdMembersMemberIdDelete) | **DELETE** /api/v1/workspaces/{workspace_id}/members/{member_id} | Delete Member |
| [**deleteWorkspaceApiV1WorkspacesWorkspaceIdDelete()**](WorkspacesApi.md#deleteWorkspaceApiV1WorkspacesWorkspaceIdDelete) | **DELETE** /api/v1/workspaces/{workspace_id} | Delete Workspace |
| [**getWorkspaceApiV1WorkspacesWorkspaceIdGet()**](WorkspacesApi.md#getWorkspaceApiV1WorkspacesWorkspaceIdGet) | **GET** /api/v1/workspaces/{workspace_id} | Get Workspace |
| [**listMembersApiV1WorkspacesWorkspaceIdMembersGet()**](WorkspacesApi.md#listMembersApiV1WorkspacesWorkspaceIdMembersGet) | **GET** /api/v1/workspaces/{workspace_id}/members | List Members |
| [**listWorkspacesApiV1WorkspacesGet()**](WorkspacesApi.md#listWorkspacesApiV1WorkspacesGet) | **GET** /api/v1/workspaces | List Workspaces |
| [**patchMemberApiV1WorkspacesWorkspaceIdMembersMemberIdPatch()**](WorkspacesApi.md#patchMemberApiV1WorkspacesWorkspaceIdMembersMemberIdPatch) | **PATCH** /api/v1/workspaces/{workspace_id}/members/{member_id} | Patch Member |
| [**patchWorkspaceApiV1WorkspacesWorkspaceIdPatch()**](WorkspacesApi.md#patchWorkspaceApiV1WorkspacesWorkspaceIdPatch) | **PATCH** /api/v1/workspaces/{workspace_id} | Patch Workspace |


## `createMemberApiV1WorkspacesWorkspaceIdMembersPost()`

```php
createMemberApiV1WorkspacesWorkspaceIdMembersPost($workspace_id, $workspace_member_create_request, $idempotency_key): \OpenAPI\Client\Model\WorkspaceMembersListResponse
```

Create Member

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\WorkspacesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$workspace_id = 'workspace_id_example'; // string
$workspace_member_create_request = new \OpenAPI\Client\Model\WorkspaceMemberCreateRequest(); // \OpenAPI\Client\Model\WorkspaceMemberCreateRequest
$idempotency_key = 'idempotency_key_example'; // string

try {
    $result = $apiInstance->createMemberApiV1WorkspacesWorkspaceIdMembersPost($workspace_id, $workspace_member_create_request, $idempotency_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WorkspacesApi->createMemberApiV1WorkspacesWorkspaceIdMembersPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **workspace_id** | **string**|  | |
| **workspace_member_create_request** | [**\OpenAPI\Client\Model\WorkspaceMemberCreateRequest**](../Model/WorkspaceMemberCreateRequest.md)|  | |
| **idempotency_key** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\WorkspaceMembersListResponse**](../Model/WorkspaceMembersListResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createWorkspaceApiV1WorkspacesPost()`

```php
createWorkspaceApiV1WorkspacesPost($workspace_create_request, $idempotency_key): \OpenAPI\Client\Model\WorkspaceResponse
```

Create Workspace

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\WorkspacesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$workspace_create_request = new \OpenAPI\Client\Model\WorkspaceCreateRequest(); // \OpenAPI\Client\Model\WorkspaceCreateRequest
$idempotency_key = 'idempotency_key_example'; // string

try {
    $result = $apiInstance->createWorkspaceApiV1WorkspacesPost($workspace_create_request, $idempotency_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WorkspacesApi->createWorkspaceApiV1WorkspacesPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **workspace_create_request** | [**\OpenAPI\Client\Model\WorkspaceCreateRequest**](../Model/WorkspaceCreateRequest.md)|  | |
| **idempotency_key** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\WorkspaceResponse**](../Model/WorkspaceResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteMemberApiV1WorkspacesWorkspaceIdMembersMemberIdDelete()`

```php
deleteMemberApiV1WorkspacesWorkspaceIdMembersMemberIdDelete($workspace_id, $member_id): \OpenAPI\Client\Model\SimpleBoolResponse
```

Delete Member

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\WorkspacesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$workspace_id = 'workspace_id_example'; // string
$member_id = 'member_id_example'; // string

try {
    $result = $apiInstance->deleteMemberApiV1WorkspacesWorkspaceIdMembersMemberIdDelete($workspace_id, $member_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WorkspacesApi->deleteMemberApiV1WorkspacesWorkspaceIdMembersMemberIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **workspace_id** | **string**|  | |
| **member_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\SimpleBoolResponse**](../Model/SimpleBoolResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteWorkspaceApiV1WorkspacesWorkspaceIdDelete()`

```php
deleteWorkspaceApiV1WorkspacesWorkspaceIdDelete($workspace_id): \OpenAPI\Client\Model\SimpleBoolResponse
```

Delete Workspace

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\WorkspacesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$workspace_id = 'workspace_id_example'; // string

try {
    $result = $apiInstance->deleteWorkspaceApiV1WorkspacesWorkspaceIdDelete($workspace_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WorkspacesApi->deleteWorkspaceApiV1WorkspacesWorkspaceIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **workspace_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\SimpleBoolResponse**](../Model/SimpleBoolResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getWorkspaceApiV1WorkspacesWorkspaceIdGet()`

```php
getWorkspaceApiV1WorkspacesWorkspaceIdGet($workspace_id): \OpenAPI\Client\Model\WorkspaceResponse
```

Get Workspace

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\WorkspacesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$workspace_id = 'workspace_id_example'; // string

try {
    $result = $apiInstance->getWorkspaceApiV1WorkspacesWorkspaceIdGet($workspace_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WorkspacesApi->getWorkspaceApiV1WorkspacesWorkspaceIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **workspace_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\WorkspaceResponse**](../Model/WorkspaceResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listMembersApiV1WorkspacesWorkspaceIdMembersGet()`

```php
listMembersApiV1WorkspacesWorkspaceIdMembersGet($workspace_id): \OpenAPI\Client\Model\WorkspaceMembersListResponse
```

List Members

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\WorkspacesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$workspace_id = 'workspace_id_example'; // string

try {
    $result = $apiInstance->listMembersApiV1WorkspacesWorkspaceIdMembersGet($workspace_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WorkspacesApi->listMembersApiV1WorkspacesWorkspaceIdMembersGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **workspace_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\WorkspaceMembersListResponse**](../Model/WorkspaceMembersListResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listWorkspacesApiV1WorkspacesGet()`

```php
listWorkspacesApiV1WorkspacesGet($limit, $cursor): \OpenAPI\Client\Model\WorkspacesListResponse
```

List Workspaces

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\WorkspacesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$limit = 50; // int
$cursor = 'cursor_example'; // string

try {
    $result = $apiInstance->listWorkspacesApiV1WorkspacesGet($limit, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WorkspacesApi->listWorkspacesApiV1WorkspacesGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **limit** | **int**|  | [optional] [default to 50] |
| **cursor** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\WorkspacesListResponse**](../Model/WorkspacesListResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `patchMemberApiV1WorkspacesWorkspaceIdMembersMemberIdPatch()`

```php
patchMemberApiV1WorkspacesWorkspaceIdMembersMemberIdPatch($workspace_id, $member_id, $workspace_member_patch_request): \OpenAPI\Client\Model\WorkspaceMemberOut
```

Patch Member

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\WorkspacesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$workspace_id = 'workspace_id_example'; // string
$member_id = 'member_id_example'; // string
$workspace_member_patch_request = new \OpenAPI\Client\Model\WorkspaceMemberPatchRequest(); // \OpenAPI\Client\Model\WorkspaceMemberPatchRequest

try {
    $result = $apiInstance->patchMemberApiV1WorkspacesWorkspaceIdMembersMemberIdPatch($workspace_id, $member_id, $workspace_member_patch_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WorkspacesApi->patchMemberApiV1WorkspacesWorkspaceIdMembersMemberIdPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **workspace_id** | **string**|  | |
| **member_id** | **string**|  | |
| **workspace_member_patch_request** | [**\OpenAPI\Client\Model\WorkspaceMemberPatchRequest**](../Model/WorkspaceMemberPatchRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\WorkspaceMemberOut**](../Model/WorkspaceMemberOut.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `patchWorkspaceApiV1WorkspacesWorkspaceIdPatch()`

```php
patchWorkspaceApiV1WorkspacesWorkspaceIdPatch($workspace_id, $workspace_patch_request, $idempotency_key): \OpenAPI\Client\Model\WorkspaceResponse
```

Patch Workspace

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\WorkspacesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$workspace_id = 'workspace_id_example'; // string
$workspace_patch_request = new \OpenAPI\Client\Model\WorkspacePatchRequest(); // \OpenAPI\Client\Model\WorkspacePatchRequest
$idempotency_key = 'idempotency_key_example'; // string

try {
    $result = $apiInstance->patchWorkspaceApiV1WorkspacesWorkspaceIdPatch($workspace_id, $workspace_patch_request, $idempotency_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WorkspacesApi->patchWorkspaceApiV1WorkspacesWorkspaceIdPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **workspace_id** | **string**|  | |
| **workspace_patch_request** | [**\OpenAPI\Client\Model\WorkspacePatchRequest**](../Model/WorkspacePatchRequest.md)|  | |
| **idempotency_key** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\WorkspaceResponse**](../Model/WorkspaceResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

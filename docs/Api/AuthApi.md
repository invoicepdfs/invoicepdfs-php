# OpenAPI\Client\AuthApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**forgotPasswordApiV1AuthForgotPasswordPost()**](AuthApi.md#forgotPasswordApiV1AuthForgotPasswordPost) | **POST** /api/v1/auth/forgot-password | Forgot Password |
| [**logoutApiV1AuthLogoutPost()**](AuthApi.md#logoutApiV1AuthLogoutPost) | **POST** /api/v1/auth/logout | Logout |
| [**meApiV1AuthMeGet()**](AuthApi.md#meApiV1AuthMeGet) | **GET** /api/v1/auth/me | Me |
| [**patchMeApiV1AuthMePatch()**](AuthApi.md#patchMeApiV1AuthMePatch) | **PATCH** /api/v1/auth/me | Patch Me |
| [**refreshApiV1AuthRefreshPost()**](AuthApi.md#refreshApiV1AuthRefreshPost) | **POST** /api/v1/auth/refresh | Refresh |
| [**registerApiV1AuthRegisterPost()**](AuthApi.md#registerApiV1AuthRegisterPost) | **POST** /api/v1/auth/register | Register |
| [**resetPasswordApiV1AuthResetPasswordPost()**](AuthApi.md#resetPasswordApiV1AuthResetPasswordPost) | **POST** /api/v1/auth/reset-password | Reset Password |
| [**tokenExchangeApiV1AuthTokenPost()**](AuthApi.md#tokenExchangeApiV1AuthTokenPost) | **POST** /api/v1/auth/token | Token Exchange |


## `forgotPasswordApiV1AuthForgotPasswordPost()`

```php
forgotPasswordApiV1AuthForgotPasswordPost($auth_forgot_password_request): \OpenAPI\Client\Model\AuthMessageResponse
```

Forgot Password

Send a password reset email via Firebase.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$auth_forgot_password_request = new \OpenAPI\Client\Model\AuthForgotPasswordRequest(); // \OpenAPI\Client\Model\AuthForgotPasswordRequest

try {
    $result = $apiInstance->forgotPasswordApiV1AuthForgotPasswordPost($auth_forgot_password_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->forgotPasswordApiV1AuthForgotPasswordPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **auth_forgot_password_request** | [**\OpenAPI\Client\Model\AuthForgotPasswordRequest**](../Model/AuthForgotPasswordRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\AuthMessageResponse**](../Model/AuthMessageResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `logoutApiV1AuthLogoutPost()`

```php
logoutApiV1AuthLogoutPost(): \OpenAPI\Client\Model\AuthMessageResponse
```

Logout

Revoke all Firebase refresh tokens for the authenticated user.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->logoutApiV1AuthLogoutPost();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->logoutApiV1AuthLogoutPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\AuthMessageResponse**](../Model/AuthMessageResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `meApiV1AuthMeGet()`

```php
meApiV1AuthMeGet(): \OpenAPI\Client\Model\AuthMeResponse
```

Me

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->meApiV1AuthMeGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->meApiV1AuthMeGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\AuthMeResponse**](../Model/AuthMeResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `patchMeApiV1AuthMePatch()`

```php
patchMeApiV1AuthMePatch($auth_me_patch_request): \OpenAPI\Client\Model\AuthMeResponse
```

Patch Me

Update the authenticated account's name or email.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$auth_me_patch_request = new \OpenAPI\Client\Model\AuthMePatchRequest(); // \OpenAPI\Client\Model\AuthMePatchRequest

try {
    $result = $apiInstance->patchMeApiV1AuthMePatch($auth_me_patch_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->patchMeApiV1AuthMePatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **auth_me_patch_request** | [**\OpenAPI\Client\Model\AuthMePatchRequest**](../Model/AuthMePatchRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\AuthMeResponse**](../Model/AuthMeResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `refreshApiV1AuthRefreshPost()`

```php
refreshApiV1AuthRefreshPost($auth_refresh_request): \OpenAPI\Client\Model\AuthRefreshResponse
```

Refresh

Exchange a Firebase refresh token for a new ID token.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$auth_refresh_request = new \OpenAPI\Client\Model\AuthRefreshRequest(); // \OpenAPI\Client\Model\AuthRefreshRequest

try {
    $result = $apiInstance->refreshApiV1AuthRefreshPost($auth_refresh_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->refreshApiV1AuthRefreshPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **auth_refresh_request** | [**\OpenAPI\Client\Model\AuthRefreshRequest**](../Model/AuthRefreshRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\AuthRefreshResponse**](../Model/AuthRefreshResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `registerApiV1AuthRegisterPost()`

```php
registerApiV1AuthRegisterPost($auth_register_request): \OpenAPI\Client\Model\AuthRegisterResponse
```

Register

Register a new account using a Firebase ID token.  The client authenticates with Firebase (email/password, Google, etc.) and sends the resulting ID token here to create an InvoicePDFs account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$auth_register_request = new \OpenAPI\Client\Model\AuthRegisterRequest(); // \OpenAPI\Client\Model\AuthRegisterRequest

try {
    $result = $apiInstance->registerApiV1AuthRegisterPost($auth_register_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->registerApiV1AuthRegisterPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **auth_register_request** | [**\OpenAPI\Client\Model\AuthRegisterRequest**](../Model/AuthRegisterRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\AuthRegisterResponse**](../Model/AuthRegisterResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `resetPasswordApiV1AuthResetPasswordPost()`

```php
resetPasswordApiV1AuthResetPasswordPost($auth_reset_password_request): \OpenAPI\Client\Model\AuthMessageResponse
```

Reset Password

Confirm a password reset using the code from the reset email.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$auth_reset_password_request = new \OpenAPI\Client\Model\AuthResetPasswordRequest(); // \OpenAPI\Client\Model\AuthResetPasswordRequest

try {
    $result = $apiInstance->resetPasswordApiV1AuthResetPasswordPost($auth_reset_password_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->resetPasswordApiV1AuthResetPasswordPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **auth_reset_password_request** | [**\OpenAPI\Client\Model\AuthResetPasswordRequest**](../Model/AuthResetPasswordRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\AuthMessageResponse**](../Model/AuthMessageResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `tokenExchangeApiV1AuthTokenPost()`

```php
tokenExchangeApiV1AuthTokenPost($auth_token_request): \OpenAPI\Client\Model\AuthTokenResponse
```

Token Exchange

Exchange a Firebase ID token for account info.  Use this on login: the client authenticates with Firebase, sends the ID token here, and receives the InvoicePDFs account details. The Firebase token itself is used as the Bearer token for subsequent API calls.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$auth_token_request = new \OpenAPI\Client\Model\AuthTokenRequest(); // \OpenAPI\Client\Model\AuthTokenRequest

try {
    $result = $apiInstance->tokenExchangeApiV1AuthTokenPost($auth_token_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->tokenExchangeApiV1AuthTokenPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **auth_token_request** | [**\OpenAPI\Client\Model\AuthTokenRequest**](../Model/AuthTokenRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\AuthTokenResponse**](../Model/AuthTokenResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

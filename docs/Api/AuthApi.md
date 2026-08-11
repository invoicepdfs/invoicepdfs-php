# InvoicePDFs\AuthApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**exchangeAuthToken()**](AuthApi.md#exchangeAuthToken) | **POST** /api/v1/auth/token | Exchange Auth Token |
| [**getCurrentUser()**](AuthApi.md#getCurrentUser) | **GET** /api/v1/auth/me | Get Current User |
| [**logout()**](AuthApi.md#logout) | **POST** /api/v1/auth/logout | Logout |
| [**refreshAccessToken()**](AuthApi.md#refreshAccessToken) | **POST** /api/v1/auth/refresh | Refresh Access Token |
| [**register()**](AuthApi.md#register) | **POST** /api/v1/auth/register | Register |
| [**requestPasswordReset()**](AuthApi.md#requestPasswordReset) | **POST** /api/v1/auth/forgot-password | Request Password Reset |
| [**resetPassword()**](AuthApi.md#resetPassword) | **POST** /api/v1/auth/reset-password | Reset Password |
| [**updateCurrentUser()**](AuthApi.md#updateCurrentUser) | **PATCH** /api/v1/auth/me | Update Current User |


## `exchangeAuthToken()`

```php
exchangeAuthToken($auth_token_request): \InvoicePDFs\Model\AuthTokenResponse
```

Exchange Auth Token

Exchange a Firebase ID token for account info.  Use this on login: the client authenticates with Firebase, sends the ID token here, and receives the InvoicePDFs account details. The Firebase token itself is used as the Bearer token for subsequent API calls.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new InvoicePDFs\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$auth_token_request = new \InvoicePDFs\Model\AuthTokenRequest(); // \InvoicePDFs\Model\AuthTokenRequest

try {
    $result = $apiInstance->exchangeAuthToken($auth_token_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->exchangeAuthToken: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **auth_token_request** | [**\InvoicePDFs\Model\AuthTokenRequest**](../Model/AuthTokenRequest.md)|  | |

### Return type

[**\InvoicePDFs\Model\AuthTokenResponse**](../Model/AuthTokenResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getCurrentUser()`

```php
getCurrentUser(): \InvoicePDFs\Model\AuthMeResponse
```

Get Current User

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getCurrentUser();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->getCurrentUser: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\InvoicePDFs\Model\AuthMeResponse**](../Model/AuthMeResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `logout()`

```php
logout(): \InvoicePDFs\Model\AuthMessageResponse
```

Logout

Revoke all Firebase refresh tokens for the authenticated user.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->logout();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->logout: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\InvoicePDFs\Model\AuthMessageResponse**](../Model/AuthMessageResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `refreshAccessToken()`

```php
refreshAccessToken($auth_refresh_request): \InvoicePDFs\Model\AuthRefreshResponse
```

Refresh Access Token

Exchange a Firebase refresh token for a new ID token.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new InvoicePDFs\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$auth_refresh_request = new \InvoicePDFs\Model\AuthRefreshRequest(); // \InvoicePDFs\Model\AuthRefreshRequest

try {
    $result = $apiInstance->refreshAccessToken($auth_refresh_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->refreshAccessToken: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **auth_refresh_request** | [**\InvoicePDFs\Model\AuthRefreshRequest**](../Model/AuthRefreshRequest.md)|  | |

### Return type

[**\InvoicePDFs\Model\AuthRefreshResponse**](../Model/AuthRefreshResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `register()`

```php
register($auth_register_request): \InvoicePDFs\Model\AuthRegisterResponse
```

Register

Register a new account using a Firebase ID token.  The client authenticates with Firebase (email/password, Google, etc.) and sends the resulting ID token here to create an InvoicePDFs account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new InvoicePDFs\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$auth_register_request = new \InvoicePDFs\Model\AuthRegisterRequest(); // \InvoicePDFs\Model\AuthRegisterRequest

try {
    $result = $apiInstance->register($auth_register_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->register: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **auth_register_request** | [**\InvoicePDFs\Model\AuthRegisterRequest**](../Model/AuthRegisterRequest.md)|  | |

### Return type

[**\InvoicePDFs\Model\AuthRegisterResponse**](../Model/AuthRegisterResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `requestPasswordReset()`

```php
requestPasswordReset($auth_forgot_password_request): \InvoicePDFs\Model\AuthMessageResponse
```

Request Password Reset

Send a password reset email via Firebase.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new InvoicePDFs\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$auth_forgot_password_request = new \InvoicePDFs\Model\AuthForgotPasswordRequest(); // \InvoicePDFs\Model\AuthForgotPasswordRequest

try {
    $result = $apiInstance->requestPasswordReset($auth_forgot_password_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->requestPasswordReset: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **auth_forgot_password_request** | [**\InvoicePDFs\Model\AuthForgotPasswordRequest**](../Model/AuthForgotPasswordRequest.md)|  | |

### Return type

[**\InvoicePDFs\Model\AuthMessageResponse**](../Model/AuthMessageResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `resetPassword()`

```php
resetPassword($auth_reset_password_request): \InvoicePDFs\Model\AuthMessageResponse
```

Reset Password

Confirm a password reset using the code from the reset email.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new InvoicePDFs\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$auth_reset_password_request = new \InvoicePDFs\Model\AuthResetPasswordRequest(); // \InvoicePDFs\Model\AuthResetPasswordRequest

try {
    $result = $apiInstance->resetPassword($auth_reset_password_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->resetPassword: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **auth_reset_password_request** | [**\InvoicePDFs\Model\AuthResetPasswordRequest**](../Model/AuthResetPasswordRequest.md)|  | |

### Return type

[**\InvoicePDFs\Model\AuthMessageResponse**](../Model/AuthMessageResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateCurrentUser()`

```php
updateCurrentUser($auth_me_patch_request): \InvoicePDFs\Model\AuthMeResponse
```

Update Current User

Update the authenticated account's name or email.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$auth_me_patch_request = new \InvoicePDFs\Model\AuthMePatchRequest(); // \InvoicePDFs\Model\AuthMePatchRequest

try {
    $result = $apiInstance->updateCurrentUser($auth_me_patch_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->updateCurrentUser: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **auth_me_patch_request** | [**\InvoicePDFs\Model\AuthMePatchRequest**](../Model/AuthMePatchRequest.md)|  | |

### Return type

[**\InvoicePDFs\Model\AuthMeResponse**](../Model/AuthMeResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

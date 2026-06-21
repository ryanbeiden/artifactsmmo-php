# ArtifactsMmo\AccountsApi



All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createAccountAccountsCreatePost()**](AccountsApi.md#createAccountAccountsCreatePost) | **POST** /accounts/create | Create Account |
| [**forgotPasswordAccountsForgotPasswordPost()**](AccountsApi.md#forgotPasswordAccountsForgotPasswordPost) | **POST** /accounts/forgot_password | Forgot Password |
| [**getAccountAccountsAccountGet()**](AccountsApi.md#getAccountAccountsAccountGet) | **GET** /accounts/{account} | Get Account |
| [**getAccountAchievementsAccountsAccountAchievementsGet()**](AccountsApi.md#getAccountAchievementsAccountsAccountAchievementsGet) | **GET** /accounts/{account}/achievements | Get Account Achievements |
| [**getAccountCharactersAccountsAccountCharactersGet()**](AccountsApi.md#getAccountCharactersAccountsAccountCharactersGet) | **GET** /accounts/{account}/characters | Get Account Characters |
| [**resetPasswordAccountsResetPasswordPost()**](AccountsApi.md#resetPasswordAccountsResetPasswordPost) | **POST** /accounts/reset_password | Reset Password |


## `createAccountAccountsCreatePost()`

```php
createAccountAccountsCreatePost($addAccountSchema): \ArtifactsMmo\Model\ResponseSchema
```

Create Account

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new ArtifactsMmo\Api\AccountsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$addAccountSchema = new \ArtifactsMmo\Model\AddAccountSchema(); // \ArtifactsMmo\Model\AddAccountSchema

try {
    $result = $apiInstance->createAccountAccountsCreatePost($addAccountSchema);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountsApi->createAccountAccountsCreatePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **addAccountSchema** | [**\ArtifactsMmo\Model\AddAccountSchema**](../Model/AddAccountSchema.md)|  | |

### Return type

[**\ArtifactsMmo\Model\ResponseSchema**](../Model/ResponseSchema.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `forgotPasswordAccountsForgotPasswordPost()`

```php
forgotPasswordAccountsForgotPasswordPost($passwordResetRequestSchema): \ArtifactsMmo\Model\PasswordResetResponseSchema
```

Forgot Password

Request a password reset.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new ArtifactsMmo\Api\AccountsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$passwordResetRequestSchema = new \ArtifactsMmo\Model\PasswordResetRequestSchema(); // \ArtifactsMmo\Model\PasswordResetRequestSchema

try {
    $result = $apiInstance->forgotPasswordAccountsForgotPasswordPost($passwordResetRequestSchema);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountsApi->forgotPasswordAccountsForgotPasswordPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **passwordResetRequestSchema** | [**\ArtifactsMmo\Model\PasswordResetRequestSchema**](../Model/PasswordResetRequestSchema.md)|  | |

### Return type

[**\ArtifactsMmo\Model\PasswordResetResponseSchema**](../Model/PasswordResetResponseSchema.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getAccountAccountsAccountGet()`

```php
getAccountAccountsAccountGet($account): \ArtifactsMmo\Model\AccountDetailsSchema
```

Get Account

Retrieve the details of an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new ArtifactsMmo\Api\AccountsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$account = 'account_example'; // string | The name of the account.

try {
    $result = $apiInstance->getAccountAccountsAccountGet($account);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountsApi->getAccountAccountsAccountGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account** | **string**| The name of the account. | |

### Return type

[**\ArtifactsMmo\Model\AccountDetailsSchema**](../Model/AccountDetailsSchema.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getAccountAchievementsAccountsAccountAchievementsGet()`

```php
getAccountAchievementsAccountsAccountAchievementsGet($account, $type, $completed, $page, $size): \ArtifactsMmo\Model\DataPageAccountAchievementSchema
```

Get Account Achievements

Retrieve the achievements of a account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new ArtifactsMmo\Api\AccountsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$account = 'account_example'; // string | The name of the account.
$type = new \ArtifactsMmo\Model\\ArtifactsMmoModelAchievementType(); // \ArtifactsMmoModelAchievementType | Type of achievements.
$completed = True; // bool | Filter by completed achievements.
$page = 1; // int | Page number
$size = 50; // int | Page size

try {
    $result = $apiInstance->getAccountAchievementsAccountsAccountAchievementsGet($account, $type, $completed, $page, $size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountsApi->getAccountAchievementsAccountsAccountAchievementsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account** | **string**| The name of the account. | |
| **type** | [**\ArtifactsMmoModelAchievementType**](../Model/.md)| Type of achievements. | [optional] |
| **completed** | **bool**| Filter by completed achievements. | [optional] |
| **page** | **int**| Page number | [optional] [default to 1] |
| **size** | **int**| Page size | [optional] [default to 50] |

### Return type

[**\ArtifactsMmo\Model\DataPageAccountAchievementSchema**](../Model/DataPageAccountAchievementSchema.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getAccountCharactersAccountsAccountCharactersGet()`

```php
getAccountCharactersAccountsAccountCharactersGet($account): \ArtifactsMmo\Model\CharactersListSchema
```

Get Account Characters

Account character lists.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new ArtifactsMmo\Api\AccountsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$account = 'account_example'; // string | The name of the account.

try {
    $result = $apiInstance->getAccountCharactersAccountsAccountCharactersGet($account);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountsApi->getAccountCharactersAccountsAccountCharactersGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account** | **string**| The name of the account. | |

### Return type

[**\ArtifactsMmo\Model\CharactersListSchema**](../Model/CharactersListSchema.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `resetPasswordAccountsResetPasswordPost()`

```php
resetPasswordAccountsResetPasswordPost($passwordResetConfirmSchema): \ArtifactsMmo\Model\PasswordResetResponseSchema
```

Reset Password

Reset password with a token. Use /forgot_password to get a token by email.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new ArtifactsMmo\Api\AccountsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$passwordResetConfirmSchema = new \ArtifactsMmo\Model\PasswordResetConfirmSchema(); // \ArtifactsMmo\Model\PasswordResetConfirmSchema

try {
    $result = $apiInstance->resetPasswordAccountsResetPasswordPost($passwordResetConfirmSchema);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountsApi->resetPasswordAccountsResetPasswordPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **passwordResetConfirmSchema** | [**\ArtifactsMmo\Model\PasswordResetConfirmSchema**](../Model/PasswordResetConfirmSchema.md)|  | |

### Return type

[**\ArtifactsMmo\Model\PasswordResetResponseSchema**](../Model/PasswordResetResponseSchema.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

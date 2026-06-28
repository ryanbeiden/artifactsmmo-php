# ArtifactsMmo\MyAccountApi



All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**buyGemsMyBuyGemsPost()**](MyAccountApi.md#buyGemsMyBuyGemsPost) | **POST** /my/buy_gems | Buy Gems |
| [**buySubscriptionMySubscribeStripePost()**](MyAccountApi.md#buySubscriptionMySubscribeStripePost) | **POST** /my/subscribe/stripe | Subscribe with Stripe |
| [**cancelSubscriptionMySubscribeCancelPost()**](MyAccountApi.md#cancelSubscriptionMySubscribeCancelPost) | **POST** /my/subscribe/cancel | Cancel Subscription |
| [**changeEmailMyChangeEmailPost()**](MyAccountApi.md#changeEmailMyChangeEmailPost) | **POST** /my/change_email | Change Email |
| [**changePasswordMyChangePasswordPost()**](MyAccountApi.md#changePasswordMyChangePasswordPost) | **POST** /my/change_password | Change Password |
| [**getAccountDetailsMyDetailsGet()**](MyAccountApi.md#getAccountDetailsMyDetailsGet) | **GET** /my/details | Get Account Details |
| [**getBankDetailsMyBankGet()**](MyAccountApi.md#getBankDetailsMyBankGet) | **GET** /my/bank | Get Bank Details |
| [**getBankItemsMyBankItemsGet()**](MyAccountApi.md#getBankItemsMyBankItemsGet) | **GET** /my/bank/items | Get Bank Items |
| [**getGeHistoryMyGrandexchangeHistoryGet()**](MyAccountApi.md#getGeHistoryMyGrandexchangeHistoryGet) | **GET** /my/grandexchange/history | Get Ge History |
| [**getGeOrdersMyGrandexchangeOrdersGet()**](MyAccountApi.md#getGeOrdersMyGrandexchangeOrdersGet) | **GET** /my/grandexchange/orders | Get Ge Orders |
| [**getMyGemsHistoryMyGemsHistoryGet()**](MyAccountApi.md#getMyGemsHistoryMyGemsHistoryGet) | **GET** /my/gems_history | Get My Gems History |
| [**getMyPurchaseHistoryMyPurchaseHistoryGet()**](MyAccountApi.md#getMyPurchaseHistoryMyPurchaseHistoryGet) | **GET** /my/purchase_history | Get My Purchase History |
| [**getMySubscriptionMySubscriptionGet()**](MyAccountApi.md#getMySubscriptionMySubscriptionGet) | **GET** /my/subscription | Get My Subscription |
| [**getPendingItemsMyPendingItemsGet()**](MyAccountApi.md#getPendingItemsMyPendingItemsGet) | **GET** /my/pending_items | Get Pending Items |
| [**getRateLimitsMyRatesGet()**](MyAccountApi.md#getRateLimitsMyRatesGet) | **GET** /my/rates | Get Rate Limits |
| [**subscribeWithMemberTokenMySubscribeMemberTokenPost()**](MyAccountApi.md#subscribeWithMemberTokenMySubscribeMemberTokenPost) | **POST** /my/subscribe/member_token | Subscribe With Member Token |


## `buyGemsMyBuyGemsPost()`

```php
buyGemsMyBuyGemsPost($purchaseGemsRequestSchema): \ArtifactsMmo\Model\CheckoutResponseWrapperSchema
```

Buy Gems

Purchase gems. Returns a Stripe checkout URL for payment.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: JWTBearer
$config = ArtifactsMmo\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new ArtifactsMmo\Api\MyAccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$purchaseGemsRequestSchema = new \ArtifactsMmo\Model\PurchaseGemsRequestSchema(); // \ArtifactsMmo\Model\PurchaseGemsRequestSchema

try {
    $result = $apiInstance->buyGemsMyBuyGemsPost($purchaseGemsRequestSchema);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MyAccountApi->buyGemsMyBuyGemsPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **purchaseGemsRequestSchema** | [**\ArtifactsMmo\Model\PurchaseGemsRequestSchema**](../Model/PurchaseGemsRequestSchema.md)|  | |

### Return type

[**\ArtifactsMmo\Model\CheckoutResponseWrapperSchema**](../Model/CheckoutResponseWrapperSchema.md)

### Authorization

[JWTBearer](../../README.md#JWTBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `buySubscriptionMySubscribeStripePost()`

```php
buySubscriptionMySubscribeStripePost($subscribeRequestSchema): \ArtifactsMmo\Model\CheckoutResponseWrapperSchema
```

Subscribe with Stripe

Subscribe to become a member and unlock the benefits tied to your selected plan. You will receive a secure Stripe checkout URL to complete the payment.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: JWTBearer
$config = ArtifactsMmo\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new ArtifactsMmo\Api\MyAccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$subscribeRequestSchema = new \ArtifactsMmo\Model\SubscribeRequestSchema(); // \ArtifactsMmo\Model\SubscribeRequestSchema

try {
    $result = $apiInstance->buySubscriptionMySubscribeStripePost($subscribeRequestSchema);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MyAccountApi->buySubscriptionMySubscribeStripePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **subscribeRequestSchema** | [**\ArtifactsMmo\Model\SubscribeRequestSchema**](../Model/SubscribeRequestSchema.md)|  | |

### Return type

[**\ArtifactsMmo\Model\CheckoutResponseWrapperSchema**](../Model/CheckoutResponseWrapperSchema.md)

### Authorization

[JWTBearer](../../README.md#JWTBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `cancelSubscriptionMySubscribeCancelPost()`

```php
cancelSubscriptionMySubscribeCancelPost(): \ArtifactsMmo\Model\ResponseSchema
```

Cancel Subscription

Cancel subscription at the end of the current billing period.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: JWTBearer
$config = ArtifactsMmo\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new ArtifactsMmo\Api\MyAccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->cancelSubscriptionMySubscribeCancelPost();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MyAccountApi->cancelSubscriptionMySubscribeCancelPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\ArtifactsMmo\Model\ResponseSchema**](../Model/ResponseSchema.md)

### Authorization

[JWTBearer](../../README.md#JWTBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `changeEmailMyChangeEmailPost()`

```php
changeEmailMyChangeEmailPost($changeEmailSchema): \ArtifactsMmo\Model\ResponseSchema
```

Change Email

Change your account email.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: JWTBearer
$config = ArtifactsMmo\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new ArtifactsMmo\Api\MyAccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$changeEmailSchema = new \ArtifactsMmo\Model\ChangeEmailSchema(); // \ArtifactsMmo\Model\ChangeEmailSchema

try {
    $result = $apiInstance->changeEmailMyChangeEmailPost($changeEmailSchema);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MyAccountApi->changeEmailMyChangeEmailPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **changeEmailSchema** | [**\ArtifactsMmo\Model\ChangeEmailSchema**](../Model/ChangeEmailSchema.md)|  | |

### Return type

[**\ArtifactsMmo\Model\ResponseSchema**](../Model/ResponseSchema.md)

### Authorization

[JWTBearer](../../README.md#JWTBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `changePasswordMyChangePasswordPost()`

```php
changePasswordMyChangePasswordPost($changePasswordSchema): \ArtifactsMmo\Model\ResponseSchema
```

Change Password

Change your account password. Changing the password reset the account token.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: JWTBearer
$config = ArtifactsMmo\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new ArtifactsMmo\Api\MyAccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$changePasswordSchema = new \ArtifactsMmo\Model\ChangePasswordSchema(); // \ArtifactsMmo\Model\ChangePasswordSchema

try {
    $result = $apiInstance->changePasswordMyChangePasswordPost($changePasswordSchema);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MyAccountApi->changePasswordMyChangePasswordPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **changePasswordSchema** | [**\ArtifactsMmo\Model\ChangePasswordSchema**](../Model/ChangePasswordSchema.md)|  | |

### Return type

[**\ArtifactsMmo\Model\ResponseSchema**](../Model/ResponseSchema.md)

### Authorization

[JWTBearer](../../README.md#JWTBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getAccountDetailsMyDetailsGet()`

```php
getAccountDetailsMyDetailsGet(): \ArtifactsMmo\Model\MyAccountDetailsSchema
```

Get Account Details

Fetch account details.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: JWTBearer
$config = ArtifactsMmo\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new ArtifactsMmo\Api\MyAccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getAccountDetailsMyDetailsGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MyAccountApi->getAccountDetailsMyDetailsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\ArtifactsMmo\Model\MyAccountDetailsSchema**](../Model/MyAccountDetailsSchema.md)

### Authorization

[JWTBearer](../../README.md#JWTBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getBankDetailsMyBankGet()`

```php
getBankDetailsMyBankGet(): \ArtifactsMmo\Model\BankResponseSchema
```

Get Bank Details

Fetch bank details.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: JWTBearer
$config = ArtifactsMmo\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new ArtifactsMmo\Api\MyAccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getBankDetailsMyBankGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MyAccountApi->getBankDetailsMyBankGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\ArtifactsMmo\Model\BankResponseSchema**](../Model/BankResponseSchema.md)

### Authorization

[JWTBearer](../../README.md#JWTBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getBankItemsMyBankItemsGet()`

```php
getBankItemsMyBankItemsGet($itemCode, $page, $size): \ArtifactsMmo\Model\DataPageSimpleItemSchema
```

Get Bank Items

Fetch all items in your bank.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: JWTBearer
$config = ArtifactsMmo\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new ArtifactsMmo\Api\MyAccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$itemCode = 'itemCode_example'; // string | Item to search in your bank.
$page = 1; // int | Page number
$size = 50; // int | Page size

try {
    $result = $apiInstance->getBankItemsMyBankItemsGet($itemCode, $page, $size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MyAccountApi->getBankItemsMyBankItemsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **itemCode** | **string**| Item to search in your bank. | [optional] |
| **page** | **int**| Page number | [optional] [default to 1] |
| **size** | **int**| Page size | [optional] [default to 50] |

### Return type

[**\ArtifactsMmo\Model\DataPageSimpleItemSchema**](../Model/DataPageSimpleItemSchema.md)

### Authorization

[JWTBearer](../../README.md#JWTBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getGeHistoryMyGrandexchangeHistoryGet()`

```php
getGeHistoryMyGrandexchangeHistoryGet($id, $code, $page, $size): \ArtifactsMmo\Model\DataPageGEOrderHistorySchema
```

Get Ge History

Fetch your transaction history of the last 7 days (buy and sell orders).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: JWTBearer
$config = ArtifactsMmo\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new ArtifactsMmo\Api\MyAccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | Order ID to search in your history.
$code = 'code_example'; // string | Item to search in your history.
$page = 1; // int | Page number
$size = 50; // int | Page size

try {
    $result = $apiInstance->getGeHistoryMyGrandexchangeHistoryGet($id, $code, $page, $size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MyAccountApi->getGeHistoryMyGrandexchangeHistoryGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Order ID to search in your history. | [optional] |
| **code** | **string**| Item to search in your history. | [optional] |
| **page** | **int**| Page number | [optional] [default to 1] |
| **size** | **int**| Page size | [optional] [default to 50] |

### Return type

[**\ArtifactsMmo\Model\DataPageGEOrderHistorySchema**](../Model/DataPageGEOrderHistorySchema.md)

### Authorization

[JWTBearer](../../README.md#JWTBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getGeOrdersMyGrandexchangeOrdersGet()`

```php
getGeOrdersMyGrandexchangeOrdersGet($code, $type, $page, $size): \ArtifactsMmo\Model\DataPageGEOrderSchema
```

Get Ge Orders

Fetch your orders details (sell and buy orders).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: JWTBearer
$config = ArtifactsMmo\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new ArtifactsMmo\Api\MyAccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$code = 'code_example'; // string | The code of the item.
$type = new \ArtifactsMmo\Model\\ArtifactsMmoModelGEOrderType(); // \ArtifactsMmoModelGEOrderType | Filter by order type (sell or buy).
$page = 1; // int | Page number
$size = 50; // int | Page size

try {
    $result = $apiInstance->getGeOrdersMyGrandexchangeOrdersGet($code, $type, $page, $size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MyAccountApi->getGeOrdersMyGrandexchangeOrdersGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **code** | **string**| The code of the item. | [optional] |
| **type** | [**\ArtifactsMmoModelGEOrderType**](../Model/.md)| Filter by order type (sell or buy). | [optional] |
| **page** | **int**| Page number | [optional] [default to 1] |
| **size** | **int**| Page size | [optional] [default to 50] |

### Return type

[**\ArtifactsMmo\Model\DataPageGEOrderSchema**](../Model/DataPageGEOrderSchema.md)

### Authorization

[JWTBearer](../../README.md#JWTBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getMyGemsHistoryMyGemsHistoryGet()`

```php
getMyGemsHistoryMyGemsHistoryGet(): \ArtifactsMmo\Model\GemTransactionListResponseSchema
```

Get My Gems History

List all gem credits and debits.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: JWTBearer
$config = ArtifactsMmo\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new ArtifactsMmo\Api\MyAccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getMyGemsHistoryMyGemsHistoryGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MyAccountApi->getMyGemsHistoryMyGemsHistoryGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\ArtifactsMmo\Model\GemTransactionListResponseSchema**](../Model/GemTransactionListResponseSchema.md)

### Authorization

[JWTBearer](../../README.md#JWTBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getMyPurchaseHistoryMyPurchaseHistoryGet()`

```php
getMyPurchaseHistoryMyPurchaseHistoryGet(): \ArtifactsMmo\Model\PurchaseHistoryListResponseSchema
```

Get My Purchase History

List all purchases (subscriptions and gem packs).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: JWTBearer
$config = ArtifactsMmo\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new ArtifactsMmo\Api\MyAccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getMyPurchaseHistoryMyPurchaseHistoryGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MyAccountApi->getMyPurchaseHistoryMyPurchaseHistoryGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\ArtifactsMmo\Model\PurchaseHistoryListResponseSchema**](../Model/PurchaseHistoryListResponseSchema.md)

### Authorization

[JWTBearer](../../README.md#JWTBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getMySubscriptionMySubscriptionGet()`

```php
getMySubscriptionMySubscriptionGet(): \ArtifactsMmo\Model\SubscriptionResponseSchema
```

Get My Subscription

Get current subscription details.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: JWTBearer
$config = ArtifactsMmo\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new ArtifactsMmo\Api\MyAccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getMySubscriptionMySubscriptionGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MyAccountApi->getMySubscriptionMySubscriptionGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\ArtifactsMmo\Model\SubscriptionResponseSchema**](../Model/SubscriptionResponseSchema.md)

### Authorization

[JWTBearer](../../README.md#JWTBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getPendingItemsMyPendingItemsGet()`

```php
getPendingItemsMyPendingItemsGet($page, $size): \ArtifactsMmo\Model\DataPagePendingItemSchema
```

Get Pending Items

Retrieve all unclaimed pending items for your account.  These are items from various sources (achievements, grand exchange, events, etc.) that can be claimed by any character on your account using /my/{name}/action/claim/{id}.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: JWTBearer
$config = ArtifactsMmo\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new ArtifactsMmo\Api\MyAccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 1; // int | Page number
$size = 50; // int | Page size

try {
    $result = $apiInstance->getPendingItemsMyPendingItemsGet($page, $size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MyAccountApi->getPendingItemsMyPendingItemsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**| Page number | [optional] [default to 1] |
| **size** | **int**| Page size | [optional] [default to 50] |

### Return type

[**\ArtifactsMmo\Model\DataPagePendingItemSchema**](../Model/DataPagePendingItemSchema.md)

### Authorization

[JWTBearer](../../README.md#JWTBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getRateLimitsMyRatesGet()`

```php
getRateLimitsMyRatesGet(): \ArtifactsMmo\Model\RateLimitsSchema
```

Get Rate Limits

Get all rate limits.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: JWTBearer
$config = ArtifactsMmo\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new ArtifactsMmo\Api\MyAccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getRateLimitsMyRatesGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MyAccountApi->getRateLimitsMyRatesGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\ArtifactsMmo\Model\RateLimitsSchema**](../Model/RateLimitsSchema.md)

### Authorization

[JWTBearer](../../README.md#JWTBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `subscribeWithMemberTokenMySubscribeMemberTokenPost()`

```php
subscribeWithMemberTokenMySubscribeMemberTokenPost(): \ArtifactsMmo\Model\MemberTokenSubscriptionResponseSchema
```

Subscribe With Member Token

Redeem a member token to start or extend membership by 30 days. Member tokens are manually granted as rewards for events. Member tokens cannot be redeemed while a Stripe subscription is active.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: JWTBearer
$config = ArtifactsMmo\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new ArtifactsMmo\Api\MyAccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->subscribeWithMemberTokenMySubscribeMemberTokenPost();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MyAccountApi->subscribeWithMemberTokenMySubscribeMemberTokenPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\ArtifactsMmo\Model\MemberTokenSubscriptionResponseSchema**](../Model/MemberTokenSubscriptionResponseSchema.md)

### Authorization

[JWTBearer](../../README.md#JWTBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

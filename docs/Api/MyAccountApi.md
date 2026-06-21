# ArtifactsMmo\MyAccountApi



All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**changePasswordMyChangePasswordPost()**](MyAccountApi.md#changePasswordMyChangePasswordPost) | **POST** /my/change_password | Change Password |
| [**getAccountDetailsMyDetailsGet()**](MyAccountApi.md#getAccountDetailsMyDetailsGet) | **GET** /my/details | Get Account Details |
| [**getBankDetailsMyBankGet()**](MyAccountApi.md#getBankDetailsMyBankGet) | **GET** /my/bank | Get Bank Details |
| [**getBankItemsMyBankItemsGet()**](MyAccountApi.md#getBankItemsMyBankItemsGet) | **GET** /my/bank/items | Get Bank Items |
| [**getGeHistoryMyGrandexchangeHistoryGet()**](MyAccountApi.md#getGeHistoryMyGrandexchangeHistoryGet) | **GET** /my/grandexchange/history | Get Ge History |
| [**getGeOrdersMyGrandexchangeOrdersGet()**](MyAccountApi.md#getGeOrdersMyGrandexchangeOrdersGet) | **GET** /my/grandexchange/orders | Get Ge Orders |
| [**getPendingItemsMyPendingItemsGet()**](MyAccountApi.md#getPendingItemsMyPendingItemsGet) | **GET** /my/pending-items | Get Pending Items |


## `changePasswordMyChangePasswordPost()`

```php
changePasswordMyChangePasswordPost($changePassword): \ArtifactsMmo\Model\ResponseSchema
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
$changePassword = new \ArtifactsMmo\Model\ChangePassword(); // \ArtifactsMmo\Model\ChangePassword

try {
    $result = $apiInstance->changePasswordMyChangePasswordPost($changePassword);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MyAccountApi->changePasswordMyChangePasswordPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **changePassword** | [**\ArtifactsMmo\Model\ChangePassword**](../Model/ChangePassword.md)|  | |

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
getGeHistoryMyGrandexchangeHistoryGet($id, $code, $page, $size): \ArtifactsMmo\Model\DataPageGeOrderHistorySchema
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

[**\ArtifactsMmo\Model\DataPageGeOrderHistorySchema**](../Model/DataPageGeOrderHistorySchema.md)

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

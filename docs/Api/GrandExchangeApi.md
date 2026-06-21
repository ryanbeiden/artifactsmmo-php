# ArtifactsMmo\GrandExchangeApi



All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getGeHistoryGrandexchangeHistoryCodeGet()**](GrandExchangeApi.md#getGeHistoryGrandexchangeHistoryCodeGet) | **GET** /grandexchange/history/{code} | Get Ge History |
| [**getGeOrderGrandexchangeOrdersIdGet()**](GrandExchangeApi.md#getGeOrderGrandexchangeOrdersIdGet) | **GET** /grandexchange/orders/{id} | Get Ge Order |
| [**getGeOrdersGrandexchangeOrdersGet()**](GrandExchangeApi.md#getGeOrdersGrandexchangeOrdersGet) | **GET** /grandexchange/orders | Get Ge Orders |


## `getGeHistoryGrandexchangeHistoryCodeGet()`

```php
getGeHistoryGrandexchangeHistoryCodeGet($code, $account, $page, $size): \ArtifactsMmo\Model\DataPageGeOrderHistorySchema
```

Get Ge History

Fetch the transaction history of the item for the last 7 days (buy and sell orders).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new ArtifactsMmo\Api\GrandExchangeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$code = 'code_example'; // string | The code of the item.
$account = 'account_example'; // string | Account involved in the transaction (matches either seller or buyer).
$page = 1; // int | Page number
$size = 50; // int | Page size

try {
    $result = $apiInstance->getGeHistoryGrandexchangeHistoryCodeGet($code, $account, $page, $size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GrandExchangeApi->getGeHistoryGrandexchangeHistoryCodeGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **code** | **string**| The code of the item. | |
| **account** | **string**| Account involved in the transaction (matches either seller or buyer). | [optional] |
| **page** | **int**| Page number | [optional] [default to 1] |
| **size** | **int**| Page size | [optional] [default to 50] |

### Return type

[**\ArtifactsMmo\Model\DataPageGeOrderHistorySchema**](../Model/DataPageGeOrderHistorySchema.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getGeOrderGrandexchangeOrdersIdGet()`

```php
getGeOrderGrandexchangeOrdersIdGet($id): \ArtifactsMmo\Model\GEOrderResponseSchema
```

Get Ge Order

Retrieve a specific order by ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new ArtifactsMmo\Api\GrandExchangeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | The id of the order.

try {
    $result = $apiInstance->getGeOrderGrandexchangeOrdersIdGet($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GrandExchangeApi->getGeOrderGrandexchangeOrdersIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The id of the order. | |

### Return type

[**\ArtifactsMmo\Model\GEOrderResponseSchema**](../Model/GEOrderResponseSchema.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getGeOrdersGrandexchangeOrdersGet()`

```php
getGeOrdersGrandexchangeOrdersGet($code, $account, $type, $page, $size): \ArtifactsMmo\Model\DataPageGEOrderSchema
```

Get Ge Orders

Fetch all orders (sell and buy orders).  Use the `type` parameter to filter by order type; when using `account`, `type` is required to keep account searches explicit.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new ArtifactsMmo\Api\GrandExchangeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$code = 'code_example'; // string | The code of the item.
$account = 'account_example'; // string | The account that sells or buys items.
$type = new \ArtifactsMmo\Model\\ArtifactsMmoModelGEOrderType(); // \ArtifactsMmoModelGEOrderType | Filter by order type (sell or buy).
$page = 1; // int | Page number
$size = 50; // int | Page size

try {
    $result = $apiInstance->getGeOrdersGrandexchangeOrdersGet($code, $account, $type, $page, $size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GrandExchangeApi->getGeOrdersGrandexchangeOrdersGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **code** | **string**| The code of the item. | [optional] |
| **account** | **string**| The account that sells or buys items. | [optional] |
| **type** | [**\ArtifactsMmoModelGEOrderType**](../Model/.md)| Filter by order type (sell or buy). | [optional] |
| **page** | **int**| Page number | [optional] [default to 1] |
| **size** | **int**| Page size | [optional] [default to 50] |

### Return type

[**\ArtifactsMmo\Model\DataPageGEOrderSchema**](../Model/DataPageGEOrderSchema.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
